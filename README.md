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
