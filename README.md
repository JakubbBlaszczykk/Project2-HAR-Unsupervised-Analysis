# Human Activity Recognition: Unsupervised Learning Analysis

## Project Overview
This project explores **unsupervised learning techniques** to analyze human physical activities based on smartphone sensor data. Using the **UCI Human Activity Recognition (HAR)** dataset, the goal is to determine whether mathematical patterns in sensor readings can automatically group similar activities without prior knowledge of the labels.

The core challenge involves working with high-dimensional data (561 features) and effectively reducing it to visualize and cluster distinct motion patterns.

## Dataset
**Dataset:** [Human Activity Recognition Using Smartphones (UCI)](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones)
* **Source:** Accelerometer and gyroscope readings from Samsung Galaxy S II.
* **Dimensions:** 10,299 samples, 561 attributes (time and frequency domain variables).
* **Activities:** Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, Laying.

## Methodology & Tech Stack
The analysis is implemented in **Python** using the following pipeline:

1.  **Data Preprocessing**:
    * Feature scaling using `StandardScaler`.
    * Merging training and test sets for comprehensive unsupervised analysis.
2.  **Dimensionality Reduction**:
    * **PCA (Principal Component Analysis):** To reduce noise and visualize variance.
    * **t-SNE:** To visualize local structures and cluster separability in 2D/3D space.
3.  **Clustering**:
    * **K-Means Clustering:** To group data into $k=6$ clusters corresponding to the activities.
    * **Evaluation:** Comparing clusters against ground truth labels using Confusion Matrix and Adjusted Rand Index (ARI).

## Key Questions
* Can we distinguish between static (sitting, standing) and dynamic (walking) activities without labels?
* How does t-SNE compare to PCA in visualizing high-dimensional sensor data?
* Where does the K-Means algorithm fail, and why?

## Results (Preview)
*(image of your t-SNE plot once I generate it)*
> The analysis shows that dynamic activities form distinct clusters, while static activities (Standing vs. Sitting) overlap significantly due to the similar sensor orientation.

---
**Author:** Jakub Błaszczyk
