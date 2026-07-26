# 🌦️ Weather Data Analysis (2015–2024)

A data analysis project exploring 10 years of daily weather data to uncover temperature and rainfall trends over time.

## 📌 Overview

This project pulls historical weather data via the Open-Meteo API, cleans and structures it with pandas, stores it in a SQLite database, and uses SQL queries to analyze yearly and monthly trends. Results are visualized using seaborn and matplotlib.

## 🛠️ Tools & Technologies

- **Python** — pandas, numpy
- **SQL** — SQLite (data storage & querying)
- **Visualization** — seaborn, matplotlib
- **Data Source** — [Open-Meteo API](https://open-meteo.com/)

## 🔍 Process

1. **Extract** — Pulled 10 years (2015–2024) of daily temperature and precipitation data using Open-Meteo's Historical Weather API
2. **Clean** — Handled data types (fixed date parsing), checked for missing values, structured the data with pandas
3. **Load** — Pushed the cleaned dataset into a SQLite database
4. **Analyze** — Wrote SQL queries to compute yearly and monthly trends (averages, extremes)
5. **Visualize** — Built charts in seaborn/matplotlib to communicate findings

## 📊 Key Findings

- **Temperature trend:** Average max temperature rose from ~25.8°C in 2015 to ~26.9°C in 2024 — an increase of about 1°C over the decade. The trend wasn't perfectly linear: 2017 was the warmest year (27.08°C) and 2020 the coolest (25.73°C) in this dataset.
- **Rainfall pattern:** July is by far the wettest month, averaging ~13.4 mm of daily rainfall, followed by August (~11.3 mm) — together confirming a clear monsoon season from June to September. November is the driest month, averaging just ~0.17 mm of daily rainfall.

## 📈 Visuals

**Yearly Average Max Temperature**
![Yearly Temperature Trend](outputs/yearly_temp_trend.png)

**Monthly Average Temperature**
![Monthly Average Temperature](outputs/Heat_Map.png)

**Monthly Average Rainfall**
![Monthly Rainfall](outputs/Monthly_average_Rainfall.png)

## 📂 Project Structure

```
weather-data-analysis/
├── notebooks/
│   └── weather_analysis.ipynb    # Main analysis notebook
├── outputs/
│   ├── yearly_temp_trend.png
│   ├── Monthly_average_temp.png
│   └── Monthly_average_Rainfalll.png
├── README.md
└── requirements.txt
```

## 🚀 How to Run

1. Clone this repository
2. Install dependencies: `pip install -r requirements.txt`
3. Run `notebooks/weather_analysis.ipynb` — this creates a local `weather.db` SQLite file automatically, no separate database setup needed

## 🔮 Future Improvements

- Compare multiple cities side by side
- Build an interactive Power BI dashboard
- Add extreme weather event detection (heatwaves, dry spells)
- Extend historical range beyond 10 years

---

*This project was built as a hands-on way to practice pandas, SQL, and data visualization using real-world, messy weather data.*