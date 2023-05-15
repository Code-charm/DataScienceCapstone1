# Flight Cancellation Prediction 

![alt text](Flight Travel Image.png)

*Quick Fly (QF) is a US based air cargo delivery service provider.  Recently, it was brought to the attention of the leadership that QF has been paying higher than industry average claims for air cargo shipment delays caused by flight cancellation, mostly for shipments departing Los Angeles International Airport (LAX).  We need to to evaluate and identify the elements that impact the likelihood of flight cancellation out of LAX, so that QF can try to avoid those elements to ensure an improved on-time-delivery rate.*

### Data Source
We used the datasets of flight delays and cancellations published by the U.S. Department of Transportation (DOT) posted on Kaggle. The datasets consist of 3 files, airlines.csv, airports.csv and flights.csv.


### Data Wrangling
Out of the 3 datasets we have, airlines.csv and airports.csv are pretty straightforward and don’t require much cleaning work.  However, flights.csv is humongous and contains 5,819,079 entries with a lot of missing data.  That’s the file we spent most time cleaning and organizing.  There are 3 key issues identified with the flights.csv dataset.
- Missing data: deleted or replaced depending on the relevancy of missing data to our study
- Data Integrity: researched and obtained additional resources to fix data integrity issue
- Data Organization: merged 3 files into one containing all the information needed for modeling

### EDA (Exploratory Data Analysis)
We analyzed the data by airlines, destination states/airports, flight months, fight days of week, and flight days of month.  A heatmap was also conducted to show the correlations among all the numeric variables in our database.

### Modeling
After label-coding all categorical variables, standardizing all numeric features and splitting the data into train and test sets, we started the modeling process.  Since the dependent variable, “CANCELLED”, is a categorical variable, we chose the following 6 machine learning algorithms commonly used for classification problems and compared model performance metric, specifically the recall score, since we are mostly interested in identifying all flights that can potentially be cancelled.  
1. Logistic Regression
2. k-Nearest Neighbors
3. Random Forests
4. Gradient Boosting
5. Extreme Gradient Boosting
6. Decision Trees

### Conclusion 
Based upon the model performance metrics, we conlcuded that kNN is our best model. kNN delivers a recall score of 99.8%, which means it will accurately predict 99.8% of all flight cancellations.  Its overall accuracy is above 98%, which is also very impressive.
