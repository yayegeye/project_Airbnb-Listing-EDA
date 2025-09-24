# Airbnb Listings EDA: New York 2024

### Project Overview
Exploratory Data Analysis (EDA) of New York Airbnb data to uncover rental trends using Pandas, NumPy, Matplotlib, and Seaborn for data cleaning, visualization, and analysis.

### Objectives
1. Analyze room types, prices, and availability across different neighborhoods.
2. Understand host behavior and listing patterns.
3. Detect potential outliers in prices.
4. Provide recommendations for guests and hosts based on insights. 

### Dataset
**20,765 listings with 22 features**  
Key variables:  
- `id`: Unique listing ID
- `name`: Title of the Airbnb listing  
- `host_name`: Name of the host  
- `price`: Nightly rental price (USD)  
- `room_type`: Entire home/apt, Private room, or Shared room  
- `neighborhood_group`: Borough (Manhattan, Brooklyn, etc.)  
- `availability_365`: Days available per year  
- `reviews_per_month`: Average monthly reviews
- `latitude/longitude`: Geolocation of listings    

### Analysis Workflow

### 1. Data Cleaning
- Handle missing data: `price`, `neighborhood`, and `beds` columns had null values.
- Fix data types: Converted `last_review` to a **datetime** object.
- Remove outliers: Listings with prices > $1,000 were capped to avoid skewed visualizations.

### 2. EDA (Exploratory Data Analysis)  
1. **Room type distribution**: 
   - Visualized the count of each room type using **bar plots**.
   - Identified **Entire home/apt** as the most common room type.

2. **Neighborhood group insights**:
   - Analyzed **price variations by boroughs**.
   - Manhattan had the **highest average prices**.

3. **Availability trends**:
   - Used **heatmaps** to show correlations among `price`, `availability_365`, `number_of_reviews`, and `beds`.

4. **Price distribution**:
   - Used **histograms** to show the distribution of prices.
   - Majority of the listings were priced between **$50 - $300**.

5. **Host listings**:
   - Analyzed hosts with multiple listings using **boxplots** to identify key contributors.

6. **Review behavior**:
   - Used **pair plots** to show relationships between number of reviews, price, and availability.

### 3. Visualizations
- Pairplot: To see correlations among `price`, `availability`, and `number of reviews`.
- Heatmap: Showing correlations among numerical features.
- Histograms and Boxplots: To detect outliers in `price`.
- Bar Charts: Displaying room types and neighborhood group distributions.

### Key Findings
1. **Pricing trends**  
   - Manhattan most expensive ($196 avg), followed by Brooklyn
   - Entire homes cost 3x more than private rooms  
2. **Room type distribution**  
   - Entire homes/apartments are the most common, but private rooms offer budget-friendly option  
3. **Outliers**  
   - 27 listings priced > $10,000  
4. **Availability patterns**  
   - Listings with high availability tend to have lower prices and more reviews, likely due to better guest experience. 
5. **Hosts behavior**  
   - Some hosts manage multiple listings, indicating a trend toward professional hosting.

### Future Work
1. Price prediction model
2. Review sentiment analysis
3. Interactive dashboard

### Conclusion
This analysis helps guests find better stays and hosts optimize listings. Key insights show significant price variations by location and room type, and the impact of availability on reviews


