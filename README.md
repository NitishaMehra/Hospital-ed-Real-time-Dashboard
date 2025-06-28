 🏥 Hospital Emergency Room Analysis Dashboard

## 📌 Project Purpose

The goal of this project is to build a Hospital Emergency Room Analysis Dashboard using Power BI that enables hospital stakeholders to:

- 📈 Improve the efficiency of emergency room operations  
- 🚑 Identify and address bottlenecks in patient care  
- 🧠 Enhance decision-making through real-time, data-driven insights  
- 🗂️ Support strategic planning for better resource allocation and performance tracking  

---

## 📊 Key Performance Indicators (KPIs)

The dashboard visualizes the following critical emergency room KPIs:

### 1. Patient Admission Status
- **Metric:** Number and percentage of patients admitted vs. not admitted  
- **Purpose:** Understand ER load and evaluate admission patterns  

### 2. Patient Age Distribution
- **Metric:** Age group brackets: 0–4, 5–14, 15–29, 30–44, 45–59, 60–69, 70–79  
- **Purpose:** Identify the most frequent ER-visiting age groups for targeted healthcare initiatives  

### 3. Timeliness of Care
- **Metric:** Percentage of patients seen within 30 minutes  
- **Purpose:** Evaluate ER response time and service efficiency  

### 4. Gender Analysis
- **Metric:** Count of patients by gender (Male, Female)  
- **Purpose:** Analyze demographic patterns and ensure equitable care  

### 5. Department Referrals
- **Metric:** Number of patients referred from ER to each hospital department  
- **Purpose:** Understand departmental demand and referral trends  

---

## 🧮 Technical Implementation

### 📅 Calendar Table Formula

Used to generate a dynamic date table in Power BI:

= List.Dates(#date(2023,01,01), 731, #duration(1,0,0,0))
🧠 DAX Formulas
DAX Formula for Age Grouping:


Age Group =
IF([Patient Age]>=70, "70-79",
 IF([Patient Age]>=60, "60-69",
 IF([Patient Age]>=50, "50-59",
 IF([Patient Age]>=40, "40-49",
 IF([Patient Age]>=30, "30-39",
 IF([Patient Age]>=20, "20-29",
 IF([Patient Age]>=10, "10-19", "0-4")))))))
DAX Formula for Patient Attend Status (Timeliness):


Patient Attend Status = IF([Patient Waittime] < 30, "Within Time", "Delayed")
📂 Project Files
File Name Description
HospitalER.pbix Power BI dashboard project file
ER_Dataset.xlsx Source dataset used for the dashboard
README.md Project overview and documentation

---

📌 Insights & Impact
This dashboard provides clear visibility into emergency room dynamics and helps healthcare providers to:

⚡ React faster to patient surges

📋 Allocate resources based on referral trends

⏱ Improve wait times and patient satisfaction

📊 Support data-driven hospital policies

✅ Future Enhancements
🔄 Add real-time data refresh via database/API connections

🗺 Include heat maps for peak admission hours and departments

🔮 Integrate predictive analysis for future ER trends

🧑‍💻 Developed With
Microsoft Power BI

Microsoft Excel

DAX (Data Analysis Expressions)

Power Query (M Language)

---


## 👩‍💻 About Me

Hi, I’m **Nitisha Mehra** from **Indore, India** — a data enthusiast with a strong academic background in **Commerce (B.Com Hons.) from Medicaps - University** and an **MBA from Sage University**.

My core interests lie in **data analytics**, **business operations**, and applying **data-driven solutions** to real-world problems. I believe in continuous learning and enjoy turning raw data into meaningful insights that support strategic decisions.

* ✅ Communication & Collaboration
* ✅ Time Management & Problem Solving
* ✅ Client Handling & Operational Support

### 💻 Technical Skills:

* **Languages & Tools**: Python (NumPy, Pandas), SQL, Excel
* **Analytics**: Data Cleaning, Preprocessing, Visualization
* **Dashboards**: Power BI (KPI tracking, charts, graphs)
* **Other**: Google Maps Data Scraping, Web Automation

I’m curious, self-motivated, and looking to grow my career in **Data Analytics** or **Business Intelligence**.

📧 Email: [mehranitisha009@gmail.com](mailto:mehranitisha009@gmail.com)
🔗 [LinkedIn](https://www.linkedin.com/in/nitisha-mehra-680822317)

---
