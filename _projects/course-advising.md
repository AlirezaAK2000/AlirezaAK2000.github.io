---
layout: page
title: Ontology-grounded course-advising chatbot
description: An RDF-grounded chatbot using LangGraph tools to retrieve course information and check prerequisite chains.
permalink: "/projects/course-advising/"
importance: 2
featured: true
category: LLM applications
related_publications: false
---

**Independent open-source project**

I developed a chatbot around a fictional 20-course catalogue, connecting explicit course relationships to a language model through graph-backed tools and a Chainlit chat interface.

- Represented course details, credits, terms, prerequisites, and category relationships in RDF/Turtle.
- Implemented RDFLib access and prerequisite-chain and subclass traversal.
- Exposed fixed LangGraph tools for course discovery, course details, prerequisite retrieval, and checks against supplied completed courses.
- Connected the tools through a LangGraph workflow and displayed answers and tool results in Chainlit.

The implementation supports graph-grounded retrieval and checks against the completed courses supplied by the user. The catalogue is fictional, and prerequisite and category traversal use explicit graph relationships.

**Tools:** Python, RDFLib, RDF/Turtle, RDFS relationships, LangGraph, Chainlit.

[View source code](https://github.com/AlirezaAK2000/knowledge_graph_tutorial) · [Watch the project video](https://youtu.be/YPNSFnqtBl4)
