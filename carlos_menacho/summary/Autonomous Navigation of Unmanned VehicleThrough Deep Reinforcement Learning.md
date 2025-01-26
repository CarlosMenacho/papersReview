The focus is on using the Deep Deterministic Policy Gradient (DDPG) algorithm to address
issues in high-dimensional continuous action spaces. The results demonstrate that the DDPG algorithm outperforms traditional Deep Q-Network (DQN) and
Double Deep Q-Network (DDQN) algorithms in path planning tasks.

To address this challenge, the Deep Deterministic Policy Gradient (DDPG) algorithm was proposed, combining the strengths of Deep Q-Network (DQN) and Policy Gradient methods. DDPG is an off-policy algorithm designed for environments with high-dimensional continuous action spaces.

![[Pasted image 20250126195027.png]]


DDPG 

The DDPG algorithm consists of a policy network and a target network. DDPG uses a
deterministic strategy to select actions, so the output is not the probability of the behavior, but the specific behavior. is the parameter of the policy network,ta is the action, andts is the
state.

![[Pasted image 20250126195253.png]]


