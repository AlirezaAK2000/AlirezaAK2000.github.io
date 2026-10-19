---
layout: page
title: tutorials
permalink: /tutorials/
description: English-language tutorials on building LLM applications.
nav: true
nav_order: 4
---

I create English-language tutorials about LLM applications on [The AI Tutorial Guy](https://www.youtube.com/@TheAITutorialGuy), a channel I started in September 2026.

## Build a ChatGPT Plugin with Python and MCP — Beginner Tutorial

Build a Movie Night Planner plugin for ChatGPT using Python, the Model Context Protocol (MCP), Peewee, and SQLite. The tutorial covers searching IMDb movie data by genre, runtime, and saved status, recommending movies, and keeping a watchlist that persists across server restarts.

The local server exposes two MCP tools, `search_movies` and `add_to_watchlist`, and connects to ChatGPT through OpenAI’s Secure MCP Tunnel.

[Watch on YouTube](https://youtu.be/cyvovk1j0eM)

## Knowledge graphs and ontologies for LLM chatbots

This hands-on tutorial builds a course-advising chatbot around a fictional RDF/Turtle course catalogue. It demonstrates representing domain relationships, retrieving graph-grounded information with RDFLib, and exposing graph access through LangGraph tools.

[Watch on YouTube](https://youtu.be/YPNSFnqtBl4) · [Source code](https://github.com/AlirezaAK2000/knowledge_graph_tutorial) · [Project overview]({{ '/projects/course-advising/' | relative_url }})
