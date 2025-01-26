this study proposes a dynamic warning zone that creates a circular sector around humans based on the step length and speed of humans. 

To properly comprehend human behavior and keep a safe distance between the robot and the humans, warning zones are implemented during the robot’s training using deep enforcement learning techniques.


collision avoidance with deep reinforcement learning (CADRL) , long short-term memory (LSTM-RL), and social attention with reinforcement learning (SARL).


The learning-model methods present human-aware navigation as a Markov decision process (MDP) and use deep V-learning, where the agent chooses an action based on the state value approximated by the neural networks  By maximizing the total reward of the action, the deep reinforce- ment learning (DRL) technique selects the optimal policy for leading the robot through environmental interaction

-  Robots are trained with the dynamic warning zones around humans based on their size, speed, and the length of steps they take, to avoid collisions. The warning zone is a circular space that the robot avoids crossing to keep a comfortable distance from humans. 
-  A proposed reward function evaluates the distance between the robot’s position and the goal to reach a short- distance goal. A positive reward is given to the robot when it gets closer to the goal, and a negative reward when it moves away from the goal. 
- The proposed navigation system model is integrated into the robot operating system (ROS) for extensive evalua- tion in three different simulated and real scenarios

Metodology

![[Pasted image 20250125135503.png]]

The observations such as position and velocity are provided to the deep neu- ral network framework. With a pre-trained value network N , a path is planned by selecting actions that maximize the cumulative reward. 

![[Pasted image 20250125135728.png]]

Training setup

![[Pasted image 20250125135813.png]]

