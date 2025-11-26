---
marp: true
theme: product-docs
paginate: true
_paginate: true
footer: "Product Docs | Email: 25ds1000231@ds.study.iitm.ac.in | Page ${page} / ${pages}"
title: "Product Documentation – Nimbus Core"
author: "Bipul Lahiri"
description: "Architecture, API, overview and complexity analysis"
---

<style>
/* @theme product-docs */
section {
  background: radial-gradient(circle at top left, #1e293b 0, #020617 45%, #000 100%);
  color: #e5e7eb;
  font-family: system-ui, sans-serif;
}

h1, h2, h3 {
  color: #fbbf24;
}

pre {
  background: rgba(15, 23, 42, 0.98);
  padding: 1rem;
  border-radius: .5rem;
  font-size: .85rem;
}

.badge {
  background: linear-gradient(90deg, #2563eb, #22c55e);
  padding: 0.2em 0.8em;
  border-radius: 99px;
  font-size: 0.7em;
  text-transform: uppercase;
}
</style>

<!-- _class: lead -->

# Nimbus Core  
Product Documentation

<span class="badge">Architecture · Operations · API</span>

---

## Contact

**Author:** Bipul Lahiri  
**Email:** 25ds1000231@ds.study.iitm.ac.in  

Documentation goals:

- Versioned in Git
- Developer-friendly and maintainable
- Auto-exportable to HTML/PDF/PPTX
- Centralized product truth

---

<!-- BACKGROUND IMAGE SLIDE -->
<!-- _backgroundImage: url('https://images.pexels.com/photos/1181467/pexels-photo-1181467.jpeg?auto=compress&cs=tinysrgb&w=1600') -->
<!-- _backgroundSize: cover -->
<!-- _backgroundColor: rgba(0,0,0,0.55) -->

# System Overview

- API Gateway  
- Orchestration Service  
- Worker nodes  
- Event & metrics pipeline  

---

## High-Level Architecture

```mermaid
graph TD
  A[Client] --> B[API Gateway]
  B --> C[Orchestrator]
  C --> D[Workers]
  C --> E[(Doc Store)]
  C --> F[(Metrics DB)]
