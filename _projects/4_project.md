---
layout: page
title: "Data Infrastructure & Predictive Marketing Analytics — Novo Nordisk"
description: Enterprise data warehouse modernization × SHAP-based marketing attribution
img: assets/img/6.jpg
importance: 3
category: Industry
---

<p class="project-hero-subtitle">
Spearheaded enterprise database modernization and built explainable ML attribution models to optimize pharmaceutical marketing ROI.
</p>

<div class="kpi-grid">
  <div class="kpi-card">
    <div class="kpi-value kpi-value-sm">4.2s → 2.8s</div>
    <div class="kpi-label">Query Latency<span class="kpi-sub">−33% improvement</span></div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value kpi-value-sm">5 DBs → 1</div>
    <div class="kpi-label">Unified Data System</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">¥2.0M</div>
    <div class="kpi-label">Budget Optimized<span class="kpi-sub">~$280K USD</span></div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">+23%</div>
    <div class="kpi-label">Projected ROI Lift</div>
  </div>
</div>

<h2 class="project-section-title">Overview</h2>

As a **Data Analyst** at Novo Nordisk (China), I wore dual hats spanning **Data Engineering** and **Data Science**. I collaborated closely with the **Microsoft China** team to modernize the company's fragmented data infrastructure, then leveraged this unified data to build predictive attribution models that fundamentally transformed how pharmaceutical promotional budgets were allocated.

<div class="pillar-card">
  <div class="pillar-badge">Pillar 1 · Data Engineering & BI</div>
  <h3>Enterprise Data Warehouse Modernization</h3>

  <h4>Situation</h4>
  <p>The business intelligence ecosystem was bottlenecked by data silos across <strong>5 heterogeneous legacy databases</strong>, leading to sluggish report rendering and frustrating user experiences for frontline business teams.</p>

  <h4>Task</h4>
  <p>Consolidate the underlying data architecture into a unified system and aggressively optimize query performance for downstream executive dashboards.</p>

  <h4>Technical Execution</h4>
  <ul>
    <li>Partnered with <strong>Microsoft China</strong> engineers to execute a seamless, company-wide SQL database migration.</li>
    <li>Audited and entirely refactored <strong>200+ complex stored procedures</strong> to ensure architectural consistency.</li>
    <li>Conducted deep execution-plan analysis to optimize sub-optimal SQL queries. Streamlined complex <strong>DAX</strong> expressions within the Power BI semantic data model to reduce computational overhead.</li>
  </ul>

  <h4>Results</h4>
  <ul>
    <li>Slashed core business report query latency by <strong>33%</strong> (from 4.2s to 2.8s).</li>
    <li>Significantly enhanced data retrieval efficiency and user experience for <strong>200+ cross-functional stakeholders</strong>.</li>
  </ul>

  <div class="tech-stack-grouped" style="margin-top: 1.25rem; margin-bottom: 0;">
    <div class="tech-group">
      <span class="tech-group-label">Tech Stack</span>
      <div class="tech-group-pills">
        <span class="pill">SQL Performance Tuning</span>
        <span class="pill">Data Warehouse</span>
        <span class="pill">DAX</span>
        <span class="pill">Power BI Semantic Model</span>
      </div>
    </div>
  </div>
</div>

<div class="pillar-card">
  <div class="pillar-badge">Pillar 2 · Data Science</div>
  <h3>ML-Driven Marketing Attribution & ROI Optimization</h3>

  <h4>Situation</h4>
  <p>Promotional budgets for pharmaceutical products were traditionally allocated based on heuristics and historical momentum, lacking rigorous visibility into which specific marketing levers actually drove sales conversions.</p>

  <h4>Task</h4>
  <p>Build an analytical framework to quantify the true impact of diverse marketing campaigns and mathematically optimize budget distribution.</p>

  <h4>Technical Execution</h4>
  <ul>
    <li>Ingested, cleansed, and aggregated high-dimensional historical sales and promotional data.</li>
    <li>Developed a predictive modeling framework utilizing <strong>Multivariate Regression</strong> to establish baseline relationships.</li>
    <li>Applied <strong>SHAP</strong> (SHapley Additive exPlanations) values to demystify the model — rigorously deconstructing the output to identify the marginal contribution (key drivers) of individual marketing factors on final sales conversion.</li>
    <li>Translated these complex statistical findings into an interactive <strong>Power BI</strong> dashboard, enabling leadership to interact with data-driven insights intuitively.</li>
  </ul>

  <div class="callout">
    <div class="callout-icon">💡</div>
    <div class="callout-body">
      <p class="callout-title">Focus on Model Interpretability</p>
      <p class="callout-text">
        In the pharmaceutical industry, model transparency is as critical as accuracy. By utilizing SHAP values, I transformed a <em>"black-box"</em> prediction into clear, actionable business drivers — directly building trust with non-technical marketing stakeholders.
      </p>
    </div>
  </div>

  <h4>Results</h4>
  <ul>
    <li>Delivered a data-backed budget allocation strategy that actively optimized a <strong>¥2,000,000 (~$280,000)</strong> promotional budget.</li>
    <li>Projected to lift overall marketing <strong>ROI by 23%</strong>, shifting the team from intuition-based to algorithm-driven financial planning.</li>
  </ul>

  <div class="tech-stack-grouped" style="margin-top: 1.25rem; margin-bottom: 0;">
    <div class="tech-group">
      <span class="tech-group-label">TechStack</span>
      <div class="tech-group-pills">
        <span class="pill">Python</span>
        <span class="pill">Multivariate Regression</span>
        <span class="pill">SHAP Values</span>
        <span class="pill">Marketing Attribution</span>
      </div>
    </div>
  </div>
</div>
