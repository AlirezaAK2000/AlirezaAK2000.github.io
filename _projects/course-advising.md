---
layout: page
title: Knowledge-graph course-advising chatbot
description: A tutorial chatbot using RDF course relationships and LangGraph tools
  to answer course and prerequisite questions.
permalink: "/projects/course-advising/"
importance: 4
category: LLM applications
related_publications: false
---

**Educational open-source project · English-language tutorial**

I developed a chatbot around a fictional course catalogue to demonstrate how explicit relationships can ground an LLM application's tool use.

- Represented course details, credits, terms, prerequisites, and category relationships in RDF/Turtle.
- Implemented RDFLib access and prerequisite-chain and subclass traversal.
- Exposed fixed LangGraph tools for course discovery, course details, prerequisite retrieval, and checks against supplied completed courses.
- Published a hands-on tutorial in English with the implementation.

The tutorial uses a fictional course catalogue to demonstrate graph-grounded retrieval and prerequisite checks.

**Tools:** Python, RDFLib, RDF/Turtle, RDFS relationships, LangGraph.

[Watch the tutorial](https://youtu.be/YPNSFnqtBl4) · [View source code](https://github.com/AlirezaAK2000/knowledge_graph_tutorial)
