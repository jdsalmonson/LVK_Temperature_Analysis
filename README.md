## LVK Air and Ocean Buoy Temperature Analysis

This repository contains support material for my [blog post](https://jdsalmonson.github.io/livermore-summer-2024/) on the Summer of 2024 in Livermore, CA.  It contains notebooks and data for analyzing temperature data from the Livermore Airport (LVK) as well as ocean buoy temperature.  

20 years of hourly temperature data was obtained from the [NOAA](https://www.ncei.noaa.gov/access/search/data-search/local-climatological-data-v2?bbox=37.740,-121.823,37.612,-121.695&pageNum=2&dataTypes=HourlyDryBulbTemperature&dataTypes=HourlyWetBulbTemperature&dataTypes=MonthlyMaximumTemperature&dataTypes=MonthlyMeanTemperature&dataTypes=MonthlyMinimumTemperature&startDate=2024-01-01T00:00:00&endDate=2024-10-01T23:59:59).  Other forms of data are available, including data data for pay ($100 per location) from [meteoblue](https://www.meteoblue.com/en/weather/historyclimate/weatherarchive/livermore-municipal-airport_united-states_5367403?fcstlength=1y&year=2024&month=10).

To complement the temperature data at the Livermore airport, I also download the ocean surface temperature data over the last 20 years from the [NOAA webpage for ocean buoy 46214](https://www.ndbc.noaa.gov/station_page.php?station=46214) off the coast, at the edge of the continental shelf.

### Setup

To quickly setup the environment using `uv` and the `requirements.txt` file to run the notebooks:
```bash
cd LVK_Temperature_Analysis

uv venv  # creata a python environment
source .venv/bin/activate  # activate the environment
uv pip install -r requirements.txt  # install packages
```

Or alternatively, create a `micromamba` environment and install the necessary packages:
```bash
micromamba env create -p "./.venv_lvk" "python=3.13"
micromamba activate "./.venv_lvk"
micromamba install "uv"
uv pip install ipykernel ipywidgets # for notebooks
uv pip install numpy scipy matplotlib plotly polars pandas # for analysis
uv pip install rich
uv pip install flit ruff
```

