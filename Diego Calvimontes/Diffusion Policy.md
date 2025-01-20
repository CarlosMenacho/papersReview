
This is Imitation Learning. The model is based on the Diffusion model, which is a generative model that can learn the distribution of a dataset and therefore be able to create new data points from this distribution. In the paper they formulate the Denoising Diffusion Probabilistic Models. This works having an initial sampled action sequence, then it's injected random noise into the model and gradually denoising it up to a noiseless action.
![[Pasted image 20250119014739.png]]

They tried with two different approaches, the first one was with a 1D temporal CNN that is from another paper and it was modified and the second it was a Time-series diffusion transformer witch was based in the architecture from minGPT to reduce the over-smoothing effect in CNN models.
Both of them works great but the CNN performs poorly when the desired action sequence changes quickly and sharply through time and the transformer is more sensitive to hyperparameters.
An advantage of Diffusion Policy is that has a great synergy with position control than velocity control.