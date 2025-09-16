Airbnb NYC Data Analysis
- Project Overview

This project focuses on Exploratory Data Analysis (EDA) of the Airbnb NYC dataset.
The goal is to clean, transform, and analyze the data to uncover insights about hosts, prices, availability, and reviews.

 - Dataset

Source: Airbnb NYC (2019) public dataset

Size: ~49,000 rows

Features include:

id, name, host_id, host_name

neighbourhood_group, neighbourhood, room_type

price, minimum_nights, number_of_reviews, last_review

reviews_per_month, availability_365

 Steps Performed
 
1. Data Loading & Inspection

Loaded dataset into Jupyter Notebook.

Inspected shape, dtypes, columns, head, and tail.

2. Data Cleaning

Handled missing values:

name, host_name, last_review, reviews_per_month contained missing values.

Filled text columns (name, host_name) with "Unknown".

Filled numeric columns with median values.

Converted datatypes:

Changed last_review to datetime format.

Checked duplicates: None found.

Renamed columns: Converted all column names to snake_case style.

3. Handling Outliers

minimum_nights: Fixed unrealistic values (>1000 days) by capping at 365 days.

price: Removed extreme values (> $5000).

4. Exploratory Data Analysis (EDA)

Value counts: Distribution of room_type and neighbourhood_group.

Average price by neighbourhood_group.

Correlation analysis:

Created a heatmap.

Found mostly weak positive or negative correlations, no strong relationships.

5. Feature Engineering

Created new features:

price_per_night = price / minimum_nights

Extracted year and month from last_review

Created has_reviews column → 1 if reviews > 0 else 0

6. Advanced Analysis

Top 10 hosts with most listings

Average reviews by room type

Neighbourhood with highest number of listings

Relationship between availability_365 and reviews:

Weak positive correlation

Being available more days slightly increases chance of reviews

But availability alone does not strongly determine review count

 --> Key Insights

Room types: Entire home/apartment and private room dominate listings.

Neighbourhood trends: Some groups have higher average prices.

Outliers matter: Without cleaning minimum_nights and extreme prices, results are misleading.

Correlation: No strong linear relationships between numeric variables.

Availability vs Reviews: Availability affects reviews slightly, but not a major driver.

Hosts: A few top hosts own a large number of listings.
