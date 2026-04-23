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

<p class="project-sub-title">System Architecture — Dual-Routing Decision Flow</p>

<div class="branch-diagram">
  <div class="branch-single">
    <div class="branch-node-label">Input</div>
    <div class="branch-node-title">User Query</div>
  </div>

  <div class="branch-arrow-down">↓</div>

  <div class="branch-decision">
    <div class="branch-node-title">Agentic LLM Router</div>
    <div class="branch-node-sub">DeepSeek-Chat · Function Calling</div>
  </div>

  <div class="branch-fork">
    <svg viewBox="0 0 620 36" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
      <line x1="310" y1="0" x2="310" y2="16" stroke="currentColor" stroke-width="2"/>
      <line x1="90" y1="16" x2="530" y2="16" stroke="currentColor" stroke-width="2"/>
      <line x1="90" y1="16" x2="90" y2="30" stroke="currentColor" stroke-width="2"/>
      <line x1="530" y1="16" x2="530" y2="30" stroke="currentColor" stroke-width="2"/>
      <polygon points="84,28 96,28 90,36" fill="currentColor"/>
      <polygon points="524,28 536,28 530,36" fill="currentColor"/>
    </svg>
  </div>

  <div class="branch-split">
    <div class="branch-node">
      <div class="branch-node-label">Branch 1 · Domain</div>
      <div class="branch-node-title">SemanticRetriever</div>
      <div class="branch-node-sub">FAISS + gte-small-zh</div>
    </div>
    <div class="branch-node">
      <div class="branch-node-label">Branch 2 · Recency</div>
      <div class="branch-node-title">WebSearchTool</div>
      <div class="branch-node-sub">DuckDuckGo API</div>
    </div>
  </div>

  <div class="branch-merge">
    <svg viewBox="0 0 620 36" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
      <line x1="90" y1="0" x2="90" y2="20" stroke="currentColor" stroke-width="2"/>
      <line x1="530" y1="0" x2="530" y2="20" stroke="currentColor" stroke-width="2"/>
      <line x1="90" y1="20" x2="530" y2="20" stroke="currentColor" stroke-width="2"/>
      <line x1="310" y1="20" x2="310" y2="32" stroke="currentColor" stroke-width="2"/>
      <polygon points="304,30 316,30 310,38" fill="currentColor"/>
    </svg>
  </div>

  <div class="branch-single">
    <div class="branch-node-label">Aggregation</div>
    <div class="branch-node-title">Context Assembly</div>
    <div class="branch-node-sub">retrieve → reason → generate</div>
  </div>

  <div class="branch-arrow-down">↓</div>

  <div class="branch-final branch-single">
    <div class="branch-node-title">Final Response</div>
  </div>
</div>

<p class="diagram-caption">The agent chooses retrieval strategy per query — domain knowledge routes to the private vector store, time-sensitive queries route to the web.</p>

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
