# Patient_Visit_Analysis_EDA

This repository contains a Python-based project focused on cleaning and analyzing a medical appointment dataset. The aim is to prepare the data for insightful analysis and visualization related to appointment no-shows and health indicators.

## 🎯 Project Objectives

The main objectives of this project are:

- 🧹 Clean the dataset by removing invalid or missing values.
- 🔄 Convert and correct data types (especially datetime columns).
- ➕ Engineer new features for deeper analysis (e.g., age groups, time differences).
- 📊 Transform and visualize the data to explore health-related trends and appointment attendance.

## 🧾 Dataset Description

The dataset contains the following columns:

- `PatientId`: Unique identifier for each patient.
- `AppointmentID`: Unique identifier for each appointment.
- `Gender`: Gender of the patient (`F` or `M`).
- `ScheduledDay`: Date and time when the appointment was scheduled.
- `AppointmentDay`: Actual date of the appointment.
- `Age`: Age of the patient.
- `Neighbourhood`: Location of the patient.
- `Scholarship`: Whether the patient has a scholarship (0 = No, 1 = Yes).
- `Hipertension`, `Diabetes`, `Alcoholism`, `Handcap`: Binary indicators for health conditions.
- `SMS_received`: Whether the patient received an SMS reminder.
- `No-show`: Whether the patient missed the appointment (`Yes` = missed, `No` = attended).

## 🛠️ Data Cleaning Steps

- Removed rows with missing or anomalous values in `Neighbourhood` or `Age`.
- Corrected mislabeled values in the `No-show` column and renamed it as `visiting`.
- Converted `ScheduledDay` and `AppointmentDay` to datetime.
- Calculated `diff_time` between scheduling and appointment.
- Removed duplicate rows and outliers.

## 🔄 Data Transformation

- Created new column: `age_category` for grouped age analysis.
- Melted health condition columns (`Hipertension`, `Diabetes`, etc.) into a long format.
- Grouped and aggregated data by `Gender`, `Age Category`, and `Neighbourhood`.

## 📊 Visualizations

The project includes several visualizations:

- Age distribution and no-show comparison
- Appointment attendance by gender and weekday
- Distribution of illnesses by age group and gender
- Most active neighborhoods and their no-show rates

## 📂 File Structure

```
appointment_analysis/
├── p7 - data.csv
├── appointment_analysis.py
├── README.md
└── assets/
    └── [optional figures or charts]
```

## 🚀 How to Run

Ensure that the CSV file is present in your working directory and run the script using Python:

```bash
python appointment_analysis.py
```

## 📝 Notes

- Outliers in age (e.g., >110 or <0) are removed for cleaner analysis.
- The column `No-show` was renamed and inverted to `visiting` to improve interpretation (`yes` = attended).
- Includes both categorical and temporal data handling.

## 📄 License

MIT License. See `LICENSE` for details.

---

Built for healthcare data enthusiasts and analysts 🩺📊
