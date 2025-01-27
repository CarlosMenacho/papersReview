**Markov Decision Process :** 
![[Markov_Definition.png]]
![[Markov_Diagram.png]]
https://www.youtube.com/watch?v=4Fqt2Nk2lhY

**Robust Markov Decision Process :**

The main difference between MDP and RMDP is that it further accounts for parametric uncertainty in the environment. This is done by implementing an observation history to estimate a range of parameters instead of assuming fixed parameters. Furthermore, RMDP guarantees certain probability of success in a worst case scenario.

![[Robust_Markov_Chain.png]]

**Conference Paper Problem to Tackle :**

The conference paper establishes that RL has been used in robotics for some time now. However, the main issue lies within implementing the deduced policies in a different environment than the one it has learnt said policies.

To solve this issue, the author propose a RMDP which attempts to obtain a generalized understanding of the dynamics of the system within different environments to achieve higher robustness in its control under adverse circumstances.

With this purpose in mind, the RMDP controller is validated within a virtual environment simulating the dynamics of a quadcopter.

![[Quadcopter_Diagram.png]]

**Implemented Pipeline :**

![[Quadcopter_Pipeline.png]]

The pipeline shows a controller diagram and a NN architecture. The controller structure is a simple feedback based controller where policies determine the actions of the system. For the NN there are three fully connected 64 neuron NN with tanh activation. The first NN attempts to create a policy based on the state, on the other hand, the second NN is an adversary policy where based on the state it creates an adverse condition. Finally the third NN acts as a critic to evaluate the effectiveness of the chosen policies.

The model is trained using the Action Robust Deep Deterministic Policy Gradient algorithm which requires a single parameter alpha that determines the adversarial network influence as in the probability to oppose the current state action. Furthermore during training it used an off-policy method, taking advantage of previous information. Moreover, the training implemented noise towards the action policy of nature Ornstein–Uhlenbeck to more accurately simulate real world noise.