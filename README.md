# No-Show Medical Appointments Analysis

Exploratory Data Analysis (EDA) project using the Brazilian Medical Appointment dataset.

The goal of this project is to identify factors associated with missed medical appointments and investigate the relationship between appointment attendance, waiting time, SMS reminders, demographic variables, and medical conditions.

---

## Dataset

Dataset: No-show Appointments (Brazil)

The dataset contains more than 110,000 medical appointments and includes:

- Demographic information
- Medical conditions
- Appointment scheduling details
- SMS reminders
- Healthcare location information

---

## Research Questions

1. What factors are associated with missed medical appointments?

2. Why do patients receiving SMS reminders appear to have higher no-show rates?

---

## Data Wrangling

The following cleaning and transformation steps were performed:

- Converted date columns to datetime format.
- Removed invalid age values.
- Encoded the target variable (`No-show`) as a binary indicator.
- Created `WaitingDays`.
- Created `HasHandicap`.
- Converted identifier columns to string type.
- Investigated unusual values in `Handcap`.

---

## Key Findings

### Neighbourhood Matters

No-show rates vary considerably between neighbourhoods, suggesting that location may be one of the strongest factors associated with appointment attendance.

![Neighbourhood Analysis](images/neighbourhood_no_show_rate.png)

---

### Longer Waiting Times Are Associated With More Missed Appointments

Patients with longer waiting periods were more likely to miss appointments.

![Waiting Time Distribution](images/waiting_days_distribution.png)

---

### SMS Reminders and Waiting Time

At first glance, patients receiving SMS reminders appeared more likely to miss appointments.

However, further investigation showed that patients receiving SMS reminders experienced substantially longer waiting times.

- Median waiting time without SMS: 0 days
- Median waiting time with SMS: 14 days

![SMS Waiting Time](images/sms_waiting_days.png)

---

### Waiting Time Explains Much of the SMS Effect

After grouping patients by waiting-time intervals, no-show rates were consistently lower among patients who received SMS reminders.

This suggests that the apparent negative effect of SMS reminders is largely explained by longer waiting periods rather than the reminders themselves.

![SMS and Waiting Time](images/sms_waiting_bins.png)

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Limitations

This investigation is based on exploratory data analysis and does not establish causal relationships.

Several potentially important variables were not available in the dataset, including:

- Transportation access
- Income level
- Appointment type
- Healthcare facility characteristics

No formal statistical hypothesis testing or predictive modeling was performed.

---

## Author

José Arturo Trelles Hernández
