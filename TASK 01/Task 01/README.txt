TASK 01: Exploring and Visualizing a Simple Dataset
OBJECTIVE:
Understand how to read, summarize, and visualize a dataset.
---
DATASET:
The "Iris Dataset" is a well-known dataset used for data analysis and machine learning practice.
It contains measurements of iris flowers from three different species:

* Setosa
* Versicolor
* Virginica

FEATURES IN DATASET:
sepal_length – Length of the sepal (cm)
sepal_width – Width of the sepal (cm)
petal_length – Length of the petal (cm)
petal_width – Width of the petal (cm)
species – Type of iris flower
---
LIBRARIES:
Pandas – Data handling and analysis
Seaborn – Dataset loading and visualization
Matplotlib – Plot creation
---
DATASET EXPLORATION:
The dataset was loaded using the Seaborn library and stored in a pandas DataFrame.
The following functions were used to understand the dataset structure:

 `.shape` – Displays number of rows and columns.
 `.columns` – Shows column names.
 `.head()` – Displays the first five records of the dataset.

This step helped in understanding the dataset layout and available features before visualization.
---
VISUALIZATION:

### 1. SCATTER PLOT

A scatter plot was created to analyze the relationship between **petal length** and **petal width**.

PURPOSE:

* To observe relationships between variables.
* To identify clustering among different species.

OBSERVATION:
Different species formed distinct clusters, showing that petal measurements help differentiate flower types.
---
### 2. HISTOGRAM

A histogram was plotted for **sepal length** to examine data distribution.

PURPOSE:

* To understand how values are distributed.
* To identify the most frequently occurring range.

OBSERVATION:
Most sepal length values were concentrated around a central range, showing a balanced distribution.

---

### 3. BOX PLOT

A box plot compared sepal length across species.

PURPOSE:

* To compare spread and median values.
* To detect possible outliers.

OBSERVATION:
Each species showed different median sepal lengths and variation, indicating measurable differences among species.
---
CONCLUSION:
The Iris dataset was successfully explored using basic data visualization techniques. Scatter plots revealed relationships and clustering between variables, histograms showed feature distributions, and box plots highlighted variation among species. These visualizations provide valuable insights into the dataset and help in understanding patterns before applying machine learning models.
Student Assignment – Data Exploration and Visualization
