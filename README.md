# Car Sales Dashboard

### Dashboard Link :  
https://app.powerbi.com/view?r=eyJrIjoiZDY5ODExMDAtNDczOC00MmUwLWI3NzQtNDdmMGFhM2JlZTIyIiwidCI6IjYyOTA2MWUyLTg4MGMtNDI4Zi1iMTIxLWY5NjYxMDVlMmFhMyJ9
## Problem Statement

This dashboard helps to effectively track and analyse sales performance of cars across various locations in the UK.The objective of this project is to design and develop a dynamic and interactive Car Sales Dashboard using Power BI. The dashboard will visualize critical KPIs related to car sales, helping us understand sales performance over time and make data-driven decisions.

There is a noticeable upward trend in sales, with more frequent peaks in the latter part of the timeline. Data shows that 'SUV' and 'Hatchback' are the most popular body styles in terms of sales.

Major cities like London, Birmingham, and Manchester consistently outperform smaller cities in terms of car sales. There are notable price disparities based on color, with black cars commanding higher average prices than red or pale white models.

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a excel file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
- Step 4 : It was observed that in none of the columns errors & empty values were present except column named "Engine".
- Step 5 : For calculating time intelligence metrics, calendar table has been created based on the maximum and minimum dates in the excel. 
- Step 6 : In the report view, under the view tab, theme was selected.
- Step 7 : Since the data contains various key attributes, multiple visuals have been added to the in report.

  (a) Area chart representing sales weekly trend

  (b) Map visual showing sales across various regions in UK
  
  (c) Donut chart showing distribution of sales by body style
  
  (d) Donut chart showing distribution of sales by color

  (e) Grid view showing company wise sales  

- Step 8 : Visual filters (Slicers) were added for  fields named "Body style", Dealer_Name, Transmission and Engine.
- Step 9 : Card visuals were added to the canvas, one representing Total sales, Avg sales and Total cars sold.         
- Step 10 : A bar chart was also added monthly view representing cars sold monthly trend. While creating this visual, field named "Gender" was also added to the Legends bucket, thus number of cars sold were also seggregated according the gender. 
  
- Step 12 : In the report view, under the insert tab, 4 text boxes were added to the canvas, in one of them name of the dashboard was mentioned & in the other 'Sales Insights', 'Menu' and 'Filters' texts were inserted .
- Step 13 : In the report view, under the insert tab, using buttons option a page navigator was added to the report in order to select following views.

  (1) Yearly Overview

  (2) Monthly Overview
  
  (3) Details

     <img width="134" alt="Screenshot 2024-10-08 102618" src="https://github.com/user-attachments/assets/69f362e0-979a-4add-9070-8d193c3b1238">


- Step 14 : Following KPI's added to Yearly Overview tab

   ### Sales Overview:

   • Year-to-Date (YTD) Total Sales

   • Year-over-Year (YOY) Growth in Total Sales

   • Difference between YTD Sales and Previous Year-to-Date (PTYD) Sales

   ### Average Price Analysis:
   • YTD Average Price

   • YOY Growth in Average Price

   • Difference between YTD Average Price and PTYD Average Price

  ### Cars Sold Metrics:

   • YTD Cars Sold

   • YOY Growth in Cars Sold

   • Difference between YTD Cars Sold and PTYD Cars Sold
  ### Charts Details
   1. YTD Sales Weekly Trend: Display a line  chart illustrating the weekly trend of YTD sales. The X-axis should represent weeks, and the Y-axis should show the total sales amount.
   2. YTD Total Sales by Body Style: Visualize the distribution of YTD total sales across different car body styles using a Pie chart.
   3. YTD Total Sales by Color: Present the contribution of various car colors to the YTD total sales through a pie chart.
   4. YTD Cars Sold by Dealer Region: Showcase the YTD sales data based on different dealer regions using a map chart to visualize the sales distribution geographically.
   5. Company-Wise Sales Trend in Grid Form: Provide a tabular grid that displays the sales trend for each company. The grid should showcase the company name along with their YTD sales figures.

