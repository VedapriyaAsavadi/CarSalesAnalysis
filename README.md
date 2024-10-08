# Car Sales Dashboard

### Dashboard Link :  
https://app.powerbi.com/view?r=eyJrIjoiZDY5ODExMDAtNDczOC00MmUwLWI3NzQtNDdmMGFhM2JlZTIyIiwidCI6IjYyOTA2MWUyLTg4MGMtNDI4Zi1iMTIxLWY5NjYxMDVlMmFhMyJ9
## Problem Statement

This dashboard helps to effectively track and analyse sales performance of cars across various locations in the UK.The objective of this project is to design and develop a dynamic and interactive Car Sales Dashboard using Power BI. The dashboard will visualize critical KPIs related to car sales, helping us understand sales performance over time and make data-driven decisions.

There is a noticeable upward trend in sales, with more frequent peaks in the latter part of the timeline. Data shows that 'SUV' and 'Hatchback' are the most popular body styles in terms of sales.

Major cities likes London ,Birmingham and Manchester have higher sales compared to smaller cities. There are noticeable differences in average prices based on color. Red cars are priced higher on average compared to Black and Pale White cars.

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

     <img width="79" alt="Navigator" src="https://github.com/user-attachments/assets/968f2e0b-6fba-4526-8ec8-79dd61e9db3a">


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
 
 
 <img width="65" alt="YOYgrowth" src="https://github.com/user-attachments/assets/720b770f-fff3-4681-bba6-bd96972e572b">

- Step 19 : New measure was created to calculate YOY Sales Growth%  .
 
  Following DAX expression was written to find YOY Sales Growth% ,
 
      YOY Sales Growth% = Car_Sales_Data[Sale Difference]/Car_Sales_Data[PTYD Total Sales]

    
 A card visual was used to represent this Sale Difference.
 
 
 <img width="77" alt="%YOYgrowth" src="https://github.com/user-attachments/assets/a91c68ce-a35b-4a03-8da3-a5f999534276">

- Step 20 : New measure was created to calculate YTD Avg Price  .
 
  Following DAX expression was written to find YTD Avg Price,
 
      YTD Avg Price = TOTALYTD([Avg Price],Calender_Table[Date])  where
      Avg Price = SUM(Car_Sales_Data[Price (£)])/COUNT(Car_Sales_Data[Car_id])

    
 A card visual was used to represent this YTD Avg Price.
 
 <img width="95" alt="YTDavgPrice" src="https://github.com/user-attachments/assets/31eb4089-b1c8-4cef-97b2-7ac857b24ae8">

- Step 21 : New measure was created to calculate Avg Price Diff  .
 
  Following DAX expression was written to find Avg Price Diff,
 
      Avg Price Diff = [YTD Avg Price]-[PYTD Avg Price] where
      YTD Avg Price = TOTALYTD([Avg Price],Calender_Table[Date])
      PYTD Avg Price = CALCULATE([Avg Price],SAMEPERIODLASTYEAR(Calender_Table[Date]))

    
 A card visual was used to represent this Avg Price Diff.
 
 
 <img width="67" alt="YOYAvgPriceGrowth" src="https://github.com/user-attachments/assets/a0ddcd46-5cca-4526-bab7-58f77522764d">

- Step 22 : New measure was created to calculate YOY Avg Price Growth.
 
  Following DAX expression was written to find YOY Avg Price Growth,
 
       YOY Avg Price Growth = [Avg Price Diff]/[PYTD Avg Price]

    
 A card visual was used to represent this YOY Avg Price Growth.
 
 
  <img width="79" alt="%YOYAvgPricegrowth" src="https://github.com/user-attachments/assets/92b01865-8e51-4a2a-8ccc-e0b6b31816cc">

- Step 23 : New measure was created to calculate YTD Cars Sold.
 
  Following DAX expression was written to find YTD Cars Sold,

      YTD Cars Sold = TOTALYTD(COUNT(Car_Sales_Data[Car_id]),Calender_Table[Date])

    
 A card visual was used to represent this YTD Cars Sold.
 
 
 <img width="89" alt="YTDcarssold" src="https://github.com/user-attachments/assets/2e837fd1-88aa-4439-b09c-eeecb9f6dba7">

