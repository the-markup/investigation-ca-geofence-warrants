# TK
This repository contains code and data to reproduce the findings featured in our story, "[TK](https://themarkup.org/TK)."

Data we used to perform our analysis is in the `data` folder.

Jupyter notebooks used for data collection, preprocessing, and analysis are in the `notebooks` folder.

## Installation
### Python
Make sure you have Python 3.6+ installed. We used [virtualenv](https://docs.python-guide.org/dev/virtualenvs/) to create a Python 3.8 virtual environment.

Then install the Python packages:<br>
`pip install -r requirements.txt`

## Notebooks
These notebooks have already been run and do not need to run sequentially.

### `0-clean-data.ipynb`

This notebook generates a clean CSV of each line item included in the `Items to be searched for:` column for a reviewer to mark as a probable reference to a geofence warrant or not.

### `1-filter-data.ipynb`

This notebook generates the `data/calecpa-google-warrants.csv` and `data/probable-geofence-warrants.csv` filtered CSVs, and generates yearly counts.

## Data

### Input Data

| File | Description |
|------|-------------|
| **`data/ca-doj/*.csv`** | These are the CSVs included in the State of California Department of Justice's "[Electronic Search Warrant Notifications](https://openjustice.doj.ca.gov/data)" dataset on OpenJustice |
| **`data/google/Geofence Warrants by Jurisdiction, 2018 through 2020 - Geofence Warrants by Jurisdictions 2018 through 2020.csv`** | This is the CSV included in Google's "[Supplemental Information on Geofence Warrants in the United States](https://services.google.com/fh/files/misc/supplemental_information_geofence_warrants_united_states.pdf)" |

### Output

| File | Description |
|------|-------------|
| **`data/probable-geofence-warrants.csv`** | This is a filtered list of warrants included in the State of California Department of Justice's dataset. Rows included in this dataset contained a  |
| **`data/calecpa-google-warrants.csv`** | This is a filtered list of warrants included in the State of California Department of Justice's dataset. Rows included in this dataset mention Google in at least one cell. |
| **`data/geofence-references-key.csv`** | This is a list of each line item included in the `Items to be searched for:` column, manually marked as a probable reference to a geofence warrant or not. |
