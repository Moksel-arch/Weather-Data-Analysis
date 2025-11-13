Weather Data Analysis
EXPLORING WEATHER DATA USING NUMPY

Weather Data Analysis Tool

A Python tool for generating and analyzing synthetic weather data with NumPy. It shows off data‑analysis tricks for temperature patterns, stats, and weather‑event detection.

Features
Synthetic Weather Data Generation – Create realistic temperature data for any number of days.

Statistical Analysis – Calculate averages, extremes, and temperature ranges.

Heatwave Detection – Spot periods of consecutive hot days.

Comprehensive Reporting – Generate detailed analysis reports.

Installation
Prerequisites
- Python 3.7 or higher
- NumPy

Setup

Clone the repository:


bash
git clone https://github.com/Moksel-arch/weather-data-analysis.git
cd weather-data-analysis


Install dependencies:


bash
pip install -r requirements.txt


Usage
Basic Usage

Run the main script to see a demonstration:


bash
python weather_analyzer.py


Using as a Module


import numpy as np
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


WEATHER DATA ANALYSIS REPORT

BASIC STATISTICS:
Average minimum temperature: 2.32°C
Average maximum temperature: 19.85°C
Highest temperature: 35°C on day 123
Lowest temperature: -10°C on day 45

TEMPERATURE RANGES:
Average daily temperature range: 17.53°C
Largest daily temperature range: 34°C on day 67

HEATWAVE ANALYSIS:
Number of heatwaves (3+ consecutive days >30°C): 2
Heatwave periods:
1. Days 120-125 (6 days)
2. Days 200-203 (4 days)


API Reference
Functions

- generate_weather_data(days=365, seed=42) – Returns an array (days, 3) with [day, min_temp, max_temp].
- basic_statistics(data) – Returns average temps and extreme values.
- daily_temperature_range(data) – Returns daily ranges and the max range info.
- identify_heatwaves(data, threshold=30, min_duration=3) – Returns count and periods of heatwaves.

Testing
Run the unit tests:


bash
python -m pytest tests/


Contributing
Fork the repo, create a feature branch, commit, push, and open a pull request.

License
MIT License – see LICENSE file for details.

Acknowledgments
Built with NumPy for efficient numerical computing. Inspired by real‑world weather analysis needs. Designed for education and research.

Future Enhancements
- Add visualization with matplotlib
- Implement seasonal pattern analysis
- Support multiple weather stations
- Create a web interface for data visualization
- Add export functionality for various formats

Contact
Mokgadi Selepe – mokgadi9939@gmail.com

[Project Link](https://github.com/Moksel-arch/weather-data-analysis.)
