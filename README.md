# 📉 Customer Churn Prediction on Retail Company

This project builds a **machine learning model** to predict whether a retail customer will churn (stop purchasing) or stay.  
The aim is to help the business team design **marketing, retention, and sales strategies** to reduce churn and increase revenue.

🔗 [Google Colab Notebook](https://colab.research.google.com/drive/1B0Ot4Et55hLfWVkmY3JoYq9Fz5sdzVJb?usp=sharing)  
📊 [Presentation Slides](https://www.canva.com/design/DAGxb0xbPsc/k0loegvXURimcvUb1Fop_A/edit?utm_content=DAGxb0xbPsc&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)  
📂 [Dataset (Kaggle)](https://www.kaggle.com/datasets/sahilprajapati143/retail-analysis-large-dataset)  
💻 [GitHub Repository](https://github.com/antoniuswisnumurti/Final-Project-Customer-Churn-on-Retail-Company/tree/main)

---

## 📌 Problem Statement
The company has a high volume of transactions, especially in the USA.  
Analysis shows **77% of customers churn**, while only 23% stay.  
The goal is to **predict customer churn** based on transaction history and behavior, so the company can:  
- Identify at-risk customers early  
- Improve retention through targeted campaigns  
- Increase overall revenue  

---

## 📂 Project Structure

---

## ⚙️ Data Understanding
- Source: [Retail Analysis Large Dataset (Kaggle)](https://www.kaggle.com/datasets/sahilprajapati143/retail-analysis-large-dataset)  
- Period: March 2023 – February 2024  
- Size: 302,006 rows × 30 columns  
- After preprocessing: 31,236 rows × 160 columns:contentReference[oaicite:0]{index=0}

---

## 🔄 Data Preprocessing
1. **Filter Data** → USA only  
2. **Alter Data Types** → convert date to datetime  
3. **Remove Duplicates**  
4. **Handle Missing Values** → logical formulas for `Total Purchases`, `Amount`, `Total Amount`  
5. **Drop Useless Features** → e.g., Year, Month, Customer Segment  
6. **RFM Segmentation** → used as features  
7. **Define Churn** → using observation vs. label window (cut-off Nov 30, 2023, +90 days)  
8. **Encoding & Scaling** → OneHotEncoder + scaling  
9. **Handle Class Imbalance** → SMOTE  
10. **Split Dataset** → Train, Validation, Test:contentReference[oaicite:1]{index=1}

---

## 🤖 Modeling
Four models were trained and compared:  
- k-Nearest Neighbors (kNN)  
- Random Forest  
- Logistic Regression  
- XGBoost  

**Best Model → XGBoost**  
- Validation Recall: **0.99**  
- Test Recall: **0.99**  
- Highest recall → ideal for churn prediction (focus on catching churners even if some false positives occur):contentReference[oaicite:2]{index=2}

---

## 📊 Feature Importance (XGBoost + SHAP)
- **Order Status = Delivered** → churners often end with a final delivered order.  
- **Customer Segment = Potential Loyalists** → most likely to churn if not nurtured.  
- **Frequency** → low visit frequency strongly linked to churn.  
- **Shipping Method = Express / Same-day** → dissatisfaction with delivery reliability.  

---

## 🎯 Business Insights & Recommendations
1. **Order Delivered as Last Touchpoint**  
   - Send thank-you notes, discount codes, or repurchase reminders after delivery.  
   - Collect feedback immediately post-purchase.  

2. **Potential Loyalists at Risk**  
   - Exclusive promotions (discounts, bundles, early-bird offers).  
   - Clear loyalty pathway → convert to “Loyal Customers.”  
   - Personalized follow-ups to strengthen relationship.  

3. **Low Frequency Customers**  
   - Early re-engagement campaigns (“We miss you!” vouchers).  
   - Gamify repeat purchases with points, milestones, or streaks.  
   - Monitor declining frequency as an early churn signal.  

4. **Express & Same-day Shipping**  
   - Audit actual vs. promised delivery times.  
   - Be transparent about realistic delivery times.  
   - Post-shipment care → vouchers or apologies if delays occur:contentReference[oaicite:3]{index=3}  

---

## ✅ Summary
- Churn rate: **77%** of customers  
- Best Model: **XGBoost (Recall: 99%)**  
- Key Risk Indicators: *Delivered orders, Potential Loyalist segment, Low frequency, Express shipping*  
- If implemented, recommendations can:  
  - Reduce churn  
  - Trigger repeat purchases  
  - Boost customer loyalty & revenue  

---

## 🛠️ Tools & Technologies
- Python (Pandas, NumPy, Scikit-learn, XGBoost)  
- Google Colab  
- SHAP (model interpretability)  
- Matplotlib & Seaborn  

---

## 👤 Author
**Antonius Wisnumurti Sulistyanto**  
- [LinkedIn](https://www.linkedin.com/in/antonius-wisnumurti-sulistyanto/)  
- 📧 antoniuswisnumurti@gmail.com  

---
