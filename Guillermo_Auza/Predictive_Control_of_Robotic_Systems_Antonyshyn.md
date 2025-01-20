https://doi.org/10.1007/s10846-024-02118-y

The Journal states that Reinforcement Learning (RL) in robotics suffers from sparse rewards and sample efficiency, focusing on control systems for robotics due to having most of the time binary outcomes from actions. 

To tackle this problem, Model Predictive Control (MPC) was introduced, where the systems dynamics was modeled and given certain constraints to solve an optimization problem where it predicts future states based on the current systems behavior with a cost function.

![[MPC_Diagram.png]]

eventually RL started being used to learn the plants behavior in certain environments, nevertheless, this approach required of extensive data and had low sample efficiency since this method was not based on a dynamic model, instead learning policies to tackle the control problem.

![[RL_Diagram.png]]

Finally, Model Based Reinforcement Learning (MBRL) was introduced to tackle the problems with MPC and RL in robotics. This type of approach focuses on learning or tweaking the systems dynamic model to incorporate policies. This methodology allows the agent to simulate the interactions it has with the environment to predict future outcomes from its actions. However, this approach suffers in sparse reward scenarios and may require a starting cost function or may rely on Hindsight Experience Replay (HER) to improve sample efficiency.

![[MBRL_Diagram.png]]

Finally, the journal proposes their own model Deep Value-and-Predictive-Model Control (DVPMC). This model takes advantage of MPC principles and incorporates an optimizer to evaluate the best course of action, furthermore, DVPMC learns the dynamic model and value function. Finally DVPMC uses a replay buffer for experience storage and value function training.

| Feature            | **DVPMC**                                   | **General MBRL**                                                        |
| ------------------ | ------------------------------------------- | ----------------------------------------------------------------------- |
| **Optimization**   | Cross Entropy                               | policy optimization                                                     |
| **Value Function** | Learnt Value Function                       | preexisting Value Function / None                                       |
| **Dynamics Model** | Learnt Dynamic Model                        | Learns dynamics models for policy improvement, planning, or simulation. |
| **Sparse Rewards** | value function                              | Hindsight Experience Replay                                             |
| **Focus**          | Robotic Control and Sparse Reward Scenarios | Broader Scope                                                           |
![[DVMPC_Diagram.png]]a 

