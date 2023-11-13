# sql-challenge

Use Python and SQLAlchemy to do a basic climate analysis and data exploration of your climate database.

## Part 1: Analyze and Explore the Climate Data

Perform a precipitation analysis and then a station analysis by completing the steps in the following two subsections.

### Precipitation Analysis

1. Find the most recent date in the dataset.

2. Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.

3. Select only the "date" and "prcp" values.

4. Load the query results into a Pandas DataFrame. Explicitly set the column names.

5. Sort the DataFrame values by "date".

6. Plot the results by using the DataFrame plot method.

7. Use Pandas to print the summary statistics for the precipitation data.

### Station Analysis

1. Design a query to calculate the total number of stations in the dataset.

2. Design a query to find the most-active stations (that is, the stations that have the most rows). To do so, complete the following steps:

• List the stations and observation counts in descending order.

• b. Answer the following question: which station id has the greatest number of observations?

3. Design a query that calculates the lowest, highest, and average temperatures that filters on the most-active station id found in the previous query.

4. Design a query to get the previous 12 months of temperature observation (TOBS) data. To do so, complete the following steps:

• Filter by the station that has the greatest number of observations.

• Query the previous 12 months of TOBS data for that station.

• Plot the results as a histogram with bins=12.

5.Close your session.

## Part 2: Design Your Climate App

Now that you’ve completed your initial analysis, you’ll design a Flask API based on the queries that you just developed. To do so, use Flask to create your routes as follows:

1.  /

Start at the homepage.

List all the available routes.

/2. api/v1.0/precipitation

• Convert the query results from your precipitation analysis (i.e. retrieve only the last 12 months of data) to a dictionary using date as the key and prcp as the value.

• Return the JSON representation of your dictionary.

3.  /api/v1.0/stations

• Return a JSON list of stations from the dataset.

4.  /api/v1.0/tobs

• Query the dates and temperature observations of the most-active station for the previous year of data.

• Return a JSON list of temperature observations for the previous year.

5.  /api/v1.0/<start> and /api/v1.0/<start>/<end>

• Return a JSON list of the minimum temperature, the average temperature, and the maximum temperature for a specified start or start-end range.

• For a specified start, calculate TMIN, TAVG, and TMAX for all the dates greater than or equal to the start date.

• For a specified start date and end date, calculate TMIN, TAVG, and TMAX for the dates from the start date to the end date, inclusive.

## Resources

Tools :
Python v3.10.11
jupyter notebook v6.5.2
Flask v2.2.2

Python Modules:

matplotlib v3.7.1
numpy v1.24.3
pandas v1.5.3
sqlalchemy v1.4.39
datetime (native to Python)

## Results

![image](https://github.com/ShubhangiBidkar/sqlalchemy-challenge/assets/38162670/8728b977-8c8a-402f-8101-4fb92de0c29d) 

![image](https://github.com/ShubhangiBidkar/sqlalchemy-challenge/assets/38162670/bb1b1564-d431-430c-b567-9ab3c704015d)

![image](https://github.com/ShubhangiBidkar/sqlalchemy-challenge/assets/38162670/339146f5-4a52-45e9-b1be-0f125b177e59)

![image](https://github.com/ShubhangiBidkar/sqlalchemy-challenge/assets/38162670/9e4bca40-bd02-4233-9e95-1d475f5e27f3)

![image](https://github.com/ShubhangiBidkar/sqlalchemy-challenge/assets/38162670/1260b2cb-d338-4714-88fe-7baffe6cef31)

![image](https://github.com/ShubhangiBidkar/sqlalchemy-challenge/assets/38162670/99ee9c1a-b4c8-434e-ace7-ba80efcf6852)






