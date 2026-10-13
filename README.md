# Venue Visitor Data Visualisation & Exploratory Analysis

## Project Overview

This project explores venue visitor behaviour using Python-based data analysis and visualisation techniques. The objective is to identify meaningful patterns in visitor volumes, spending behaviour, demographic characteristics, and temporal demand to better understand how different venues perform.

Using daily visitor records and venue-level summary attributes, the analysis combines data preparation, statistical exploration, correlation analysis, segmentation, and a range of visualisation techniques to transform raw data into actionable analytical insights.

The project was completed as part of the **COMP 1800 – Data Visualisation** module and demonstrates the application of exploratory data analysis (EDA) to a real-world-style venue analytics problem.

## Objectives

- Analyse and compare total visitor volumes across venues.
- Identify relationships between visitor numbers, average spending, age, travel distance, visit duration, and gender distribution.
- Segment venues according to their total visitor volumes.
- Investigate weekly and seasonal visitor demand patterns.
- Compare the daily visitor distributions of high- and medium-volume venues.
- Identify unusual visitor patterns and account for differences in venue operating periods.
- Communicate analytical findings through clear, informative visualisations.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data manipulation, aggregation, and time-series preparation |
| NumPy | Numerical operations and normalisation |
| Matplotlib | Statistical and comparative visualisations |
| Seaborn | Correlation heatmaps and pairwise analysis |
| Jupyter Notebook | Interactive analysis and reproducible experimentation |

## Visualisation Techniques

The analysis uses multiple visualisation approaches, selected according to the analytical question being investigated.

### 1. Visitor Volume Segmentation

A sorted bar chart compares total visitor numbers across venues. Venues are classified using predefined visitor thresholds:

- Very Low: fewer than 10,000 visitors
- Low: 10,000 to fewer than 40,000
- Medium: 40,000 to 100,000
- High: more than 100,000

This reveals an uneven distribution of visitor demand, with a small number of venues attracting substantially more visitors than the majority.

### 2. Correlation Heatmap

A correlation matrix examines relationships between six venue characteristics: total visitors, average age, distance travelled, visit duration, female percentage, and average spend.

The analysis identifies several notable relationships, including a strong positive correlation between visitor numbers and distance travelled, and between average age and average spend.

### 3. Visitor Numbers vs Average Spend

A dual-axis line chart compares total visitors and average spend across venues.

This highlights an important distinction between visitor volume and spending per visitor: venues with the largest crowds are not necessarily those with the highest average spend.

### 4. Radar Chart of High-Spending Venues

A radar chart compares the normalised characteristics of five selected venues with high average spending.

The visualisation explores differences in visitor volume, average age, distance travelled, visit duration, gender distribution, and average spend.

### 5. Weekly Visitor Distribution

A box plot compares total daily visitor numbers across the seven days of the week.

This helps identify differences in typical demand, variability, and unusually high or low visitor days.

### 6. Monthly Visitor Distribution

Monthly box plots compare daily visitor distributions for selected high- and medium-volume venues throughout the year.

The analysis helps identify seasonal changes, differences between venue groups, and unusual daily observations.

### 7. Pairwise Attribute Exploration

A pair plot provides an overview of pairwise relationships between numerical venue characteristics, supporting further exploratory analysis.

## Key Findings

The analysis identified the following patterns:

- **Uneven visitor distribution:** A small number of venues account for substantially higher visitor volumes, while many venues attract fewer visitors.
- **Visitor volume and travel distance:** Total visitors and distance travelled have a reported correlation of approximately **0.92**.
- **Age and spending:** Average age and average spend show a positive correlation of approximately **0.79**.
- **Visitor volume and spending:** The correlation between total visitors and average spend is approximately **-0.21**, indicating a weak negative relationship.
- **Visit duration and visitor demographics:** Visit duration and female percentage show a positive correlation of approximately **0.67**.
- **Weekly demand:** Sundays, Saturdays, and Mondays generally show higher visitor numbers, while Wednesdays and Thursdays tend to be quieter.
- **Seasonal behaviour:** Visitor numbers are generally higher in January, November, and December, with lower demand during the summer months.
- **Operating-period effects:** Some venues opened later or closed before the end of the observation period, which can influence their recorded visitor totals.

These findings suggest that venue performance should be evaluated using multiple indicators rather than total visitor numbers alone.

*Note: Correlations indicate associations, not causation. Average spend is not equivalent to total revenue or profit.*

## Methodology

The project follows an exploratory data analysis workflow:

1. **Data acquisition:** Load daily visitor records and venue-level attributes from the provided dataset source.
2. **Data preparation:** Parse dates, combine venue characteristics into a summary DataFrame, and aggregate daily visitor counts.
3. **Exploratory analysis:** Examine distributions, descriptive statistics, and differences between venues.
4. **Segmentation:** Classify venues by total visitor volume using predefined thresholds.
5. **Visual analysis:** Develop comparative, distributional, temporal, and correlation-based visualisations.
6. **Interpretation:** Compare findings across multiple charts to develop a consistent understanding of visitor behaviour.
7. **Critical review:** Consider the limitations of fixed segmentation thresholds and the influence of venue operating periods.

## Repository Structure

```text
venue-visitor-data-visualisation/
├── README.md
├── Visualisations.ipynb
├── COMP_1800_Data_Visualisation_Report.pdf
├── requirements.txt
└── .gitignore
```

The repository contains the analysis notebook, coursework report, project documentation, and environment dependencies.

## Getting Started

### Prerequisites

- Python 3.10 or later
- Jupyter Notebook or JupyterLab
- An internet connection to retrieve the source datasets

### Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/venue-visitor-data-visualisation.git
cd venue-visitor-data-visualisation
```

Create and activate a virtual environment:

```bash
python -m venv .venv
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open `Visualisations.ipynb` and execute the notebook cells in order.

### Dataset Access

The notebook retrieves the visitor data and venue attributes from externally hosted CSV files. Internet access is therefore required, and the availability of the original dataset links may affect reproducibility.

The notebook uses the following dataset source:

- `VenueDailyVisitors.csv`
- `VenueAge.csv`
- `VenueDistance.csv`
- `VenueDuration.csv`
- `VenueGender.csv`
- `VenueSpend.csv`

## Limitations and Future Improvements

Potential extensions include:

- Replacing fixed visitor thresholds with quantile-based segmentation or clustering.
- Adding a formal data validation and missing-value handling pipeline.
- Developing an interactive dashboard for filtering venues and exploring time periods.
- Investigating seasonal patterns using more formal statistical methods.
- Comparing visitor volume with total revenue, where suitable revenue data is available.
- Improving reproducibility by documenting dataset provenance, dependency versions, and data preparation steps.

## Skills Demonstrated

Python · Exploratory Data Analysis · Data Cleaning · Data Aggregation · Statistical Analysis · Correlation Analysis · Data Visualisation · Time-Series Exploration · Data Storytelling · Analytical Communication

## Academic Context

This project was completed as part of the COMP 1800 – Data Visualisation module. The repository is intended to demonstrate analytical methods, coding practices, and interpretation of data through visualisation.

The project uses a dataset provided for the coursework, and the notebook adapts and extends visualisation approaches introduced during the module.


