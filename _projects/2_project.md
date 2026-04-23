---
layout: page
title: "Industrial AI Platform — Midea Group"
description: "Digital Factory Brain · Optimization, VLM fine-tuning, and agentic MLOps"
img: assets/img/project_industrial_ai.png
importance: 2
category: Industry
---

<p class="project-hero-subtitle">
Architecting scalable decision-intelligence and vision-language agents to drive energy optimization and automate industrial safety operations across global manufacturing facilities.
</p>

<div class="kpi-grid">
  <div class="kpi-card">
    <div class="kpi-value kpi-value-sm">4h → &lt;10 min</div>
    <div class="kpi-label">Inspection Time<span class="kpi-sub">−95% reduction</span></div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value kpi-value-sm">2 wks → 0.5 d</div>
    <div class="kpi-label">Model Deployment Cycle<span class="kpi-sub">28× faster</span></div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">¥2.1M</div>
    <div class="kpi-label">Annual Savings per Plant</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">98.5%</div>
    <div class="kpi-label">Defect Recall<span class="kpi-sub">92% overall accuracy</span></div>
  </div>
</div>

<h2 class="project-section-title">Overview</h2>

As an **Algorithm Engineer** at Midea Group, I spearheaded the development of two core AI systems within the **"Digital Factory Brain"** initiative. My work bridged the gap between advanced predictive modeling, operations research, and large vision-language models (VLMs) — delivering robust, production-ready solutions that significantly reduced operational costs and mitigated safety risks.

<div class="pillar-card">
  <div class="pillar-badge">Pillar 1 · Optimization & ML</div>
  <h3>AI-Driven Micro-Grid Scheduling Agent</h3>

  <h4>Situation</h4>
  <p>Manufacturing plants faced exorbitant peak-hour electricity costs. While facilities had localized solar generation and battery storage, the highly stochastic nature of weather and dynamic factory loads made traditional, rule-based energy dispatch strategies highly inefficient.</p>

  <h4>Task</h4>
  <p>Design an autonomous scheduling agent to optimize battery charge/discharge cycles in real-time — maximizing energy arbitrage (buy low, discharge high) and minimizing carbon footprint.</p>

  <h4>Technical Execution</h4>
  <ul>
    <li><strong>Predictive Modeling.</strong> Developed a high-precision 24-hour forecasting model using <strong>XGBoost</strong> to predict solar power generation and factory load. Engineered complex features including rolling windows, time-lag variables, and real-time meteorological data.</li>
    <li><strong>Mathematical Optimization.</strong> Formulated a <strong>Mixed-Integer Linear Programming (MILP)</strong> model using the <strong>Gurobi</strong> solver. Translated complex, highly constrained physical and economic logic (battery degradation, dynamic pricing, concurrent charge/discharge restrictions) into mathematical constraints.</li>
    <li><strong>Dynamic Rolling Horizon.</strong> Implemented a robust closed-loop control mechanism executing rolling optimizations at 5-minute intervals, ensuring high resilience against real-world uncertainties (sudden weather shifts or production-line halts).</li>
    <li><strong>Causal Evaluation.</strong> Conducted rigorous <strong>Difference-in-Differences (DiD)</strong> analysis against control-group factories to isolate and scientifically prove the algorithm's direct economic contribution, stripping away seasonal or policy-driven confounders.</li>
  </ul>

  <h4>Results</h4>
  <ul>
    <li>Slashed predictive <strong>MAPE by 28%</strong>, creating a tighter search space for the optimization solver.</li>
    <li>Achieved annual direct energy cost savings of <strong>¥2.1M RMB</strong> at the pilot plant.</li>
    <li>Abstracted the logic into a modular architecture, enabling rapid deployment across <strong>34 global factories</strong> and contributing to significant ESG carbon-reduction targets.</li>
  </ul>

  <div class="tech-stack-grouped" style="margin-top: 1.25rem; margin-bottom: 0;">
    <div class="tech-group">
      <span class="tech-group-label">Tech Stack</span>
      <div class="tech-group-pills">
        <span class="pill">XGBoost</span>
        <span class="pill">Gurobi</span>
        <span class="pill">MILP</span>
        <span class="pill">Genetic Algorithms</span>
        <span class="pill">Causal Inference (DiD)</span>
      </div>
    </div>
  </div>
</div>

<div class="pillar-card">
  <div class="pillar-badge">Pillar 2 · LLM / VLM & MLOps</div>
  <h3>Autonomous Safety Inspection Agent</h3>

  <h4>Situation</h4>
  <p>Traditional industrial safety inspections required over 4 hours of manual effort, suffered from a "risk vacuum" between patrols, and relied on subjective human judgment — leading to inconsistent compliance reporting.</p>

  <h4>Task</h4>
  <p>Redefine the conventional object-detection workflow into an end-to-end <em>"Multi-modal to Structured Report"</em> generation system using cutting-edge Large Vision-Language Models (VLMs).</p>

  <h4>Technical Execution</h4>
  <ul>
    <li><strong>Parameter-Efficient Fine-Tuning (PEFT).</strong> Leveraged <strong>LoRA</strong> to fine-tune the foundational <strong>Qwen-VL</strong> model on 55,000+ proprietary domain images. Specifically targeted the Transformer <code>c_attn</code> and <code>mlp.c_proj</code> layers to "distill" expert safety standards into the model while keeping computational overhead near zero.</li>
    <li><strong>Active Learning & MLOps Pipeline.</strong> Architected a <em>human-in-the-loop</em> continuous learning system. High-confidence predictions automatically generated structured JSON reports, while low-confidence anomalies were routed to safety engineers. Corrected labels were automatically merged into nightly incremental training jobs — enabling the model to self-evolve.</li>
    <li><strong>Conversational Agent Workflow.</strong> Productized the complex machine learning pipeline into a conversational LLM agent. Empowered non-technical frontline workers to execute the full lifecycle — <em>Scene Definition → Data Upload → Auto-labeling → Model Fine-tuning</em> — using natural language.</li>
  </ul>

  <h4>Results</h4>
  <ul>
    <li>Achieved <strong>98.5% defect recall</strong> and <strong>92% overall detection accuracy</strong>, maintaining an <strong>800 ms</strong> inference response time.</li>
    <li>Compressed end-to-end factory inspection and reporting time by <strong>95%</strong> (from 4 hours to under 10 minutes).</li>
    <li>Reduced the iteration cycle for deploying models in new environments from <strong>2 weeks to 0.5 days</strong>, showcasing extreme scalability.</li>
  </ul>

  <div class="tech-stack-grouped" style="margin-top: 1.25rem; margin-bottom: 0;">
    <div class="tech-group">
      <span class="tech-group-label">Tech Stack</span>
      <div class="tech-group-pills">
        <span class="pill">Qwen-VL</span>
        <span class="pill">LoRA / PEFT</span>
        <span class="pill">Active Learning</span>
        <span class="pill">MLOps</span>
        <span class="pill">Prompt Engineering</span>
      </div>
    </div>
  </div>
</div>
