# Conceptual Contracts: Vision-Language-Action (VLA) Pipeline

This document defines the conceptual "API" and interaction patterns for the VLA pipeline components.

### 1. Voice-to-Text Interface

- **Contract**: Transcribes raw audio input into a text transcript.
- **Input**: `Voice Command` (audio data).
- **Output**: `Text Transcript` (string).
- **Purpose**: To convert spoken language into a machine-readable format for the LLM.

### 2. Cognitive Planner (LLM) Interface

- **Contract**: Decomposes a user's command (text) into a sequence of high-level tasks.
- **Inputs**:
  - `Text Transcript` (the user's command).
  - `World State` (optional, for context-aware planning).
- **Output**: `Task Plan` (a structured list of tasks).
- **Purpose**: To provide a high-level, common-sense plan for achieving the user's goal.

### 3. Action Translator Interface

- **Contract**: Translates a high-level `Task Plan` into a sequence of low-level, executable ROS 2 actions.
- **Inputs**:
  - `Task Plan` (from the LLM).
  - `World State` (for grounding tasks in the environment, e.g., finding object coordinates).
- **Output**: `Action Sequence` (a list of ROS 2 action goals).
- **Purpose**: To bridge the gap between abstract planning and the robot's specific capabilities.

### 4. Perception System Interface

- **Contract**: Provides real-time information about the environment.
- **Inputs**: Raw sensor data (camera images, LiDAR scans).
- **Outputs**:
  - `World State` updates (e.g., object locations, map changes).
  - `Vision Data` for other modules.
- **Purpose**: To enable the robot to "see" and understand its surroundings.

### 5. Navigation System Interface (e.g., Nav2)

- **Contract**: Executes navigation goals to move the robot from one point to another.
- **Input**: A navigation goal from the `Action Sequence`.
- **Output**: Status updates (e.g., success, failure, progress) and physical movement of the robot.
- **Purpose**: To handle all aspects of autonomous mobility.

### 6. Manipulation System Interface

- **Contract**: Executes manipulation goals, such as grasping or releasing an object.
- **Input**: A manipulation goal from the `Action Sequence`.
- **Output**: Status updates and physical movement of the robot's arms/grippers.
- **Purpose**: To enable physical interaction with objects in the environment.
