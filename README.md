### Healthcare Industry Case Study: Predicting No-Show Appointments

#### Problem Statement
The goal is to predict whether a patient will show up for a scheduled medical appointment. The dataset consists of 300k medical appointments and includes 15 variables describing each appointment.

#### Dataset Description
- **PatientId:** Unique identifier for a patient.
- **AppointmentID:** Unique identifier for each appointment.
- **Gender:** Indicates whether the patient is male or female.
- **DataMarcacaoConsulta:** The date of the actual appointment.
- **DataAgendamento:** The date when the appointment was scheduled.
- **Age:** Age of the patient.
- **Neighbourhood:** Location where the appointment takes place.
- **Scholarship:** Indicates if the patient is part of the Bolsa Família program.
- **Hipertension:** Indicates if the patient has hypertension.
- **Diabetes:** Indicates if the patient has diabetes.
- **Alcoholism:** Indicates if the patient has a history of alcoholism.
- **Handcap:** Indicates if the patient has a handicap.
- **SMS_received:** Number of SMS reminders sent to the patient.
- **No-show:** Indicates if the patient showed up for the appointment.

#### Approach
1. **Data Cleaning and Preparation:**
   - Check for missing values and erroneous entries.
   - Correct column name typos.
   - Convert `AppointmentRegistration` and `Appointment` columns to `datetime64` format.
   - Calculate `AwaitingTime` and convert it to absolute values.
   - Create a new feature `HourOfTheDay` indicating the hour at which the appointment was booked.
   
2. **Outlier Detection:**
   - Identify and remove outliers from the `Age` variable using appropriate plots.

3. **Exploratory Data Analysis (EDA):**
   - Analyze the probability of showing up concerning different features.
   - Create scatter plots and trend lines to examine the relationship between the probability of showing up with respect to age, hour of the day, and awaiting time.
   - Create bar graphs to depict the probability of showing up for conditions like diabetes, alcoholism, hypertension, smoking, and scholarship.

4. **Gender and Reminder Analysis:**
   - Create separate bar graphs to show the probability of showing up for male and female patients, the day of the week, and SMS reminders.

5. **Predictive Modeling:**
   - Focus on features that show the most variation in the probability of showing up:
     - Age
     - Diabetes
     - Alcoholism
     - Hypertension
     - Smoking
     - Scholarship
     - Tuberculosis

6. **Visualization:**
   - Create a dashboard in Tableau using appropriate chart types and metrics useful for the business.


