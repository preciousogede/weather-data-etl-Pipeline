# Weather Data ETL Pipeline

## Project Overview

This project demonstrates a simple ETL (Extract, Transform, Load) pipeline using real-time weather data from the OpenWeather API.

The project collects weather information for multiple cities, transforms the extracted data into a clean and structured dataset, stores it as a CSV file, and performs basic analysis to identify patterns across cities.

## Data Source

**OpenWeather API**

The weather data was collected using the OpenWeather Current Weather API.

The following fields were collected:

- City Name
- Temperature (°C)
- Humidity (%)
- Weather Condition
- Wind Speed (m/s)
- Date and Time

## ETL Process

### 1. Extract

Weather data was extracted from the OpenWeather API using Python.

The pipeline collected real-time weather information for 20 cities, including Lagos, London, New York, Dubai, Tokyo, Paris, and others.

### 2. Transform

The extracted data was processed using Pandas.

The transformation steps included:

- Structuring the API response into a Pandas DataFrame
- Renaming columns for consistency and easier analysis
- Converting Unix timestamps into readable datetime values
- Verifying the dataset for data quality issues

The final dataset contained no missing values or duplicate records.

### 3. Load

The transformed dataset was saved as a CSV file:

`weather_data.csv`

This created a structured dataset ready for further analysis or visualization.

## Tools Used

- **Python** – Data extraction and processing
- **Pandas** – Data transformation and analysis
- **Requests** – API requests
- **Google Colab** – Development environment
- **OpenWeather API** – Data source
- **CSV** – Data storage

## Analysis

Basic analysis was performed to:

- Compare temperatures across cities
- Identify cities with the highest humidity
- Compare weather conditions across cities
- Identify the hottest and coolest cities

## Key Findings

Based on the collected weather data:

- **Dubai** recorded the highest temperature at **35.96°C**.
- **Johannesburg** recorded the lowest temperature at **10.94°C**.
- **Lagos** recorded the highest humidity at **92%**, followed by **Accra (88%)** and **Singapore (86%)**.
- **Broken clouds** was the most common weather condition, occurring in **9 of the 20 cities**.
- The dataset showed noticeable differences in temperature, humidity, and weather conditions across the selected cities.

## Project Files

- [Weather ETL Notebook](Weather_ETL.ipynb) – Notebook containing the ETL process and analysis
- [Weather Dataset](weather_data.csv) – Transformed weather dataset
- `README.md` – Project documentation

## Note on API Key

The OpenWeather API requires an API key to retrieve weather data.

For security, the API key used during development has not been included in this repository. The notebook contains a placeholder instead of the actual key.

## Conclusion

This project demonstrates the use of Python to build a basic ETL workflow that connects to an external API, extracts and transforms data, stores the result in a structured format, and generates insights from the collected data.
