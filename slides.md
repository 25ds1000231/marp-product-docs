---
marp: true
theme: product-docs
paginate: true
_paginate: true
footer: "Product Docs – v1.0 | 25ds1000231@ds.study.iitm.ac.in | Page ${page} / ${pages}"
title: "Product Documentation – Nimbus Core"
description: "Architecture, API surface, and operational workflows"
author: "Bipul Lahiri"
---

<style>
/* @theme product-docs */
section {
  background: radial-gradient(circle at top left, #1e293b 0, #020617 45%, #000 100%);
  color: #e5e7eb;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
  padding: 2.5rem;
}

h1, h2, h3 {
  color: #fbbf24;
  letter-spacing: 0.02em;
}

code, pre {
  font-family: "JetBrains Mono", ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
}

pre {
  background: rgba(15, 23, 42, 0.98);
  border-radius: 0.75rem;
  padding: 1rem 1.25rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.6);
  font-size: 0.8rem;
}

code {
  background: rgba(15, 23, 42, 0.9);
  border-radius: 0.4rem;
  padding: 0.1em 0.35em;
}

section.lead {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: center;
}

.badge {
  display: inline-block;
  background: linear-gradient(90deg, #2563eb, #22c55e);
  padding: 0.2em 0.8em;
  border-radius: 999px;
  font-size: 0.7em;
  text-transform: uppercase;
  letter-spacing: 0.12em;
}

.meta {
  font-size: 0.8em;
  opacity: 0.8;
  margin-top: 1rem;
}

.grid-2 {
  display: grid;
  grid-template-columns: 1.2fr 1fr;
  gap: 1.75rem;
  align-items: flex-start;
}

.callout {
  border-left: 4px solid #38bdf8;
  padding-left: 0.9rem;
  font-size: 0.9em;
  opacity: 0.95;
}

table {
  border-collapse: collapse;
  width: 100%;
  font-size: 0.85em;
}

th, td {
  border: 1px solid rgba(148, 163, 184, 0.4);
  padding: 0.4rem 0.6rem;
}

th {
  background: rgba(15, 23, 42, 0.9);
}

.kpi-pill {
  display: inline-block;
  padding: 0.1em 0.6em;
  border-radius: 999px;
  background: rgba(34, 197, 94, 0.1);
  border: 1px solid rgba(34, 197, 94, 0.5);
  font-size: 0.75em;
}
</style>

<!-- _class: lead -->

# Nimbus Core  
Product Documentation

<span class="badge">Architecture · API · Operations</span>

---

**Owner:** Bipul Lahiri  
**Email:** 25ds1000231@ds.study.iitm.ac.in  

- Version-controlled with Git
- Written in Marp-flavoured Markdown
- Exportable to **HTML**, **PDF**, or **PPTX**
- Optimized for engineering + stakeholder audiences

---

## Documentation Goals

- Provide a **single source of truth** for the product
- Keep docs **close to the code** in Git
- Enable:
  - Developer onboarding
  - Architecture reviews
  - Incident post-mortems
- Make it easy to export:
  - HTML slides for web
  - PDF for offline review
  - PPTX for executive presentations

---

<!-- _class: lead -->
<!-- _backgroundImage: url('https://images.pexels.com/photos/1181467/pexels-photo-1181467.jpeg?auto=compress&cs=tinysrgb&w=1600') -->
<!-- _backgroundSize: cover -->
<!-- _backgroundColor: rgba(0,0,0,0.65) -->

# System Overview

High-level architecture of **Nimbus Core**  
and its integration points.

---

## High-Level Architecture

<div class="grid-2">

<div>

**Core components**

- API Gateway  
- Orchestration Service  
- Worker Pool (Async jobs)  
- Document Store (JSON / blobs)  
- Metrics & Logging pipeline  

</div>

<div>

```mermaid
graph TD
  A[Client] --> B[API Gateway]
  B --> C[Orchestrator]
  C --> D[Workers]
  C --> E[(Doc Store)]
  C --> F[(Metrics DB)]
