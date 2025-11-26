---
marp: true
theme: product-docs
paginate: true
footer: "Email: 25ds1000231@ds.study.iitm.ac.in | Page ${page} / ${pages}"
title: "Product Documentation – Nimbus Core"
author: "Bipul Lahiri"
description: "Architecture, API overview and complexity analysis"
---

<style>
/* @theme product-docs */
section {
  background: radial-gradient(circle at top left, #1e293b 0, #020617 45%, #000 100%);
  color: #e5e7eb;
  font-family: system-ui, sans-serif;
}
h1,h2,h3 { color: #fbbf24; }
pre {
  background: rgba(15, 23, 42, 0.98);
  padding: 1rem;
  border-radius: 6px;
}
</style>

# Nimbus Core  
Product Documentation

---

## Contact

**Author:** Bipul Lahiri**  
**Email:** 25ds1000231@ds.study.iitm.ac.in**

---

<!-- backgroundImage: url("https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg") -->
<!-- backgroundSize: cover -->
<!-- backgroundColor: rgba(0, 0, 0, 0.5) -->

# Platform Architecture

- API Gateway  
- Orchestration engine  
- Workers  
- Metrics and logs  

---

## Architecture Diagram

```mermaid
graph TD
  A[Client] --> B[API Gateway]
  B --> C[Orchestrator]
  C --> D[Workers]
  C --> E[(Doc Store)]
  C --> F[(Metrics DB)]
