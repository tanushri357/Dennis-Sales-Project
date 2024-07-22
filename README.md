
# Dennis Sales summery report-

## Instroduction - 

An online national clothing chain needs your help creating a targeted marketing campaign. Sales have been flat and they want to lure lost customers back. They want to advertise specific products to specific customers in specific locations, but they don’t know who to target. They have three products in mind:

-Shirts,
t-shirts,
teans,
tackets.
bottoms,
dL Women.

In this project, you do analys the product's sales, revenue,cost of Dennis Lingo brand on the basis of catagory,sub-catagory and country for the year 2014 - 2017. We mainly performed the analysis on the basis of two parameter -
Finacial & Product.

### Steps followed 

- Step 1 : Create storage in Azure cloud (ADLS,Blob) and Load data into it, dataset are csv file.

![image](https://github.com/user-attachments/assets/7f51ee4f-4c70-4b14-9c3e-63d79f9f26dd)

 ![image](https://github.com/user-attachments/assets/0a3b5229-085a-4962-9b28-7294c302a182)

- Step 2 : Create ADF(Azure data fabric) in Azur cloud and collect data from on-prem and othr azure storage through creating two link services.
          
      In on-prem there is no storage need to create as data is directly coming from external resource (commonly SQL server /mySQL).In that cases we direct create link service from on-prem to ADF.


- Step 3 : Create datasets and do data transmission through ADF data flow as per requirment and the will create pipeline for each data-flow.After creating pipelines we need to join each pipelines and then run the pipelines.

![image](https://github.com/user-attachments/assets/0e49cdfe-9001-4520-91a9-0e7dcff0bf84)

- Step 4 : Create one more account i.e. Azure SQL database in which final data will store after data transmission once pipeline will trigger.We need to create one more link service from ADF to Azure SQL dartabase to transfer the data.

![image](https://github.com/user-attachments/assets/1c7fbef8-ab15-4e8d-8220-1e12144d1383)

![image](https://github.com/user-attachments/assets/3734446a-aab4-43f2-9d47-d7c247fe0139)

- Step 5 : Upload the data from Azur SQL database to Power Bi desktop to build a report, as data transmission already done in ADF so did not use power query in Power Bi desktop.

![image](https://github.com/user-attachments/assets/f011922f-7bfa-483a-821b-af46585fb7b1)

- Step 6 : Calculated previousmonth profit,MOM groth(%),QOQ growth, avrage profit, revenue,cost and quantity with the help of DAX.
- Step 7 : In the report view, under the view tab, theme was selected.
- Step 8 : Since the data contains various ratings, thus in order to represent ratings, a new visual was added using the three ellipses in the visualizations pane in report view. 

- Step 9 : Eight cards visuals were added to the canvas - Tota and avg profit,revenue,cost and quantity.Although, by default, while calculating average, blank values are ignored.
- Step 10 : different Visuals was used to analys below parameters,

1.Financial analysis-

- MOM Growth(%).

- Quarterly growth.

- Revenue by Month, year, querter.

- Country wise total profit, revenue and quantity.

2.Product analysis-

- Yearly growth on revenue on product saling.

- Profit erning on product in countries.



- Step 11 : In the report view, under the insert tab, two buttons were added for page navigation.
- Step 12 : In the report view, under the insert tab, using shapes option from elements group a rectangle was inserted & similarly using image option company's logo was added to the report design area. 

- Step 13 : for calculating MOM growth(%) following DAX expression was written;
       
        1. Previous month Profit = CALCULATE([Total Profit],PREVIOUSMONTH(DateMaster[Date]))
        2. MOM% Growth = (([Total Profit]-[Previous month Profit])/[Total Profit])


- Step 14 : After creating the reports,the report was then published to Power BI Service.
 
 ![image](https://github.com/user-attachments/assets/64fcd059-5d7d-47ca-8c3f-e8707562ea50)

## Snapshot of Dashboard (Power BI Service)

![image](https://github.com/user-attachments/assets/33693656-c9e7-4052-9a00-16963eace6e4)

 
 ## Report Snapshot (Power BI DESKTOP)

 
![image](https://github.com/user-attachments/assets/f86d207f-bbc3-4eec-9191-c7c19b34ef6d)

## Report Analysis-

1. On year 2014 MOM growth(%) was negative in 5 months(Feb,May, Aug,Sep and Nov ),while on year 2016 growth decreases more it covered 8 months, however on year 2017 it recovers and it turns into 5 month from 8 months.
2. If we talk about querterly growth on 2014 profit was low on Q3 approx 4.8M however  for year 2015 and 2016 Q3 was leading and on 2017 Q4 was on highest in terms of profit.
3. In Germany the cost is more then other countries while in denmerk the cost is very less thus we need to increase the quantity to genarate more profits.
4. Revenue increases on year 2015 again it decreased on year 2016, however we can observe a huge increment in revenue on year 2017, so the startegies we followed to inreac=se the sales we need follow the same to maintain the growth in revenue and can earn more profits.


