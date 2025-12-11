# Wine-Classification

## Problem Statement
- This dataset contains the properties of red and white wines.

- The purpose of this analysis and modeling is to see if we can predict the type of wine (red or white) based on different properties. 

## Data Dictionary (Generated using ChatGPT)

| **Column Name**          | **Type**   | **Description**                                                                                                        |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------- |
| **fixed acidity**        | float      | Non-volatile acids (tartaric acid, etc.) that do not evaporate easily. Contributes to the overall acidity of the wine. |
| **volatile acidity**     | float      | Amount of acetic acid (vinegar smell). High values negatively impact wine quality.                                     |
| **citric acid**          | float      | Citric acid content. Adds freshness and flavor; small quantities are desirable.                                        |
| **residual sugar**       | float      | Sugar remaining after fermentation. Higher values result in sweeter wine.                                              |
| **chlorides**            | float      | Salt content of the wine. Higher chloride levels can indicate salinity defects.                                        |
| **free sulfur dioxide**  | float      | SO₂ that is not bound. Prevents microbial growth and wine oxidation.                                                   |
| **total sulfur dioxide** | float      | Sum of free + bound SO₂. Excessive levels can produce off-flavors.                                                     |
| **density**              | float      | Density of the wine (g/cm³). Depends on sugar, alcohol, and dissolved substances.                                      |
| **pH**                   | float      | Acidity level of the wine. Lower pH = more acidic. Typical range: 2.87–3.82.                                           |
| **sulphates**            | float      | Potassium sulphate levels. Acts as an antimicrobial and preservative.                                                  |
| **alcohol**              | float      | Alcohol content by volume (%). Higher alcohol often correlates with higher quality.                                    |
| **quality**              | int (0–10) | Sensory-based quality score given by experts (target variable).                                                        |
| **red_wine**                 | string     | 1 - Red, 0 - White                               |


## Executive Summary

### Data Cleaning Steps
No data cleaning had to be done as the data had no missing values, and outliers seemed to be all true values (no clerical errors). 

### Key Visualizations
Include key visualizations that highlight important aspects of the data. Use graphs, charts, or any other visual representation to make your points.

#### Visualization 1: [Wine Counts]
The below barplot shows how many of each wine type is in the dataset. Clearly, the data contains more information on white wines than red wines. 

![bar chart](./images/wine_counts_bar.png)

#### Visualization 2: [Density vs Alcohol]
The below scatterplot shows the correlation between density and alcohol. More importantly, it shows us a clear difference betwee red and white wines. They seem to group close together, but they have a separation. 

![scatter plot 1](./images/density_alcohol.png)

#### Visualization 3: [Volatile vs Citric]
We see the same thing here (to a lesser extent) where the white wines group more to the left, and the red wines group more towards the center, with a bit among the white wines. 

![scatter plot 2](./images/volatile_citric.png)

## Conclusions/Recommendations
I utilized 3 different modeling techniques: K Nearest Neighbors, Random Forest, and Logistic Regression. 

Below are the results

| Model | Score |
| ---- | ---- |
| Random Forest | 0.9945 |
| KNN | 0.9938 |
| Logistic Regression | 0.992 |

The scores were all very close, but Random Forest has the least misses, as seen in the below confusion matrix.

![confusion](./images/rf_conf.png)

In the confusion matrix, we see that it only incorrectly predicted 9 wines. It classified 5 white wines as red, and 4 red wines as white.

## Additional Information
Original Dataset is from [here](https://archive.ics.uci.edu/dataset/186/wine+quality)

---

Feel free to replace the placeholders with your actual content. Additionally, if you have images for your visualizations, make sure to replace the placeholder paths with the correct file paths or URLs.

Once you've filled in the content, save the file with a `.md` extension (e.g., `README.md`). You can use this Markdown file on platforms like GitHub to provide a well-structured README for your analysis.
