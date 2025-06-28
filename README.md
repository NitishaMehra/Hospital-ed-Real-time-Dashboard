📌 Project Purpose
The goal of this project is to build a Hospital Emergency Room Analysis Dashboard using Power BI that enables hospital stakeholders to:
📈 Improve the efficiency of emergency room operations
🚑 Identify and address bottlenecks in patient care
🧠 Enhance decision-making through real-time, data-driven insights
🗂️ Support strategic planning for better resource allocation and performance tracking

DAX Formula For Patient Attend Status :
=IF([Patient Waittime]<30,"Within Time","Delay")

📊 Key Performance Indicators (KPIs)
The dashboard visualizes the following critical emergency room KPIs:

1. Patient Admission Status
Metric: Number and percentage of patients admitted vs. not admitted

Purpose: Understand ER load and evaluate admission patterns
2. Patient Age Distribution
Metric: Patients grouped by age brackets:

0–4, 5–14, 15–29, 30–44, 45–59, 60–69, 70–79
Purpose: Identify most frequent ER-visiting age groups for targeted healthcare initiatives

3. Timeliness of Care
Metric: Percentage of patients seen within 30 minutes
Purpose: Evaluate ER response time and service efficiency

4. Gender Analysis
Metric: Count of patients by gender (Male, Female, Other/Unspecified)
Purpose: Analyze demographic patterns and ensure equitable care

5. Department Referrals
Metric: Number of patients referred from ER to each hospital department
Purpose: Understand departmental demand and referral trends

🧮 Technical Implementation
📅 Calendar Table Formula
Used to generate a dynamic date table in Power BI:

powerquery
Copy
Edit
= List.Dates(#date(2023,01,01),731,#duration(1,0,0,0))
🧠 DAX Formulas
1. DAX Formula for Age Group
DAX
Copy
Edit
Age Group = 
IF([Patient Age]>=70, "70-79",
    IF([Patient Age]>=60, "60-69",
        IF([Patient Age]>=50, "50-59",
            IF([Patient Age]>=40, "40-49",
                IF([Patient Age]>=30, "30-39",
                    IF([Patient Age]>=20, "20-29",
                      IF([Patient Age]>=10, "10-19", "0-4") 
                )
            )
        )
    )
)
3. DAX Formula for Patient Attend Status (Timeliness)
DAX
Copy
Edit
Patient Attend Status = 
IF([Patient Waittime] < 30, "Within Time", "Delayed")
📂 Project Files
File	Description
.pbix file	Power BI dashboard project
.xlsx file	Source dataset used for the dashboard
README.md	Project overview and documentation

📌 Insights & Impact
This dashboard provides clear visibility into emergency room dynamics. It helps healthcare providers:

React faster to patient surges
Allocate resources based on referral trends
Improve wait times and patient satisfaction
Support data-driven hospital policies

✅ Future Enhancements
Add real-time data refresh via database or API connection
Include heat maps for peak admission hours and departments
Integrate predictive analysis for future ER trends

🧑‍💻 Developed With
Microsoft Power BI
Microsoft Excel
DAX (Data Analysis Expressions)
Power Query (M Language)









