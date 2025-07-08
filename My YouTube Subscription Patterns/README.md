# 📺 My YouTube Subscription Patterns

## 📌 Project Description
A personal data exploration of my YouTube subscription and viewing habits. This project uses clustering and time-series analysis to uncover content category trends and shifts in my consumption patterns over time.

---

## 📊 Dataset Overview
- **Data Source**: YouTube subscription and viewing history (exported CSV)
- **Preprocessing**:  
  - Consolidated monthly view counts  
  - Categorized channels into custom buckets (e.g., Vlog, Education, Shorts)  
  - Cleaned inconsistent names and missing values
- **Focus Metrics**:
  - `year_month`
  - `channel`
  - `subscription_count` / `view_count`

---

## 🔍 Key Findings

### 1. Subscription clusters reveal content-focused engagement
- Channels grouped into clusters: **Entertainment**, **Education**, **Shorts**
- Visualization by category showed seasonal shifts — more **Educational content** in exam months

### 2. Significant spikes in short-form content
- Notable increases in monthly Shorts consumption (e.g., `시간 훅 가는 쇼츠`) during late 2024
- Suggests periods of casual or quick content preference

### 3. Dominant channels persisted over time
- A few channels (e.g., `리쥬라이크`, `AKA`) maintained consistent high-view shares
- However, channel clusters fluctuated, indicating evolving interests

---

## 📈 Visualization Highlights
- **Horizontal stacked bar chart** showing monthly category composition
- **Timeline line plot** for individual channels to display usage trends
- **Cluster distribution heatmap** to illustrate grouping consistency

---

## 🧠 Reflection on Data Approach

### ✅ What worked well:
- Custom channel categorization added interpretability to user behavior
- Aggregation by month simplified trend visualization and inference
- Clustering enhanced understanding beyond raw view counts

### 🛠 What could be improved:
- Category labeling was manual — could be semi-automated using text analysis
- Analyzed shorter time window; a longer timeline may reveal richer seasonal patterns

### 💡 Improvement Ideas:
- Auto-assign categories using NLP topic modeling
- Integrate watch duration for sentiment/engagement deeper understanding
- Build an interactive web dashboard (Streamlit / Dash)

---

## 🧰 Tools Used
- Python (pandas, matplotlib, seaborn, scikit-learn)
- Jupyter Notebook
- Techniques: Time series aggregation, clustering (K-Means), stacked bar & line plots

---

## 📁 Folder Structure
```
/My YouTube Subscription Patterns
|-- data/
|   |-- subscriptions.csv
|   |-- views_cleaned.csv
|-- notebooks/
|   |-- 1_data_cleaning.ipynb
|   |-- 2_clustering_and_visuals.ipynb
|-- README.md
```

---

## ✅ Summary
This project uncovers monthly and categorical patterns in my YouTube usage, combining clustering with time-based visualizations. It’s a personal reflection disguised as data exploration—showing how your digital habits change with life.  
Great for portfolios, as it melds analysis with personal narrative.

---

## 🔗 References
- YouTube Data Tools
- Scikit-learn K-Means & Time-Series Plotting Docs
- Matplotlib Horizontal Stack & Line Plot Guides

