---
layout: page
title: Manufacturing root-cause assistant
description: An RDF-grounded assistant that connects operational observations to possible
  fault causes, checks, and corrective actions.
permalink: "/projects/manufacturing-knowledge-graph/"
importance: 3
category: LLM applications
related_publications: false
---

**Independent open-source project**

I built an assistant that combines a manufacturing ontology with structured LLM extraction, custom Python rules, and deterministic graph traversal.

- Modelled parameters, symptoms, failure modes, and potential causes in RDF/Turtle with RDFLib.
- Used structured extraction to turn natural-language observations into inputs for numeric checks and symptom mappings.
- Traversed graph relationships to return potential causes, supporting checks, procedures, and corrective actions.
- Added deterministic pipeline tests for a threshold violation and an in-range measurement.

The prototype uses demonstration manufacturing data, custom checks, and graph traversal.

**Tools:** Python, RDF, Turtle, RDFLib, Gemini structured extraction.

[View source code](https://github.com/AlirezaAK2000/production-support-kg)
