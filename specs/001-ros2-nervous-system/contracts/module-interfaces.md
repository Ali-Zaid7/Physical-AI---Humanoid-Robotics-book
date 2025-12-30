# Conceptual Contracts: ROS 2 Primitives

This document defines the conceptual "API" and interaction patterns for the ROS 2 concepts covered in this module.

### Node-to-Node Communication

- **Contract**: Nodes communicate over the ROS 2 graph.
- **Mechanism 1: Topics (Publisher/Subscriber)**
  - **Purpose**: For continuous data streams (e.g., sensor data, state updates). This is a one-to-many communication pattern.
  - **Interface**:
    - **Publisher**: Publishes a message of a specific type to a named topic.
    - **Subscriber**: Subscribes to a named topic and receives messages of that type.
  - **Example**: A camera node publishes `sensor_msgs/Image` messages to the `/camera/image_raw` topic. A separate image processing node subscribes to this topic.

- **Mechanism 2: Services (Client/Server)**
  - **Purpose**: For request/response interactions. This is a one-to-one communication pattern.
  - **Interface**:
    - **Service Server**: Waits for a request, performs a task, and sends a single response.
    - **Service Client**: Sends a request and waits for the response.
  - **Example**: A "pick_object" service that takes an object's coordinates as a request and returns a boolean indicating success or failure.

- **Mechanism 3: Actions (Action Client/Action Server)**
  - **Purpose**: For long-running tasks that require feedback and the ability to be preempted or canceled.
  - **Interface**:
    - **Action Server**: Accepts a goal, provides periodic feedback on its progress, and returns a final result.
    - **Action Client**: Sends a goal, can receive feedback, and gets the final result. Can also send a cancellation request.
  - **Example**: A "navigate_to_pose" action that takes a target location as a goal, provides feedback on the robot's current distance to the target, and returns a result upon arrival (or failure).

### Robot Modeling

- **Contract**: A robot's physical structure is defined by a URDF file.
- **Interface**:
  - **Links**: Define the rigid parts of the robot (e.g., torso, upper arm, gripper).
  - **Joints**: Define the kinematic relationship and motion constraints between two links (e.g., revolute, prismatic, fixed).
- **Example**: A URDF file describes an arm with a series of links connected by revolute joints, forming a kinematic chain. ROS 2 tools can then parse this file to understand the robot's state.
