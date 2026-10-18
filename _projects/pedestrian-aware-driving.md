---
layout: page
title: Pedestrian-aware driving in CARLA
description: A custom image-based environment and DQN, PPO, and discrete SAC agents
  for pedestrian collision avoidance.
permalink: "/projects/pedestrian-aware-driving/"
importance: 2
category: research
related_publications: false
---

**B.Sc. thesis · Amirkabir University of Technology · completed June 2023**

I developed a CARLA simulation for studying pedestrian-aware longitudinal driving with deep reinforcement learning. The agent observes stacked semantic-segmentation frames and chooses whether to accelerate, coast, or brake; steering is fixed for the selected routes.

### Contributions

- Implemented a synchronous CARLA environment with vehicle and pedestrian spawning, camera observations, collision and lane-invasion sensors, and episode cleanup.
- Developed convolutional policies and training workflows for DQN, PPO, and discrete SAC in PyTorch.
- Designed rewards that combine route progress with penalties for nearby pedestrians and collisions.
- Added checkpointing, TensorBoard logging, and an evaluation harness for comparing trained agents across routes and pedestrian populations.

**Supervisor:** Prof. Ahmad Nickabadi.  
**Tools:** Python, PyTorch, CARLA, CUDA, NumPy, TensorBoard.

[View source code](https://github.com/AlirezaAK2000/Bsc-Project)
