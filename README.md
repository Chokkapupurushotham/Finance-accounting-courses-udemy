# Finance-accounting-courses-udemy

FINANCE AND ACCOUNTING COURSES ANALYSIS USING UDEMY DATA

PROJECT OVERVIEW

This project focuses on analyzing a dataset of over 13,000 finance and accounting-related courses from Udemy. The goal is to understand trends in course pricing, popularity, discount strategies, and learner engagement. The project includes data cleaning, transformation, feature engineering, category classification, and visual analysis to uncover insights valuable to learners, instructors, and e-learning platforms.

OBJECTIVES

Analyze subscriber trends, ratings, and reviews for finance-related courses
Evaluate pricing, discount patterns, and currency conversion
Categorize courses by topic using keyword-based classification
Identify top-rated and most-subscribed courses
Prepare data for future modeling and forecasting of course performance

TOOLS AND TECHNOLOGIES USED

Python (Pandas, NumPy, Seaborn, Matplotlib, Plotly, Scikit-learn)
Jupyter Notebook
Machine Learning Model: Random Forest Regressor

DATA OVERVIEW

The dataset includes over 13,000 course records from Udemy with features such as course ID, title, price (original and discounted), ratings, reviews, lectures, test counts, and creation/publishing dates. Key variables:
title, is_paid, num_subscribers, avg_rating, num_reviews, num_published_lectures, price_detail_amount, discount_price_amount, created, published_time

DATA CLEANING AND PREPROCESSING

Missing values were handled using median imputation.
Currency values were converted from INR to USD using a fixed conversion factor (1/82).
Datetime fields were converted using pd.to_datetime.
Unnecessary columns (like URLs, price strings) were dropped.
Categorical fields like is_paid were encoded using One-Hot Encoding.
Outliers were identified and visualized using boxplots.

FEATURE ENGINEERING

A new column was created to calculate the discount percentage.
The course title column was cleaned (lowercased, stripped, non-alphanumeric characters removed).
A custom function was used to categorize course titles into categories like Finance, Business, Data Science, Management, etc.
This allowed better grouping for visual and statistical analysis.

EXPLORATORY DATA ANALYSIS

Top Rated Courses
The highest-rated courses included niche and expert-level content. Ratings ranged from 4.6 to 5.4.

Most Subscribed Courses
Courses like "An Entire MBA in 1 Course" and "The Complete SQL Bootcamp" had over 300K subscribers, showing strong interest in practical business and technical content.

Top Discounted Courses
Some courses offered up to 59% off their original price. Most discounts ranged between 15% and 20%.

Most Expensive Courses
Courses focused on leadership, diversity, marketing, and professional certification were the highest priced, reaching up to $156 USD.

Course Growth Over Time
Course creation peaked around 2020, reflecting the online learning boom. Growth was consistent from 2016 to 2020.

CATEGORY ANALYSIS

Courses were categorized into 13 groups: Finance, Business, Management, Data Science, Project Management, Writing, Communication, etc.
The “Other” category contained over 8,600 courses due to generic or unclear titles.
Spreadsheet (Excel), Communication, and Sales/Marketing were well represented.
Finance had 1,119 courses, Business had 1,450.

Average Reviews by Category
Courses in Data Visualization, Database, and Communication received the most reviews on average, showing high learner interaction.

Average Discounts by Category
Spreadsheet, Communication, and Finance had the highest average discount percentages. Database courses had the least.

Paid vs Free Courses
Most categories were dominated by paid content. Finance had 1,035 paid and 84 free courses. Some categories had exclusively paid content.

MACHINE LEARNING MODEL

A Random Forest Regressor was trained to predict the number of subscribers using features such as average rating, number of reviews, number of lectures, and price.
The model was evaluated using Mean Squared Error and R-squared score.
The prediction performance was acceptable and could be improved with hyperparameter tuning or additional feature engineering.

VISUAL INSIGHTS

Scatterplots and bar charts helped highlight subscriber behavior, discount strategies, and rating distribution.
Histograms and normal distribution plots were used to check the spread and skewness of numerical features.
Line charts showed course growth trends over time.

DATA EXPORT

The final cleaned and processed dataset was saved to a CSV file (Cleaned_Udemy_data.csv) for future analysis or modeling.

CONCLUSION

This project successfully analyzed over 13,000 finance and accounting-related courses from Udemy. The findings revealed popular content categories, pricing strategies, and learner behavior. Through feature engineering, category classification, and model training, the dataset was transformed into a valuable source of insight. These insights can support educators, learners, and e-learning platforms in designing, pricing, and marketing future courses more effectively.
