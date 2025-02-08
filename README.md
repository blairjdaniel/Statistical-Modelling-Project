# Statistical Modelling Project

This project aims to analyze and model the relationship between the number of bikes in a particular location and the characteristics of Points of Interest (POIs) in that location using data from Yelp and Foursquare APIs. The project is divided into several parts, each focusing on different aspects of data collection, exploration, and modeling.

## Part 1: Data Collection

1. **Collect Data from Yelp and Foursquare APIs**:
   - Use the Yelp and Foursquare APIs to collect data on POIs in your location.
   - Ensure that you gather sufficient data to perform meaningful analysis.

2. **Compare the Quality of the Yelp and Foursquare APIs**:
   - Evaluate which API provides the most complete information or better coverage for your location.
   - Define 'coverage' based on criteria such as the number of POIs, number of reviews per POI, or number of different attributes of each POI.

3. **Challenges**:
    - filtering for Milan was hard as it was in Italian

## Part 2: Data Exploration and Visualization

1. **Explore and Visualize the Data**:
   - Use data visualization techniques to explore the collected data.
   - Identify patterns, trends, and insights from the data.
2. **Challenges**:
    - I had a lot of trouble with creating a loop to iterate through the df then append the right data to the dictionary. I needed to use Larry and mentors quite a bit. 
    - I wish I was more comfortable right away and got results for so much more than just the rating. 

## Part 3: Joining Data

1. **Join the Data**:
   - Combine the data collected from Yelp and Foursquare APIs to create a new dataframe.
   
2. **Data Visualization**:
   - Use data visualization techniques to further explore the joined data.

3. **Create an SQLite Database**:
   - Design and create an SQLite database to store the collected POI data.
   - Validate the data to ensure its integrity and accuracy.

4. **Challenges**:
    - I had trouble seeing what my final dataframe should look like. With Brian's help, I was able to take all the data I stored and narrow it down to the bike_stations only which really helped.

## Part 4: Building a Model

1. **Build a Regression Model**:
   - Use Python’s `statsmodels` module to build a regression model that demonstrates the relationship between the number of bikes in a particular location and the characteristics of the POIs in that location.

2. **Interpret Results**:
   - Expand on the model output and derive insights from your model.

3. **Stretch Goal**:
   - Consider how to turn the regression problem into a classification problem. Sketch out your approach without coding.

4. **Challenges**:
    - Initial results showed very low and even negative numbers, suggesting no linear effect of the features on the number of bikes available.
    - Realized that batching venues into three types might not be effective and considered using more detailed venue types.
    - After further analysis, found that the venue type POI did not significantly predict the number of free bikes, as indicated by its p-value.
    - Suggested using other POI features such as distance for better predictions.
    - Achieved a better result with the model, which claimed an R-squared value of 0.821, indicating it could predict the number of free bikes using the       'timestamp_encoded', 'name_encoded', 'venue_type_encoded', and 'latitude' columns.


## Notebooks

- **yelp_foursquare_EDA.ipynb**: Notebook for data collection, exploration, and visualization.
- **joining_data.ipynb**: Notebook for joining data and creating an SQLite database.
- **model_building.ipynb**: Notebook for building and interpreting the regression model.
