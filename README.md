# NSEAutomated-Report-Retrieval_November_2024

---

# NSE Report Downloader and Validator

This project automates the process of downloading and validating NSE (National Stock Exchange) reports. The program performs the following tasks:
- Downloads CSV reports from the NSE website.
- Validates the CSV files for existence, structure, data types, and anomalies.
- Logs the validation results for easier tracking.

## Features
- **File Existence Check**: Verifies if the specified file exists and if it's a valid CSV.
- **Duplicate Handling**: Verifies if the specified file is a duplicate.
- **Data_Retrieval**: automated report downloading module
- **CSV Loading**: Loads the CSV file into a pandas DataFrame for further processing.
- **Column Validation**: Ensures that all columns are present and have valid names.
- **Data Type Validation**: Checks for consistent data types within each column.
- **Anomaly Detection**: Identifies missing values or empty rows.
- **Logging**: Detailed logging for each step of the process, including success and error messages.

## Requirements
Before running the script, ensure you have the following installed:
- Python 3.x
- pandas (`pip install pandas`)
- selenium (`pip install selenium`)

## File Structure
```text
NSE_Report_Downloader/
│
├── nse_report_downloader.log       # Log file for the process
├── main.py                         # Main script to initiate the report downloading and validation
├── csv_validation.py               # Contains the validation logic for CSV files
└── duplicates_handler.py
└── Data_retrieval.py
                            # Additional modules as needed (e.g., for downloading or file handling)
```

## Installation
1. Clone or download the repository.
2. Install the required dependencies:

   ```bash
   pip install pandas
   pip install selenium
   ```

3. Ensure you have access to the `nse_report_downloader.log` log file for monitoring the script's activities.

## Usage
1. **Set Up Download Directory**: Update the `download_directory` in `main.py` to your preferred location for storing the downloaded reports.
2. **Run the Script**: Execute the `main.py` script to initiate the download and validation process.

   ```bash
   python main.py
   ```

3. The script will:
   - Download the reports.
   - Validate the CSV files.
   - Handle the duplicate reports
   - Log any errors or issues with the files.

4. **Log File**: Check the `nse_report_downloader.log` file for detailed logs on the validation process.

## Logging
The script uses Python's `logging` module to log detailed information about its execution. Log messages are written to both the console and the `nse_report_downloader.log` file.

### Log Levels:
- **INFO**: Information about the script's progress.
- **WARNING**: Potential issues, such as missing values or anomalies.
- **ERROR**: File-related errors (e.g., file not found, invalid format).
- **CRITICAL**: Critical issues that may halt the execution of the script.





## Troubleshooting
- **File Not Found**: Ensure that the file path you provide is correct and that the file exists in the specified location.
- **Invalid File Format**: Ensure that the file is a `.csv` file.
- **Missing Columns or Invalid Data**: Check the CSV file to ensure that it matches the expected format, and that there are no missing columns or inconsistent data types.



