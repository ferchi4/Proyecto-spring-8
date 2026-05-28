# **Urban Mobility Analysis: Taxis in Chicago and the Impact of Weather**

This project explores taxi service patterns in Chicago using trip data from O'Hare International Airport. The main objective is to identify leading companies, neighborhoods with the highest demand, and, through a hypothesis test, determine whether weather conditions significantly affect trip duration on a key route.

**Objective**

The project focuses on testing the following hypothesis:

*   **Null Hypothesis (H0):** The average trip duration from the Loop neighborhood to O'Hare Airport does **not** vary between rainy Saturdays and Saturdays with good weather.
*   **Alternative Hypothesis (H1):** The average trip duration from the Loop to O'Hare Airport **does** vary between rainy Saturdays and Saturdays with good weather (specifically, it is expected to be longer on rainy days).

**🛠️ Technologies Used**

*   **Python:** Main language for analysis.
*   **Pandas:** For data manipulation and cleaning.
*   **Matplotlib and Seaborn:** For data visualization and chart creation.
*   **SciPy:** For conducting the statistical hypothesis test (Welch's t-test).
*   **Jupyter Notebook:** Interactive environment for development of the analysis.

**Key Steps**

1.  **Exploratory Data Analysis (EDA):**
    *   Dataset quality was evaluated by checking data types, null values, and duplicates.
    *   Basic cleaning was performed to ensure data integrity.

2.  **Visualization of Demand Patterns:**
    *   The 10 neighborhoods with the highest average completed trips were identified and graphed, highlighting high-activity zones like the Loop and River North.
    *   The 20 taxi companies with the highest number of trips were visualized, revealing high market concentration in a few companies, led by *Flash Cab*.

3.  **Hypothesis Testing:**
    *   Weather data was prepared by filtering trips taken on Saturdays and classifying them by weather condition ("Bad" for rain, "Good" for good weather).
    *   A Welch's t-test was applied to compare the means of two independent groups (rainy Saturdays vs. normal Saturdays) without assuming equal variances.
    *   The distribution of trip duration for both groups was visualized using density plots (KDE).

**Results**

The analysis confirms that:

*   **Market Concentration:** Companies like *Flash Cab* and *Taxi Affiliation Services* dominate the number of trips, and most trips end in central neighborhoods like the Loop and River North.
*   **Impact of Weather on Trip Duration:** The hypothesis test rejects the null hypothesis. A statistically significant difference in trip duration was found.
    *   The average duration on rainy Saturdays was **40.2 minutes**, while on normal Saturdays it was **33.9 minutes**.
*   **Statistical Conclusion:** With an extremely low p-value (p < 0.05), it is concluded that bad weather (rain) significantly increases travel time on the analyzed route, likely due to increased traffic congestion or slower driving conditions.

**How to Run the Project**

1.  Clone this repository to your local machine.
    ```bash
    git clone (https://github.com/ferchi4/Proyecto-spring-8)
    ```

2.  Ensure you have the necessary dependencies installed:
    ```bash
    pip install pandas numpy matplotlib seaborn scipy jupyter
    ```

3.  Place the CSV files (`moved_project_sql_result_01.csv`, `moved_project_sql_result_04.csv`, `moved_project_sql_result_07.csv`) in the same directory as the notebook.

4.  Open and run the `proyecto8.ipynb` file in Jupyter Notebook.
    ```bash
    jupyter notebook proyecto8.ipynb
    ```
