                                                      To find What Drives the Price of a Car

                                                                Problem Overiew:

In this application we will explore a dataset from Kaggle that contains information on 400K used cars. The goal is to determine which factors make a car more or less expensive. And to provide clear recommendations on what consumers value in a used car.

                                                                About the dataset:

The dataset has 426880 data samples with 18 features.

                                                                The Features are:

![image](https://user-images.githubusercontent.com/5465929/181698350-1c3d1b5c-ba08-4d22-895f-e91ffae137e0.png)




                                                                  Cleaning the dataset:

Data samples with both manufacturer & model nulls are dropped.

The feature model has long string, so extracted the first word and updated the values like  f-150, f150.

Dropped the data samples with odometer & price with 0 values as this application focuses on recommending the used car dealers to build their inventory.

The null values in model and manufacturer are filled by getting the maximum model for the manufacturer.


                                                                      Data Analysis:

Maximum cars sold for manufacture are - ford, chevrolet, toyota, honda,nissan

Most of the cars are in good or excellent condition.

Almost 95% of the vehicles are with 4,6,8 cylinders.

Almost 95% of the vehicles are clean title_status and fuel type is gas.

Maximum transmission is automatic and drive is 4wd.

Mostly sold vehicle types are sedan and SUV.

Most of the car paint color is white.

Maximum car sold in the states - California, Florida, Texas, New York.

Maximum used cars are  5 to 14 years old.

![image](https://user-images.githubusercontent.com/5465929/181699137-2fed940e-8dde-4dad-a78e-89b45bdde5b3.png)


Maximum sold cars are with odometer reading - 150K - 175K & 20K - 30K.

Maximum used car price is 10K - 20K.

The 5 manufacturers with high prices are ferrari, aston-martin, porsche, mercedes-benz, bmw.

Plotting the top 30 Maximum Manufacture sold by State tells that ford is the maximum sold in more than 14 states followed by chevrolet.

Chevrolet- Silverado is the maximum sold used car.


                                                        Feature selection:
year & odometer are Multicollinearity features, so year is removed.
Using the feature selection methods the following features are used in modeling
'cylinders', 'odometer', 'fuel_code', 'title_status_code','transmission_code', 'drive_code', 'paint_color_code'

                                                          Modeling:
Multiple regression (Ridge regression, Lasso regression, Linear regression model) models are used for prediction.

                                                        Recommendation:
This analysis is not done for commercial or elite vehicles.
It is recommended to have an inventory of used cars odometer readings 150K - 175K & 20K - 30K in 1:3 ratio.
Recommend having the below model in the inventory.



                                                           Future:
Build the manufacture & model inventory with the new car price to clean the data better.