- Step 24 : New measure was created to calculate Cars Sold Diff.
 
  Following DAX expression was written to find Cars Sold Diff,

       Cars Sold Diff = [YTD Cars Sold]-[PYTD Cars Sold] where
       PYTD Cars Sold = CALCULATE(COUNT(Car_Sales_Data[Car_id]),SAMEPERIODLASTYEAR(Calender_Table[Date]))
   
 A card visual was used to represent this Cars Sold Diff.
 
 
 <img width="71" alt="CarssoldYOYgrowth" src="https://github.com/user-attachments/assets/ea396a31-80e0-4316-8fcd-4cbfd77227a1">
 
- Step 25 : New measure was created to calculate YOY Car Sold Growth.
 
  Following DAX expression was written to find YOY Car Sold Growth,

       YOY Car Sold Growth = Car_Sales_Data[Cars Sold Diff]/[PYTD Cars Sold]
    
 A card visual was used to represent this YOY Car Sold Growth.
 
  <img width="78" alt="Carssold%YOYgrowth" src="https://github.com/user-attachments/assets/16c876d7-00e6-4f7d-9090-a3715368b9f4">
  
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

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] YTD sales for year 2023 is £370M and there is a noticeable upward trend in sales, with more frequent peaks in the latter part of the timeline, indicating increased sales activity as time progresses. 
Sales have been increased by 23.5% compared o last years.

Average price of the car stand at £28K with London having the highest average price of £28.3k and Birmingham having lowest avg price of £27.8k.

           
### [2] YTD Sales by body style

    a) SUV - 26.9%
    b) Hatchback  - 22.3%
    c) Saloon - 19.8%
    d) Passenger - 17%
    e) Convertible - 13.8%

 Sales are higher for SUV and Hatchback and saloon are the preferred body types for the year 2023.There may be opportunities to increase sales for 'Convertible' and 'Passenger' body styles, which have lower sales counts.
  
### [3]YTD Sales by car color 
  
      1.1) YTD sales contribution by pale white cars - 47%
      1.2) YTD sales contribution by black cars - 34%
      1.3) YTD sales contribution by red cars - 19%

    ##Average price by color

   2.1)The average price of Pale white car is £27.4K
   2.2)The average price of Black car is £28.6K
   2.3)The average price if Red car is £28.4K

Conclusion and Insights
White cars have the highest sales, followed by black, and then red cars. This higher sales might be associated with lower price of the car .
There are noticeable differences in average prices based on color. black cars are priced higher on average compared to red and Pale White cars.


 ### [4]Cars sold Regional Trends

London -17.31%
Birmingham -15.93%
Manchester- 14.42%
Leeds- 13.19%
Oxford- 13.12%
Liverpool -13.04%
Glasgow	-12.99%

London tends to have higher car sold followed by Birmingham ,Manchester Leeds , Oxford , Liverpool and Glasgow.
 
Higher sales might be related to other factor like population density and area size.
         
### Transmission Type

3.1) 48 % of cars sold (with YTD sales £176M) corresponds to car type 'Manual'.

3.2) 52 % car sold (with YTD sales £194M) corresponds to car type 'Automatic'.
       
       thus, more customers are showing interest for automatic cars.

### Type of Camshaft

The average price of Double Overhead Camshaft car is approximately £28.1K.It accounts for £194M annual sales.

The average price of Overhead Camshaft car is approximately £27.9K.It accounts for £177M annual sales.

Conclusion and Insights

Cars with a Double Overhead Camshaft tend to be priced higher than those with an Overhead Camshaft.Sales are higher for Double Overhead Camshaft car compared to Overhead Camshaft cars.

### Top5 performing Dealer with 5% of contribution to total YTD sales

1.Rabun Used Car Sales
2.Progressive Shippers Cooperative Association No
3.Tri-State Mack Inc
4.Saab-Belle Dodge
5.Star Enterprises Inc

 ### [5] Top 10 companies with >4% contribution to total YTD sales

Chevrolet
Ford
Dodge
Oldsmobile
Mercedes-B
Mitsubishi
Volkswagen
Toyota
Chrysler

Monthly sales trend with Gender

Sales tends to be higher during the second half of the years with December showing highest number of sales.
Male contributes to 77% of total sales as compared to Female papulation
thus, male papulation showing interest to buy cars as compared to Female papulation.
