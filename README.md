# Weather-Data-Analysis
EXPLORING-WEATHER-DATA-USING-NUMPY


Weather Data Analysis Tool 🌤️
A Python tool for generating and analyzing synthetic weather data using NumPy. This project demonstrates data analysis techniques for temperature patterns, statistical calculations, and weather event identification.
Features

🌡️ Synthetic Weather Data Generation: Create realistic temperature data for any number of days
📊 Statistical Analysis: Calculate averages, extremes, and temperature ranges
🔥 Heatwave Detection: Identify periods of consecutive hot days
📈 Comprehensive Reporting: Generate detailed analysis reports

Installation
Prerequisites

Python 3.7 or higher
NumPy library

Setup

Clone the repository:

bashgit clone https://github.com/yourusername/weather-data-analysis.git
cd weather-data-analysis

Install dependencies:

bashpip install -r requirements.txt
Usage
Basic Usage
Run the main script to see a demonstration:
bashpython weather_analyzer.py
Using as a Module
pythonimport numpy as np
from weather_analyzer import generate_weather_data, basic_statistics, identify_heatwaves

# Generate weather data
weather_data = generate_weather_data(days=365, seed=42)

# Get basic statistics
avg_min, avg_max, max_temp_info, min_temp_info = basic_statistics(weather_data)
print(f"Average max temperature: {avg_max:.2f}°C")

# Identify heatwaves
num_heatwaves, heatwave_periods = identify_heatwaves(weather_data)
print(f"Number of heatwaves: {num_heatwaves}")
Example Output
============================================================
WEATHER DATA ANALYSIS REPORT
============================================================

📊 BASIC STATISTICS:
Average minimum temperature: 2.32°C
Average maximum temperature: 19.85°C
Highest temperature: 35°C on day 123
Lowest temperature: -10°C on day 45

🌡️  TEMPERATURE RANGES:
Average daily temperature range: 17.53°C
Largest daily temperature range: 34°C on day 67

🔥 HEATWAVE ANALYSIS:
Number of heatwaves (3+ consecutive days >30°C): 2
Heatwave periods:
  1. Days 120-125 (6 days)
  2. Days 200-203 (4 days)
API Reference
Functions
generate_weather_data(days=365, seed=42)
Generates synthetic weather data for analysis.
Parameters:

days (int): Number of days to generate data for
seed (int): Random seed for reproducibility

Returns:

np.ndarray: Array with shape (days, 3) containing [day, min_temp, max_temp]

basic_statistics(data)
Calculates basic temperature statistics.
Parameters:

data (np.ndarray): Weather data array

Returns:

Tuple containing average temperatures and extreme values

daily_temperature_range(data)
Analyzes daily temperature ranges.
Parameters:

data (np.ndarray): Weather data array

Returns:

Tuple containing daily ranges and maximum range information

identify_heatwaves(data, threshold=30, min_duration=3)
Identifies heatwave periods in the data.
Parameters:

data (np.ndarray): Weather data array
threshold (int): Temperature threshold for hot days
min_duration (int): Minimum consecutive days for heatwave

Returns:

Tuple containing number of heatwaves and their periods

Project Structure
weather-data-analysis/
├── weather_analyzer.py     # Main analysis module
├── README.md              # Project documentation
├── requirements.txt       # Python dependencies
├── examples/              # Example scripts and notebooks
│   ├── basic_usage.py
│   └── advanced_analysis.py
├── tests/                 # Unit tests
│   ├── __init__.py
│   ├── test_weather_analyzer.py
│   └── test_data_generation.py
└── docs/                  # Additional documentation
    └── api_reference.md
Testing
Run the unit tests to ensure everything works correctly:
bashpython -m pytest tests/
Contributing

Fork the repository
Create a feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m 'Add amazing feature')
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request

License
This project is licensed under the MIT License - see the LICENSE file for details.
Acknowledgments

Built with NumPy for efficient numerical computing
Inspired by real-world weather data analysis needs
Designed for educational and research purposes

Future Enhancements

 Add visualization capabilities with matplotlib
 Implement seasonal pattern analysis
 Add support for multiple weather stations
 Create web interface for data visualization
 Add export functionality for different formats

Contact
Mokgadi Selepe - mokgadi9939@gmail.com
Project Link: https://github.com/Moksel-arch/weather-data-analysis
