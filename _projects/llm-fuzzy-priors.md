---
layout: page
title: LLM-generated fuzzy priors for RL
description: Executable fuzzy controllers and uncertainty-aware arbitration for sample-efficient
  deep reinforcement learning.
permalink: "/projects/llm-fuzzy-priors/"
importance: 1
category: research
related_publications: false
---

**M.Sc. thesis · University of Tehran · ongoing, expected January 2027**

Can knowledge from a language model become a useful control prior without requiring language-model calls during environment interaction?

### Approach

- Built a LangGraph pipeline to generate structured fuzzy rules from task, state, and action descriptions.
- Implemented zero-order Takagi–Sugeno–Kang fuzzy inference in PyTorch.
- Integrated multiple fixed fuzzy policies with TD3 using an auxiliary MC-dropout critic and uncertainty-aware action arbitration.
- Evaluated in MuJoCo and Meta-World, using multi-seed experiments, controlled ablations, and statistical analysis.

The MuJoCo experiments cover six locomotion tasks, five training seeds, and 600,000 environment steps per condition. I also evaluate the approach on Meta-World. Findings remain part of ongoing research.

**Advisors:** Prof. Majid Nili Ahmadabadi and Prof. Babak Nadjar Araabi.  
**Affiliation:** Cognitive Systems Lab, University of Tehran.  
**Related manuscript:** _Sample-Efficient Deep Reinforcement Learning with LLM-Generated Fuzzy Prior Policies_ — in preparation.
