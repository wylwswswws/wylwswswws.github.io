---
layout: page
title: "Predictive Churn Modeling & Retention Strategy"
description: Large-scale ML pipeline from distributed data processing to SHAP-driven interventions
img: assets/img/project_churn.png
importance: 2
category: Academic
---

<p class="project-hero-subtitle">
Architecting a large-scale machine learning pipeline from distributed data processing to SHAP-driven strategic interventions and A/B testing frameworks.
</p>

<div class="kpi-grid">
  <div class="kpi-card">
    <div class="kpi-value">50M+</div>
    <div class="kpi-label">Raw Data Logs Processed</div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">0.89</div>
    <div class="kpi-label">Model AUC Score<span class="kpi-sub">89% accuracy</span></div>
  </div>
  <div class="kpi-card">
    <div class="kpi-value">15%</div>
    <div class="kpi-label">Projected Churn Reduction</div>
  </div>
</div>

<h2 class="project-section-title">Overview</h2>

Led a comprehensive data science initiative for a highly competitive telecommunications provider facing elevated customer attrition. By processing massive transactional logs and building robust predictive models, I transformed raw behavioral data into a **proactive, data-driven retention engine** — completing the full lifecycle from data engineering to strategic business experimentation.

<h2 class="project-section-title">Challenge</h2>

The business was losing revenue due to high churn rates, and customer acquisition costs far outweighed retention costs. The existing retention strategy was reactive. The challenge was twofold: process over **50 million unorganized historical transaction and customer service logs** to accurately predict *who* would churn, and scientifically determine *why* and *how* to retain them before they left.

<h2 class="project-section-title">Technical Approach & Execution</h2>

**Distributed Data Engineering & Feature Engineering.** Leveraged **Spark SQL** to ingest, clean, and aggregate 50M+ raw logs down to a structured feature store of 50,000+ high-resolution user profiles. Conducted extensive EDA to engineer **50+ composite features** capturing dynamic behavioral patterns (tenure-to-cost ratios, service engagement, and historical billing preferences).

**Imbalanced Classification Modeling.** Addressed severe target class imbalance using a hybrid approach of **SMOTE** (Synthetic Minority Over-sampling Technique) and **cost-sensitive learning** (class weight adjustments). Developed and tuned an **XGBoost** classifier, strategically optimizing for **Recall and AUC** over raw accuracy to ensure the maximum number of true at-risk customers were identified without excessive false positives.

<div class="callout">
  <div class="callout-icon">💡</div>
  <div class="callout-body">
    <p class="callout-title">Why Recall &amp; AUC, not Accuracy?</p>
    <p class="callout-text">
      In highly imbalanced churn scenarios, naive accuracy is a vanity metric — predicting "no churn" for everyone might yield 95% accuracy but <strong>$0 business value</strong>. By optimizing for Recall, the model prioritizes identifying true at-risk users, maximizing the operational ROI of retention campaigns.
    </p>
  </div>
</div>

**Model Interpretability (XAI).** Deployed **SHAP** (SHapley Additive exPlanations) to unpack the algorithmic "black box." Isolated and quantified the top churn drivers, revealing that **legacy DSL service usage, imminent contract expirations, and paper-billing habits** were the strongest indicators of attrition.

**Productization & A/B Testing Framework.** Operationalized the ML output by creating a dynamic **"Customer Health Score"** dashboard in **Tableau**. Translated these scores into automated business rules and designed a rigorous A/B testing methodology to scientifically evaluate the ROI of differentiated interventions (e.g., proactive fiber-optic upgrades vs. targeted cashback promos).

<p class="project-sub-title">Closed-Loop Analytics Framework</p>

<div class="loop-diagram">
  <svg class="loop-arrows" viewBox="0 0 500 500" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <defs>
      <marker id="ch-arrow" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse">
        <path d="M 0 0 L 10 5 L 0 10 z"/>
      </marker>
    </defs>
    <path d="M 325 100 Q 400 140 355 215" marker-end="url(#ch-arrow)"/>
    <path d="M 355 285 Q 400 360 325 400" marker-end="url(#ch-arrow)"/>
    <path d="M 175 400 Q 100 360 145 285" marker-end="url(#ch-arrow)"/>
    <path d="M 145 215 Q 100 140 175 100" marker-end="url(#ch-arrow)"/>
  </svg>

  <div class="loop-node loop-top">
    <div class="loop-node-title">Data Engineering</div>
    <div class="loop-node-sub">Spark · Feature Store</div>
  </div>
  <div class="loop-node loop-right">
    <div class="loop-node-title">ML Prediction</div>
    <div class="loop-node-sub">XGBoost · SMOTE</div>
  </div>
  <div class="loop-node loop-bottom">
    <div class="loop-node-title">Actionable Insight</div>
    <div class="loop-node-sub">SHAP · Tableau</div>
  </div>
  <div class="loop-node loop-left">
    <div class="loop-node-title">Experimentation</div>
    <div class="loop-node-sub">A/B Testing · ROI</div>
  </div>

  <div class="loop-center">Closed-Loop<br>Analytics</div>
</div>

<p class="diagram-caption">Every experiment feeds back into the next iteration — data becomes culture, not a one-off report.</p>

<h2 class="project-section-title">Business Impact</h2>

- Engineered a high-performing XGBoost model achieving an **AUC of 0.89** and a comprehensive **accuracy of 89%**, effectively capturing the most critical at-risk segments.
- Formulated a targeted retention playbook projected to drive a **15% reduction in overall customer churn**.
- Successfully established a closed-loop analytics culture within the team:
*Data Insight → Algorithmic Prediction → Strategic Intervention → Experimental Evaluation.*

<h2 class="project-section-title">Tech Stack</h2>

<div class="tech-stack-grouped">
  <div class="tech-group">
    <span class="tech-group-label">Big Data & Processing</span>
    <div class="tech-group-pills">
      <span class="pill">PySpark</span>
      <span class="pill">Spark SQL</span>
      <span class="pill">EDA</span>
    </div>
  </div>
  <div class="tech-group">
    <span class="tech-group-label">Machine Learning</span>
    <div class="tech-group-pills">
      <span class="pill">XGBoost</span>
      <span class="pill">SMOTE</span>
      <span class="pill">Imbalanced Data</span>
    </div>
  </div>
  <div class="tech-group">
    <span class="tech-group-label">Analytics & Strategy</span>
    <div class="tech-group-pills">
      <span class="pill">SHAP</span>
      <span class="pill">A/B Testing</span>
      <span class="pill">Tableau</span>
    </div>
  </div>
</div>
