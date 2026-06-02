# Customer Churn Analytics - SaaS Industry
## AI-Powered Data Analytics & Strategic Recommendations

**Status:** ✅ Complete | **Last Updated:** May 31, 2026

---

## 🎯 Project Overview

This project delivers a comprehensive **data-driven analysis** of customer churn in a SaaS subscription-based business. Combining **structured customer data** (95k records) with **unstructured exit interviews** (3.5k responses), we identify churn drivers, customer sentiment patterns, and actionable retention strategies.

### Key Metrics
- **Total Customers Analyzed:** 94,526
- **Churned Customers:** 19,656 (20.79%)
- **Monthly Revenue at Risk:** $706,868
- **Exit Interviews Analyzed:** 3,285
- **Analysis Scope:** Demographic, behavioral, geographic, financial

---

## 📊 Project Deliverables

### ✅ Task 1: Data Cleaning
**Status:** Complete | **Data Retention:** 99.1% (Customers), 91.1% (Interviews)

- ✓ Removed duplicates, fixed missing values, standardized formats
- ✓ Fixed inconsistent labels (Gender, Subscription Type, Region)
- ✓ Validated numeric ranges (Age: 18-80, Tenure, Support Tickets)
- ✓ Cleaned HTML tags, emojis, and special characters from text
- ✓ **Output:** `customers_cleaned.csv`, `interviews_cleaned.csv`, `merged_churn_data.csv`

**Quality Metrics:**
- Missing values: 0.0%
- Duplicates: 0.0%
- Data quality score: 100%

---

### ✅ Task 2: Exit Reason Classification
**Status:** Complete | **Classification Coverage:** 100%

Categorized 3,285 exit interviews into 7 core reasons using AI-assisted analysis:

| Reason | Count | % | Top Indicator |
|--------|-------|---|---|
| **Support** | 1,317 | 40.1% | Slow response times |
| **Product** | 654 | 19.9% | Reliability issues |
| **Price** | 646 | 19.7% | Cost sensitivity |
| **Competitor** | 264 | 8.0% | Better alternatives |
| **Performance** | 128 | 3.9% | Speed/stability |
| **Value** | 127 | 3.9% | ROI not justified |
| **Onboarding** | 115 | 3.5% | Poor initial setup |

**Output:** `Task_2_Exit_Reason_Classification.xlsx`

---

### ✅ Task 3: Mood Analysis
**Status:** Complete | **Coverage:** 100%

Extracted customer sentiment from exit interviews:

| Mood | Count | % | Meaning |
|------|-------|---|---------|
| **Neutral** | 2,417 | 73.6% | Rational business decision |
| **Disappointed** | 475 | 14.5% | Unmet expectations |
| **Hopeful** | 393 | 12.0% | Open to alternatives |

**Critical Finding:** 65.3% of price-sensitive customers are disappointed (high-friction exit).

**Output:** `Task_3_Mood_Analysis.xlsx`

---

### ✅ Task 4: Exploratory Data Analysis (EDA)
**Status:** Complete

#### Churn by Subscription Type
- **Basic:** 22.13% churn (6,901 customers) ⚠️ HIGH RISK
- **Standard:** 22.22% churn (6,225 customers) ⚠️ HIGH RISK
- **Premium:** 18.40% churn (4,050 customers)
- **Enterprise:** 14.67% churn (607 customers) ✓ STABLE
- **Other:** 20.40% churn (1,873 customers)

#### Churn by Tenure
- **0-1 Year:** 23.59% churn ⚠️ CRITICAL (new customer risk)
- **1-2 Years:** 20.47% churn
- **2-3 Years:** 20.85% churn
- **3-5 Years:** 20.59% churn
- **5-10 Years:** 20.39% churn
- **10+ Years:** 20.00% churn ✓ STABLE

#### Churn by Spend Bracket
- **$0-25/mo:** 22.24% churn (low-value risk)
- **$25-50/mo:** 20.85% churn
- **$50-100/mo:** 18.40% churn
- **$100+/mo:** 15.17% churn ✓ STABLE (high-value)

#### Churn by Support Tickets
- **0 tickets:** 20.01% churn
- **1-2 tickets:** 20.71% churn
- **3-4 tickets:** 22.90% churn
- **5+ tickets:** 27.78% churn ⚠️ HIGH CORRELATION

**Output:** `Churn_Analysis_Summary.xlsx`

---

