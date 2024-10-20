# [PowerBI] Purchasing Performance Operational Dashboard
## **I.INTRODUCTION**
### **1. BUSINESS QUESTIONS**
Adventure Works Cycles is a fictitious bicycle manufacturer. Its purchasing department is responsible for procuring goods, raw materials, and semi-finished products essential for bicycle production. The management team expects that ***inventory is ordered adequately*** to meet sales demands, ***delivered on time***, and purchased at ***optimized costs***. 

This Operational Dashboard is designed with Design Thinking approach and Power BI tools to provide Purchasing Manager with a clear overview of department performance while offering actionable recommendations. The goal is to facilitate informed decision-making and enhance overall operational efficiency.

### **2. DATASET**
AdventureWorks database supports standard online transaction processing scenarios for Adventure Works Cycles. Scenarios include Manufacturing, Sales, Purchasing, Product Management, Contact Management, and Human Resources.
- Dataset: The dataset can be found in Google BigQuery under ID: `adventureworks2019`
- Data Dictionary: https://drive.google.com/file/d/1bwwsS3cRJYOg1cvNppc1K_8dQLELN16T/view

## **II.DESIGN THINKING APPROACH**
### Stage 1: Empathize
|5W1H|---|
|---|---|
|Who will be viewing this Dashboard?|	Senior managers (CEO, Purchasing Manager, Finance Manager)|
|If we had to choose only one key Stakeholder, who would it be?| Purchasing Manager|
|What problem does this Dashboard solve?	| 1. Purchasing Department Overall Performance<br>2. Forecast upcoming purchasing demand<br>3. Vendor quality assessment|
|Describe the problem in one sentence |	Help purchasing manager to grasp the Department Overall Performance, and Details of inventory, vendor to develop optimized operational strategy.|
|When and where will Stakeholders view this Dashboard?| 1. When review department performance in weekly BOD meeting.<br>2. Daily performance review with team, in team meeting.<br>3. Use personally when developing plans and allocating tasks for team members.|
|Why do stakeholders need this Dashboard?| 1. To optimize department performance.<br>2. To develop purchasing plan.|
|How have stakeholders been achieving their goals so far?	|Know the performance <br>--> Find aspect that can be optimized <br>--> Develop Action plan to implement the optimization|

|Empathy Map|---|
|---|---|
|**Thinking and feeling**<br>_What does the stakeholder think and feel?_|	I'm facing pressure from the CEO, but I believe that there're some aspects my deparment did great but some aspects can be optimized too.|
|**Seeing**<br>_What does the stakeholder see?_|	Purchasing Department was claimed of its poor performance.|
|**Saying and doing**<br>_What does the stakeholder say and do?_	|"Which aspect in purchasing process should I optimized?".|
|**Pains**<br>_What are the biggest problems and challenges?_|1. How is the department's overall performance?<br>- Is the product cost optimized?<br>- Is the delivery on time?<br>- Is the product quantity sufficiently purchased? <br>- Is the product supplied meet quality standard?<br>2. If any of the above being No, then where the wrong is? How to fix it via choosing vendor and forecasting purchasing demand?|
|**Gains**<br>_What are the opportunities and benefits?_|	By spotting the unoptimized parts, Purchasing manager can enhance the overall performance of the department.|

### Stage 2: Define Point of View
|Northstar Metric|---|
|---|---|
|What VALUE you want to measure?|Expenditure to have products as inventory (buying, transporting).|
|WHEN the value DELIVERY SUCCESS?|When the product is considered inventory.|
|Northstar Metric Name|Spend|
|WHY do you choose this metric?|Purchasing department activities should be based on spend optimization. The more optimized the spending, the more efficiently capital is used.|

Dimension Data Group
|**Group 1** - Overview|**Group 2** - Inventory Management|**Group 3** - Vendor Management|
|---|:---:|:---:|
|_Product: Price, Quality, Quantity<br>Logistics: Freight, Delivery Time, Shipment Modes_|	_Available stock<br>Unsafe stock<br>Lead time<br>Due date_|_Number of vendors<br>Vendor ratings<br>Vendor diversity<br>Lead time_|

Define Point of View
|View	|Description	|	Why	|
|---|:---:|---|
|**View1**| Overview|	Overall Performance of Purchasing Department.	|			
|**View2**| Inventory Management|	Current Inventory Status and Demand of Products to buy.	|		
|**View3**| Vendor Management|	Assess the vendor quality to optimize the product price, lead time.|

Growth Formula
|Northstar Metric:|Spend|
|---|---|
|View 1 breakdown	| Total spend overall<br>Spend by product, vendor<br>Freight by product|
|View 2 breakdown	| Spend by inventory<br>Spend by inventory need to buy	|
|View 3 breakdown	| Spend by vendor |

