# Global Terrorism Analysis Dashboard (Power BI)

## Overview

This project presents an **interactive Power BI dashboard** analyzing global terrorism incidents using the **Global Terrorism Database (GTD)**.
The dashboard visualizes trends in terrorism incidents, fatalities, injuries, attack types, and geographical distribution from **1970–2017**.

The report is designed as a **scrollable infographic-style dashboard** that allows users to explore terrorism trends over time and understand patterns across countries and attack types.

---

# Dataset

**Dataset Name:** Global Terrorism Database (GTD)

**Source:** National Consortium for the Study of Terrorism and Responses to Terrorism (START)

**Dataset Link:**
https://www.kaggle.com/datasets/START-UMD/gtd

**File Used:**

```
globalterrorismdb_0718dist.csv
```

### Key Columns Used

| Column          | Description                   |
| --------------- | ----------------------------- |
| iyear           | Year of the incident          |
| imonth          | Month of the incident         |
| iday            | Day of the incident           |
| country_txt     | Country where attack occurred |
| city            | City of incident              |
| latitude        | Latitude coordinate           |
| longitude       | Longitude coordinate          |
| attacktype1_txt | Type of attack                |
| nkill           | Number of fatalities          |
| nwound          | Number of injured             |

---

# Project Objective

The objective of this dashboard is to:

• Analyze global terrorism trends over time
• Identify countries with the highest number of incidents
• Understand the distribution of different attack types
• Visualize geographic patterns of terrorism
• Explore yearly and monthly trends in incidents and fatalities

---

# Dashboard Features

The dashboard includes several interactive visual components.

---

# 1. Terrorism Overview Section

Provides a high-level introduction to global terrorism trends.

Features:

• Total number of incidents (1970–2017)
• Introductory description of terrorism trends
• Large KPI visual highlighting total incidents

---

# 2. Incident Trend Analysis

Visualizes how terrorism incidents evolved over time.

Visual Used:
• Line Chart

Fields Used:

| Axis   | Field              |
| ------ | ------------------ |
| X-axis | iyear              |
| Y-axis | Count of incidents |

Insights:
• Rapid increase in incidents after 2010
• Clear long-term trend in global terrorism activity

---

# 3. Geographic Distribution (Map)

Displays where terrorism incidents occur around the world.

Visual Used:
• Map Visualization

Fields Used:

| Field       | Data            |
| ----------- | --------------- |
| Latitude    | latitude        |
| Longitude   | longitude       |
| Bubble Size | Total Incidents |

Features:
• Global spatial analysis of terrorism events
• Interactive geographic filtering

---

# 4. Fatalities Analysis

Shows yearly fatalities caused by terrorism.

Visual Used:
• Line Chart with data markers

Fields Used:

| Axis   | Field        |
| ------ | ------------ |
| X-axis | iyear        |
| Y-axis | Sum of nkill |

Features:
• Trend of fatalities over decades
• Peak periods of high casualties

---

# 5. Incident Types Breakdown

Displays the distribution of different attack types.

Visual Used:
• Horizontal Bar Chart

Fields Used:

| Axis   | Field              |
| ------ | ------------------ |
| Y-axis | attacktype1_txt    |
| X-axis | Count of incidents |

Examples of attack types:

• Bombing / Explosion
• Armed Assault
• Assassination
• Hostage Taking
• Infrastructure Attack

This visual helps identify **most common terrorist tactics**.

---

# 6. Top Countries by Terrorism Incidents

Displays countries with the highest number of incidents.

Visual Used:
• Horizontal Bar Chart

Fields Used:

| Axis   | Field              |
| ------ | ------------------ |
| Y-axis | country_txt        |
| X-axis | Count of incidents |

Insights:
• Countries like Iraq, Pakistan, Afghanistan, and India show high incident counts.

---

# 7. 2017 Timeline Analysis

An interactive section showing **monthly attack patterns in 2017**.

Visuals Used:

• Country Slicer (scrollable country selection)
• Monthly Donut Charts
• KPI Cards for incidents, fatalities, and injured

Fields Used:

| Field           | Purpose               |
| --------------- | --------------------- |
| imonth          | Monthly analysis      |
| attacktype1_txt | Attack type breakdown |
| nkill           | Fatalities            |
| nwound          | Injuries              |

Features:

• Select a country using the slicer
• Dashboard dynamically updates monthly attack patterns
• Displays type of attacks for each month

---

# 8. Country-Level Armed Assault Analysis

Displays statistics specifically for **Armed Assault incidents in India**.

Metrics Calculated:

• Total incidents
• Total fatalities
• Total injured

Measures used:

```
Armed Assault Incidents India
Armed Assault Fatalities India
Armed Assault Injured India
```

---

# Data Modeling

Power BI measures were created using **DAX** for custom calculations.

Examples:

```
Armed Assault Incidents India =
CALCULATE(
COUNTROWS(globalterrorismdb_0718dist),
globalterrorismdb_0718dist[country_txt] = "India",
globalterrorismdb_0718dist[attacktype1_txt] = "Armed Assault"
)
```

---

# Dashboard Design

The dashboard was designed as a **scrollable storytelling report**.

Design features include:

• Infographic-style layout
• Section-based analysis
• Minimalistic background theme
• Interactive slicers and filters
• KPI indicators
• Data-driven storytelling

---

# Tools Used

| Tool             | Purpose                   |
| ---------------- | ------------------------- |
| Power BI Desktop | Data visualization        |
| Power Query      | Data preparation          |
| DAX              | Measures and calculations |
| Power BI Service | Dashboard publishing      |

---

# Key Insights

From the analysis:

• Terrorism incidents increased significantly after 2010
• Bombing/Explosion is the most common attack type
• Several countries experience higher concentration of attacks
• Fatality rates fluctuate significantly across years
• Attack types vary across regions and months

---

# How to Run the Project

1. Install **Power BI Desktop**
2. Download the dataset
3. Open the `.pbix` file
4. Refresh the data source if necessary
5. Explore the interactive dashboard

---

---
