# forecast-rossman-store-sales
**_License:
This is a personal project of Tung Pham in order to serve as the final project for the Data Mining course taken at the University of Economics and Law (VNU-HCM)_**

**Post for Udacity Data Scientist assignment 1 project:** https://medium.com/@phamduytung999/ever-wondered-how-drugstores-predict-their-daily-sales-for-weeks-in-advance-56acc52a446b 

**Dataset ak**
   - Kaggle link of the dataset: https://www.kaggle.com/competitions/rossmann-store-sales/data
   - Source: Rossmann Corp
   - License: Subject to Competition Rules
   - Short description: The dataset is provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. The data ranges in which company provided constraint from 01/01/2013 to 31/07/2015 and is collected at a daily frequency, considered all the sale of all the stores available.

**Describe the dataset:**
  With a quick glimpse at the dataset, we could observe there are 2 main csv files included in, namely rossman_train and rossman_store. In the rossman_train file, there are 1,017,210 observations with 9 recorded attributes. 
  
  Data – Historical sales (rossman_train.csv file): 
  -	Store: a unique id for each store
  -	DayOfWeek: the date of week in which the store sale information record (1 = Mon, 2 = Tues, 3 = Wed, 4 = Thur, 5 = Fri, 6 = Sat, 7 = Sun)
  -	Date: that date of recording store sale information
  -	Sales: the turnover for any given day (this is what you are predicting)
  -	Customers: the number of customers on a given day
  -	Open: an indicator for whether the store was open: 0 = closed, 1 = opened 
  -	Promo: indicates whether a store is running a promo on that day
  -	StateHoliday: indicates a state holiday. Normally all stores, with few exceptions, are closed on state holidays. Note that all schools are closed on public holidays and weekends. 0 = none, 1 = holiday.
  -	SchoolHoliday: indicates if the (Store, Date) was affected by the closure of public schools.
  In the rossman_store file, there are 1115 observations with 10 attributes. 
  
  Data – Stores (rossman_store.csv file):
  -	Store: a unique id for each store
  -	StoreType: differentiates between 4 different store models: a, b, c, d
  -	Assortment: describes an assortment level: a = basic, b= extra, c = extended
  -	CompetitionDistance – distance in meters to the nearest competitor store
  -	CompetitionOpenSince[Month/Year]: gives the approximate year and month of the time the nearest competitor was opened
  -	Promo2: Promo2 is a continuting and consecutive promotion for some stores: 0 = store is not participating, 1 = store is participating
  -	Promo2Since[Week/Year]: describes the calendar week and year when the store started participating in Promo2
  -	PromoInterval – describes the consecutive intervals Promo2 is started, naming the months the promotion is started anew. E.g., “Feb,May,Aug,Nov” means each round starts in February, May, August, November of any given year for that store

**The problem statement:**
  Rossman operates over 3,000 drug stores in 7 European countries. Currently, Rossman store managers are tasked with predicting their daily sales for up to 6 weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied. Historical sales data for 1,115 Rossmann stores are provided. 
With all this information, the task for us is to predict the sales of the Rossman stores for the next 6 weeks.

**Natural of the case:**
  This dataset and problem represent a type of data, modeling and analysis which is called “Time series”. The dataset provided is a time series data, which is a collection of quantities that are assembled over even intervals in time and ordered chronologically, in this case, it’s the information about Rossman store sale situation over the given time period. And because data points in time series are collected at adjacent time periods, there is potential for correlation between observations. If the correlation between these observations exists, it could reveal hidden insights and enable deeper understanding of the situation for those who are responsible. The use of time series model and analysis could be for a variety of reasons: predicting future outcomes, understanding past outcomes, making policy suggestions, and much more. In this case to forecast Rossman sales for 6 weeks in advance. 
