---
layout: page
title: Robot visual memory
description: Searchable visual memory using vision-language models, Neo4j scene graphs, and natural-language image retrieval.
permalink: "/projects/robot-visual-memory/"
importance: 1
featured: true
category: computer vision
related_publications: false
---

**Independent open-source project**

How can a robot's recorded observations become a searchable memory with evidence that can be inspected?

I built a pipeline that turns OpenEQA/HM3D indoor exploration recordings into a graph of objects, attributes, states, and spatial relationships. Natural-language questions retrieve relevant frames together with their captions and matched graph constraints.

### Approach

- Sampled frames across an ordered recording and used vision-language models to extract captions and scene graphs, caching the results for reuse.
- Stored environments, frames, and frame-scoped object observations in Neo4j, retaining attributes, states, and directed spatial relationships.
- Implemented a local rule-based question parser and parameterized Cypher queries to rank frames by matching objects, attributes, states, and relationships.
- Returned original images and supporting graph evidence through a retrieval notebook.

### Recorded pilot

One 400-frame episode was sampled to 200 frames, producing **2,113 object observations** and **2,036 relationships**. These counts describe the indexed visual memory; retrieval accuracy was not benchmarked.

The system retrieves evidence from recorded observations. Objects are scoped to individual frames, spatial directions are image-relative, and the parser can omit qualifiers. Results can be partial matches rather than complete answers.

**Tools:** Python, vision-language models, Neo4j, Cypher, Jupyter, Docker Compose.

[View source code](https://github.com/AlirezaAK2000/robot-visual-memory) · [Watch the project video](https://youtu.be/EFQhyWLB4j4)
