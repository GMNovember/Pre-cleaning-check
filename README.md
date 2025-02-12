# Dataset Precheck Script

## Overview
The Dataset Precheck Script is a Python-based tool that analyzes datasets before cleaning to ensure data integrity. It supports CSV, TSV, and JSON formats and performs various checks such as detecting encoding, identifying missing values, checking for duplicate rows, and assessing data consistency.

## Features
- Detects file encoding.
- Converts JSON to CSV if necessary.
- Checks for missing or duplicate headers.
- Translates foreign language headers to English.
- Analyzes dataset structure (number of rows and columns, data types).
- Identifies common columns across multiple datasets for potential merging.
- Detects missing values.
- Finds duplicate rows.
- Identifies invalid characters.
- Detects mixed data types in columns.
- Identifies potential outliers using the IQR method.

## Requirements
- Python 3.8+
- Required Python libraries:
  - pandas
  - json
  - chardet
  - langdetect
  - deep_translator

Install dependencies using:
```sh
pip install pandas chardet langdetect deep_translator
```

## Usage
1. Place all dataset files (CSV, TSV, JSON) inside a directory (e.g., `datasets/`).
2. Run the script using:
```sh
python dataset_precheck.py
```
3. The script will analyze all supported files in the specified directory and output results.

## Functions
### `detect_encoding(file_path)`
Detects the encoding of a given file.

### `convert_json_to_csv(json_file, csv_file)`
Converts a JSON file to CSV format.

### `load_data(file_path)`
Loads a CSV or TSV file into a pandas DataFrame, detecting the appropriate delimiter and encoding.

### `check_headers(df)`
Checks for missing or duplicate headers in the dataset.

### `translate_headers(df)`
Detects and translates foreign-language headers into English.

### `analyze_structure(df)`
Analyzes dataset structure, including row and column count and data types.

### `find_common_columns(dfs)`
Finds common columns across multiple datasets.

### `check_missing_values(df)`
Identifies missing values in the dataset.

### `check_duplicate_rows(df)`
Counts the number of duplicate rows.

### `check_invalid_characters(df)`
Removes invalid characters from text columns.

### `check_mixed_data_types(df)`
Identifies columns that contain mixed data types.

### `check_outliers(df)`
Detects numerical outliers using the IQR method.

## License
This script is open-source and provided under the MIT License.

