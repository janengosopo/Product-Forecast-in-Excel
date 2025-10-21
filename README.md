# **Product Forecasting in Excel**

## **1. Project Overview**

This project presents a **Product Forecasting model built in Microsoft Excel** to estimate monthly demand for a *10-Piece Set*.
It includes three forecasting methods: **Linear Regression**, **Multiple Regression**, and **Seasonality Modeling**.
Each method is evaluated to identify which best captures sales patterns and seasonal demand fluctuations.

It also demonstrates how forecasting in Excel can support **data-driven demand planning** and **sales forecasting** in consumer goods or retail environments.

---

## **2. Key Business Questions**

The project answers:

* What is the expected monthly sales demand for the 10-Piece Set?
* How do time, price, and external market factors influence sales?
* How does seasonality affect monthly sales performance?
* Which forecasting approach provides the most accurate and reliable results?

---

## **3. Forecasting Methods in Excel**

### **Data Preparation**

* **Dataset:** Monthly sales data for the 10-Piece Set in 2024 and 2025.
* **Key Variables:**

  * Time in month
  * Sale price
  * Total Home Sales
* Data was cleaned, formatted, and used consistently across all forecasting models to ensure comparability.

---

### **Method 1: Linear Regression**

**Objective:** Forecast sales using only time as a predictor.

* **Model:** `Sales = a + b(Time)`
* **Result:** R² = **0.44**
* **Interpretation:** Time explains ~44% of variation in sales. The model identifies a general upward trend but lacks accuracy for months with strong seasonal patterns.

---

### **Method 2: Multiple Regression**

**Objective:** Incorporate additional predictors (price and market conditions).

* **Model:** `Sales = a + b₁(Time) + b₂(Price) + b₃(Total Home Sales)`
* **Result:** R² = **0.85**
* **Interpretation:** There is a substantial improvement. The model shows relationships between price, home sales, and product demand, providing more accurate forecasts.

---

### **Method 3: Seasonality Modeling**

**Objective:** Capture recurring monthly fluctuations using **binary variables** for some specific months.

* **Model:** `Sales = a + b₁(Time) + b₂(Feb) + b₃(Mar) + b₄(Apr) + ...`
* **Approach:** Introduced binary variables (1/0) for selected months to model seasonal peaks and dips in sales.
* **Result:** R² = **0.95**
* **Interpretation:** This is the strongest model. It effectively explains nearly all sales variance and reveals strong seasonal demand patterns (e.g., peaks in spring and steady declines in mid-year).

---

## **4. Insights**

### **Model Performance Comparison**

| Model                   |     Variables Included    | R² (Goodness of Fit) | Interpretation                                      |
| :---------------------- | :-----------------------: | :------------------: | :-------------------------------------------------- |
| **Linear Regression**   |            Time           |         0.44         | Captures only trend, limited accuracy               |
| **Multiple Regression** | Time, Price, Home Sales |         0.85         | Strong improvement, captures external influences    |
| **Seasonality Model**   |   Time, Binary Months |       **0.95**       | Best performer, accurately models cyclical patterns |

---

### **Key Findings**

* The **Seasonality Model** has the highest R² (**0.95**). It shows that **monthly patterns and seasonal effects** play a major role in product demand.
* **Multiple Regression** also has a high R² (**0.85**). It proves that **price sensitivity** and **market trends** significantly influence sales.
* **Linear Regression** works as a solid baseline for detecting long-term trends.
* The inclusion of **binary month indicators** in the seasonality model improves accuracy by capturing recurring seasonal peaks.

---


## **5. Project Structure**

```
README.md                       : Main project documentation  
Product Forecast in Excel.xlsx   : Excel workbook with models and outputs  
```

---

## **6. How to Use**

1. Click the Excel file **Product Forecast in Excel.xlsx**.
2. Choose **View raw**. The file will be automatically downloaded to your computer.
3. Review each sheet:

   * **Overview:** Source data
   * **Linear Reg:** Simple time-based model
   * **Multi Reg:** Multiple regression with price and market variable (Home Sales)
   * **Seasonality modeling:** Seasonal regression with binary month variables
