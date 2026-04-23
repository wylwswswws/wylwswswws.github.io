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

**Scalable Data Engineering & ETL.** Spearheaded the development of a robust data pipeline utilizing **AWS** and **Databricks**. Orchestrated **PySpark** and advanced SQL to ingest, process, and align millions of rows of multi-source heterogeneous data — historical point-of-sale records, marketing event logs, and social media sentiment indexes — into a unified feature store.

**Hybrid Predictive Architecture (Residual Modeling).** Designed an innovative two-stage forecasting framework to isolate and predict complex variance:
- Leveraged **Prophet** to establish a baseline, capturing macro time-series trends and periodic seasonality.
- Employed **XGBoost** to model the non-linear residuals (the variance unexplained by Prophet), utilizing external features such as social media hype and promotional events.
- Applied **Bayesian Optimization** for hyperparameter tuning, drastically reducing computational overhead while avoiding the curse of dimensionality.

**Causal Inference & Advanced Feature Engineering.** Formulated a rigorous statistical approach to transform seemingly random market noise into predictable business windows. Conducted **Granger Causality Tests** and **Difference-in-Differences (DiD)** analysis — controlling for confounding variables like marketing spend and holidays — to scientifically prove that social media discussion volume acts as a leading indicator for sales with a 2–3 week lag.

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