### ✅ Task 5: Power BI Dashboard Data Preparation
**Status:** Complete

Pre-processed datasets for interactive dashboards:

| Dataset | Purpose | Records |
|---------|---------|---------|
| `churn_by_subscription.csv` | Subscription segment analysis | 5 types |
| `churn_by_tenure.csv` | Customer lifecycle trends | 6 cohorts |
| `churn_by_region.csv` | Geographic patterns | 6 regions |
| `exit_reasons_mood_matrix.csv` | Reason × Mood crosstab | 21 cells |
| `mood_summary.csv` | Sentiment distribution | 3 categories |

**Dashboard Features:**
- KPI cards (churn rate, revenue impact, customer count)
- Segmentation charts (subscription, tenure, region, spend)
- Reason distribution bar charts
- Mood sentiment analysis
- Interactive filters by dimension

**Output:** `Task_5_PowerBI_Dashboard.xlsx`

---

### ✅ Task 6: Business Storytelling & Recommendations
**Status:** Complete

#### 5-Slide Executive Presentation

**Slide 1:** Title Slide
- Topic: Customer Churn Analytics
- Context: SaaS retention strategy

**Slide 2:** The Churn Challenge
- 20.79% churn rate (19,656 customers)
- $706k monthly revenue at risk
- High-risk segments identified

**Slide 3:** Top Churn Drivers
- Support (40.1%) - primary pain point
- Product (19.9%) - secondary issues
- Price (19.7%) - cost sensitivity

**Slide 4:** Customer Sentiment
- 73.6% neutral exits (rational)
- 14.5% disappointed (service failure)
- 12.0% hopeful (retention opportunities)

**Slide 5:** Strategic Recommendations
1. **Emergency:** Support crisis (hire 25-30% more staff)
2. **Early engagement:** Enhanced onboarding for new customers
3. **Price strategy:** Flexible plans & commitment discounts

#### Detailed Business Report
- Executive summary
- Methodology
- Findings by dimension
- Customer sentiment analysis
- Financial impact assessment
- 5 strategic recommendations
- Implementation roadmap
- Risk mitigation strategies

**Output:** 
- `Churn_Analytics_Presentation.pptx` (5 slides)
- `Churn_Analytics_Business_Report.docx` (15+ pages)

---

## 📁 Repository Structure

```
customer-churn-analytics/
├── README.md (this file)
├── METHODOLOGY.md
├── DATA_DICTIONARY.md
│
├── 1_DATA_CLEANING/
│   ├── Task_1_Data_Cleaning.docx
│   ├── customers_cleaned.csv (94,526 records)
│   ├── interviews_cleaned.csv (3,285 records)
│   └── merged_churn_data.csv (comprehensive dataset)
│
├── 2_CLASSIFICATION_MOOD/
│   ├── Task_2_Exit_Reason_Classification.xlsx
│   ├── Task_3_Mood_Analysis.xlsx
│   └── classification_model.py
│
├── 3_EDA_ANALYSIS/
│   ├── Churn_Analysis_Summary.xlsx
│   ├── churn_by_subscription.csv
│   ├── churn_by_tenure.csv
│   ├── churn_by_region.csv
│   └── exploratory_analysis.py
│
├── 4_POWERBI_DASHBOARD/
│   ├── Task_5_PowerBI_Dashboard.xlsx
│   ├── exit_reasons_mood_matrix.csv
│   └── mood_summary.csv
│
├── 5_BUSINESS_STORYTELLING/
│   ├── Churn_Analytics_Presentation.pptx
│   ├── Churn_Analytics_Business_Report.docx
│   └── recommendations.md
│
├── CODE/
│   ├── project1_complete_analysis.py
│   ├── data_cleaning.py
│   └── visualization_utilities.py
│
└── DOCS/
    ├── methodology.md
    ├── glossary.md
    └── references.md
```

---

## 🔍 Key Findings

### 1. Support Crisis (40% of Exits)
**Problem:** Slow response times, delayed ticket resolution
**Impact:** 1,317 customer mentions, $530k+ revenue loss
**Sentiment:** Mostly neutral (88.5%), indicating rational business decision

### 2. New Customer Vulnerability (23.6% first-year churn)
**Problem:** Weak onboarding, unclear ROI
**Impact:** 2,209 customers in 0-1Y cohort
**Opportunity:** Enhanced onboarding can reduce by 15%

