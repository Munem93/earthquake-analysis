(This project is intended for exploratory analysis only, not for scientific prediction or hazard assessment)


Overview:

This project analyses earthquake data collected over the last two months using Python. The dataset contains 8,886 earthquake records, including information such as magnitude, depth, location, event type, and measurement errors.

The project performs:

Data loading and cleaning
Exploratory data analysis (EDA)
Visualisation of earthquake patterns
Filtering earthquakes in California with specific characteristics
Insights into magnitude, depth, and geographical distribution
This project demonstrates practical skills in Python, pandas, NumPy, matplotlib, seaborn, and general data‑analysis workflows.

Objectives: 

Understand global earthquake patterns from the last two months
Identify the distribution of earthquake magnitudes and depths
Filter and analyse earthquakes in California with specific criteria
Visualise relationships between magnitude, depth, and location
Demonstrate reproducible data analysis using Python

Dataset: 
The dataset (all_month.csv) contains 22 columns and 8,886 rows.
Key fields include:
time — timestamp of the event
latitude, longitude — location
depth — depth in km
mag — magnitude
magType — magnitude scale used
place — nearest location
type — event type (earthquake, quarry blast, explosion, ice quake)
horizontalError, depthError, magError — measurement uncertainties

Example from the dataset:
“time, latitude, longitude, depth, mag, magType, … place, type, status”

Tools and Libraries:

This project uses the following Python libraries:
pandas for data manipulation
NumPy for numerical operations
matplotlib for plotting
seaborn for statistical visualisation

Exploratory Data Analysis: 

1. Histograms of All Earthquake Features
A histogram was generated to visualise the distribution of all numerical columns.
This helps identify:

Common magnitude ranges
Depth distribution
Frequency of measurement errors

2. Event Type Distribution
The dataset contains four event types:

Type	Count
Earthquake	8,746
Quarry blast	82
Explosion	39
Ice quake	19


Earthquakes make up the overwhelming majority of events.

California Earthquake Filtering:

A filtered dataset was created to focus on California earthquakes with the following criteria:
place contains "CA"
type = earthquake
magType = md
gap < 50
mag < 1
depth > 1
This produced a clean subset of 38 earthquakes, which was exported as filtered.csv.

Visualisations:

1. Latitude vs Longitude Scatter Plot
Shows geographical clustering of earthquakes.
Key insight:

High density of events around California, especially near The Geysers region.

2. Magnitude vs Depth Scatter Plot
Reveals that:

Most earthquakes occur at shallow depths

Magnitudes typically range from –1 to 4.8

Deeper quakes are less frequent

Summary of Key Insights:

Earthquakes are most common in California and Alaska within this dataset.
Magnitudes cluster between 0.8 and 2.0, with a long tail up to 7.5.
Depths vary widely, from shallow surface quakes to deep events over 600 km.
California earthquakes with low magnitude and small gap values tend to occur at shallow depths.

Limitations:

Missing values in several columns (nst, gap, dmin, horizontalError, etc.)
Dataset does not include:

Tectonic plate information
Soil type or geological structure
Population density or infrastructure data
Filtering by "CA" in the place field may include edge cases
Magnitude scales (md, ml, mww, etc.) vary in sensitivity

