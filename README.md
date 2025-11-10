
# 🍽️ Zomato Dataset Exploratory Data Analysis (EDA)

This project performs a comprehensive exploratory data analysis (EDA) on the Zomato dataset. The goal is to uncover patterns and insights related to restaurant distributions, user ratings, online delivery services, and geographical variations.

## 📊 Table of Contents

  * [Project Overview](https://www.google.com/search?q=%23-project-overview)
  * [Analysis Pipeline](https://www.google.com/search?q=%23-analysis-pipeline)
  * [Key Insights & Visualizations](https://www.google.com/search?q=%23-key-insights--visualizations)
  * [Tools Used](https://www.google.com/search?q=%23-tools-used)
  * [How to Run](https://www.google.com/search?q=%23-how-to-run)
  * [Future Work](https://www.google.com/search?q=%23-future-work)

## Project Overview

This analysis uses two datasets:

  * `zomato.csv`: Contains detailed information about restaurants, including location, cuisines, cost, and ratings.
  * `Country-Code.xlsx`: A mapping file to link country codes with their respective country names.

The primary objective is to clean, merge, and analyze this data to answer key business questions, such as:

  * What is the geographical spread of Zomato's listings?
  * What do user ratings tell us about customer satisfaction?
  * Which countries and cities have the highest concentration of restaurants?
  * Where is the online delivery service most prevalent?

## 🚀 Analysis Pipeline

1.  **Data Loading:** Imported the `zomato.csv` and `Country-Code.xlsx` files using Pandas.
2.  **Data Cleaning & Preprocessing:**
      * Merged the two datasets on `"Country Code"` to add full country names to the main dataframe.
      * Checked for missing values. Found and visualized 9 missing entries in the `'Cuisines'` column using a Seaborn heatmap.
3.  **Exploratory Data Analysis (EDA):**
      * Analyzed the geographical distribution of restaurants by country and city.
      * Investigated the relationship between `Aggregate rating`, `Rating color`, and `Rating text`.
      * Examined the distribution and origin of zero ratings.
      * Identified which countries offer online delivery.
      * Mapped currencies to their respective countries.

## 📈 Key Insights & Visualizations

### 🌎 Geographical Distribution

  * **Top 3 Countries:** The vast majority of Zomato's listings are in **India** (94.39%), followed by the **United States** (4.73%) and the **United Kingdom** (0.87%).

  * **Top 5 Cities:** The top 5 cities with the most restaurant listings are all within the National Capital Region (NCR) of India:

    1.  New Delhi (68.87%)
    2.  Gurgaon (14.07%)
    3.  Noida (13.59%)
    4.  Faridabad (3.16%)
    5.  Ghaziabad (0.31%)

### ⭐ Rating Analysis

  * **Rating Distribution:** A significant number of restaurants (2,148) have a rating of **0.0 ("Not Rated")**. This suggests many new listings or a low rate of user feedback for certain entries.
  * **Common Ratings:** The most frequent *actual* ratings fall in the "Average" category (Orange color), specifically between 2.5 and 3.4.
  * **Zero Ratings:** The overwhelming majority of "Not Rated" (0.0) entries originate from **India** (2,139 out of 2,148).

### 🚀 Service Analysis

  * **Online Delivery:** The online delivery service is primarily available in **India** and the **UAE**. Other countries in this dataset do not appear to have this feature enabled.
  * **Currency:** The analysis successfully maps various currencies (like Botswana Pula, Brazilian Real, Dollar, Pounds, and Indian Rupees) to their corresponding countries.

## 💻 Tools Used

  * **Python**
  * **Pandas:** For data manipulation and analysis.
  * **NumPy:** For numerical operations.
  * **Matplotlib:** For basic data visualization.
  * **Seaborn:** For advanced statistical visualization.
  * **Jupyter Notebook:** As the development environment.

## 🛠️ How to Run

1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repository-name.git
    ```
2.  Install the required libraries:
    ```bash
    pip install pandas numpy matplotlib seaborn jupyterlab openpyxl
    ```
3.  Launch Jupyter Notebook or Jupyter Lab:
    ```bash
    jupyter lab
    ```
4.  Open the `.ipynb` file and run the cells sequentially.

## 🔮 Future Work

The notebook identifies a next step which can be implemented:

  * Analyze the `Cuisines` column to find and visualize the **Top 10 most popular cuisines** across the dataset.