- Step 15 : Following KPI's added to monthly Overview tab

   ## Sales Overview:

   • Year-to-Date (YTD) Total Sales

   • Month-to-Date (MTD) Total Sales

   • Year-over-Year (YOY) Growth in Total Sales

   • Difference between YTD Sales and Previous Year-to-Date (PTYD) Sales

   ## Average Price Analysis:
   • YTD Average Price

   • MTD Average Price

   • YOY Growth in Average Price

   • Difference between YTD Average Price and PTYD Average Price

  ## Cars Sold Metrics:

   • YTD Cars Sold

   • MTD Cars Sold

   • YOY Growth in Cars Sold

   • Difference between YTD Cars Sold and PTYD Cars Sold
  ## Charts Details
   1. MTD Sales Weekly Trend: Display a line  chart illustrating the weekly trend of MTD sales. The X-axis should represent weeks, and the Y-axis should show the total sales amount.
   2. MTD Total Sales by Body Style: Visualize the distribution of MTD total sales across different car body styles using a Pie chart.
   3. MTD Total Sales by Color: Present the contribution of various car colors to the MTD total sales through a pie chart.
   4. MTD Cars Sold by month and gender: Showcase the MTD Car sold based on different months and gender using a bar chart. 
   5. Company-Wise Sales Trend in Grid Form: Provide a tabular grid that displays the sales trend for each company. The grid should showcase the company name along with their MTD sales figures.

- Step 16 : Following KPI's added to Details Overview tab

   ## Sales Overview:

   • Year-to-Date (YTD) Total Sales

   • Month-to-Date (MTD) Total Sales

   • Year-over-Year (YOY) Growth in Total Sales

   • Difference between YTD Sales and Previous Year-to-Date (PTYD) Sales

   ## Average Price Analysis:
  
   • YTD Average Price

   • MTD Average Price

   • YOY Growth in Average Price

   • Difference between YTD Average Price and PTYD Average Price

  ## Cars Sold Metrics:

   • YTD Cars Sold

   • MTD Cars Sold

   • YOY Growth in Cars Sold

   • Difference between YTD Cars Sold and PTYD Cars Sold
   ## Detailed Grid
  
   It shows all Car Sales Information including car model, body style, colour,  sales amount, dealer region, date, etc. 
       
 - Step 17 : New measures was created to represent YTD Total Sales.
 
   Following DAX expression was written to find YTD Total Sales,
 
        YTD Total Sales = TOTALYTD(SUM(Car_Sales_Data[Price (£)]),Calender_Table[Date])
 
   A card visual was used to represent this YTD Total Sales
 
   Snap of YTD Total Sales
 
     <img width="121" alt="Screenshot 2024-10-04 212123" src="https://github.com/user-attachments/assets/a38b4c7a-0b67-4424-b4af-8938cc9ec51b">

 
 - Step 18 : New measure was created to calculate Sale Difference .
 
   Following DAX expression was written to find Sale Difference ,
 
       Sale Difference = Car_Sales_Data[YTD Total Sales]-Car_Sales_Data[PTYD Total Sales] where
       YTD Total Sales = TOTALYTD(SUM(Car_Sales_Data[Price (£)]),Calender_Table[Date])
       PTYD Total Sales = CALCULATE(SUM(Car_Sales_Data[Price (£)]),SAMEPERIODLASTYEAR(Calender_Table[Date]))

    
   A card visual was used to represent this Sale Difference.
 
 
    <img width="95" alt="Screenshot2" src="https://github.com/user-attachments/assets/02e9a60c-5c94-42ed-9569-d7abcf57698c">

- Step 19 : New measure was created to calculate YOY Sales Growth%  .
 
  Following DAX expression was written to find YOY Sales Growth% ,
 
      YOY Sales Growth% = Car_Sales_Data[Sale Difference]/Car_Sales_Data[PTYD Total Sales]

    
   A card visual was used to represent this Sale Difference.
 
 
   <img width="92" alt="Screenshot3" src="https://github.com/user-attachments/assets/b8a1d769-cab2-42ce-9b01-aed1ed60cba1">

- Step 20 : New measure was created to calculate YTD Avg Price  .
 
  Following DAX expression was written to find YTD Avg Price,
 
      YTD Avg Price = TOTALYTD([Avg Price],Calender_Table[Date])  where
      Avg Price = SUM(Car_Sales_Data[Price (£)])/COUNT(Car_Sales_Data[Car_id])

    
   A card visual was used to represent this YTD Avg Price.
 
   <img width="107" alt="Screenshot 4" src="https://github.com/user-attachments/assets/31baf11e-e414-4582-88d9-017fc1c0834c">

