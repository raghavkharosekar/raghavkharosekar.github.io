---
layout: default
title: "Homework 6.1 Visualizations"
---

# Homework 6.1: Visualizations with Python, Altair, and Vega-Lite

This page contains the write-up and visualizations for Homework 6.1. Two visualizations were created using Python, Altair, and Vega-Lite based on the Building Inventory dataset. Each plot focuses on a unique aspect of the data, showcasing different analytical approaches and design choices.

---

## Visualization 1: Distribution of Building Usage by County
This visualization is a bar chart showing the number of buildings by usage type (`Usage Description`) across counties. The primary goal of this visualization is to provide an overview of how buildings are utilized in different counties and to identify trends in building usage. For example, counties with high numbers of "Education" or "Storage" buildings stand out in this representation.

### Design Choices
- **Encoding**:
  - The `x-axis` represents the number of buildings.
  - The `y-axis` lists counties, sorted by the total number of buildings for better readability.
  - The `Usage Description` is encoded as color, using a distinct categorical color palette to differentiate usage types.
- **Color Scheme**: The categorical palette was chosen to ensure that each usage type is easily distinguishable.
- **Data Transformations**:
  - Missing values in the `Usage Description` column were replaced with "Unknown".
  - The data was grouped by `County` and `Usage Description` to calculate the count of buildings for each combination.

This bar chart provides a clear and static view of the data, serving as a foundation for understanding the distribution of building types across counties.

![Visualization 1: Bar Chart](assets/bar_chart.html)

---

## Visualization 2: Interactive Scatter Plot of Square Footage by Usage
This visualization is an interactive scatter plot showing the square footage of buildings, categorized by usage type (`Usage Description`) and grouped by county. The goal is to allow users to explore the relationship between building sizes and their usage, while providing the flexibility to focus on specific usage types.

### Design Choices
- **Encoding**:
  - The `x-axis` represents square footage, showing the size of buildings.
  - The `y-axis` lists counties.
  - The `Usage Description` is represented by color, helping users distinguish building purposes.
- **Color Scheme**: A categorical color palette was used to differentiate usage types clearly.
- **Data Transformations**:
  - Rows with zero or missing square footage were removed to ensure accurate representation of building sizes.
  - Missing values in the `Usage Description` column were replaced with "Unknown".
- **Interactivity**:
  - A legend-based multi-selection filter was added, allowing users to dynamically include or exclude specific usage types. 
  - This interactivity makes the scatter plot highly engaging and enhances its usability, enabling users to explore detailed relationships between building sizes and purposes.

This scatter plot’s interactivity is its most notable feature, making it easy to drill down into specific aspects of the dataset.

![Visualization 2: Scatter Plot](assets/scatter_plot.html)

---

## Interactivity Details
For the second plot, the interactive multi-selection filter allows users to focus on specific usage types. By selecting or deselecting categories in the legend, users can dynamically update the visualization. This interactivity helps uncover insights such as which usage types dominate certain counties or how specific usage types compare in terms of building size.

---

## Data and Notebook Links
Explore the dataset and notebook used to create these visualizations:

- [The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
- [The Analysis](https://github.com/USERNAME/REPOSITORY_NAME/blob/main/Workbook.ipynb)

---

## Notes on Homework #5
While some aspects of the bar chart (grouping and color encoding) were inspired by Homework #5, this plot is entirely different as it focuses on building usage by county. In Homework #5, the focus was on filtering temporal data, while here the emphasis is on categorical and geographical distribution. The scatter plot is a new addition, specifically designed to explore building sizes with interactivity.

