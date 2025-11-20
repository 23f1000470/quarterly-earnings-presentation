---
marp: true
title: Product Documentation Presentation
author: 23f1000470@ds.study.iitm.ac.in
theme: custom
paginate: true
---

<!--
  Embedded custom theme for Marp slides.
  Keep this near the top so Marp picks it up as a theme.
-->
<style>
:root{
  --bg: #ffffff;
  --fg: #0b2545;
  --accent: #0066ff;
  --slide-padding: 48px;
}

section {
  background: var(--bg);
  color: var(--fg);
  padding: var(--slide-padding);
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
}

/* Title sizing */
h1 { font-size: 48px; margin-bottom: 8px; }
h2 { font-size: 32px; margin-bottom: 6px; }

/* Accent box - for notes/announcements */
.accent-box {
  padding: 18px;
  border-radius: 10px;
  background: linear-gradient(180deg, #f6fbff 0%, #eef6ff 100%);
  border: 1px solid rgba(0,102,255,0.12);
}

/* Make code blocks wrap on narrow screens */
pre {
  white-space: pre-wrap;
  word-break: break-word;
}

/* Footer for validators / humans */
.footer-email {
  text-align:center;
  font-size:0.9rem;
  opacity:0.9;
  margin-top:18px;
}

/* Helper: ensure background images cover */
.bg-cover { background-size: cover; background-position: center; }
</style>

<!-- Title slide -->
# Product Documentation Presentation
### Prepared by: **23f1000470&#64;ds.study.iitm.ac.in**

---

<!-- Slide with background image -->
<!-- _backgroundImage: https://images.unsplash.com/photo-1526378722484-c1d4c85e3d6c?w=1600&q=80&auto=format&fit=crop -->
<!-- _backgroundSize: cover -->
# Project Overview
This documentation provides end-to-end technical guidance for engineers and product teams.

---

# Key Features
- Version-controlled documentation (Markdown in Git)
- Exportable to PDF, HTML and PPT
- Developer-friendly formatting and automation
- CI-driven rendering and publishing

---

# Algorithmic Complexity (Math)
We often state complexity formally:

$$
T(n) = O(n \log n)
$$

Explain assumptions and whether this is average or worst-case.

---

# Complexity Derivation (Master Theorem)
1. Partition cost: \(O(n)\)  
2. Two recurrences: \(2T(n/2)\)  
By the Master theorem:
$$
T(n) = O(n \log n)
$$

---

# Custom Styled Notes
<div class="accent-box">
**Release Notes (v1.3.0)**

- New API endpoints for bulk export  
- Improved caching with LRU policy  
- OAuth2 refresh tokens enabled
</div>

---

# Code Example
```javascript
// Fetch docs index
async function fetchIndex() {
  const res = await fetch('/api/docs/index.json');
  return res.json();
}
