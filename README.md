# 📱 Play Store App Review Analysis

An end-to-end **Exploratory Data Analysis (EDA)** project on Google Play Store app data and user reviews — combining Python-based data analysis with an interactive **Power BI dashboard** to deliver actionable insights for app developers and businesses.

---

## 📌 Project Overview

The Google Play Store is a highly competitive digital marketplace. This project analyzes app metadata and user review sentiment to uncover what drives app success — covering ratings, installs, pricing, category trends, and user satisfaction. The goal is to equip developers with **data-driven strategies** to improve app quality, boost visibility, and enhance user experience.

- **Project Type:** EDA  
- **Contribution:** Individual  
- **Tools Used:** Python (Pandas, Matplotlib, Seaborn), Google Colab, Power BI

---

## 🗂️ Repository Structure

playstore_eda_project/
│
├── dashboard_screenshots/              # Power BI dashboard preview images
├── datasets/                           # App dataset & user review dataset
├── Google_Play_Store_Analytics_Dashboard.pbix   # Power BI dashboard file
├── Project_PlayStore_App.ipynb         # Full EDA notebook (Python)
└── README.md

---

## 📊 Dataset Overview

Two publicly available datasets were used:

| Dataset | Description | Size |
|---|---|---|
| **App Dataset** | App name, category, rating, reviews, size, installs, type (free/paid), price, last updated, etc. | ~10,358 entries |
| **User Review Dataset** | Translated user reviews labeled with sentiment (Positive/Neutral/Negative), along with polarity & subjectivity scores | ~29,644 entries |

---

## 🧹 Data Cleaning & Preprocessing

- **Type Conversion:** Converted `Reviews`, `Installs`, `Size`, `Price`, and `Last Updated` into proper numeric/datetime formats.
- **Missing Values:** Imputed using **median** (numerical columns like `Size`, `Rating`) and **mode** (categorical columns like `Type`, `Android Ver`); placeholder `"Unknown"` used for `Current Ver`. Rows with missing `Translated_Review` were dropped.
- **Normalization:** Removed non-numeric characters (`+`, `M`, `$`) from numeric fields.
- **Formatting:** Standardized the `Android Ver` column for consistency.

---

## 🔍 Exploratory Data Analysis & Key Insights

The analysis covers **20+ visualizations** across Univariate, Bivariate, and Multivariate analysis, including histograms, boxplots, scatter plots, heatmaps, and pairplots.

### App-Level Insights
- Most apps are rated **above 4.0**, indicating strong overall user satisfaction.
- **FAMILY, GAME, and TOOLS** dominate the category landscape; **BEAUTY, COMICS, and PARENTING** are underrepresented — signaling niche opportunities.
- **92.6% of apps are free**; paid apps show a marginally higher average rating (~4.2 vs ~4.1).
- Apps sized between **10–50 MB** tend to receive more installs and better engagement.
- **Reviews and Installs** show the strongest correlation (**0.63**) — popularity drives engagement, not rating.
- **Price shows no correlation** with installs, suggesting higher pricing doesn't deter downloads on its own.
- App update frequency has grown sharply since 2016, reflecting increasing developer activity and competition.

### Sentiment & Review Insights
- Overall sentiment distribution: **58% Positive, 26% Neutral, 16% Negative** (Python EDA) — Power BI dashboard reflects a similarly strong positive skew (**~64% Positive**).
- Sentiment **polarity** is slightly skewed positive, while **subjectivity** scores show a mix of factual and opinion-based reviews.
- Polarity and Subjectivity show a **moderate positive correlation (0.29)**, while review count shows a weak negative correlation with polarity (**-0.10**) — suggesting apps with more visibility may attract more critical feedback.
- Sentiment clusters clearly by category: positive reviews lean toward higher subjectivity, while negative reviews are more concentrated near neutral/objective subjectivity.

---

## 📈 Power BI Dashboard

An interactive two-page dashboard was built to present findings in a business-friendly format:

**Page 1 — App Overview**
- Total App Installs: **147 Bn**
- App Count: **9,638**
- Average App Rating: **4.20**
- Visuals: Apps by Category, Free vs Paid Distribution, Content Rating Breakdown, App Update Trend Over the Years

**Page 2 — User Overview**
- Total Reviews: **27.89K**
- Apps Reviewed: **865**
- Average Sentiment Polarity: **0.19**
- Visuals: Overall Sentiment Distribution, Top Reviewed Apps, Average Sentiment Polarity Gauge

📷 *See `dashboard_screenshots/` for visuals.*

---

## 💡 Business Recommendations

1. **Enhance App Quality** — Address apps rated below 4.0 through targeted UX/feature improvements.
2. **Target High-Demand Categories** — Focus on COMMUNICATION, GAME, and FAMILY for acquisition; explore niche categories (BEAUTY, COMICS) for lower competition.
3. **Optimize User Engagement** — Encourage reviews from satisfied users and respond proactively to negative feedback.
4. **Adopt a Freemium Model** — With 92%+ apps free, in-app purchases/ads balance demand with monetization.
5. **Monitor & Update Regularly** — Frequent updates correlate with stronger user retention.

---

## ✅ Conclusion

This analysis of Play Store app data and user reviews uncovers the key drivers of app success and provides actionable insights for developers in a competitive market. By prioritizing app quality, optimal sizing, user engagement, and informed category/monetization strategy, developers can boost visibility, build user trust, and achieve sustainable long-term growth within the Play Store ecosystem.

---

## 🛠️ How to Use

1. Clone this repository
2. Open `Project_PlayStore_App.ipynb` in Google Colab or Jupyter Notebook to explore the full EDA
3. Open `Google_Play_Store_Analytics_Dashboard.pbix` in Power BI Desktop to interact with the dashboard

---

## 👤 Author

**Ruchi Nailwal**
