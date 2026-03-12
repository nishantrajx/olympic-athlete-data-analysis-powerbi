# 🏅 Olympic Athlete Data Analysis Dashboard

**Power BI | Power Query | DAX | Data Visualization**

---

# 📌 Project Overview

This project analyzes historical **Olympic athlete and medal data (1896–2016)** to uncover trends in athlete participation, country performance, medal distribution, and athlete demographics.

Using **Power BI**, the dataset was cleaned, modeled, and visualized to build an **interactive dashboard** that allows users to explore Olympic statistics through dynamic filters and charts.

The analysis focuses on identifying **top-performing countries, athlete participation trends, medal distribution patterns, and age-related performance insights**.

---

📊 Analytical Questions Answered

The dashboard was designed to answer the following analytical questions:

1. How has athlete participation evolved across Olympic years?

The analysis examines participation trends across Summer and Winter Olympics to understand how global engagement in the Olympic Games has expanded over time.

2. Which countries have achieved the highest medal performance?

The dashboard identifies top-performing countries based on total medal counts and medal type distribution.

3. How are medals distributed across Gold, Silver, and Bronze categories?

This analysis evaluates the proportional distribution of medals across categories to understand competition outcomes.

4. What is the typical age range of medal-winning athletes?

The analysis explores the age distribution of medal-winning athletes to identify peak performance age groups.

5. Which athletes have achieved the highest number of Olympic medals?

This objective identifies top athletes based on total medal counts across Olympic events.

---

# 📂 Dataset

The dataset used in this project contains historical Olympic records.

**Dataset Details**

* Total Records: **270,000+ athlete entries**
* Time Period: **1896 – 2016**
* Attributes: **15 columns**

Key columns include:

* Athlete ID
* Athlete Name
* Gender
* Age
* Height
* Weight
* Country (NOC)
* Olympic Year
* Season (Summer / Winter)
* City
* Sport
* Event
* Medal

---

# 🛠 Tools and Technologies

### Data Visualization

* Power BI

### Data Transformation

* Power Query Editor

### Data Modeling

* Power BI Data Model

### Calculations

* DAX (Data Analysis Expressions)

---

# 🔧 Data Preprocessing

Data preprocessing was performed using **Power Query Editor** to improve data quality before analysis.

### Handling Missing Values

Missing values were addressed using statistical methods:

* **Age** → replaced with median value **24**
* **Height** → replaced with median value **175 cm**
* **Weight** → replaced with median value **70 kg**
* **Medal** → replaced with category **"No Medal"**

Median values were used instead of mean to minimize the effect of extreme values.

---

### Data Type Corrections

Correct data types were assigned to support accurate analysis.

Examples:

* ID → Whole Number
* Age → Whole Number
* Height → Whole Number
* Weight → Decimal Number
* Year → Whole Number
* Text fields → Text format

---

### Text Cleaning

Text columns were standardized using:

* Trim
* Clean
* Proper case formatting

This ensured consistent labels in slicers and visualizations.

---

### Country Code Standardization

Some country codes contained suffixes such as:

```
USA-1
USA-2
```

These suffixes were removed to ensure correct country-level aggregation.

---

### Calculated Columns Created

Additional calculated columns were created to simplify analysis.

Examples:

**Gender Column**

```
Male
Female
```

**Medal Flag**

Binary indicator:

```
1 → Medal Winner
0 → No Medal
```

---

# 📊 Data Modeling

The dataset was loaded as a **single fact table (`athlete_events`)** in Power BI.

A single-table model was used because the dataset already contained all required attributes.

Advantages of this model:

* Simpler architecture
* Faster dashboard performance
* Easier DAX calculations
* Reduced relationship complexity

---

# 📈 DAX Measures

Several DAX measures were created to support dashboard KPIs.

Examples include:

**Total Athletes**

```
Total Athletes = DISTINCTCOUNT(athlete_events[ID])
```

**Total Medals**

```
Total Medals = COUNT(athlete_events[Medal])
```

**Gold Medals**

```
Gold Medals = CALCULATE(COUNT(athlete_events[Medal]), athlete_events[Medal] = "Gold")
```

**Silver Medals**

```
Silver Medals = CALCULATE(COUNT(athlete_events[Medal]), athlete_events[Medal] = "Silver")
```

**Bronze Medals**

```
Bronze Medals = CALCULATE(COUNT(athlete_events[Medal]), athlete_events[Medal] = "Bronze")
```

These measures dynamically update based on slicer selections.

---

# 📊 Dashboard Analysis

The dashboard explores several analytical objectives.

---

# 1️⃣ Athlete Participation Trends

**Objective**

Analyze how athlete participation has changed over time.

**Visualization**

Line Chart

**Axes**

* X-axis → Year
* Y-axis → Total Athletes
* Legend → Season

**Insight**

Athlete participation has steadily increased over time, with **Summer Olympics showing significantly higher participation than Winter Olympics**.

---

# 2️⃣ Top Performing Countries

**Objective**

Identify countries with the highest Olympic medal counts.

**Visualization**

Stacked Bar Chart

**Axes**

* X-axis → Total Medals
* Y-axis → Country
* Legend → Medal Type

**Insight**

Countries such as **United States, Russia, Germany, and Great Britain consistently dominate Olympic medal counts**.

---

# 3️⃣ Medal Distribution

**Objective**

Analyze the distribution of Gold, Silver, and Bronze medals.

**Visualization**

Donut Chart

**Insight**

The distribution of medals across categories is relatively balanced, reflecting competitive parity across events.

---

# 4️⃣ Age Distribution of Medal Winners

**Objective**

Understand how athlete age influences medal performance.

**Visualization**

Stacked Column Chart

**Insight**

Athletes between **20–30 years old win the majority of Olympic medals**, indicating peak athletic performance within this range.

---

# 5️⃣ Top Olympic Athletes

**Objective**

Identify athletes with the highest medal counts.

**Visualization**

Stacked Bar Chart

**Insight**

The visualization highlights **top athletes who achieved consistent medal success across multiple Olympic Games**.

---

# 🎛 Interactive Dashboard Features

The dashboard includes several slicers for dynamic analysis:

* Year (range slider)
* Season (Summer / Winter)
* Gender
* Event

These filters allow users to **explore Olympic data interactively and perform customized analysis**.

---

# 📊 Key Insights

Important findings from the analysis include:

* Olympic participation has **steadily increased over time**
* **Summer Olympics dominate participation levels**
* Countries like **USA and Russia lead medal counts**
* Most medal-winning athletes fall within the **20–30 age range**

---

# 📁 Project Structure

```
olympic-data-analysis-powerbi
│
├── data
│   └── athlete_events.xlsx
│
├── dashboard
│   └── olympic_dashboard.pbix
│
├── report
│   └── olympic_analysis_report.pdf
│
├── images
│   ├── participation_trend.png
│   ├── medal_distribution.png
│   ├── top_countries.png
│   └── age_analysis.png
│
└── README.md
```

---

# 🚀 Future Improvements

Possible extensions of this project include:

* Integration of **geospatial medal analysis**
* Development of **predictive models for medal outcomes**
* Creation of **interactive web dashboards using Streamlit**

---

# 👨‍💻 Author

**Nishant**

B.Tech Computer Science and Engineering

Lovely Professional University

---

