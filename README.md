# Surfs up!!
Weather analysis for your Hawaii business venture
 
#### Overview
Your ice cream and surf shop in Oahu is getting real traction with some interested parties, and you might be able to land a healthy investment soon! It's all really exciting stuff, but first it's a smart idea to do some extra analysis on the temperatures during the months of June and December. These two months show the hottest and coldest temperatures that your shop will have to endure, so having some analysis showing that your shop can survive the elements year-round will be helpful to investors.

#### Resources
- Data source: hawaii.sqllite
- Software: Visual Studio Code 1.58, SQLite 3.36, DB Browser for SQLite Version 3.12.2, Python 3.7.6, Jupyter Notebook 6.3

#### Results
Before speeding off into the months of June and December, we have to set up the database source within the python code we are running. After importing any necessary dependencies, we can set up our engine so that it can be linked to python and each table is assigned a reference.

![Before temps](https://user-images.githubusercontent.com/84139177/129970220-4209c54a-f853-4883-a6c7-ce46eb4d1b21.png)

Once our introduction is set up, we can delve into the specific queries for the months of June and December. We must import the sqlalchemy extract function for our queries so we design a data request applied to a specific month. Once we link with the table resource and extract data for the months of June and December, we can add those temperature data points to a list and a subsequent ataframe. Then, using the describe() function, we can generate summary statistics.

The extract query for June filters temperatures within the month equal to "6", and
![June](https://user-images.githubusercontent.com/84139177/129971102-eb882ea2-829b-4ae1-8faa-10ea0dd98488.png)

the extact query for December filters temperatures within the month equal to "12."
![Dec](https://user-images.githubusercontent.com/84139177/129971112-22af7719-f585-4bf5-ba89-01a46461db4f.png)

##### Key differences between June and December
- We have less data from December to work with (1517 total) than June (1700 total). It will likely not make a huge difference between our results, but, in general, it should be noted that our summary statistics only represent a small sample of the weather environment.
- June looks like a great month for ice cream with a minimum of 64 degrees. December, on the other hand, has a minimum of 56 degrees, which is not great weather for selling ice cream. December has a chance of maintaing a revenue stream with a monthly max currently at 83 degrees, but there will be risk invovled.
- The mean temperatures of June and December differ by about 4 degrees. Only 4 degrees! If the hottest and coldest months share similar average temperatures suited for ice cream and surfing, then it can be safe to say that the rest of the year will be suited for business as well. 

#### Summary
As the generated statistics show, there are no extreme temperatures in Oahu, and your ice cream and surf shop will have a very good chance of creating revenue year-round! Just to be safe, we can generate additional queries for the month of June and December that give more insight. We can use the query that we used for temperature and replace the column we are filtering through to "Measurement.prcp." This way, we can generate summary statistics for the precipiation points during June and December and look for any outliers.

![Prcp](https://user-images.githubusercontent.com/84139177/129975546-647375c5-ba4e-4d34-9dd2-1df32d002f6f.png)

The average precipitation for both June and December fall within measurements for light and moderate rainfall, which should be manageable. You should show this additional information to your possible investors.
