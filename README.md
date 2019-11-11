# crowd_prediction

This project contains a multi class classification problem under which we need to predict the crowd at the railway station using the train data. Some of the features given are.
1. id-code -- unique code
2. current_date
3. current_time
4. source_name
5. destination_name	
6. train_name	
7. 	is_weekend
8. country_code_source	
9. longitude_source	
10. latitude_source	
11. mean_halt_times_source	
12. country_code_destination	
13. longitude_destination	
14. latitude_destination	
15. mean_halt_times_destination	
16. current_year	
17. current_week	
18. current_day	
19. target --- output variable('high', 'medium', 'low')

## Preprocessing
All the numerical missing values are replaced by 0 and categorical features are replaced with empty string ''.

## Featurization
All the categorical features are featurized using the FeatureHashing technique.
Some additional features are extracted from the current time(absolute time, hour of the day) and current day(day of the year)

## Cross Validation and Modelling
A 3 fold cross validation is done on the train data after splitting the whole data into train and test data.
XGBoost algorithm is used for classification and the hyperparameters obtained are used on the train data to fit the model