- Step 21 : New measure was created to calculate Avg Price Diff  .
 
  Following DAX expression was written to find Avg Price Diff,
 
      Avg Price Diff = [YTD Avg Price]-[PYTD Avg Price] where
      YTD Avg Price = TOTALYTD([Avg Price],Calender_Table[Date])
      PYTD Avg Price = CALCULATE([Avg Price],SAMEPERIODLASTYEAR(Calender_Table[Date]))

    
   A card visual was used to represent this Avg Price Diff.
 
 
   <img width="82" alt="Screenshot 5" src="https://github.com/user-attachments/assets/bd65fffe-dc0c-4540-9f63-39bcd172c11b">

- Step 22 : New measure was created to calculate YOY Avg Price Growth.
 
  Following DAX expression was written to find YOY Avg Price Growth,
 
       YOY Avg Price Growth = [Avg Price Diff]/[PYTD Avg Price]
    
   A card visual was used to represent this YOY Avg Price Growth.
 
     <img width="98" alt="Screenshot 6" src="https://github.com/user-attachments/assets/8d514591-62be-4bf2-877c-a6959edaff15">

- Step 23 : New measure was created to calculate YTD Cars Sold.
 
  Following DAX expression was written to find YTD Cars Sold,

      YTD Cars Sold = TOTALYTD(COUNT(Car_Sales_Data[Car_id]),Calender_Table[Date])

    
  A card visual was used to represent this YTD Cars Sold.
 
 
    <img width="104" alt="Screenshot 7" src="https://github.com/user-attachments/assets/b3ae1a95-8521-4749-9c4f-fd88ca6985ab">

- Step 24 : New measure was created to calculate Cars Sold Diff.
 
  Following DAX expression was written to find Cars Sold Diff,

       Cars Sold Diff = [YTD Cars Sold]-[PYTD Cars Sold] where
       PYTD Cars Sold = CALCULATE(COUNT(Car_Sales_Data[Car_id]),SAMEPERIODLASTYEAR(Calender_Table[Date]))
   
  A card visual was used to represent this Cars Sold Diff.
 
 
    <img width="79" alt="Screenshot8" src="https://github.com/user-attachments/assets/f30fa0db-f59c-4df4-9987-a6b99518f0e0">
 
- Step 25 : New measure was created to calculate YOY Car Sold Growth.
 
  Following DAX expression was written to find YOY Car Sold Growth,

       YOY Car Sold Growth = Car_Sales_Data[Cars Sold Diff]/[PYTD Cars Sold]
    
   A card visual was used to represent this YOY Car Sold Growth.
 
    <img width="97" alt="Screenshot9" src="https://github.com/user-attachments/assets/0616ed99-5fd3-454f-97b6-ad8ed44d386b">
  
- Step 26 : New measure was created to calculate MTD Total Sales.
 
  Following DAX expression was written to find MTD Total Sales,

      MTD Total Sales = TOTALMTD(sum(Car_Sales_Data[Price (£)]),Calender_Table[Date])
  Displayed card metric

      MTD KPI = CONCATENATE("MTD Total Sales : ",FORMAT([MTD Total Sales]/1000000,"£0.00M"))

    
   A card visual was used to represent this MTD Total Sales.
 
     <img width="163" alt="MTDtotalsales" src="https://github.com/user-attachments/assets/6a5ef949-04bb-4d29-bbe3-ce6527e3e03c">
 
- Step 27 : New measure was created to calculate  MTD Avg Price.
 
  Following DAX expression was written to find  MTD Avg Price,

     MTD Avg Price = TOTALMTD([Avg Price],Calender_Table[Date])
  Displayed card metric
  
      MTD Avg KPI = CONCATENATE("MTD Avg Price : ",FORMAT([MTD Avg Price]/1000,"£0.00K"))

    
  A card visual was used to represent this MTD Avg Price.

     <img width="161" alt="MTDAvgPrice" src="https://github.com/user-attachments/assets/369ce3f6-eca4-485c-b015-b8a30859a872">

- Step 28 : New measure was created to calculate  MTD Cars Sold.
 
  Following DAX expression was written to find  MTD Cars Sold,

      MTD Cars Sold = TOTALMTD(COUNT(Car_Sales_Data[Car_id]),Calender_Table[Date])
    
   A card visual was used to represent this MTD Cars Sold.

     <img width="156" alt="MTDcarssold" src="https://github.com/user-attachments/assets/eba1aa5f-47a1-4580-8d18-bac91b980cc9">
  
 - Step 29 : A button was added to reset all the slicers selected.

    <img width="114" alt="clearbutton" src="https://github.com/user-attachments/assets/dc727b8a-dda8-44ea-b624-1af1b1c9fc3b">
        
 - Step 30 : The report was then published to Power BI Service.
 
   <img width="358" alt="publishreport" src="https://github.com/user-attachments/assets/e870fe65-ef45-4cf7-9218-10e58be7c4d8">

