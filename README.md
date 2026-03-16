# Smartphone-Usage-Addiction-Analysis
# Introduction:
This dashboard presents a comprehensive analysis of smartphone usage patterns among 7,500 users. It highlights segmentation by age, gender, usage intensity, and addiction severity, offering clear behavioural insights. The findings reveal consistent screen time across demographics, with moderate to severe usage emerging as the dominant trend.
# Objective:
•	Analyze smartphone usage patterns among 7,500 users, segmented by age, gender, and usage intensity.
•	Identify addiction severity levels (None, Mild, Moderate, Severe) to understand the prevalence of higher risk categories.
•	Compare screen time averages across demographics (age groups, gender, academic work response) to highlight behavioral consistency and minor variations.
•	Provide actionable insights into user engagement and risk factors, supporting meaningful interpretation for dashboards and reports.
# Dataset Description:
- Identifiers: Each record has a unique transaction_id and user_id to track individual users.
- Demographics: Includes age and gender to analyze usage patterns across different groups.
- Usage Metrics: Captures daily_screen_time_hours, social_media_hours, gaming_hours, and weekend_screen_time to measure engagement.
- Derived Columns: Total Screentime Usage and Total Usage classify users into categories (Low, Medium, High).
- Lifestyle Factors: Tracks work_study_hours, sleep_hours, notifications_per_day, and app_opens_per_day to understand balance and habits.
- Psychological Indicators: Includes stress_level and academic_work_impact to assess behavioral effects.
- Addiction Measures: addiction_level and addicted_label indicate severity (None, Mild, Moderate, Severe) and whether a user is flagged as addicted.
# Data Cleaning (Power Query) & Data Imputation:
•	Use Remove Duplicates to ensure unique transaction_id and user_id.
•	Apply Fill Down/Replace Values for missing data.
•	Use Change Type to set correct data types (whole number, decimal, text).
•	Apply Trim/Clean to remove extra spaces or hidden characters in text fields.
•	Use Replace Values to standardize categories (e.g., “Yes/No” for academic work impact).
•	Created Total Screentime Usage by summing daily_screen_time_hours + social_media_hours + gaming_hours.
•	Added Total Usage as a categorical column based on thresholds:
o	Low Usage → ≤ 8 hours
o	Medium Usage → 8–12 hours
o	High Usage → > 12 hours
•	Verified that each user’s Total Screentime Usage correctly matches the assigned Total Usage category.
•	Standardized labels to ensure consistency (only “Low Usage”, “Medium Usage”, “High Usage”).
•	Create Conditional Columns to verify or recalculate derived fields (e.g., addicted_label based on addiction_level). 
# Data Exploration:
# Descriptive statistics Total Screentime Usage:	
•	📊 Average screen time: Mean is about 12.79 hours per day.
•	⚖️ Spread of data: Standard deviation is 3.27 hours, showing moderate variation among users.
•	📈 Central tendency: Median is 12.78 hours (very close to mean), Mode is 11.25 hours.
•	🔄 Distribution shape: Skewness is nearly 0 (−0.01), meaning the data is almost symmetric.
•	📉 Peakedness: Kurtosis is −0.62, indicating a slightly flatter distribution than normal.
•	📐 Range: Usage spans from 3.92 hours (minimum) to 21.34 hours (maximum), a range of 17.42 hours.
•	🔢 Sample size: Total of 7,500 users, with a combined screentime sum of 95,906.84 hours.
•	📏 Precision: Standard error is 0.038, showing the mean is estimated with high accuracy.
# Descriptive statistics Sleep hours:
•	😴 Average sleep: Mean is about 6.74 hours per day.
•	📊 Central tendency: Median is 6.72 hours, Mode is 7.77 hours.
•	⚖️ Variation: Standard deviation is 1.28 hours, showing moderate differences in sleep among users.
•	📐 Range: Sleep spans from 4.5 hours (minimum) to 9 hours (maximum), a range of 4.5 hours.
•	🔄 Distribution shape: Skewness is close to 0 (0.02), meaning the data is nearly symmetric.
•	📉 Peakedness: Kurtosis is −1.18, indicating a flatter distribution than normal.
•	🔢 Sample size: Total of 7,500 users, with a combined sleep sum of 50,531.71 hours.
•	📏 Precision: Standard error is 0.015, showing the mean is estimated with high accuracy.
# Pivot Table:
1.	Screen time usage is nearly identical across genders, with male users showing a slightly higher average (100.64%) compared to female (99.56%) and other (99.78%).
2.	The majority of users fall into medium usage (4,133), followed by High usage (2,794), while Low usage (573) is the smallest segment among the 7,500 users.
3.	Average daily screen time remains consistent across genders and academic work responses, hovering around 12.7–12.9 hours, with only marginal differences between Yes and No groups.
4.	Average daily screen time across ages 18–35 is about 7.5 hours, with slightly higher usage observed around ages 21, 26, 29, and 35.
5.	Smartphone usage levels are evenly distributed across genders, with medium usage being the largest segment (≈4,133 users), followed by high usage (≈2,794), while low usage remains the smallest (≈573).
6.	Among 7,500 users, moderate addiction severity is the largest group (2,874), followed by severe (2,434), while mild (1,373) and none (819) are much smaller segments.
# Project Insights:
•	Screen Time Patterns: Average daily screentime is around 12.8 hours, consistent across genders and academic work responses, showing minimal demographic variation.
•	Age Trends: Users aged 21, 26, 29, and 35 show slightly higher screen time, but overall usage remains steady (~7.5 hours) across ages 18–35.
•	Usage Segmentation: Majority of users fall into Medium Usage (≈4,133), followed by High Usage (≈2,794), while Low Usage is rare (≈573).
•	Addiction Severity: Most users are in Moderate (2,874) or Severe (2,434) categories, highlighting significant risk levels compared to Mild (1,373) or None (819).
•	Sleep Behavior: Average sleep is 6.7 hours, with moderate variation (range 4.5–9 hours), suggesting reduced rest among heavy users.
•	Lifestyle Impact: Higher screentime correlates with increased stress levels and academic work impact, reinforcing the behavioral risks of excessive smartphone use.
•	Overall Insight: The dataset reveals a dominance of medium to severe smartphone addiction, stable usage across demographics, and lifestyle trade offs in sleep and stress.
# Conclusion:
The analysis shows that most users spend heavy amounts of time on smartphones, averaging nearly 13 hours daily. Moderate to severe addiction levels dominate, with clear impacts on sleep and stress. Overall, the findings highlight consistent high engagement and significant behavioral risks across demographics.
