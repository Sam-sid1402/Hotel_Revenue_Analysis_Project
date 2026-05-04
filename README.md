# Hotel Revenue and Cancellation Analysis

## Project Overview

This project analyzes hotel booking data to understand revenue performance, cancellation behavior, and distribution channel efficiency. The goal is to identify patterns that affect hotel revenue and provide business recommendations based on data.

The project includes data cleaning, feature engineering, SQL analysis, KPI calculation, data visualization, and an exploratory machine learning model for booking cancellation prediction.

## Business Questions

This analysis focuses on the following questions:

- Which hotel type generates more revenue?
- How do cancellation rates differ between hotel types?
- Which distribution channels bring the most revenue?
- Which channels have the highest cancellation risk?
- How does lead time affect cancellation probability?
- Can booking features help predict cancellations?

## Dataset

The dataset contains hotel booking records with information about:

- hotel type
- booking dates
- lead time
- length of stay
- distribution channel
- market segment
- ADR
- cancellation status
- guest information

To simulate real-world data quality issues, missing values, duplicates, inconsistent categories, outliers, and invalid values were intentionally introduced and then handled during cleaning.

## Tools Used

- Python
- pandas
- NumPy
- Matplotlib
- SQLite
- SQL
- scikit-learn
- Jupyter Notebook

## Project Workflow

1. Data Cleaning

The cleaning process included:

- removing duplicate bookings
- handling missing values
- standardizing distribution channel names
- correcting invalid guest values
- removing impossible bookings with zero nights
- handling ADR outliers
- creating a clean arrival date column

2. Feature Engineering

New features were created to support analysis:

- total nights
- total price
- realized revenue
- month
- season
- price group

Canceled bookings were assigned zero realized revenue.

3. SQL Analysis

SQL was used to analyze:

- hotel performance by revenue, ADR, and cancellation rate
- distribution channel performance
- cancellation rate by lead time group

4. Machine Learning

An exploratory Random Forest model was built to predict booking cancellations.

The model was evaluated using:

- accuracy
- precision
- recall
- F1-score
- confusion matrix

Since cancellation prediction involves imbalanced classes, class balancing was applied to improve recall for canceled bookings.

## Key Insights

- City hotels generated higher total revenue due to higher booking volume and stronger ADR.
- City hotels also had higher cancellation rates, making part of their demand less reliable.
- TA/TO channels produced the highest revenue but also showed high cancellation risk.
- Direct and corporate channels had lower cancellation rates, suggesting more stable demand.
- Bookings made more than 90 days in advance had significantly higher cancellation rates.
- Last-minute bookings were more reliable but may represent lower planning visibility for hotels.

## Business Recommendations

- Reduce overdependence on high-cancellation channels by encouraging more direct bookings.
- Monitor long lead-time bookings more carefully, as they carry higher cancellation risk.
- Use cancellation risk signals to improve overbooking and revenue management decisions.
- Strengthen direct booking incentives to improve revenue stability.
- Track cancellation rate together with revenue, not separately, because high revenue channels may also create operational uncertainty.

## Future Improvements

Possible future improvements include:

- building an interactive Tableau dashboard
- adding more advanced feature engineering
- comparing multiple machine learning models
- adding cross-validation
- creating cancellation risk segments
- estimating potential revenue loss from cancellations
