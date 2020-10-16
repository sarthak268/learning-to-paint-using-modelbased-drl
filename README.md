# Learning to paint using Model-based DRL

Teach an agent to use a replicate an image by decomposing it to a set of strokes that can be painted on a canvas in some sequence. The agent will learn to paint the next stroke based on the current set of strokes on the canvas and the image being replicated. For this we follow the approach followed in paper Huang <i>et al.</i> alongside some of our own modifications. We aim to design a model-based TD3 approach as well as a model-based PPO approach and compare it to their model-based DDPG for the task of learning to paint.
<br>
<br>
Try it out on [Collaboratory](https://colab.research.google.com/drive/10MUpheaGSuTJvbWqem37Ju8XgWHD59VS) 

### Contributions
- Trained the actor model using TD3 instead of DDPG. Within TD3, we implemented a policy update using both Proximal Policy gradient, and naive policy optimization.
For TD3, we add an additional critic model in order to overcome the shortcomings of DDPG which is well known to overestimate the learnt value functions. 
PPO is an efficient version of TRPO, which uses a trust region to figure the direction and magnitude of gradient update
- Compared the quantitative as well as qualitative performance of the TD3 (PPO and naive) model with baseline (with DDPG).

### Requirements to visualize training graphs - TensorboardX
`pip install tensorboardX`  
`tensorboard --log_dir=<path to log folder> --port=<port>`  

### Saved Log files
- DDPG log files can be found [here](https://drive.google.com/drive/folders/1wwnKuTvGCdIsp-LW8GnUXYPHHy0X1a2L?usp=sharing)  
- TD3 log files can be found [here](https://drive.google.com/drive/folders/12a2aQzOdb2Nux4K94p81OJ4bS5g3JiCz?usp=sharing)  
- TD3-PPO log files can be found [here](https://drive.google.com/drive/folders/1US8Ik3_SpV-b1M9sYrgWQl4bJmd1psCw?usp=sharing) 

<a href="https://drive.google.com/drive/folders/14PAuod0_vA0IVl-7ryvYDzJW-YZ3Vvx4?usp=sharing">Link to the video results</a>
