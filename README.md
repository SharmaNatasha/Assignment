# Sales Data Analysis with User and Weather Data

This project provides a Python script to analyze sales data, enriching it with user and weather information. It offers insights into customer behavior and potential correlations with weather patterns.

**Requirements:**

    Python 3.x
    pandas library
    requests library
    matplotlib library (for visualizations)
    seaborn library (for enhanced visualizations)
    numpy library (for numerical operations)
    sqlalchemy library (for database interaction)

**Installation:**

Ensure you have Python 3.x installed.

Open a terminal or command prompt and navigate to the project directory.

Install the required libraries using pip:

pip install pandas requests matplotlib seaborn numpy sqlalchemy

**Data Files:**

    Replace the placeholder path (/content/AIQ - Data Engineer Assignment - Sales data.csv) with the actual location of your CSV file containing sales data.

**API Credentials:**

    Create an account on OpenWeatherMap (https://openweathermap.org/) to obtain an API key.
    Replace the api_key variable in the script with your own API key.
    
**Database Storage:**

    The script includes functions for storing data in a SQLite database using SQLAlchemy.
    If you intend to use database storage, uncomment the lines related to create_database_engine and store_data functions, and configure your database connection details.

**Running the Script:**

Execute the Python script using the following command:

    python sales_analysis.py

**Explanation:**

    **Data Fetching:**
    
    The script retrieves user data from the JSONPlaceholder API (user_data_url).
    For each sale in the CSV file, it fetches weather data from the OpenWeatherMap API (weather_api_url) using the customer's latitude and longitude.

**Data Transformation:**

    The script transforms the sales data by:
    Merging user data with sales data based on customer ID (assuming a customer_id column exists in both datasets).
    Adding weather information (temperature and condition) for each sale.
    
**Data Analysis:**

    The script performs various analyses, including:
    Total sales per customer
    Average order quantity per product
    Top selling products (by total sales)
    Top spending customers (by total sales)
    Sales trends over time (if a date column exists)
    Average sales amount per weather condition (if weather data is available)
    Additional insights (e.g., top product purchased by each customer)
    The analysis results are printed to the console, and some visualizations are created using matplotlib and seaborn.
    
**Output:**

The script displays insightful visualizations and statistics about your sales data.

**Further Enhancements:**

    Implement error handling for API calls and data storage.
    Explore more sophisticated data analysis techniques and visualizations.
    Consider using a stream processing framework for real-time data analysis.