# Snapshot of Dashboard (Power BI Service)

<img width="698" alt="webview" src="https://github.com/user-attachments/assets/bdfb4b99-c145-44bd-9de1-212383c27d74">

 
 # Report Snapshot (Power BI DESKTOP)

 
<img width="670" alt="destopscreenshot" src="https://github.com/user-attachments/assets/809110f7-408e-4737-ab4a-adcd5703bd15">

<img width="664" alt="MTDoverview" src="https://github.com/user-attachments/assets/b8093acd-91ae-44a9-9c0e-02635517dbc0">

<img width="665" alt="DetailedView" src="https://github.com/user-attachments/assets/00c47999-d809-4074-a723-e5eea56a6a68">

# Insights

A single page report was created using Power BI Desktop & published to Power BI Service.

Following inferences can be drawn from the dashboard.

### [1] YTD Sales Trend
 
YTD sales for year 2023 is £370M and there is a noticeable upward trend in sales, with more frequent peaks in the latter part of the timeline, indicating increased sales activity as time progresses. 
Sales increased by 23.5% in 2023 compared to the previous year.

The average price of a car in the UK is £28,000. However, there are regional variations in prices. London has the highest average price at £28.3k, while Birmingham has the lowest average price at £27.8K.

           
### [2] YTD Sales by body style

    a) SUV - 26.9%
    b) Hatchback  - 22.3%
    c) Saloon - 19.8%
    d) Passenger - 17%
    e) Convertible - 13.8%

 SUV, hatchback, and saloon body types have dominated sales in 2023. Convertible and passenger vehicles could benefit from increased marketing or promotional efforts to boost sales.
  
### [3] YTD Sales by car color
  
      1.1) YTD sales contribution by pale white cars - 47%
      1.2) YTD sales contribution by black cars - 34%
      1.3) YTD sales contribution by red cars - 19%

  #### Average price by color

    2.1) The average price of Pale white car is £27.4K
    2.2) The average price of Black car is £28.6K
    2.3) The average price if Red car is £28.4K

Conclusion and Insights:

White cars are the most popular choice, followed by black and red. This higher demand may be correlated with lower prices.
There are noticeable differences in average prices based on color. Black cars tend to command higher average prices than red and pale white vehicles.

 ### [4] "Total Cars sold" Regional Trends

    London -17.31%
    Birmingham -15.93%
    Manchester- 14.42%
    Leeds- 13.19%
    Oxford- 13.12%
    Liverpool -13.04%
    Glasgow	-12.99%

 London, Birmingham, Manchester, Leeds, Oxford, Liverpool, and Glasgow lead in car sales, with London at the forefront. Factors such as population density and city size may influence these sales figures.
         
### [5] Transmission Type

    1) 48 % of cars sold (with YTD sales £176M) corresponds to car type 'Manual'.

    2) 52 % car sold (with YTD sales £194M) corresponds to car type 'Automatic'.
       
thus, more customers are showing interest for automatic cars.

### [6] Type of Camshaft impact on sales

The average price of Double Overhead Camshaft (DOHC) car is approximately £28.1K.It accounts for £194M annual sales.

The average price of Overhead Camshaft (OHC) car is approximately £27.9K.It accounts for £177M annual sales.

Conclusion and Insights:

The market for DOHC cars is stronger than for OHC cars, even though DOHC vehicles generally come at a higher cost. This indicates that consumers value the performance advantages offered by DOHC engines.

### [7] Top5 performing dealers with 5% of contribution to total YTD sales

    1.Rabun Used Car Sales
    2.Progressive Shippers Cooperative Association No
    3.Tri-State Mack Inc
    4.Saab-Belle Dodge
    5.Star Enterprises Inc

 ### [8] Top 5 companies with >4% contribution to total YTD sales

    1.Chevrolet
    2.Ford
    3.Dodge
    4.Oldsmobile
    5.Mercedes-B

### [9] Monthly sales trend by Gender

Sales typically peak in the latter half of the year, with December being the most popular month for car purchases in 2023.
Men account for 77% of total car sales, significantly outnumbering women. This suggests a stronger preference for car ownership among the male population.

