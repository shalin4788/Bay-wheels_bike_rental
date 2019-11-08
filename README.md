# Bay-wheels_bike_rental

**Install**
- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)

You will also need to have software installed to run and execute an iPython Notebook

Install Anaconda, a pre-packaged Python distribution that contains all of the necessary libraries and software for this project.

### Run

In a terminal or command window, navigate to the top-level project directory `finding_donors/` (that contains this README) and run one of the following commands:

```bash
ipython notebook finding_donors.ipynb
```  
or
```bash
jupyter notebook finding_donors.ipynb
```

This will open the iPython Notebook software and project file in your browser.

# SF - FordGo Bike Rental Data Exploration

Created univariate, bivariate and multivariate plots using matplotlib and seaborn libraries as a part of Exploratory analysis to find out the co-relation between multiple categorical and numeric variables. The conclusion suggesting variable(s) with highest impact on ‘duration of trip’ was conveyed via Explanatory analysis.

## Dataset

There are 519,700 bike trips in the dataset with 20 columns. This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. The information about the data can be found in the https://www.bikeshare.com/data/ website and the actual data file can be found at following location - https://s3.amazonaws.com/baywheels-data/index.html

## Dataset features
Only following 7 features of our interest Note: Station name, id, latitudes, longitudes are of no value for the subject of investigation to this dataset
- There are no ordered (ordinal) factor variables
- The following are numeric variables: duration_sec, start_hour, member_birth_year
- The following are nominal - non ordered variables : month, day_of_week, member_gender, user_type

## Summary of Findings

In the exploration, I created univariate charts for the numeric variables as well as categorical variables to find out the trend of data surrounding duration_sec

Then I plotted Bivariate charts and found that there was a no linear relationship between duration and start hour OR duration and birth year.
Outside the numeric variables of interest, I verified the relationship between duration and categorical variables namely: day_of_week, month, user_type and gender. Since gender was not important for the investigation of this dataset, I decided to focus on the 3 categorical variables.
Conclusions of Bivariate chats:
- What day of week has the highest bike trip duration?
From the results, it shows the median trip duration is maximum during SAturday, attributing to weekend time AND not necessarily to working hours of weekdays
- What month has the highest bike trip duration?
From the results, it shows that the median trip duration is maximum during September, however there is not much difference across months which indicates a week co-relation
- Does the user being a subscriber OR Customer affect trip duration?
Yes, because Customers travel for larger duration based on the median value as determined from above box plot

Then I plotted multivariate charts to find out the relationship of a) Duration by user type and day of week b)
Duration by user type and month since those variables very showing as having some trend finding on the duration

*Summary*
- To summarize, weekends were more popular and it spiked the peak time and average time, with the exception of Sunday for 'Subscriber' giving no specific co-relation as to why
- Customers, though had fewer trips travelled for longer duration compared to Subscribers
- September had the most trips and most average trip duration , followed by OCtober
- There are few outliers in the month of December where people are making trips for longer time, maybe due to festive season

## Key Insights for Presentation

For the presentation, I focus on just the influence of the four categorical variables - day_of_Week, month, user_type
Afterwards, I introduce each of the categorical variables one by one. To start,
1) I create Scatter plots to track relationship between duration and other numeric variables - start hour and birth year
2) Then I create Box plots to track relationship between duration and categorical variables since there was no strong relationship concluded between numeric variables
3) Then I create heat maps and regplots (interchangeably) to track relationship of duration and Birth year on categorical variables just to see the impact of Birth year on duration w/ other categorical variables combined
4) IN the end, I created lineplot to see the effect of a)duration by User Type and Day of week b) Duration by User type and month

## List of resources used during the creation of the project.
https://www.lyft.com/bikes/bay-wheels/system-data
https://lovestats.wordpress.com/2011/09/02/what-is-nominal-data-mrx/
https://stackoverflow.com/questions/28062745/frequency-and-rotation-of-x-axis-labels-in-matplotlib
https://stackoverflow.com/questions/27237453/distribute-y-axis-ticks-evenly-between-minum-and-maximum
https://stackoverflow.com/questions/8384120/equivalent-function-for-xticks-for-an-axessubplot-object
