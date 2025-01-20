**Paper 1: Deep Reinforcement Learning with Enhanced PPO for Safe Mobile Robot Navigation**

- utilizes LiDAR sensor data and a deep neural network to generate control signals guiding it toward a specified target while avoiding obstacles
- wide range of applications, from search and rescue missions in disaster-stricken areas to autonomous exploration of remote and hazardous locations
- they use gazebo and turtlebot
- These inputs include laser readings across 30 dimensions
- By iteratively updating both networks, the system continuously improves in its ability to not only choose optimal actions (via the actor) but also in evaluating the potential future rewards of current states (via the critic).
- Deep Deterministic Policy Gradient and proximal policy optimization
![[Pasted image 20250112154953.png]]


**Paper 2: Reinforcement learning in robotic applications: a comprehensive survey**

1. **Actor-Critic Methods**: These algorithms combine value-based and policy-based approaches, where the actor updates the policy and the critic evaluates the action taken by the actor.
2. **Deep Reinforcement Learning (DeepRL)**: This approach utilizes deep learning techniques to handle high-dimensional state spaces, allowing for more complex decision-making.
3. **Multi-Agent Reinforcement Learning**: This involves multiple agents learning simultaneously, which is particularly useful in environments where agents must interact with each other.
4. **Human-Centered Algorithms**: These algorithms focus on improving human-robot interaction, making robots more intuitive and responsive to human needs.

The survey highlights:

- **Land-Based Applications**: Such as autonomous vehicles and robotic manipulators.
- **Water-Based Applications**: Including underwater exploration and autonomous marine vehicles.
- **Air-Based Applications**: Encompassing drones and aerial robotics.




**Paper 3:  Learning for a Robot: Deep Reinforcement Learning, Imitation Learning, Transfer Learning**

- imitation learning is proposed that robot learns from images,videos,or an expert
- Improving the efficiency and the generalization in robot learning is also seeking further research attention.
- transfer learning is the appropriate algorithm that train the data in simulation, then the policy refined can be reused on a physical platform

![[Pasted image 20250112154104.png]]


**Paper 4: Deep Reinforcement Learning-based Obstacle Avoidance for Robot Movement in Warehouse Environments**


- For pedestrian behaviour, the historical trajectories of pedestrians can be fitted by mathematical models such as Hidden Markov Models and Gaussian Mixture Models to analyse their trajectories
- the robots cant always adapt to the random behaviour of the pedestrian
- Based on the spatial behaviours of the pedestrians, the reward function for reinforcement learning is redesigned by penalising the state of entering into the pedestrian within a private distance as well as the state of excessive angular velocity change
- Dynamic obstacles around pedestrians are encoded using angular pedestrian grid and temporal features

![[Pasted image 20250112154010.png]]


To see:
https://journals.sagepub.com/doi/full/10.1177/0278364920987859
