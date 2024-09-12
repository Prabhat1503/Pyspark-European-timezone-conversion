# Pyspark-European-timezone-conversion-and-Monthly-Sales-Data-Analysis

This repository contains a PySpark notebook for performing timezone conversions and processing sales data using Databricks. The notebook reads sales data from a CSV file, applies timezone conversions, and processes the data by month.


## Notebook Overview

The notebook performs the following operations:

1. **Initialization**: Sets up a Spark session and defines the schema for the CSV data.
2. **Data Loading**: Loads the sales data from a CSV file stored in DBFS.
3. **Timestamp Conversion**: Converts the `ModifiedDate` column to a timestamp format.
4. **Random Seconds Addition**: Adds a random number of seconds to the London time for variability.
5. **Timezone Conversion**: Converts the timestamp to various European timezones (London, Berlin, Paris, Madrid, Rome).
6. **Daylight Saving Time Check**: Determines if daylight saving time (DST) is in effect based on the day of the year.
7. **Monthly Data Processing**: Extracts year and month from the `ModifiedDate`, filters data for each month, and stores it in a dictionary.

## How to Run on Databricks

1. **Upload Data**:
   - Navigate to the Databricks workspace and upload the CSV file to DBFS (Databricks File System).
   - Use the path `/FileStore/tables/Sales_SalesOrderDetail-2.csv` for the CSV file in the notebook.

2. **Create a Cluster**:
   - Ensure you have a Databricks cluster running. You can create a new cluster from the Databricks workspace.

3. **Import and Run the Notebook**:
   - Import the PySpark notebook into your Databricks workspace.
   - Attach the notebook to your running cluster.
   - Run all the cells in the notebook.

4. **View Results**:
   - The notebook will display data with timezone conversions and print monthly data to the console.
   - Optionally, uncomment lines to save the processed monthly data to CSV files on DBFS.

## Example Output

The notebook prints data for each month with the following columns:
- `London_Time`
- `Berlin_Time`
- `Paris_Time`
- `Madrid_Time`
- `Rome_Time`
  
  ![image](https://github.com/user-attachments/assets/ffbbcf50-3a83-4ce5-a0df-81dbb1ecaf4d)


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

