# JDSearch Marketplace Discovery Funnel Optimization

## Overview

This project analyzes marketplace search and product interaction data to identify
conversion bottlenecks across the discovery-to-purchase funnel and translate
behavioral insights into product optimization opportunities.

The project combines SQL-based funnel analysis with an interactive Power BI dashboard
to investigate how users progress from product discovery to clicks, carts, and purchases.

## Business Objective

Identify where marketplace users drop off during the search-to-purchase journey and
prioritize product interventions that could improve conversion.

## Tools Used

- SQL
- DuckDB
- Python
- Pandas
- Jupyter Notebook
- Power BI

## Dataset

The dataset contains marketplace search behavior and candidate-product interactions.

Interaction labels include:

- No interaction
- Click
- Cart
- Purchase

Raw data is not included in the public repository because of file size and
potential redistribution constraints.

## Analytical Workflow

1. Audited the dataset structure and interaction labels.
2. Expanded candidate-product lists into product-level observations.
3. Enriched interactions with product category metadata.
4. Built category-level funnel metrics.
5. Analyzed search exploration and candidate-set size.
6. Compared click-to-cart and cart-to-purchase conversion across categories.
7. Conducted product-level sensitivity analysis using different engagement thresholds.
8. Built an interactive three-page Power BI dashboard.
9. Translated the findings into potential product interventions and experiment metrics.

## Key Findings

- Analyzed 15.5M+ product-search interactions.
- Evaluated conversion performance across 69 product categories.
- Identified category 98719916 as a potential post-cart conversion opportunity.
- Observed a 1.06 percentage-point gap versus the peer benchmark in
  purchase-after-cart conversion.
- Estimated approximately 70 illustrative additional purchases if benchmark
  conversion were achieved at the same cart volume.

The incremental purchase estimate is illustrative and should not be interpreted
as a causal forecast.

## Product Recommendation

Investigate potential post-cart purchase friction in category 98719916.

Potential areas include:

- Delivery and availability transparency
- Total cost visibility
- Product information and reviews
- Return and cancellation policies
- Payment and checkout friction
- Buyer confidence at the final purchase stage

A potential experiment would test enhanced purchase-confidence information and use
purchase-after-cart conversion as the primary metric.

Potential guardrail metrics include:

- Payment failure rate
- Checkout latency
- Cancellation rate
- Refund rate

## Power BI Dashboard

The dashboard contains three pages.

### 1. Marketplace Funnel Overview

Provides an overview of candidate observations, clicks, carts, purchases, and
category-level conversion.

### 2. Category Bottleneck Diagnostics

Compares cart-after-click and purchase-after-cart conversion to identify the
stage where categories experience friction.

### 3. Category 98719916 — Opportunity Deep Dive

Focuses on a potential post-cart conversion opportunity using benchmark comparison,
sensitivity analysis, and recommended product interventions.

## Dashboard Preview

### Marketplace Funnel Overview

![Marketplace Funnel Overview](dashboard/screenshots/page_1_funnel_overview.png)

### Category Bottleneck Diagnostics

![Category Bottleneck Diagnostics](dashboard/screenshots/page_2_bottleneck_diagnostics.png)

### Opportunity Deep Dive

![Opportunity Deep Dive](dashboard/screenshots/page_3_opportunity_deep_dive.png)

## Repository Structure

```text
dashboard/          Power BI report and dashboard screenshots
dashboard_data/     Aggregated datasets used in Power BI
data/               Dataset files and data documentation
outputs/            Saved analytical tables
src/                SQL scripts and supporting code
