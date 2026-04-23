---
layout: page
title: "AI-Driven Demand Forecasting & Inventory Optimization"
description: Wharton AI & Analytics Accelerator × Spencer's Gifts
img: assets/img/project_forecasting.png
importance: 1
category: Industry
---

<p class="project-hero-subtitle">
Architecting a scalable hybrid machine learning pipeline to capture non-linear market dynamics and drive data-informed retail strategies.
</p>

<div class="kpi-grid">
  <div class="kpi-card">
    <div class="kpi-value">91.2%</div>
    <div class="kpi-label">Forecast Accuracy</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">+25%</div>
    <div class="kpi-label">Sales Efficiency</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">−18%</div>
    <div class="kpi-label">Excess Inventory</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">500+</div>
    <div class="kpi-label">Retail Stores Empowered</div>
  </div>
</div>

<h2 class="project-section-title">Context & Challenge</h2>

As a **Data Scientist** leading the Wharton AI & Analytics Accelerator Team, I partnered with **Spencer's Gifts**, a major specialty retailer with 500+ locations. The business was struggling with severe inventory mismatches: frequent stockouts of highly viral, pop-culture IP merchandise, and capital-draining overstock of slow-moving items. Traditional time-series forecasting models fell short — they relied solely on historical sales and completely missed the sudden, non-linear demand spikes driven by social media virality and rapid market trends.

<h2 class="project-section-title">Task</h2>

Transition the company from *"experience-based"* to *"data-driven"* inventory management. This required building an end-to-end scalable data pipeline and an advanced predictive architecture capable of digesting unstructured external signals, identifying causal relationships, and delivering highly accurate SKU-level forecasts.

<h2 class="project-section-title">Technical Approach & Execution</h2>

<p class="project-sub-title">End-to-End System Architecture</p>

<div class="arch-diagram">
  <div class="arch-node">
    <div class="arch-node-stage">01 · Source</div>
    <div class="arch-node-title">Raw Data</div>
    <div class="arch-node-tech">
      <span>AWS S3</span>
      <span>POS</span>
      <span>Social</span>
    </div>
  </div>
  <div class="arch-connector"></div>
  <div class="arch-node">
    <div class="arch-node-stage">02 · ETL</div>
    <div class="arch-node-title">Transform & Align</div>
    <div class="arch-node-tech">
      <span>Databricks</span>
      <span>PySpark</span>
    </div>
  </div>
  <div class="arch-connector"></div>
  <div class="arch-node">
    <div class="arch-node-stage">03 · Store</div>
    <div class="arch-node-title">Feature Store</div>
    <div class="arch-node-tech">
      <span>SQL</span>
      <span>Unified</span>
    </div>
  </div>
  <div class="arch-connector"></div>
  <div class="arch-node featured">
    <div class="arch-node-stage">04 · Model</div>
    <div class="arch-node-title">Hybrid Forecasting</div>
    <div class="arch-node-tech">
      <span>Prophet</span>
      <span>XGBoost</span>
    </div>
  </div>
  <div class="arch-connector"></div>
  <div class="arch-node">
    <div class="arch-node-stage">05 · Deliver</div>
    <div class="arch-node-title">Decision Dashboard</div>
    <div class="arch-node-tech">
      <span>Power BI</span>
    </div>
  </div>
</div>

<p class="diagram-caption">From raw AWS logs to an actionable inventory-health score — every stage is version-controlled and reproducible.</p>

**Scalable Data Engineering & ETL.** Spearheaded the development of a robust data pipeline utilizing **AWS** and **Databricks**. Orchestrated **PySpark** and advanced SQL to ingest, process, and align millions of rows of multi-source heterogeneous data — historical point-of-sale records, marketing event logs, and social media sentiment indexes — into a unified feature store.

**Hybrid Predictive Architecture (Residual Modeling).** Designed an innovative two-stage forecasting framework to isolate and predict complex variance:
- Leveraged **Prophet** to establish a baseline, capturing macro time-series trends and periodic seasonality.
- Employed **XGBoost** to model the non-linear residuals (the variance unexplained by Prophet), utilizing external features such as social media hype and promotional events.
- Applied **Bayesian Optimization** for hyperparameter tuning, drastically reducing computational overhead while avoiding the curse of dimensionality.

**Causal Inference & Advanced Feature Engineering.** Formulated a rigorous statistical approach to transform seemingly random market noise into predictable business windows. Conducted **Granger Causality Tests** and **Difference-in-Differences (DiD)** analysis — controlling for confounding variables like marketing spend and holidays — to scientifically prove that social media discussion volume acts as a leading indicator for sales with a 2–3 week lag.

