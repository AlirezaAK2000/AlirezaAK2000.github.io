---
layout: page
title: Knowledge-graph navigation with verifiable rewards
description: Training language models to navigate knowledge graphs through multi-step tool use, supervised fine-tuning, and verifiable rewards.
permalink: "/projects/kg-navigation-rlvr/"
importance: 3
featured: true
category: research
related_publications: false
---

**Independent research project**

How can a language model learn to navigate a knowledge graph through a sequence of tool calls and receive rewards that can be checked against the graph?

I built a synthetic academic knowledge graph and a training pipeline for studying this question. The model discovers available relations, retrieves neighboring entities, and submits an answer. A separate verifier checks correctness against the graph.

### Approach

- Constructed a reproducible RDF/Turtle graph with 2,000 entities and 5,000 navigation facts across eight entity types and 16 relation types.
- Generated one- to four-hop questions with executable relation programs, reference paths, and grouped splits that separate underlying graph queries.
- Implemented a discovery-constrained tool environment with explicit interaction budgets, keeping gold answers separate from model-visible observations.
- Built a Qwen3-1.7B training pipeline using supervised fine-tuning (SFT), group relative policy optimization (GRPO), and NF4 QLoRA, with answer and retrieval rewards, assistant-only loss masking, and trajectory diagnostics.
- Compared vanilla, SFT-only, SFT + GRPO, and GRPO-only policies on the same test questions, using disjoint query pools for SFT and GRPO.

### Recorded results

The saved single-seed experiment evaluated every variant on the same **30 test questions**:

| Variant    | Correct answers | Test accuracy |
| ---------- | --------------- | ------------- |
| Vanilla    | 4/30            | 13.3%         |
| SFT        | 16/30           | 53.3%         |
| GRPO only  | 15/30           | 50.0%         |
| SFT + GRPO | 20/30           | 66.7%         |

These results describe one small-sample experiment. Training uses one- to three-hop queries, while evaluation includes four-hop queries. Train and test share a fictional academic graph, so this comparison measures new queries over known facts rather than transfer to an unseen graph.

**Tools:** Python, RDFLib, RDF/Turtle, PyTorch, Qwen3, Transformers, TRL, PEFT, LoRA/QLoRA, Jupyter.

[View source code](https://github.com/AlirezaAK2000/kg-navigation-rlvr) · [Watch the project video](https://youtu.be/3DPmP_FSbZA)
