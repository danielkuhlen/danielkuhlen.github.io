---
layout: page
title: Software
permalink: /software/
nav: true
nav_order: 4
description: R packages and templates.
---

<!-- Inline page-specific styling -->
<style>
  .page--software .pub-card {
    display: flex;
    align-items: center;
    margin-bottom: 2rem;
  }

  .page--software .pub-thumb {
    width: 120px;
    min-width: 120px;
    flex-shrink: 0;
  }

  .page--software .pub-thumb img {
    width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: var(--shadow-1);
  }

  .page--software .pub-meta {
    padding-left: 1.5rem;
  }

  .page--software .pub-links .btn {
    margin-right: 0.35rem;
    margin-top: 0.35rem;
  }

  /* Optional: make it stack vertically on small screens */
  @media (max-width: 600px) {
    .page--software .pub-card {
      flex-direction: column;
      align-items: flex-start;
    }

    .page--software .pub-meta {
      padding-left: 0;
      padding-top: 1rem;
    }
  }
</style>

<div class="page--software">
  <div class="pub-list">

    <!-- Card 1 -->
    <article class="pub-card">
      <div class="pub-thumb">
        <img src="{{ '/assets/img/software/academicwriting_hex.png' | relative_url }}" alt="academicwritingr hex sticker">
      </div>
      <div class="pub-meta">
        <h3 class="pub-title">
          <a href="https://github.com/danielkuhlen/academicwriting" target="_blank" rel="noopener">academicwriting</a>
        </h3>
        <div class="pub-venue">
          A Quarto template for a reproducible, integrated and reproducible writing process. that consolidates Quarto templates for academic articles, abstracts, pre-analysis plans,
          conference presentations, and R&R memos, keeping all files in a clean, organized structure.
        <div class="pub-links">
          <a class="btn btn-sm" href="https://github.com/danielkuhlen/academicwriting" target="_blank" rel="noopener">GitHub</a>
        </div>
      </div>
    </article>

  </div>
</div>