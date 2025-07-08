🎯 Objective
This project explores the relationship between a wine's chemical properties and its perceived quality, with the goal of understanding which compounds most strongly influence taste, and how accurately we can predict quality using machine learning models. Beyond prediction, the aim is to demystify what "good wine" might chemically mean.

📊 Dataset Overview
Data Source: UCI Wine Quality Dataset – Red Wine

Observations: 1,599 red wine samples, each with 11 physicochemical features and a quality score (0–10)

Preprocessing:

Removed outliers in free sulfur dioxide and total sulfur dioxide via IQR

Applied log transformation for improved model stability

Created a correlation heatmap to evaluate feature interactions

🔍 Key Findings
1. Alcohol is the kingmaker of wine quality
Among all features, alcohol had the strongest positive correlation with wine quality (R² ≈ 0.47).

This aligns with the sensory perception that higher alcohol often accompanies more body and richness in red wine.

2. Sulfur dioxide variables introduced subtle complexity
total sulfur dioxide and free sulfur dioxide weren’t dominant predictors alone, but including them alongside citric acid, density, and fixed acidity noticeably improved model performance.

Especially in tree-based models, they helped uncover non-linear interactions that linear models missed.

3. Random Forest outperformed other models
Model	MSE ↓	R² ↑
Linear Regression	0.555	0.155
Random Forest	0.450	0.320
XGBoost	0.498	0.247

Random Forest achieved the best performance in both MSE and R² with just 5 features.

XGBoost showed promise, but underperformed slightly due to lack of tuning or perhaps insufficient feature complexity.

📈 Visualization Highlights
📌 Lower-triangle heatmap revealed meaningful correlations between chemical features, helping avoid redundancy.

📌 Bar chart of feature importances from the Random Forest model clearly highlighted the influence of density and total sulfur dioxide.

📌 Model performance comparison chart displayed the strengths and weaknesses of each regression model using side-by-side bar plots.

🤔 Reflection on Data Approach
What worked well:
I iteratively built up from simple models to complex ones, giving me insight into what each model learned.

Focused feature selection enabled clearer interpretation.

Visualization at each step supported decision-making (e.g., removing outliers, selecting features).

What could improve:
A more diverse feature set (including alcohol, sulphates, volatile acidity) would likely boost performance further.

XGBoost wasn’t tuned—grid search or Bayesian optimization could improve its potential.

Improvement Ideas:
Perform PCA to reduce dimensionality and observe its effect on model performance.

Explore classification framing (e.g., low vs high quality) to simplify the target.

Visualize predicted vs. actual wine quality with regression line overlays.

🧠 Why This Matters
This project isn't just about wine—it's about how data can explain human sensory experiences.
By analyzing chemical fingerprints, we inch closer to understanding how structured data translates into subjective perception.

For aspiring data scientists, it demonstrates a clean workflow:

data prep → EDA → modeling → interpretation → storytelling.

🗂️ Next Steps
Expand feature set to include alcohol, sulphates, pH, etc.

Tune XGBoost and test LightGBM.

Convert this analysis into an interactive web app (e.g., Streamlit or Flask).

🔗 Tools Used
Python (pandas, seaborn, matplotlib, scikit-learn, xgboost)

Jupyter Notebook

Visualizations: correlation heatmap, feature importance bar chart, model comparison bar chart

✅ Summary
This project translates the chemistry of wine into data, and the data into insight.
It balances interpretability and performance, while showing that even five features can teach us something meaningful about what makes wine taste “good.”
It belongs in a portfolio not just for the technical execution—but for the curiosity it conveys.


