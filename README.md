## **SPEED CAMERA VIOLATIONS**
### **Link for Project - 2 Observable:**  https://observablehq.com/@indureddypati/project2
  
Team COD
  
Shiva Praveen Donga (UIN: 676463688)
  
Indu Reddy Pati (UIN: 657783668)


## 1. **Introduction:**
  
In this project, we used a Speed Camera Violation dataset to visualize the attributes of interest. The main goal of this project is to explore data visualization. We used Pandas, GeoPandas, Matplotlib and Jupyter to import, transform, visualize and analyze a dataset. Before visualizing the dataset, we have done data preprocessing and data cleaning. We comprehensively explored the dataset using different plotting techniques. We explored every insight possible in the dataset using multiple attributes.

## 2. **Data Description:**

**2.1. Dataset Overview:**

The dataset is obtained from the [Chicago Data portal](https://data.cityofchicago.org/Transportation/Speed-Camera-Violations/hhkd-xvj4). The camera and radar system has recorded the violations that have been reported. The data that we considered is from July 1st 2014 to August 31st 2022. This dataset has 9 attributes (Columns) and 309,320 data rows. The attributes are: ADDRESS, CAMERA\_ID, VIOLATION\_DATE, VIOLATIONS, X\_COORDINATE, Y\_COORDINATE, LATITUDE, LONGITUDE and LOCATION.

![alt text](https://github.com/uic-vis/project-1-team-cod/blob/main/images/Initial_DF.png?raw=true)

**2.2. Data Cleaning:**

The dataset consists of null values so we tried to remove NAN or null values. There are a total 309,320 data rows of which 11,782 rows have null values. So, we used .dropna() to remove (or drop) all the null values. After dropping all the null values, the dataset has 297,538 rows in total.

<img width="1147" alt="Screen Shot 2022-11-04 at 10 39 50 PM" src="https://user-images.githubusercontent.com/53014597/200099292-e4514be6-6e00-4be5-947f-835b0f9060a9.png">

**2.3. Extraction:**

We extracted the required extra columns from already present columns Dataset - weekday, year, month, day from VIOLATION\_DATE.

<img width="1157" alt="Screen Shot 2022-11-04 at 10 37 04 PM" src="https://user-images.githubusercontent.com/53014597/200099218-f6cc5b86-604f-443c-a555-575cd576d933.png">

**2.4. Data Aggregation:**

Aggregate the Speed Violations Data as required such as AddressWise, MonthWise, Yearwise.
<img width="1074" alt="Screen Shot 2022-11-04 at 10 44 32 PM" src="https://user-images.githubusercontent.com/53014597/200099409-3e2a7acf-0ca4-4140-986f-3369566d304b.png">

## **3.Questions and Observations:**

**3.1. Question - 1:** 

What is the Trend in Speed Violations over the Years (2014 - 2022)? Did they Increase(↑) or Decrease(↓)?

We plotted the bar chart with the number of violations over the years. From the bar chart we can see that Over the years 2014-2020 there has been a slight decrease in the violations.
<img width="1201" alt="Screen Shot 2022-11-05 at 2 59 26 AM" src="https://user-images.githubusercontent.com/53014597/200110020-2e767d30-466d-4fa6-a443-c6d9107ab098.png">

From the above Bar Chart, it is hard to know the change in the number of violations. So, we defined a Divergent Bar Chart, to know the Relative and Absolute Difference in the violations for Current Year compared to Previous Year.

<img width="1157" alt="Screen Shot 2022-11-05 at 3 05 26 AM" src="https://user-images.githubusercontent.com/53014597/200110259-ce2b5823-a3b2-418d-8e12-391d7f6059d1.png">

Toggle below Radio buttons for Absolute or Relative Change in Violations.

<img width="1167" alt="Screen Shot 2022-11-05 at 3 08 39 AM" src="https://user-images.githubusercontent.com/53014597/200110323-5e8215e9-63a1-4990-be1a-68b456b54e43.png">

**Observation for Question - 1:**

Note: 2014 and 2022 are outliers as complete data is not available (Available Data is from 1st July 2014 to 31st August 2022).
- If we see the Bar Chart, over the years 2015-2020 there has been a slight decrease in the violations.
- And There is a peak  increase in the year 2021. But absolute or relative increase in Number of Violations can't be said from Bar Chart.
- So, We created a Divergent Chart, from which we can see that Number of Violations from 2020 to 2021 increased by almost 3 times(288%).
- Reason, could be people preferring to use there own vechiles to avoid the public crowd due to Pandemic.

**3.2. Question - 2:**

What are the Number of Speed Violations per Chicago Street (2014 - 2022)?

Using x and y coordinates and address  given in the data set we plotted the interactive bubble plot with x - coordinate on x-axis and y - coordinate on y-axis on Chicago Map.

<img width="1017" alt="Screen Shot 2022-11-05 at 3 20 22 AM" src="https://user-images.githubusercontent.com/53014597/200110657-47d4ac2f-4197-4752-a494-af6dbd0d191f.png">

We took number of speed violations based on Color Legend for Bubble Chart. <img width="338" alt="Screen Shot 2022-11-05 at 3 22 32 AM" src="https://user-images.githubusercontent.com/53014597/200110715-7ded16bc-3f8b-492b-b2af-317b80537e78.png">

- As it is hard to tell from Bubble Size and Color the Number of Violations. We have created a hover effect for this interactive bubble chart. So, when we hover Over the Bubbles it gives Street Name and Number of Violations

**Observations for Question - 2:**
- From the plot we can observe that over the year 2014-2022, the most violations are from Irving park with 760522 violations.
- And next most violations are from the same neighborhood which is Western with 610585 violations. 
- The least violations is from Superior St. With 235 violations. This neighborhood has less violations compared to other neighborhoods.
- From this we can say that more violations streets are to north of Chicago than south.

**3.3. Question - 3:** 

What is the trend in Speed Violations across different months from 2014 - 2022?

We plotted the  bar chart with comparison on increase or decrease with other bars(Months) . In this we have Months on x-axis and Violations on y-axis. And we have a number of violations on each bar.

<img width="1177" alt="Screen Shot 2022-11-05 at 3 49 54 AM" src="https://user-images.githubusercontent.com/53014597/200111741-b4a7910c-42c9-4709-b8fa-6d9604035721.png">

- For easy to interpret and comparison of one month with other months. We made the Bar Chart interactive, the percentage of decrease or increase is shown when we hover over a particular month bar.

**Observations for Question - 3:**
- When we compared the least violation month february with highest violation month(July) there is an increase of +94.04%.
- Most violations and least Violations: July - 1159159,   Feb - 596287 respectively.
- The months of a summer have more violations than the winter season.
- Reasons for more summer violations could be:  
    People being on trips for summer vacation and People prefer public transport in winter than own vehicle and the other reason could be Brake Lockup due to Cold Weather.
    
**3.4.Questions - 4:** 

What is the trend in Speed Violations across Weekdays from 2014 - 2022?

We created a Linked View for Brushable Scatter Chart and Bar Chart. Scatter plot has the x and y coordinates from the data set and Bar plot has the weekdays which we extracted from given date of violation  data from the dataset.

<img width="1068" alt="Screen Shot 2022-11-05 at 4 03 31 AM" src="https://user-images.githubusercontent.com/53014597/200112162-55bc6f94-1ba8-412d-b18a-093b96740ebb.png">

- We created a Brush on Scatter Chart to Update the Bar Chart when we Brush on particular x and y coordinate on scatter plot we can see updated weekdays number of violations on bar chart. This helps user to easily interact and interpret the Number of violations for weekdays on x and y coordinates of Chicago.

**Observations for Question - 4:**
- Overall Friday has most number of violations in any particular area.
- Weekends have less violations when compared to weekdays.
- Reasons for Less violations on Weekends could be:  
    People being on trips for weekends to different cities or resting at home (Not in rush for not being late to work).
- From question 2 we saw Irving park has more violations when we brush that exact same irving park coordinates in this scatter, Saturday has most violations.


