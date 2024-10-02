# High-Frequency-Trading-Predictions

Getting the data from Kaggle for high frequency trading in which we will focus on to predict whether our model will be able to predict that the particular stock will able to give profit in next 1 second or not.
Predicting 1 means that the profit will be made in next 1 second and 0 will means that the there will be no change in price or it will even decrease.
As in high frequency trading we only concern about next 1 second that it will rise or not because in high frequency trading the operations like selling and buyings are performed under a fraction of seconds.
And we got our data.
First we  will load data and check for the the columns which are not useful to us like id in our case, it will be useful for tracking but not for analzying the data so we remove it.
Second we find missing values in the table that which columns are containing the highest missing values and filling those values.
There were enough rows who were having missing values approx 20% of the rows were having missing values in open_position_qty and closed_position_qty

We scaled the data using MinMaxScaler because that will be appropriate fit to our model right now
Applying catboostregressor to calculate the logloss function
Now when we applied catboostregressor we got logloss of 0.605
Now we will merge the bid,ask,bidvol and askvol columns and perform catboost regressor to check if the logloss decreases or not
we did not merge just added new columns which displays maxBID, minASK, totalBIDVOL, totalASKVOL and difference between bid and ask and it gave us logloss around 0.59 reduced the error by 1.5%
so now when we removed the rest of the data like all the ask,bid,askcol,bidvol columns the logloss increases by 3% and became 0.62 
so rest alot things can be done as the columns will remain same 
but try hyper tuning the other parameters

Data Link:- https://www.kaggle.com/competitions/caltech-cs155-2020/data
