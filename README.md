# Lotte World Busan — Visitor Sentiment & Text Mining Analysis

**Dong-A University | Team Academic Project | KH Coder · Excel · Descriptive Statistics · CONA**

---

## Business Problem

Lotte World Busan (opened 2022) needed structured intelligence from unstructured visitor feedback to identify operational pain points, satisfaction drivers, and strategic improvement areas.

**Core questions:**
- Which experience dimensions drive satisfaction vs. dissatisfaction?
- What language patterns appear in low-rating reviews?
- What operational areas (pricing, staffing, facilities) require immediate attention?
- What recommendations are data-supported vs. anecdotal?

---

## Dataset

| Attribute | Value |
|---|---|
| Source | Google Maps customer reviews (public data) |
| Total reviews | **887** |
| Languages | Korean, English, Chinese, Japanese, others |
| Rating scale | 1–5 stars |
| Coverage | Full visitor experience (rides, food, staff, facilities, pricing) |
| Collection period | 2022–2024 (post-opening) |

---

## Key Findings

### Overall Satisfaction

| Metric | Value |
|---|---|
| Mean rating | **3.78 / 5.0** |
| Median | 4.0 |
| Std. deviation | 1.29 |
| 4–5 star share | **66.6%** |
| 1–2 star share | **16.4%** |

### Satisfaction by Category

| Category | Mean | Median | Std. Dev | Assessment |
|---|---|---|---|---|
| Family & Kids | **4.00** | 4.0 | 1.04 | ✅ Strongest dimension |
| Attraction & Entertainment | 3.67 | 4.0 | 1.15 | ✅ Positive |
| Time & Visitation | 3.10 | 3.25 | 1.49 | ⚠️ Mixed — high variance |
| Facilities & Services | 3.06 | 3.25 | 1.37 | ⚠️ Below average |
| Pricing & Discounts | **1.80** | 2.0 | 0.84 | ❌ Critical weakness |
| **Overall** | **3.78** | **4.0** | **1.29** | — |

---

## Methodology

### Phase 1 — Data Collection & Preprocessing
- Collected 887 reviews from Google Maps spanning multiple languages
- Cleaned and structured raw text; removed noise and non-informative entries
- Assigned 1–5 star ratings to each review entry

### Phase 2 — Text Mining & Keyword Frequency Analysis (KH Coder)
- Applied noun extraction and frequency analysis using KH Coder
- Identified top 100 nouns across all reviews
- Top 5 keywords: **ride** (305), **good** (266), **child** (177), **fun** (161), **time** (157)
- Note: "weekday" (76) far outranks "weekend" (27) — visitors prefer off-peak days

### Phase 3 — Co-occurrence Network Analysis (CONA)
- Constructed co-occurrence network to map semantic relationships between high-frequency terms
- Identified **7 major visitor behavior and theme clusters** from network topology
- Clusters correspond to distinct visitor archetypes: family visitors, thrill-seekers, weekend planners, etc.

### Phase 4 — Keyword-Level Rating Assignment
- Mapped each high-frequency keyword to its associated average star rating
- Grouped keywords into 5 business dimensions
- Calculated weighted means per dimension

### Phase 5 — Descriptive Statistical Analysis
- Computed mean, median, std. deviation, min, and max per category
- Cross-referenced keyword sentiment with rating distributions

### Phase 6 — Business Recommendations
Generated operational recommendations across 5 areas:
- **Pricing**: introduce tiered tickets; improve discount visibility and card discount availability
- **Facilities**: parking management, rest area expansion, staffing improvements
- **Queue management**: Magic Pass expansion, off-peak incentives, real-time wait-time display
- **Attractions**: increase adult rides; expand ride diversity beyond the "Big 3 Giants"
- **Timing**: promote weekday visits; extend evening parade schedule

---

## Critical Findings in Detail

### Pricing & Discounts (Mean: 1.80) — Highest Risk
| Keyword | Rating | Frequency |
|---|---|---|
| card | 1.0 | 20 |
| fee | 1.0 | 28 |
| discount | 2.0 | 42 |
| money | 2.0 | 15 |
| price | 3.0 | 36 |

Card-based discounts are expected but inconsistently available. Parking fees generate disproportionate negative reviews.

### Time & Visitation (Mean: 3.10) — High Variance (σ = 1.49)
| Keyword | Rating | Frequency |
|---|---|---|
| time | 1.0 | 157 |
| hour | 1.5 | 84 |
| day | 1.0 | 73 |
| weekday | 4.0 | 76 |
| weekend | 4.5 | 27 |
| morning | 4.5 | 19 |
| minute | 5.0 | 67 |

Wait times are the primary frustration. Morning and weekday visitors report significantly better experiences.

---

## Repository Structure

```
lotte-world-busan-visitor-analytics/
│
├── README.md
├── .gitignore
│
├── data/
│   └── raw/
│       └── reviews_raw_887.xlsx          ← 887 raw reviews with ratings
│
├── analysis/
│   ├── category_statistics.xlsx          ← keyword-level ratings by dimension
│   └── descriptive_statistics.xlsx       ← mean/median/std per category
│
├── reports/
│   ├── statistical_analysis.docx         ← written statistical report
│   └── final_report.docx                 ← full team project report
│
├── text_mining/
│   ├── cona_network.png                  ← co-occurrence network diagram
│   ├── cona_clusters.png                 ← cluster visualization
│   └── keyword_frequency_kh.png          ← KH Coder frequency output
│
├── visualizations/
│   ├── rating_distribution.png
│   ├── category_comparison.png
│   └── keyword_frequency.png
│
└── methodology/
    └── analysis_methodology.md
```

---

## Tools Used

| Tool | Purpose |
|---|---|
| **KH Coder** | Text mining, noun extraction, Co-occurrence Network Analysis (CONA) |
| **Excel / Google Sheets** | Rating analysis, descriptive statistics |
| **Google Maps** | Primary data source (public reviews) |

---

## Team

Dong-A University — Data Analytics Academic Project, Busan, South Korea
