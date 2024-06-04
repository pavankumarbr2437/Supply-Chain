
# Supply Chain Management

# Supply Chain Dashboard Link

https://app.powerbi.com/links/ne1TOBnD7W?ctid=0abc8a22-567e-4918-b31c-0bdf83a88a27&pbi_source=linkShare


## Problem Statement

This dashboard helps the customers  understand their demand and supply .To know their total sales, region wise sales, day wise sales and month wise sales. Therby increasing business sales by achieving KPI's and analyzing trends.



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : Achieved KPI's for Supply Chain dashboard like  Total Sales(MTD,QTD,YTD)
(a) Product Wise Sales
(b) Sales Growth 
(c) Daily Sales Trend
(d) State Wise Sales
(e) Top 5 Store Wise Sales
(f) Region Wise Sales 
 (g) Total Inventory 
 (h) Inventory Value
 (i) Over stock, Out Stock , Under stock

- Step 5 : For calculating these KPI's used DAX formulas.
Last_Year_Sales = CALCULATE(SUM('F-Point of Sales'[Sales Amount]),DATEADD('F-Sales'[Date].[Date],-1,YEAR)
Sales MTD = 
IF(
	ISFILTERED('F-Sales'[Date]),
	ERROR("Time intelligence quick measures can only be grouped or filtered by the Power BI-provided date hierarchy or primary date column."),
	TOTALMTD(SUM('F-Point of Sales'[Sales Amount]), 'F-Sales'[Date].[Date])
)
Sales QTD = 
IF(
	ISFILTERED('F-Sales'[Date]),
	ERROR("Time intelligence quick measures can only be grouped or filtered by the Power BI-provided date hierarchy or primary date column."),
	TOTALQTD(SUM('F-Point of Sales'[Sales Amount]), 'F-Sales'[Date].[Date])
YTD = TOTALYTD(SUM('F-Point of Sales'[Sales]),'F-Sales'[Date])

- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7  : Visual filters (Slicers) were added.
- Step 8  : dashboard was created by Displaying all these KPI's and trends by using different visuals.

 - Step 18 : The report was then published to Power BI Service.
 
 

# Snapshot of Dashboards (Power BI Service)

![Supply Chain -1](https://github.com/pavankumarbr2437/Supply-Chain/assets/145674009/bd9eccd3-e4cd-4f27-99f4-2c8b07ac22cd)

![SC -2](https://github.com/pavankumarbr2437/Supply-Chain/assets/145674009/8c4f48f5-df04-4b5e-8a0a-b0ec134a8386)



 
 
# Insights

: Increased sales by 23.08% over 3 years, starting from 2020
