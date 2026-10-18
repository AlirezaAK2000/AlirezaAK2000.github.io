---
layout: page
title: research
permalink: /research/
description: Learning with explicit knowledge, language-model priors, and uncertainty.
nav: true
nav_order: 1
---

## LLM-generated priors for reinforcement learning

Deep reinforcement learning can require substantial interaction before useful behavior emerges. My M.Sc. thesis studies whether qualitative knowledge from a large language model can be converted into executable policies that help an agent learn more efficiently.

I developed a pipeline that transforms structured task descriptions into fuzzy rule-based controllers implemented in PyTorch. An uncertainty-aware arbitration mechanism uses MC dropout to choose between these fixed controllers and a learned TD3 policy. The language model generates priors before training; it is not called at each environment step.

I evaluate the approach using multi-seed experiments and statistical analysis on MuJoCo, with additional evaluation on Meta-World. The work examines both useful and misleading priors and the limits of uncertainty-based selection.

**Thesis:** Improving the Sample Efficiency of Deep Reinforcement Learning Using Large Language Model Priors.  
**Institution:** University of Tehran · Cognitive Systems Lab.  
**Advisors:** Prof. Majid Nili Ahmadabadi and Prof. Babak Nadjar Araabi.  
**Expected completion:** January 2027.

[Read the project overview]({{ '/projects/llm-fuzzy-priors/' | relative_url }})

## Manuscript in preparation

**Sample-Efficient Deep Reinforcement Learning with LLM-Generated Fuzzy Prior Policies.**

Status: **manuscript in preparation**.

## Earlier research

- **Pedestrian-aware driving:** compared DQN, PPO, and discrete SAC for longitudinal control and collision avoidance in a custom CARLA environment. [Project and code]({{ '/projects/pedestrian-aware-driving/' | relative_url }}).
- **Controlled image generation:** researched StyleGAN and GAN inversion as a research assistant at Amirkabir University of Technology, September 2021–March 2022.
