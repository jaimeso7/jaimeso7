---
name: Chicago Traffic Crash Analysis – Interactive Dashboards
tools: [Python, bqplot, ipywidgets, HTML]
image: Week14/crash_month_overview.png
description: Two interactive dashboard-style visualizations exploring Chicago traffic crashes using Python, pandas, and bqplot.
custom_js:
  - justcharts
---

# Chicago Traffic Crash Analysis – Interactive Dashboards

This project analyzes traffic crash patterns across Chicago using data from the Chicago Data Portal.  
Two interactive dashboards were built in Python using bqplot and ipywidgets to explore how timing, environmental conditions, and posted speed limits relate to crash frequency.  
The dashboards allow users to examine patterns across months, hours, contributing causes, and roadway conditions. Static images are shown below, and the fully interactive version is available in the linked notebook.

---

# Visualizations

## **Dashboard 1 – Monthly, Hourly, and Cause-Based Crash Patterns**

Below is a static export of the primary dashboard used to explore temporal and causal crash patterns.  
The interactive notebook allows filtering by year range, hour-of-day range, crash causes, and (when run locally) geographic selection.

<img src="{{ site.baseurl }}/assets/img/crash_dashboard_main.png" style="width: 100%">

### **Explanation**

This dashboard highlights how crash activity varies throughout the year and day.  
The “Crashes by Month” plot acts as the **driver**, letting users click one or more months to filter all other visuals. Once selected, the dashboard updates to show the top primary crash causes during those months and when—by hour—those crashes occur most often.

Before visualizing, the raw dataset is processed into usable components such as `YEAR`, `MONTH`, and `HOUR`, allowing the dashboard to clearly show consistent patterns such as morning-rush spikes or seasonal increases. While the map-based heat layer cannot render on PrairieLearn or GitHub Pages, the notebook's local version includes full geographic filtering.

---

## **Dashboard 2 – Crashes by Posted Speed Limit (Weather & Lighting Filters)**

Below is a static version of the second dashboard, which centers on environmental conditions.

<img src="{{ site.baseurl }}/assets/img/crash_weather_speed.png" style="width: 100%">

### **Explanation**

This visualization focuses on how posted speed limits relate to crash frequency when weather and lighting conditions change.  
Users can choose from conditions such as **Snow**, **Rain**, **Clear**, **Daylight**, **Darkness**, or **Street Lights On/Off**.  
The bar chart updates instantly to show how many crashes occurred at each speed limit under the selected factors.

This helps reveal how environmental stressors interact with roadway design—for example, lower-speed areas experiencing more crashes during snow, or higher-speed zones showing increased nighttime risk. It offers a direct way to compare how conditions shape driving outcomes.

---

# Search the Data & Methods

You can access the dataset and the full analysis notebook using the buttons below.

<div class="left">
{% include elements/button.html link="https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if" text="Chicago Crash Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jsoto2003/jsoto2003.github.io/blob/main/python_notebook/crash-viz-project/crash_dashboards.ipynb" text="The Analysis Notebook" %}
</div>

<br><br>

---

# Files Used

- **Dataset:** `traffic_crashes_full.csv`  
- **Notebook:** `python_notebook/crash-viz-project/crash_dashboards.ipynb`  
- **Exported Figures:**  
  - `crash_dashboard_main.png`  
  - `crash_weather_speed.png`  
  - `crash_month_overview.png`  

This project integrates Python-based data processing, interactive dashboard construction with bqplot, and full web deployment using Jekyll on GitHub Pages.
o