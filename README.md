# Revenue Potential Analysis on Google Play Store Apps

This project presents an exploratory data analysis (EDA) focused on understanding the impact of pricing strategies on the performance and revenue potential of apps available on the Google Play Store.

The goal is to uncover patterns in app installs, user ratings, and monetization models to help developers and businesses make informed decisions about app pricing and category targeting.

## Dataset Overview

- **Source**: Google Play Store Dataset (from Kaggle)
- **Number of records**: Approximately 10,000 apps
- **Key features**:
  - App name, Category
  - Rating, Reviews
  - Installs
  - Price, Type (Free or Paid)
  - Size, Content Rating
  - Last Updated

## Data Cleaning and Preparation

To ensure accurate and meaningful analysis, the following steps were performed:

- Removed duplicate entries.
- Dropped rows with missing values in important fields: Rating, Installs, Price, and Type.
- Cleaned the `Installs` column by removing characters such as '+' and ',' and converted it to an integer.
- Cleaned the `Price` column by removing the '$' symbol and converted it to a float.
- Replaced non-numeric values such as 'Free' in the `Price` column with 0.
- Created a new column called `Estimated_Revenue`, calculated as:  
  `Estimated_Revenue = Price × Installs`  
  (Note: This is a rough estimate and does not account for in-app purchases or ads.)

## Exploratory Data Analysis

### Free vs Paid Apps Comparison

- Compared app ratings and install counts between free and paid apps.
- Found that free apps dominate the store, but paid apps tend to have slightly higher average ratings.

### Revenue Estimation

- Estimated the potential revenue for each paid app.
- Identified the top 10 revenue-generating paid apps.
- Analyzed the distribution of revenue across price ranges and app categories.

### Price Optimization

- Grouped paid apps into pricing bins (e.g., $0–1, $1–5, $5–10, etc.).
- Calculated average ratings and installs for each pricing bin.
- Identified that apps priced in the $1–$5 range tend to perform well in both installs and user satisfaction.

### Category-wise Revenue

- Analyzed total estimated revenue by app category.
- Found that categories such as Games, Productivity, and Tools generated the highest revenues among paid apps.

## Key Insights

- Free apps dominate in volume and downloads, but paid apps show slightly better user ratings.
- The $1–$5 price range appears to be the most effective in balancing revenue and customer satisfaction.
- Revenue is highly concentrated in a few categories, suggesting targeted opportunities for monetization.

## Conclusion

This analysis provides meaningful insights into how app pricing affects performance on the Google Play Store. It can help developers and businesses:

- Decide between offering free vs paid apps.
- Choose optimal price ranges for better market response.
- Focus on high-revenue categories when planning app development.

## Future Work

- Develop predictive models for app revenue or success using machine learning.
- Apply natural language processing (NLP) to analyze app descriptions.
- Build an interactive dashboard using Streamlit to explore the dataset in real time.

## Project Files

- `EDA.ipynb`: Jupyter Notebook with full analysis, visualizations, and commentary.
- `cleaned_playstore_revenue_analysis.csv`: (Optional) Cleaned dataset used for analysis.

## Tools and Technologies Used

- Python 3
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly Express
- Jupyter Notebook

## How to Run

1. Clone this repository to your local machine.
2. Install required Python libraries (`pandas`, `numpy`, `seaborn`, `matplotlib`, `plotly`).
3. Open `EDA.ipynb` in Jupyter Notebook or a compatible IDE.
4. Run the notebook step by step to reproduce the analysis.