### 3. Price Sensitivity (19.7% of exits)
**Problem:** Cost not justified vs. alternatives
**Impact:** 646 mentions, heavily disappointed (65.3%)
**Opportunity:** Flexible pricing, commitment discounts

### 4. Geographic Hotspots
**High-risk regions:** North (21.0%), South (21.0%)
**Opportunity:** Regional strategy differentiation

### 5. Spend Correlation
**Finding:** Lower-spend customers (<$25/mo) have highest churn (22.2%)
**Implication:** Difficulty retaining entry-level segment

---

## 💡 Strategic Recommendations

### RECOMMENDATION 1: Emergency Support Intervention 🚨
**Priority:** CRITICAL | **Timeline:** Immediate (0-3 months)

**Problem:** Support issues drive 40% of churn
**Action Items:**
- Hire 25-30% additional support staff
- Implement SLA: <2 hour response, <24 hour resolution
- Establish support ticket escalation protocol
- Add 24/7 support for Premium/Enterprise customers

**Expected Impact:**
- Retain 400-500 customers in 6 months
- Reduce support-related churn from 40% to 25%
- Revenue recovery: $150k-$200k monthly

**Investment:** $180k-$250k (annual salaries + training)
**ROI:** 6-9 months

---

### RECOMMENDATION 2: Early Engagement Program 📅
**Priority:** HIGH | **Timeline:** 1-2 months implementation

**Problem:** New customers (0-1Y) have 23.6% churn rate
**Action Items:**
- Develop 30-day structured onboarding program
- Assign success managers to new customers
- Monthly ROI check-ins & success metrics dashboard
- Early warning system for at-risk customers (days 30-90)
- Quarterly business reviews for high-value accounts

**Expected Impact:**
- Reduce first-year churn from 23.6% to 20%
- Retain 1,100+ new customers annually
- Revenue stability: $44k monthly

**Investment:** $120k-$150k (staff, systems, training)
**ROI:** 3-4 months

---

### RECOMMENDATION 3: Flexible Pricing Strategy 💰
**Priority:** HIGH | **Timeline:** 2-3 months implementation

**Problem:** 19.7% exit due to price; 65.3% are disappointed
**Action Items:**
- Introduce lower-tier plan at $9.99/month entry point
- Offer 15% discount for 12-month prepay
- Create "startup" bundle at 40% discount first year
- Volume discounts for team plans
- Custom pricing for enterprise (negotiated)

**Expected Impact:**
- Retain 300-400 price-sensitive customers
- Increase LTV through longer commitments
- Revenue recovery: $100k-$120k monthly

**Investment:** $50k (marketing, implementation)
**ROI:** 2-3 months

---

### RECOMMENDATION 4: Product Reliability Initiative ✅
**Priority:** MEDIUM | **Timeline:** 3-6 months

**Problem:** 19.9% exit due to product issues (reliability, features)
**Action Items:**
- Conduct product audit (performance, stability)
- Implement performance SLA (99.9% uptime guarantee)
- Add top 5 requested features within 6 months
- Quarterly product roadmap transparency
- Customer advisory board for feedback

**Expected Impact:**
- Retain 150-200 customers from product category
- Reduce product-related churn from 19.9% to 12%
- Improve NPS by 15+ points

---

### RECOMMENDATION 5: Regional Strategy Differentiation 🗺️
**Priority:** MEDIUM | **Timeline:** Ongoing

**Problem:** Geographic variation (21.0% vs 20.5%) suggests localization gap
**Action Items:**
- Establish region-specific support teams
- Localize onboarding in key languages
- Region-specific pricing/promotions
- Local customer success events
- Implement region-specific product features

**Expected Impact:**
- Reduce high-risk region churn by 2-3%
- Improve customer satisfaction by 20%
- Better market penetration in stable regions

---

## 📈 Expected Business Impact (12 Months)

| Scenario | Baseline | With Actions | Impact |
|----------|----------|--------------|--------|
| **Churn Rate** | 20.79% | 17.5% | -3.3 pp |
| **Monthly Revenue Loss** | $706,868 | $531,650 | -$175,218 |
| **Customers Retained** | — | 2,850+ | +$342k annual |
| **Customer LTV** | $2,370 | $2,850 | +20% |
| **Support Satisfaction** | 65% | 85% | +20 pp |

**Total Opportunity:** $3-4M annual revenue recovery

---

## 🛠️ Technology Stack

