
# 🌦️ Real-Time Weather Data ETL using Python and MySQL

This project demonstrates a real-time ETL (Extract, Transform, Load) pipeline using Python, the OpenWeatherMap API, and MySQL. It is ideal for beginners looking to gain hands-on experience in working with APIs, data transformation, and database storage using Jupyter Notebook.

## 📌 Objective

To extract real-time weather data using the OpenWeatherMap API, transform the data into a structured format, and load it into a MySQL database for storage and further analysis.

## 🛠 Tech Stack

- Python 3.x
- Jupyter Notebook
- OpenWeatherMap API
- MySQL
- `requests` (Python HTTP library)
- `mysql-connector-python` (for database connection)

## 🔄 ETL Process

### 🔹 Extract

Using the `requests` library, we send an HTTP GET request to the OpenWeatherMap API to retrieve current weather data for a given city. The data is returned in JSON format.

### 🔹 Transform

The JSON response is parsed to extract relevant fields such as:
- City name
- Temperature (in Celsius)
- Humidity
- Weather description

Data is validated and cleaned (e.g., checking for missing or invalid fields).

### 🔹 Load

The transformed data is inserted into a MySQL database table called `weather_data` using a parameterized SQL `INSERT` statement. A timestamp is also added to track when the data was recorded.

## 🗂️ Database Schema

```sql
CREATE TABLE weather_data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    city VARCHAR(100),
    temperature FLOAT,
    humidity INT,
    weather VARCHAR(100),
    timestamp DATETIME
);

## ✨ Features

- 🔌 API Integration: Fetches real-time weather data from the OpenWeatherMap API.
- 🔄 ETL Workflow:
  - Extract: Retrieves live weather data for a specific city.
  - Transform: Cleans and structures JSON data for database compatibility.
  - Load: Inserts transformed data into a MySQL database.
- 🗃️ MySQL Integration: Connects seamlessly with a MySQL database to store and query data.
- 📊 Scalable Structure: Easy to extend for additional cities or different API sources.
- 📝 Jupyter Notebook Implementation: Entire ETL process is demonstrated with explanations in an interactive notebook format.
- ✅ Error Handling: Handles API errors and ensures data quality during transformation.
- 🔧 Customizable: Users can easily modify the city name or API to suit their needs.

## ✅ Use Cases
- Learn how ETL pipelines work
- Practice API integration with Python
- Build a real-time data ingestion tool
- Understand how to interact with SQL databases programmatically

## 📌 Conclusion

This project serves as a practical example of building a real-time ETL pipeline using live weather data. By integrating API data extraction, data transformation, and database loading, it demonstrates the foundational steps of data engineering. It is a great starting point for learners aiming to work with APIs, automate data pipelines, and store structured data in relational databases like MySQL. With further enhancements, this project can evolve into a complete real-time data monitoring and analytics system.

![Screenshot 2025-05-21 180041](https://github.com/user-attachments/assets/f416f508-8821-4f14-9378-48d8ef48f93d)



