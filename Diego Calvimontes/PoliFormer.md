The main topic of the paper is about a policy transformer to use in a simulated robot, that when its pass to a real robot you don't have to do any fine-tuning to make the robot work in a real environment.

In this paper there are many other technologies which are implemented in the robot, it has a one-hot embedding layer to give it instructions, a camera with object recognition. The dataset used is ProcTHOR-10K, which has several simulated house environments to test the robots and for the agent is used LoCoBot. 

![[Pasted image 20250114145306.png]]

 Also was used the Strecht RE-1 agent in the dataset AI2-THOR but it was too slow so its movement was approximate via a teleportation-with-collision-checks.
![[Pasted image 20250114154051.png]]

#### PoliFormer Architecture
![[Pasted image 20250114150436.png]]
The first part is an ego-centric RGB observation using the camera, they choose DINOv2 for the dense prediction and sin-to-real transfer abilities.

To get the goal specification its use an encoder, for LoCoBot is used a noe-hot embedding layer and it use EmbCLIP for the ObjectNav Benchmarks. In other hand the benchmarks for Stretch RE-1 are the same as the SPOC and it is used FLAN-T5 small model to encode the given natural language goal

The central part consist in a non-causal transformer state encoder that receives the visual representation, the goal feature, and an embedding of a STATE token and returns the corresponding STATE token as the state feature vector. After that, it has a causal transformer decoder to perform explicit memory modeling over time, enabling long-horizon and short-horizon planning, it use a KV-cache to reduce the required time (t$^2$) to compute the representation in t.

#### Scalable RL Training Recipe
They parallelize the training process using multi-node training, they use 192 parallel rollouts for Stretch RE-1 agents and 384 for LoCoBot agents. Also it is used DD-PPO with 4 nodes and a total of 32 A6000 GPUs and 512 CPU cores. they train the agent for 4.5 days.