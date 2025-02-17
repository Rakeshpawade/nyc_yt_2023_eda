# New York City Yellow Taxi Data Analysis

## Objective
In this case study, you will be learning exploratory data analysis (EDA) with the help of a dataset on yellow taxi rides in New York City. This will enable you to understand why EDA is an important step in the process of data science and machine learning.

## Problem Statement
As an analyst at an upcoming taxi operation in NYC, you are tasked to use the 2023 taxi trip data to uncover insights that could help optimize taxi operations. The goal is to analyze patterns in the data that can inform strategic decisions to improve service efficiency, maximize revenue, and enhance passenger experience.

## Data Understanding
The yellow taxi trip records include fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts.

The data is stored in Parquet format (*.parquet*). The dataset is from 2009 to 2024. However, for this assignment, we will only be using the data from 2023.

The data for each month is present in a different parquet file. You will get twelve files for each of the months in 2023.

The data was collected and provided to the NYC Taxi and Limousine Commission (TLC) by technology providers like vendors and taxi hailing apps.

You can find the link to the TLC trip records page here: [TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

### Data Description
You can find the data description here: [Data Dictionary](https://www.nyc.gov/assets/tlc/downloads/pdf/data_dictionary_trip_records_yellow.pdf)

### Trip Records
| Field Name             | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| VendorID               | A code indicating the TPEP provider that provided the record.               |
| tpep_pickup_datetime   | The date and time when the meter was engaged.                               |
| tpep_dropoff_datetime  | The date and time when the meter was disengaged.                            |
| Passenger_count        | The number of passengers in the vehicle.                                    |
| Trip_distance          | The elapsed trip distance in miles reported by the taximeter.               |
| PULocationID           | TLC Taxi Zone in which the taximeter was engaged.                           |
| DOLocationID           | TLC Taxi Zone in which the taximeter was disengaged.                        |
| RateCodeID             | The final rate code in effect at the end of the trip.                       |
| Store_and_fwd_flag     | This flag indicates whether the trip record was held in vehicle memory.     |
| Payment_type           | A numeric code signifying how the passenger paid for the trip.              |
| Fare_amount            | The time-and-distance fare calculated by the meter.                         |
| Extra                  | Miscellaneous extras and surcharges.                                        |
| MTA_tax                | 0.50 USD MTA tax that is automatically triggered based on the metered rate. |
| Improvement_surcharge  | 0.30 USD improvement surcharge assessed trips at the flag drop.             |
| Tip_amount             | Tip amount – This field is automatically populated for credit card tips.    |
| Tolls_amount           | Total amount of all tolls paid in trip.                                     |
| Total_amount           | The total amount charged to passengers.                                     |
| Congestion_Surcharge   | Total amount collected in trip for NYS congestion surcharge.                |
| Airport_fee            | 1.25 USD for pick up only at LaGuardia and John F. Kennedy Airports.        |

### Taxi Zones
Each of the trip records contains a field corresponding to the location of the pickup or drop-off of the trip, populated by numbers ranging from 1-263. These numbers correspond to taxi zones, which may be downloaded as a table or map/shapefile and matched to the trip records using a join.

## Requirements
Ensure you have the following Python libraries installed before running the notebook:

```bash
pip install pandas numpy matplotlib seaborn
```

Recommended versions:
- numpy: 1.26.4
- pandas: 2.2.2
- matplotlib: 3.10.0
- seaborn: 0.13.2

## Usage
1. Clone the repository and navigate to the project folder:
   ```bash
   git clone <repo-url>
   cd <project-folder>
   ```
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook EDA_Assg_NYC_Taxi_Starter.ipynb
   ```
3. Run each cell sequentially to perform data analysis.

## Outline
The notebook is structured as follows:
1. **Introduction**: Overview of the problem, dataset and objectives.
2. **Data Understanding**: Reading Parquet files and inspecting data structure.
   - **Data Description**: Refer to Trip Records.
3. **Data Preparation**: Import required libraries, load dataset and perform data sampling.
3. **Data Cleaning**: Handling missing values, outliers, and data inconsistencies.
4. **Exploratory Data Analysis**:
   - **General EDA: Finding Patterns and Trends**: Analyze Numerical or Categorical variables.
   - **Detailed EDA: Insights and Strategies**: Basic analyses for finding trends and patterns.
6. **Conclusion**: Summarizing findings and potential improvements.

## Data Handling
- The dataset consists of multiple Parquet files.
- Data is loaded in chunks to prevent memory overload.
- Basic exploratory steps include:
  - Checking missing values
  - Visualizing trip distributions
  - Analyzing fare and distance trends

## Key Features
- Reads taxi trip data from Parquet files.
- Uses Pandas and NumPy for data manipulation.
- Generates visualizations using Matplotlib and Seaborn.
- Includes filtering and data sampling strategies for efficient analysis.

## Notes
- Ensure Parquet files are stored in the correct directory (`trip_records/`).
- The notebook filters warnings for better readability.

## License
This project is released under an open-source license. Feel free to modify and contribute.