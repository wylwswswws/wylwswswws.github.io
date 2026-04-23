---
layout: page
title: "Agentic RAG System for Real-Time Knowledge Retrieval"
description: Dual-routing RAG agent · Tool-calling · LLM-as-a-Judge evaluation pipeline
img: assets/img/project_agentic_rag.png
importance: 1
category: Academic
---

<p class="project-hero-subtitle">
Architecting a dual-routing Retrieval-Augmented Generation (RAG) agent with tool-calling capabilities and an automated LLM-as-a-Judge evaluation pipeline.
</p>

<div class="kpi-grid">
  <div class="kpi-card">
    <div class="kpi-value">+15%</div>
    <div class="kpi-label">QA Quality Score<span class="kpi-sub">vs. naive RAG baseline</span></div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">≤ 2s</div>
    <div class="kpi-label">Avg. Response Latency</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">3,000+</div>
    <div class="kpi-label">Auto-Evaluated QA Pairs</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">100%</div>
    <div class="kpi-label">Private Deployment<span class="kpi-sub">on-prem · zero data leakage</span></div>
  </div>
</div>

<h2 class="project-section-title">Overview</h2>

Engineered an advanced, locally deployed **Agentic RAG system** designed to answer complex, fact-based queries. By dynamically routing between a private vector database and real-time web search, the system overcomes the notorious **"knowledge cutoff"** limitation of traditional Large Language Models and significantly reduces hallucinations.

<h2 class="project-section-title">Challenge</h2>

Traditional RAG pipelines rely heavily on static local databases, rendering them ineffective for queries requiring up-to-date or temporal information. Furthermore, standard implementations lack the *"reasoning"* capability to decide **when** to search the web versus **when** to query local knowledge — leading to inefficient retrieval and compromised response accuracy.

<h2 class="project-section-title">Technical Approach & Execution</h2>

**Dual-Routing Retrieval Architecture.** Designed a hybrid data-fetching pipeline. Built an offline semantic index using **FAISS** and **gte-small-zh** embeddings for deep, domain-specific knowledge retrieval. In parallel, integrated **DuckDuckGo APIs** to facilitate real-time, online information extraction for trending topics.

**Agentic Reasoning via Tool Calling.** Leveraged the **DeepSeek-Chat** model's native **Function Calling** mechanisms to encapsulate two core tools: `SemanticRetriever` and `WebSearchTool`. Empowered the LLM to act as an autonomous agent that dynamically decides the optimal retrieval strategy based on user intent — creating a robust *"Retrieve → Reason → Generate"* closed-loop workflow.

<div class="callout">
  <div class="callout-icon">💡</div>
  <div class="callout-body">
    <p class="callout-title">Beyond Naive RAG: Why Agentic Routing?</p>
    <p class="callout-text">
      A static RAG pipeline treats every query identically. An <strong>agentic</strong> architecture lets the LLM reason about <em>intent</em> first — fetching from the private vector store for stable domain knowledge, or calling the web for time-sensitive queries. This mirrors how a human expert approaches research.
    </p>
  </div>
</div>

**Automated Evaluation Pipeline (LLM-as-a-Judge).** To rigorously quantify system performance, I constructed an automated evaluation framework. Deployed DeepSeek-Chat as an impartial *"judge"* to score **3,000+ real-world QA pairs** across three distinct dimensions: **Correctness, Completeness, and Timeliness**.

<h2 class="project-section-title">System Impact</h2>

- The agentic routing mechanism boosted comprehensive **QA quality score by 15%** compared to a naive RAG baseline.
- Achieved highly optimized average **response latency of ≤ 2 seconds**, ensuring a seamless real-time user experience while running entirely in a **privately deployed environment** for maximum data privacy.
- Established a reusable automated evaluation harness that can benchmark any future RAG / agent iteration against a standardized rubric.

<h2 class="project-section-title">Tech Stack</h2>

<div class="tech-stack-grouped">
  <div class="tech-group">
    <span class="tech-group-label">LLM & Frameworks</span>
    <div class="tech-group-pills">
      <span class="pill">DeepSeek-Chat</span>
      <span class="pill">Agentic Workflow</span>
      <span class="pill">Tool Calling</span>
    </div>
  </div>
  <div class="tech-group">
    <span class="tech-group-label">Vector Search & Embedding</span>
    <div class="tech-group-pills">
      <span class="pill">FAISS</span>
      <span class="pill">gte-small-zh</span>
    </div>
  </div>
  <div class="tech-group">
    <span class="tech-group-label">Evaluation</span>
    <div class="tech-group-pills">
      <span class="pill">LLM-as-a-Judge</span>
      <span class="pill">Automated Testing Pipeline</span>
    </div>
  </div>
</div>
