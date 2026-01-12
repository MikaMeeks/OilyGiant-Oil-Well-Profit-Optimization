# **OilyGiant Oil Well Profit Optimization (Sprint 9 — Machine Learning in Business)**

A machine learning and business analytics project focused on selecting the most profitable region for drilling new oil wells. Using geological data from three regions, this project builds predictive models, estimates potential profit, and evaluates financial risk using bootstrapping.

---

## **📂 Project Overview**
OilyGiant plans to develop a new oil well field and must choose the region with the highest expected profit and lowest financial risk. This project uses machine learning to predict oil reserves, selects the most promising wells, and applies statistical bootstrapping to estimate profit distribution and risk of losses.

This project includes:
- Data preparation and exploration  
- Linear regression modeling for each region  
- RMSE evaluation  
- Profit calculation based on business constraints  
- Bootstrapping with 1000 samples  
- Risk assessment and region selection  

---

## **🧰 Tools & Technologies**
- **Python**  
- **pandas, NumPy**  
- **scikit‑learn (LinearRegression, train_test_split, metrics)**  
- **matplotlib, seaborn**  
- **Bootstrapping (NumPy sampling)**  
- **Jupyter Notebook**

---

## **📊 Key Steps**

### **1. Data Preparation**
- Loaded geological data from three regions  
- Inspected features (`f0`, `f1`, `f2`) and target (`product`)  
- Split each region’s dataset into **75% training** and **25% validation**  
- Ensured consistent preprocessing across all regions  

---

### **2. Model Training & Evaluation**
For each region:
- Trained a **Linear Regression** model  
- Generated predictions for the validation set  
- Calculated **RMSE**  
- Compared predicted vs. actual reserve volumes  
- Analyzed model stability and suitability  

---

### **3. Profit Calculation Setup**
Business constraints:
- 500 wells explored per region  
- Only the **top 200 predicted wells** are developed  
- Development budget: **$100 million**  
- Revenue: **$4,500 per thousand barrels**  
- Profit = revenue − development cost  

Steps:
- Calculated break‑even reserve volume  
- Compared break‑even threshold to regional averages  
- Stored key constants for profit simulation  

---

### **4. Profit Function**
Created a function to:
- Select the **top 200 predicted wells**  
- Sum their actual reserve volumes  
- Compute total profit  
- Identify the most profitable region before risk analysis  

---

### **5. Bootstrapping (1000 Samples)**
For each region:
- Simulated profit distribution using random sampling  
- Calculated:  
  - **Average profit**  
  - **95% confidence interval**  
  - **Risk of losses (probability of negative profit)**  
- Compared results to business requirements:  
  - Risk must be **< 2.5%**  

---

## **🔍 Insights & Findings**
- Linear regression performance varied significantly across regions  
- Some regions had high average reserves but unstable predictions  
- Bootstrapping revealed which region had acceptable financial risk  
- Only regions with **risk < 2.5%** were considered  
- Final selection was based on **highest average profit** among low‑risk regions  

*(You can update this section with your actual results.)*

---

## **📈 Business Impact**
This analysis helps OilyGiant:
- Minimize financial risk  
- Allocate drilling budget efficiently  
- Prioritize regions with stable, predictable reserves  
- Maximize long‑term profitability  

---

## **📁 Repository Structure**
```
oilygiant-profit-optimization/
│── README.md
│── oilygiant_profit.ipynb
│── data/ (excluded or sample only)
│── images/ (optional for charts)
```

---

## **🚀 How to Run**
1. Clone the repository  
2. Install required libraries  
3. Open the Jupyter notebook  
4. Run all cells to reproduce the analysis and results  

---

## **📬 Contact**
**Email:** iking.mika@gmail.com  
**LinkedIn:** `www.linkedin.com/in/mika-willis`
