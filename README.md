# Restaurant Records Analysis:
Situation: 
The Owners of a local Mom and Pop style restaurant, concerns with the rising cost of operations, and need an analyst to explores their orders records.

### Primary Goal:
Using Python to identify:

1. The most popular dishes.
   
2. Busiest order times.
   
3. Opportunies to streamline operations. 

There are two csv files to analyze: orders.csv and menu_items.csv, this project will require the use of both to answers the two main questions that is crucial for a business operation.

1# What items drives the most and least revenue?

2# Which time periods have the highest and lowest revenue?

### Task 1: Importing the Orders File:
<img width="572" height="458" alt="image" src="https://github.com/user-attachments/assets/916bcfb7-14cd-4cbf-bb2a-6176e3eb08ac" />

<img width="470" height="409" alt="image" src="https://github.com/user-attachments/assets/58286966-f408-4a24-af16-532e10d56f20" />

From the results from head to tail, show the first order be places on the 01/01/2023, and the last was places at the 31/03/2023, so this data is comprise of 3 months worth of record.

### Task 2: Checking data type:
<img width="711" height="389" alt="image" src="https://github.com/user-attachments/assets/e506db5c-2b61-4bab-be77-5c32dfb8b945" />


. It’ seem the data frame has 12,234 entries, meaning 12,234 items were order during the three months.

. Upon examine the datatype, a problem arises, the columns of “order_timestamp” is read as an object, when it’s should had been  data time, so that need to be reconfigured.

<img width="583" height="85" alt="image" src="https://github.com/user-attachments/assets/fdddd267-6730-4ee7-828f-4dbcef7d45bd" />

. Through the usage of the "parse_dates" features, the "order_timestamps" is convert to a datetime64 type.

. Another problem arises, the column “item_id” only have 12,097 value that is not empty, while the total entry is 12,234, meaning there are 137 missing values. 


