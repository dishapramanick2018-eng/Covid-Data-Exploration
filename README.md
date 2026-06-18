# Covid-Data-Exploration
Data Analytics Project showcasing covid vaccination analysis using SQL, Python, Power BI
# COVID-19 Data Exploration using SQL

## Project Overview

This project focuses on exploring and analyzing global COVID-19 data using SQL. The analysis is performed on COVID-19 deaths and vaccination datasets to uncover trends, infection rates, death rates, and vaccination progress across countries and continents.

The project demonstrates practical SQL skills commonly used by Data Analysts, including:

* Joins
* Common Table Expressions (CTEs)
* Temporary Tables
* Window Functions
* Aggregate Functions
* Data Type Conversions
* Views

---

## Dataset

The project uses two tables:

### CovidDeaths

Contains information about:

* Total cases
* New cases
* Total deaths
* Population
* Location
* Date
* Continent

### CovidVaccinations

Contains information about:

* New vaccinations
* Vaccination dates
* Locations

---

## Business Questions Answered

### 1. Total Cases vs Total Deaths

Analyzes the likelihood of death after contracting COVID-19.

**Metrics Used:**

* Total Cases
* Total Deaths
* Death Percentage

```sql
(total_deaths / total_cases) * 100
```

---

### 2. Total Cases vs Population

Measures the percentage of a country's population infected with COVID-19.

**Metrics Used:**

* Population
* Total Cases
* Percent Population Infected

```sql
(total_cases / population) * 100
```

---

### 3. Countries with Highest Infection Rate

Identifies countries with the highest percentage of infected population.

**Metrics Used:**

* Highest Infection Count
* Percent Population Infected

---

### 4. Countries with Highest Death Count

Ranks countries based on total COVID-19 deaths.

**Metrics Used:**

* Total Death Count

---

### 5. Death Count by Continent

Compares continents based on COVID-19 mortality figures.

**Metrics Used:**

* Maximum Total Deaths per Continent

---

### 6. Global COVID-19 Statistics

Provides worldwide COVID-19 summary metrics.

**Metrics Used:**

* Total Cases
* Total Deaths
* Global Death Percentage

---

### 7. Population vs Vaccination Analysis

Tracks cumulative vaccination progress over time.

**Techniques Used:**

* Inner Join
* Window Functions
* Running Totals

**Key Metric:**

```sql
RollingPeopleVaccinated
```

Calculated using:

```sql
SUM(new_vaccinations)
OVER (PARTITION BY location ORDER BY date)
```

---

## SQL Concepts Demonstrated

### Joins

Combined COVID death and vaccination datasets.

### Window Functions

Used running totals to calculate cumulative vaccinations.

### Common Table Expressions (CTEs)

Simplified complex calculations and improved readability.

### Temporary Tables

Stored intermediate results for further analysis.

### Data Type Conversion

Used CAST() and CONVERT() to handle numeric calculations.

### Views

Created reusable views for reporting and visualization.

---

## View Created

### PercentPopulationVaccinated

This view stores vaccination progress data and can be directly connected to visualization tools such as Power BI or Tableau.

```sql
CREATE VIEW PercentPopulationVaccinated AS
...
```

---

## Key Insights

* Identified countries with the highest infection rates relative to population.
* Compared COVID-19 death rates across countries and continents.
* Calculated global death percentages.
* Tracked vaccination rollout progress using cumulative vaccination counts.
* Created reusable SQL objects for future reporting and dashboard development.

---

## Tools Used

* SQL Server
* SQL Server Management Studio (SSMS)
* COVID-19 Dataset
* Power BI (for future visualization)

---

## Learning Outcomes

Through this project, the following data analytics skills were strengthened:

* Writing advanced SQL queries
* Data exploration and profiling
* Trend analysis
* Aggregation and reporting
* Creating reusable database objects
* Preparing datasets for dashboard visualization

---

## Author

**Disha Pramanick**

Aspiring Data Analyst skilled in SQL, Power BI, Excel, and Data Visualization, with a strong interest in transforming data into actionable business insights.
