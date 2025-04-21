# Medical Appointment No-Shows Data Cleaning and Preprocessing

## Project Overview

This project focuses on cleaning and preprocessing the "Medical Appointment No Shows" dataset from Kaggle. The goal is to prepare the data for further analysis and modeling.

## Steps Taken

1. **Data Loading:**
    - Loaded the dataset into a Pandas DataFrame using `pd.read_csv()`.

2. **Data Type Conversion:**
    - Converted the `AppointmentDay` and `ScheduledDay` columns to datetime objects using `pd.to_datetime()`.
    - Extracted the date part from the datetime objects using `.dt.date`.
    - Converted the `PatientId` column to string type using `astype(int).astype(str)`.

3. **Data Validation:**
    - Inspected the data types of all columns using `df.info()`.
    - Checked for unique values in categorical columns (`Gender`, `Scholarship`, etc.).
    - Examined the distribution of appointments across neighborhoods using `df.groupby('Neighbourhood')['PatientId'].count()`.

4. **Duplicate Handling:**
    - Searched for duplicate appointment IDs using `df[df['AppointmentID'].duplicated() == True]`.


## Data Cleaning Summary:
- Date and time features have been converted to the appropriate data type.
- 'PatientId' has been converted to a string.
- Confirmed that there are no duplicate appointments.
- Verified the types of all the features.
