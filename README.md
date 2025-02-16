# [PowerBI] Purchasing Performance Operational Dashboard
## **I.INTRODUCTION**
### **1. BUSINESS QUESTIONS**
Adventure Works Cycles is a fictitious bicycle manufacturer. Its purchasing department is responsible for procuring goods, raw materials, and semi-finished products essential for bicycle production. The management team expects that ***inventory is ordered adequately*** to meet sales demands, ***delivered on time***, and purchased at ***optimized costs***. 

This **_Operational Dashboard_** is designed with **_Design Thinking_** approach and **_Power BI_** tools to provide Purchasing Manager with a clear **_overview of department performance_** while offering actionable recommendations. The goal is to facilitate informed decision-making and **_enhance overall operational efficiency_**.

### **2. DATASET**
AdventureWorks database supports standard online transaction processing scenarios for Adventure Works Cycles. Scenarios include Manufacturing, Sales, Purchasing, Product Management, Contact Management, and Human Resources.
- Dataset: The dataset can be found in Google BigQuery under ID: `adventureworks2019`
- Data Dictionary: https://drive.google.com/file/d/1bwwsS3cRJYOg1cvNppc1K_8dQLELN16T/view

## **II.DESIGN THINKING APPROACH**
### Stage 1: Empathize

<img width="1000" alt="Vendor" src="https://github.com/user-attachments/assets/22a3078c-00d6-468c-a4e5-2c9e93b6eba4">

<img width="650" alt="Vendor" src="https://github.com/user-attachments/assets/c1eb7273-e0d7-43ca-81c9-9a76ad8b6352">

### Stage 2: Define Point of View

<img width="480" alt="Vendor" src="https://github.com/user-attachments/assets/182f85bf-d8ac-4187-88d2-7c74d4b518ea"> \

<img width="500" alt="Vendor" src="https://github.com/user-attachments/assets/e8dc8304-61aa-4f10-8d47-2139c33604a7"> \

<img width="400" alt="Vendor" src="https://github.com/user-attachments/assets/61cd34a2-fe9a-4ba6-8cd1-69e1d5e5ce86">


### Stage 3: Ideate
Brainstorming

<img width="650" alt="Vendor" src="https://github.com/user-attachments/assets/3ec97a3a-b387-4fa9-82e3-ee9f2bdcbc72">

Structure idea

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/24eac247-91d4-4c82-a28b-58e53ff9cc63" />


### Stage 4: Prototype & Review
This is implementation and review stage. Prototype and Review dashboard multiple times to achieve the final dashboard.

## **III. DASHBOARD**
### **Data Modeling**
<img width="998" alt="DataModeling" src="https://github.com/user-attachments/assets/72ff4a9f-d7f5-4b80-b343-16512f77b825">

### **View 1: Overview**
<img width="998" alt="Overview" src="https://github.com/user-attachments/assets/120a86ce-f5b1-420f-8191-66654719cb50">

➡️Insights:
- **_Low PO Accuracy_**: **_All POs_** require at **_least 4 adjustments_** during the ordering process.
- **_Price not optimized_**: Only **_~7%_** of orders have **_optimized pricing_**, with the **_total optimized value_** being **_<1%_** of the total purchase value.
- **_Defective Products_**: There’re products with **_reject quantities >1000_** (e.g. LL Crankarm) or **_reject rates >5%_** (e.g. Metal Sheet 1), which are problematic and need to be handled.

### **View 2: Inventory Management**
<img width="998" alt="Inventory" src="https://github.com/user-attachments/assets/863c3a55-5bae-4597-a0f5-901e5c97036b">

➡️Insights:
- Help to get the **_overall situation of inventory_**: **_69_** items **_needed to purchase_**. Some items have very **_low maximum order qty_**, some very **_high_**, which can be optimized.

### **View 3: Vendor Management**
<img width="998" alt="Vendor" src="https://github.com/user-attachments/assets/b5a0484b-1acb-4ed9-a284-e2d0a421bc46">

➡️Insights:
- The company **_bought most_** of its products and parts from **_Superior Bicycles_** with **_spending_** being **_4.5 million $_**
- **_113_** products being sourced from **_one single vendor_**

## **IV. INSIGHTS & RECOMMENDATIONS**
### 1. Improve PO Accuracy
- _Issue_: All POs require at least 4 adjustments during the ordering process.
- _Recommendation_: Implement a **_review and validation process_** before finalizing POs to reduce the number of adjustments. Consider **_additional training_** or a **_revised checklist_** to enhance accuracy and **_minimize errors_** during the ordering phase.

### 2. Optimize Pricing
- _Issue_: Only ~7% of orders have optimized pricing, with the total optimized value being less than 1% of the total purchase value.
- _Recommendations_:
  - **_Bulk Purchasing_**: Explore opportunities for bulk purchases to secure better pricing <br>--> Check detailed proposal in Recommendation #4
  - **_Strategic Vendor Agreements_**: Negotiate long-term contracts with key vendors for preferential pricing  <br>--> Check detailed proposal in Recommendation #5
  - **_Price Comparison_**: Regularly compare prices from multiple vendors to ensure the most competitive pricing <br>--> Check detailed proposal in Recommendation #5
 
### 3. Address Defective Products
- _Issue_: Products with reject quantities >1000 or reject rates >5% are problematic and need to be handled.
- _Recommendations_:
  - **_Immediate solution_**: Negotiate with vendors to set **_acceptable limits_** for **_reject rates and quantities_**. Develop **_vendor principle agreements_** to manage and improve **_quality standards_**.
  - **_Long-term solution_**: For products with high defect rates, find **_more vendors_** to ensure **_reliable supply_** and better quality control.
 
### 4. Optimize Stock Products
- _Recommendations_:
  - **_Prioritizing_** to order items with **_long lead times_** and **_high demand_** first, to ensure adequate stock levels.
  - For items with **_low maximum order quantities_**, negotiate with vendors to **_increase MOQ limits_**, reducing the need for multiple POs.
  - For products with **_high maximum order quantities_**, consider **_purchasing at maximum_** levels to benefit from **_volume pricing_**.
 
### 5. Vendor Management
- _Recommendations_:
  - Sign principle **_(strategic) agreements_** with **_high-spend vendors_** to **_negotiate lower prices_**.
  - **_Diversify Vendors_**: Address the issue of 113 products being sourced from one single vendor by finding additional vendors for these products. This will enable price comparisons and selection of the most cost-effective options.
