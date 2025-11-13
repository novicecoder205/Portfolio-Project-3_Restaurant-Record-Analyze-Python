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


### Task 3: Cleaning Missing Value.
. With the 137 missing values from 137s rows, those 137 row must be drops since the other information from the other columns on the rows where "item_id" is noneexistence is not useful, since it is missing.
. This need to be address to the project leader, so an investigation on why those ID are missing in the first place.

<img width="478" height="482" alt="image" src="https://github.com/user-attachments/assets/8a16936c-ccbd-455b-bf60-e7cbbd63ed2e" />

. After applying the dropna, the officials amount of rows is drops to 12097, and we save the change to our dataframe.

<img width="589" height="176" alt="image" src="https://github.com/user-attachments/assets/fba2d951-6610-45a7-959e-0877bb678b1c" />

### Task 4: Joining the two tables.
<img width="362" height="535" alt="image" src="https://github.com/user-attachments/assets/bb0f65f4-b8e6-4d4d-a08d-9ee071bd2552" />

. After loading the dataset, there seem to be no missing values, and the columns data and their types seem to be accurates. 
. Now we create a new dataframe to join the two.

<img width="689" height="294" alt="image" src="https://github.com/user-attachments/assets/701a661c-0622-4aa0-b4a4-47a884f03379" />
