---
marp: true
title: Product Documentation Presentation
author: 23f1000470@ds.study.iitm.ac.in
theme: custom
paginate: true
---

<!--
  Custom theme for Marp.
  This CSS block declares variables and styles used across slides.
  Marp will pick it up as an embedded style theme.
-->
<style>
/* Theme variables */
:root {
  --color-bg: #ffffff;
  --color-foreground: #102a43;
  --color-accent: #0066ff;
  --slide-padding: 40px;
}

/* Base slide styles */
section {
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  color: var(--color-foreground);
  padding: var(--slide-padding);
}

/* Title sizes */
h1 { font-size: 48px; margin-bottom: 8px; }
h2 { font-size: 34px; margin-bottom: 8px; }

/* Custom accent box for notes/announcements */
.marp-accent {
  border-radius: 10px;
  padding: 18px;
  background: linear-gradient(180deg, #f0f8ff 0%, #eef6ff 100%);
  border: 1px solid rgba(0,102,255,0.12);
}

/* Make code blocks wrap nicely on smaller screens */
pre {
  white-space: pre-wrap;
  word-break: break-word;
}

/* Footer for validators / simple scrapers: use HTML entity for @ */
.footer-email {
  text-align: center;
  font-size: 0.9rem;
  opacity: 0.9;
  margin-top: 18px;
}

/* Background-image helper class (when using inline background directives, keep this for fallback) */
.bg-cover {
  background-size: cover;
  background-position: center;
}
</style>

<!-- Title slide -->
# Product Documentation Presentation
### Prepared by: **23f1000470&#64;ds.study.iitm.ac.in**

---

<!-- Slide with background image (Marp directive) -->
<!-- _backgroundImage: https://images.unsplash.com/photo-1526378722484-c1d4c85e3d6c?w=1600&q=80&auto=format&fit=crop -->
<!-- _backgroundSize: cover -->
# Project Overview

This documentation provides end-to-end technical guidance for engineers and product teams.

---

# Key Features

- Version-controlled docs (Markdown in Git)
- Exportable to PDF, HTML and PPT
- Developer-friendly formatting and automation
- Easy to maintain via CI/CD

---

# Algorithmic Complexity

We use formal notation for algorithmic complexity and proofs.

$$
T(n) = O(n \log n)
$$

Explain the dominant term and assumptions (average / worst-case).

---

# Example: Complexity Derivation

1. Partition cost: \(O(n)\)  
2. Recursive halves: \(2T(n/2)\)  
3. By Master theorem: \(T(n) = O(n \log n)\)

---

# Custom Styled Slide

<div class="marp-accent">
**Release Notes (v1.3.0)**

- New API endpoints for bulk export  
- Improved caching layer (redis LRU policy)  
- Authentication module: OAuth2 + refresh tokens  
</div>

---

# Code Snippet (syntax highlighting)

```javascript
// Example: fetch docs index
async function fetchIndex() {
  const res = await fetch('/api/docs/index.json');
  return res.json();
}
