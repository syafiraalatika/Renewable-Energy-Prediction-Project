# Global Renewable Energy: An Integrated Analysis and Forecast

## Project Background

This project was undertaken from the perspective of a data professional at **NextEra Energy**, one of the world's leading renewable energy providers. In an industry driven by high capital investment and complex global factors, the key challenge is to identify not just where to invest, but *how* to invest for maximum impact.

The goal of this project is to move beyond simple production metrics and develop a deeper, strategic understanding of the global renewable energy landscape. It aims to answer critical business questions and build a predictive tool to guide future investment decisions.

Insights and recommendations are provided on the following key areas:

- **Investment Efficiency Analysis:** Identifying which countries are the most effective at converting investment dollars into renewable energy.
- **Key Driver Identification:** Quantifying the impact of economic, policy, and innovation factors on energy production.
- **Predictive Modeling:** Forecasting future energy production to aid in strategic planning and risk assessment.

The complete analysis and model development can be found in the `DS-notebook.ipynb` file in this repository.

---

## Data Structure & Initial Checks

The analysis is based on a single, comprehensive dataset (`Training_set_augmented.csv`). The dataset contains **2400 records**, each representing a specific energy type in a given country and year.

The data consists of 31 columns, which can be grouped into several key categories:
- **Identifiers:** `Country`, `Year`, `Energy Type`
- **Energy Metrics:** `Production (GWh)`, `Installed Capacity (MW)`, `Energy Consumption`
- **Economic Factors:** `Investments (USD)`, `GDP`, `R&D Expenditure`
- **Policy & Governance:** `Regulatory Quality`, `Public-Private Partnerships`, `Government Policies`
- **Environmental Factors:** `CO2 Emissions`, `Solar Irradiance`, `Wind Speed`

*Note: As this project utilizes a single flat file, a formal Entity Relationship Diagram (ERD) is not applicable.*

---

## Executive Summary

### Overview of Findings

The central finding of this analysis is that success in renewable energy is not driven by raw investment alone, but by a **supportive ecosystem**. The analysis concludes that success in the renewable sector is a function of a synergistic ecosystem where capital investment is amplified by effective policy and a strong innovation pipeline.

The analysis first identified four distinct archetypes of nations based on their investment efficiency. Subsequently, a state-of-the-art stacked ensemble model was built to predict energy production. The model's results quantitatively confirmed this "ecosystem theory" by ranking not just investment, but also regulatory quality and innovation, as top drivers of success.

---

## Insights & Findings

### Category 1: Investment Efficiency Analysis

By plotting total investment against an efficiency metric (GWh produced per million USD), the "Efficiency Frontier Matrix" was created. This visualization immediately revealed four strategic country profiles:



- **Leaders (e.g., USA, China):** High Investment, High Efficiency. These nations successfully scale their renewable energy sector.
- **Rising Stars (e.g., UK, Brazil):** Low Investment, High Efficiency. These countries are models of strategic effectiveness, achieving excellent results with less capital.
- **Inefficient Spenders (e.g., Australia):** High Investment, Low Efficiency. These nations face bottlenecks that prevent capital from translating into energy production.
- **Developing:** Low Investment, Low Efficiency. These countries are in the early stages of their renewable journey.

### Category 2: Key Driver Identification & Predictive Modeling

To quantify the factors driving these results, a stacked ensemble model was built. The model's feature importance plot revealed the "secret sauce" of successful renewable energy ecosystems:



- **Infrastructure is Foundational:** `Installed Capacity` is the single most important predictor.
- **Policy and Innovation are Multipliers:** The engineered feature, **`Innovation_x_RD`**, ranked in the top 10, proving R&D is most effective in an innovative environment. The high importance of **`Regulatory Quality`** confirms that stable governance is essential for turning investment into energy.

---

## Recommendations:

Based on these findings, the following recommendations are proposed for NextEra Energy's strategic team:

* **Look Beyond Raw Investment:** Prioritize **"Rising Star"** nations that have a proven track record of high efficiency. For **"Inefficient Spenders,"** investment should be contingent on identifying and addressing their policy or infrastructure bottlenecks.

* **Invest in Ecosystems, Not Just Projects:** Prioritize investments in countries that demonstrate both high **`Regulatory Quality`** and a strong **`Innovation Index`**, as the model proves these factors act as investment multipliers.

* **Use the Model for Strategic Forecasting:** The predictive model developed in this project should be used as a strategic tool to forecast the potential production impact of policy changes or new R&D initiatives in a target country, thereby de-risking future investments.

---

## Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made. These assumptions and caveats are noted below:

* **Data Integrity:** The analysis assumes the provided dataset is a fair and accurate representation of global renewable energy trends.
* **Metric Consistency:** The analysis relies on the assumption that metrics like `Regulatory Quality` and `Innovation Index` are consistently and accurately measured across all countries.
* **Model Limitations:** The predictive model is based on historical data. Its forecasts may not account for unforeseen future events, such as major geopolitical shifts or disruptive technological breakthroughs.
