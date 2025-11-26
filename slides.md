---
marp: true
theme: product-docs
paginate: true
footer: "Product Documentation | 25ds1000231@ds.study.iitm.ac.in | Page ${page} / ${pages}"
---

<style>
/* @theme product-docs */
section {
  background: radial-gradient(circle at top left, #1e293b 0, #020617 45%, #000 100%);
  color: #e5e7eb;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}
h1, h2, h3 {
  color: #fbbf24;
}
pre {
  background: rgba(15, 23, 42, 0.98);
  padding: 1rem;
  border-radius: 0.5rem;
  font-size: 0.85rem;
}
</style>

<!-- _class: lead -->

# 📘 Product Documentation

Maintained with **Marp**  
Version-controlled & easily convertible to PDF, PPTX, HTML

---

# ✨ Features

- Markdown-based documentation  
- Custom theme (`product-docs`)  
- Page numbers in footer  
- Background image slide  
- Math equations for complexity  

---

# 📧 Contact

**Email:** 25ds1000231@ds.study.iitm.ac.in  

This deck is intended to be stored in Git  
and exported to multiple formats via Marp.

---

<!-- background image slide with ALL common syntaxes -->
<!-- _class: bg-slide -->
<!-- _backgroundImage: url("https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg") -->
<!-- _backgroundSize: cover -->
<!-- _backgroundColor: rgba(0,0,0,0.6) -->

![bg](https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg)

# 🌍 Background Image Slide

This slide demonstrates a **full background image**.  
Both Marp directive and `![bg](...)` syntax are used.

---

# ⚙️ Algorithmic Complexity

We document computational complexity for core routines:

\[
T(n) = O(n \log n)
\]

\[
T(n, m) = O(n \cdot m)
\]

---

# 🎨 Custom Styling Example

<style scoped>
h2 {
  color: #d6336c;
  font-style: italic;
}
</style>

## Styled Heading

This slide uses **scoped CSS** to style the heading.

---

# ✅ Summary

- Custom theme (`product-docs`)  
- Email: **25ds1000231@ds.study.iitm.ac.in**  
- Page numbers via `paginate: true`  
- At least one slide with a **background image**  
- Custom styling using Marp directives  
- Mathematical equations for algorithmic complexity
