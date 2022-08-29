# Bike-Sharing-Program-
#### Purpose:
Is a bike-sharing program beneficial in Des Moines? Check out the data visualization for details!

[link to Story]()

[link to Dashboard]()

Resources: Pandas and Jupter notebook, Tableau 

Cleaning Dataset - we use Pandas to change the "tripduration" column from an integer to a datetime datatype. Then, create a set of visualizations to:

- Show the length of time that bikes are checked out for all riders and genders
- Show the number of bike trips for all riders and genders for each hour of each day of the week
- Show the number of bike trips for each type of user and gender for each day of the week.

## Deliverable 1: Change Trip Duration to a Datetime Format

using the pandas libray, we used the pandas.to_datetime() functin to change the "tripdurartion" column to the desire format. Inside the datetime function we used the The unit of the arg "Unit" which is an integer or float number that incoorporates the number of milliseconds.

Figure 2.
![This in image]()  

export the DataFrame as a new CSV file without the index column
Figure 3. 
![This in image]()  


Figure 4.
![This in image]()  


## Deliverable 2: Create Visualizations for the Trip Analysis
### How long bikes are checked out for all riders and genders?
To create this visual we added the two tripduration fields into the columns; one decrete for filtering purposes (to only show less than 1 hour, 1, 2, 3rd hour block and as continuous to display data by the minute. The citibike data was added to the rows to display total checked out bikes. 
Note: x-axis can be changed if such column is stored as continues data; discrete “pills” are distinct values that cannot be changed. Continuous fields in tableau are highlighted green while discrete fields are highlighted blue. 

Figure 5. Line Graph of Checkout Times for Users 
![This is an Image]()
 
Description of Results: This  line graph displays the amount of checked out bikes out throughout the hour block. Top of the graph we see “trip duration” broken down by 1, 2, 3-hour blocks, while the bottom x-axis showing per the minute with the hourly block.  
We immediately see a popular checkout time within the first 0hrs, 6mins timeframe (107,815 citibikes checked out!) figure 5a.
Figure 5a) Most popular checkout time
![This is an Image]()
 
although not rare, we see between 1-4 bikes checkout for a period of 23 hours.
Image 5b) Maximum time checkout 23hr+  
 
### How many trips are taken by the hour for each day of the week, for all riders and genders?
The same parameters were used( as figured 5) along with gender field in the marks section. 
Figure 6. Line Graph Checkout times by Gender 
 
Description of Results: On the “Gender(count)” field we created a calculation field. The original csv recorded gender as a number. The number 1 was documented as Male, while 2 for Female, and anything left blank was marked 0. View the calculation in figure 6a.
Figure 6a) Created the “Gender Number to String” Calculation 
![This is an Image]()

 
Straight off the bat, we see a spike of Male renters versus Females. Unbelievable most popular duration is under 10 minutes.
Figure 6b) Males Renters
 
### Create a breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender
#### Trips by Weekday for Each Hour Viz
To create this heatmap, we added Starttime and Stoptimes fields to rows and columns then filtered by the hour and weekday, respectively. The heatmap was created with count total in the color mark. We formatted the chart fields an easy read. 
Image 7. Heatmap of total trips by Weekday
![This is an Image]()
 
Description of Results: The heatmap is a perfect representation of what areas are most concentrated. In this example, it the color saturation helps the audience see what times of the week are least and most popular. To help reduce the mental process of picking out the least and most popular time is to label these cells with its count as shown in figure 7a. Most popular bike rentals is Saturdays followed by weekday evenings.
Figure 7a) Calling out Bike Checkout Time Counts 
![This is an Image]()
 
#### Trips by Gender (Weekday per Hour)
The same fields as Figure 7 were used but this time we threw in Gender. 
Image 8. Heatmap Trips by Gender (weekday per hour)
![This is an Image]()

 
Description of Results: The gradient was changed but this heatmap shows the color spectrum of rented bikes by males. Particularly most popular Monday by 6:00pm.

#### The number of bike trips broken down by gender for each day of the week by each User type (subscriber or not)
Image 9. Heatmap User Trips by Gender and Weekday 
![This is an Image]()
 
Description of Results: Adding the usertype field we can see the regular customer (top half) vs the subscriber (bottom half). We see a heavy use of  male subscribers throughout the everyday of the week. We see Monday & Saturday as the highest popular days
Figure 9a) Bike Count Breakdown 
![This is an Image]()