### Data Processing
- **Python 3.9+** (pandas, numpy, scikit-learn)
- **Excel** (pivot tables, analysis)
- **SQL** (data aggregation)

### Analysis Tools
- **Jupyter Notebooks** (exploratory analysis)
- **Python Libraries:**
  - `pandas` - data manipulation
  - `matplotlib`, `seaborn` - visualization
  - `scikit-learn` - classification

### Visualization & BI
- **Power BI** - interactive dashboards
- **Matplotlib/Seaborn** - static charts
- **Tableau** - optional advanced dashboards

### Documentation
- **Microsoft Word** - detailed reports
- **PowerPoint** - executive presentations
- **Markdown** - technical documentation

---

## 📋 Data Sources

### Structured Data (94,526 customers)
- Customer demographics (age, gender, region)
- Subscription details (type, tenure, spend)
- Support engagement (tickets, interactions)
- Churn status (binary flag)

### Unstructured Data (3,285 exit interviews)
- Free-text exit feedback
- Customer sentiment signals
- Detailed reason explanations
- Temporal patterns

### Data Quality
- **Completeness:** 99.1% (structured), 91.1% (interviews)
- **Accuracy:** Validated against business rules
- **Consistency:** Standardized formats across all fields
- **Timeliness:** Current as of Sept 2025

---

## 🚀 Getting Started

### Prerequisites
```bash
python 3.9+
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl python-docx python-pptx
```

### Quick Start
```bash
# 1. Clone repository
git clone https://github.com/yourusername/customer-churn-analytics.git
cd customer-churn-analytics

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run analysis
python CODE/project1_complete_analysis.py

# 4. View results
# - Check POWERBI_DASHBOARD/ for Power BI files
# - Open BUSINESS_STORYTELLING/ for presentation & report
```

---

## 📊 Dashboard Preview

### Power BI Dashboards Included:
1. **Overview Dashboard** - KPIs, trends, key metrics
2. **Segmentation Dashboard** - Churn by subscription, tenure, region, spend
3. **Reason Analysis** - Exit reason distribution with mood breakdown
4. **Mood Dashboard** - Sentiment patterns by reason
5. **Comparative View** - Benchmarking segments

**Dashboard Filters:**
- Subscription Type
- Tenure Group
- Region
- Spend Bracket
- Time Period

---

## 📝 Files Included

### Data Files
| File | Rows | Columns | Purpose |
|------|------|---------|---------|
| `customers_cleaned.csv` | 94,526 | 13 | Customer master data |
| `interviews_cleaned.csv` | 3,285 | 5 | Exit feedback + classification |
| `merged_churn_data.csv` | 94,526 | 18 | Combined for analysis |
| `churn_by_subscription.csv` | 5 | 6 | Dashboard dimension |
| `churn_by_tenure.csv` | 6 | 6 | Dashboard dimension |
| `churn_by_region.csv` | 6 | 6 | Dashboard dimension |
| `exit_reasons_mood_matrix.csv` | 21 | 3 | Reason-Mood crosstab |

### Analysis Files
| File | Type | Purpose |
|------|------|---------|
| `Task_1_Data_Cleaning.docx` | Document | Data cleaning methodology |
| `Task_2_Exit_Reason_Classification.xlsx` | Workbook | Classification results |
| `Task_3_Mood_Analysis.xlsx` | Workbook | Sentiment analysis |
| `Churn_Analysis_Summary.xlsx` | Workbook | EDA summary statistics |
| `Task_5_PowerBI_Dashboard.xlsx` | Workbook | Dashboard data sources |

### Deliverables
| File | Format | Pages | Purpose |
|------|--------|-------|---------|
| `Churn_Analytics_Presentation.pptx` | PowerPoint | 5 slides | Executive summary |
| `Churn_Analytics_Business_Report.docx` | Word | 15+ pages | Detailed findings |

- Completion Checklist

- ✅ Task 1: Data Cleaning (99.1% retention, 100% quality)
- ✅ Task 2: Exit Reason Classification (100% coverage, 7 categories)
- ✅ Task 3: Mood Analysis (3 sentiment categories, Reason×Mood matrix)
- ✅ Task 4: Exploratory Data Analysis (churn by 5 dimensions)
- ✅ Task 5: Power BI Dashboard Data (5 pre-processed datasets)
- ✅ Task 6: Business Storytelling (5-slide deck, 15+ page report)
- ✅ GitHub Ready (professional structure, complete documentation)

---

**
