---
layout: page
title: Software
permalink: /software/
nav: true
nav_order: 4
description: R packages and templates.
---

<!-- Optional: tiny page-local styles to size the hex thumbnails nicely -->
<style>
  /* Keep it scoped to this page by prefixing with .page--software */
  .page--software .pub-thumb{width:120px;min-width:120px}
  .page--software .pub-thumb img{width:100%;height:auto;border-radius:12px;box-shadow:var(--shadow-1)}
  .page--software .pub-meta{padding-left:1rem}
  .page--software .pub-links .btn{margin-right:.35rem;margin-top:.35rem}
</style>

<div class="page--software">
  <div class="pub-list">

    <!-- Card 1 -->
    <article class="pub-card">
      <div class="pub-thumb">
        <img src="{{ '/assets/img/software/academicwriting_hex.png' | relative_url }}" alt="mypkg hex sticker">
      </div>
      <div class="pub-meta">
        <h3 class="pub-title">
          <a href="https://cran.r-project.org/package=mypkg" target="_blank" rel="noopener">mypkg</a>
        </h3>
        <div class="pub-venue">Tools for awesome analysis</div>
        <p class="pub-abstract">
          Minimal description (1–2 sentences) of what the package does and for whom.
        </p>
        <div class="pub-links">
          <a class="btn btn-sm" href="https://cran.r-project.org/package=mypkg" target="_blank" rel="noopener">CRAN</a>
          <a class="btn btn-sm" href="https://github.com/yourname/mypkg" target="_blank" rel="noopener">GitHub</a>
          <a class="btn btn-sm" href="https://yourname.github.io/mypkg" target="_blank" rel="noopener">Docs</a>
        </div>
      </div>
    </article>