<div class="causal-chart-container">
  <div class="causal-chart-title">Granger Causality · Social → Sales (~3 week lead)</div>
  <p class="causal-chart-subtitle">Social-media sentiment spikes consistently precede the corresponding sales spike by 2–3 weeks. This deterministic lead-time became the foundation of a proactive inventory-buying strategy.</p>

  <svg class="causal-chart" viewBox="0 0 720 250" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Dual-line chart showing social-media sentiment spike leads sales volume spike by approximately three weeks">
    <line x1="60" y1="45" x2="690" y2="45" stroke="currentColor" stroke-width="1" stroke-dasharray="2 4" style="color:var(--global-divider-color)"/>
    <line x1="60" y1="125" x2="690" y2="125" stroke="currentColor" stroke-width="1" stroke-dasharray="2 4" style="color:var(--global-divider-color)"/>
    <line x1="60" y1="205" x2="690" y2="205" stroke="currentColor" stroke-width="1" style="color:var(--global-divider-color)"/>

    <g font-family="JetBrains Mono, monospace" font-size="10" style="fill:var(--global-text-color-light)">
      <text x="125" y="225" text-anchor="middle">W1</text>
      <text x="225" y="225" text-anchor="middle">W2</text>
      <text x="325" y="225" text-anchor="middle">W3</text>
      <text x="425" y="225" text-anchor="middle">W4</text>
      <text x="525" y="225" text-anchor="middle">W5</text>
      <text x="625" y="225" text-anchor="middle">W6</text>
    </g>

    <path d="M 60 158 L 170 152 Q 200 150 222 55 Q 244 55 268 148 L 360 152 L 480 152 L 600 154 L 690 153" fill="none" stroke="#0ea5e9" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"/>
    <circle cx="222" cy="55" r="4.5" fill="#0ea5e9"/>
    <text x="222" y="42" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="10" fill="#0ea5e9" font-weight="600">Viral Spike</text>

    <path d="M 60 178 L 180 178 L 300 180 L 400 180 L 480 180 Q 502 180 522 68 Q 545 68 568 180 L 690 178" fill="none" stroke="#2563eb" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round"/>
    <circle cx="522" cy="68" r="4.5" fill="#2563eb"/>
    <text x="522" y="55" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="10" fill="#2563eb" font-weight="600">Sales Spike</text>

    <g style="color:var(--global-theme-color)">
      <line x1="222" y1="190" x2="522" y2="190" stroke="currentColor" stroke-width="1.3" stroke-dasharray="4 3"/>
      <line x1="222" y1="184" x2="222" y2="196" stroke="currentColor" stroke-width="1.3"/>
      <line x1="522" y1="184" x2="522" y2="196" stroke="currentColor" stroke-width="1.3"/>
      <rect x="328" y="181" width="92" height="18" rx="3" style="fill:var(--global-surface-color)"/>
      <text x="374" y="194" text-anchor="middle" font-family="JetBrains Mono, monospace" font-size="10" font-weight="600" fill="currentColor">~3 week lag</text>
    </g>
  </svg>

  <div class="causal-chart-legend">
    <span class="legend-item"><span class="legend-swatch" style="background:#0ea5e9"></span>Social-Media Sentiment <em style="color:var(--global-text-color-light);font-style:normal;font-size:0.72rem;">(leading)</em></span>
    <span class="legend-item"><span class="legend-swatch" style="background:#2563eb"></span>Sales Volume <em style="color:var(--global-text-color-light);font-style:normal;font-size:0.72rem;">(target)</em></span>
  </div>
</div>

**Productization & Business Intelligence.** Translated complex machine learning outputs into an intuitive, dynamic **Power BI** decision dashboard. Engineered an actionable *"Inventory Health Score"*, empowering 500+ store managers to proactively optimize local stock levels — bridging the gap between algorithmic outputs and frontline business operations.

<h2 class="project-section-title">Business Impact</h2>

- Achieved a **91.2% core forecast accuracy** on held-out test sets.
- Predictive insights **reduced excess inventory by 18%** while **increasing overall sales efficiency by 25%** across the retail network.
- Successfully predicted the explosive growth scale of the **Top 3 IP-related merchandise** for H1 2025, allowing the business to secure deterministic revenue growth amidst high market volatility.

<h2 class="project-section-title">Tech Stack</h2>

<div class="tech-stack-grouped">
  <div class="tech-group">
    <span class="tech-group-label">Data Engineering</span>
    <div class="tech-group-pills">
      <span class="pill">Databricks</span>
      <span class="pill">PySpark</span>
      <span class="pill">AWS</span>
      <span class="pill">SQL</span>
    </div>
  </div>
  <div class="tech-group">
    <span class="tech-group-label">Machine Learning & Stats</span>
    <div class="tech-group-pills">
      <span class="pill">XGBoost</span>
      <span class="pill">Prophet</span>
      <span class="pill">Causal Inference (DiD)</span>
      <span class="pill">Bayesian Optimization</span>
    </div>
  </div>
  <div class="tech-group">
    <span class="tech-group-label">BI & Visualization</span>
    <div class="tech-group-pills">
      <span class="pill">Power BI</span>
    </div>
  </div>
</div>