### Stage 3: Ideate
Brainstorming
|Idea Name|Layer 0 dimension| Layer 1 dimension|Layer 2 dimension|
|---|---|---|---|
|View 1: Overview|- Total spend<br>- Total PO<br>- %PO Delivered on-time<br>- %PO revised<br>- AVG revision time<br>- %PO with price optimized<br>- Total optimized value<br>- Total freight<br>- Total product cost|- Spend by Cost type (product, freight, tax)<br>- Spend by Product Category<br>- Reject rate by Product<br>- Reject qty by Product <br>- Freight by Shipment mode|- Vendor by Reject rate by Product|
|View 2: Inventory Management|- Total unsafe product items<br>- Total safe product items|- Current stock quantity by product <br>- Quantity need to order by product<br>- MOQ by product<br>- Standard price by product<br>- Lead time by product|  |
|View 3: Vendor Management	|- Total number of vendors <br>- Number of active/inactive vendors<br>- Total purchase products|- Spend by vendor<br>- Vendor classification (Price vs Reject rate)<br>- Vendor Count by product<br>- Product, Vendor Name by Vendor Count<br>- Credit rating, preference, active status, lead time, on-time delivery rate, availability rate, reject rate by vendor<br>- Product name, price by vendor|  |

Structure idea
|   |	Metric 1 | Metric 2	| Metric 3	| Metric 4 |Metric 5 |
|---|---|---|---|---|---|
|Scorecard	|Spend	|Number of PO	|PO Accuracy	|On-time delivery Rate	|Optimized Value|

|Idea Name	| Highly important info|	Important info | Detailed info |
|---|---|---|---|
|View 1|- Total spend<br>- Total PO<br>- %PO Delivered on-time<br>- %PO revised<br>- AVG revision time<br>- %PO with price optimized<br>- Total optimized value|- Spend by Cost type (product, freight, tax)<br>- Spend by Product Category<br>- Freight by Shipment mode<br>- Total Freight<br>- Total product cost|- Reject rate by Product<br>- Reject qty by Product<br>- Vendor by Reject rate by Product|
|View 2|- Total unsafe product items<br>- Total safe product items|   |- Current stock quantity by product<br>- quantity need to order by product<br>- MOQ by product<br>- Standard price by product<br>- Lead time by product|
|View 3	|- Total number of vendors<br>- Number of active/inactive vendors|- Spend by vendor<br>- Vendor classification (Price vs Reject rate)<br>- Total purchase products<br>- Vendor count by product|- Product, Vendor Name by Vendor Count<br>- Credit rating, preference, active status, lead time, on-time delivery rate, availability rate, reject rate by vendor<br>- Product name, price by vendor|	

### Stage 4: Prototype & Review
This is implementation and review stage. Prototype and Review dashboard multiple times to achieve the final dashboard.

## **III. DASHBOARD**
### **Data Modeling**
<img width="998" alt="DataModeling" src="https://github.com/user-attachments/assets/72ff4a9f-d7f5-4b80-b343-16512f77b825">

### **View 1: Overview**
<img width="998" alt="Overview" src="https://github.com/user-attachments/assets/120a86ce-f5b1-420f-8191-66654719cb50">

### **View 2: Inventory Management**
<img width="998" alt="Inventory" src="https://github.com/user-attachments/assets/863c3a55-5bae-4597-a0f5-901e5c97036b">

### **View 3: Vendor Management**
<img width="998" alt="Vendor" src="https://github.com/user-attachments/assets/b5a0484b-1acb-4ed9-a284-e2d0a421bc46">

## **IV. INSIGHTS & RECOMMENDATIONS**
### 1. Improve PO Accuracy
- Issue: All POs require at least 4 adjustments during the ordering process.
- Recommendation: Implement a review and validation process before finalizing POs to reduce the number of adjustments. Consider additional training or a revised checklist to enhance accuracy and minimize errors during the ordering phase.

### 2. Optimize Pricing
- Issue: Only ~7% of orders have optimized pricing, with the total optimized value being less than 1% of the total purchase value.
- Recommendations:
  - Bulk Purchasing: Explore opportunities for bulk purchases to secure better pricing <br>--> Check detailed proposal in Recommendation #4
  - Strategic Vendor Agreements: Negotiate long-term contracts with key vendors for preferential pricing  <br>--> Check detailed proposal in Recommendation #5
  - Price Comparison: Regularly compare prices from multiple vendors to ensure the most competitive pricing <br>--> Check detailed proposal in Recommendation #5
 
### 3. Address Defective Products
- Issue: Products with reject quantities >1000 or reject rates >5% are problematic and need to be handled.
- Recommendations:
  - Immediate solution: Negotiate with vendors to set acceptable limits for reject rates and quantities. Develop vendor principle agreements to manage and improve quality standards.
  - Long-term solution: Seek additional vendors for products with high defect rates to ensure reliable supply and better quality control.
 
### 4. Optimize Stock Products
- Recommendations:
  - Prioritizing to order items with long lead times and high demand to ensure adequate stock levels.
  - For items with low maximum order quantities, negotiate with vendors to increase MOQ limits, reducing the need for multiple POs.
  - For products with high maximum order quantities, consider purchasing at maximum levels to benefit from volume pricing.
 
### 5. Vendor Management
- Recommendations:
  - Sign principle (strategic) agreements with high-spend vendors to negotiate lower purchase prices.
  - Diversify Vendors: Address the issue of 113 products being sourced from one single vendor by finding additional vendors for these products. This will enable price comparisons and selection of the most cost-effective options.
