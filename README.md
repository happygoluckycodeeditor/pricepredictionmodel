# pricepredictionmodel
This a python project practicing machine learning and data visualisation predicting housing prices in Mumbai and in Delhi


So for this project I am going to 3 things
1) Read and analyse a data file
2) Do some regression analysis to check price v/s area correlation for place like Mumbai (Mumbai is a city in India)
3) Make a machine learning model which can predict price for any value for area
4) Use the model for any other dataset
5) Make an interactive model

Disclaimer! 
You can download the dataset from this repository but also from Kaggle @ https://www.kaggle.com/datasets/ruchi798/housing-prices-in-metropolitan-areas-of-india
This project is inspired by a similar project by MOSES GWAZA @ https://www.kaggle.com/code/mosesgwaza/housing-prices-prediction-in-bangalore-india

So let's get started

First thing is to get some libraries and read our dataset (In this case mumbai.csv)

![image](https://user-images.githubusercontent.com/110551323/219977548-c76f5ef8-3eb2-430b-9311-ce859a950f66.png)

We can see the data and it looks fairly without a problem.

We will get into how many different kinds of data are available
![image](https://user-images.githubusercontent.com/110551323/219977643-54959211-76e7-46c5-a76f-292f8911f141.png)

Next I checked the values and their ranges
![image](https://user-images.githubusercontent.com/110551323/219977693-f0c207b9-88d6-4d68-b0d3-a1034aea392b.png)


For the next step we will import more libraries for data analysis, visualisation and machine learning
I wil also try to clean the data (Refer the code for more info)

![image](https://user-images.githubusercontent.com/110551323/219977785-d93a3c1b-091b-4be3-87e9-c55237f216f0.png)


Now I will remove all the values which are non-numerical and check for correlations between all the different variables in the dataset

![image](https://user-images.githubusercontent.com/110551323/219977838-94522013-a134-4b26-a93b-877ea6f98656.png)

As you can see, the data is there but it can be a little difficult to visualise, so lets create a heatmap and check the correlations

![image](https://user-images.githubusercontent.com/110551323/219977894-079d5516-7d13-4bbb-b61f-1f08195f5319.png)

So the correlation between price of apartment and the area of apartment is 0.66. It is not really good, but acceptable nevertheless.

Now lets plot the values for Price v/s Area for the Mumbai dataset

![image](https://user-images.githubusercontent.com/110551323/219977960-48422db1-23e6-45a8-a893-6692721cc14a.png)

Now lets draw the regression line for it in blue

![image](https://user-images.githubusercontent.com/110551323/219977982-48ff2a87-f12a-4a1f-830d-38aaca45b662.png)


Some of the values are far too off from the line and thus can be considered as outliers. Lets try to remove the outliers and plot them

![image](https://user-images.githubusercontent.com/110551323/219978017-a4ccd672-bc59-49eb-999e-ce3555b601cf.png)


Removing the outliers will give us the following graph:
![image](https://user-images.githubusercontent.com/110551323/219978043-b6b66ab8-df36-4555-a198-d248a0523ebe.png)


Now let's train a model and define a baseline for the data! Anything or any value below the baseline can be considered as not reliable

![image](https://user-images.githubusercontent.com/110551323/219978089-87312b2a-b05b-4b32-8485-b37a686bc7ac.png)


Now its time to define the MAE (Mean Absolute error) Baseline and the regresson formula for our model y = mx + b
This is a linear regression and a very simple model at that, so we can't expect the model to be exceptionally perfect and sophisticated as the real world

WE also try to check the model by using another dataset called Delhi.csv (Data for the city of Delhi in India)

![image](https://user-images.githubusercontent.com/110551323/219978173-c4251516-599b-428f-806f-53fd7fce2b20.png)

Finally we try to make a regression analysis for the new Dataset with our new model
![image](https://user-images.githubusercontent.com/110551323/219978246-120c7225-0f00-43d8-a803-b6d00b2d9339.png)

And also at the end we make an interactive slider which can predict prices and almost any value between 245 to 7000 m2

<img width="740" alt="image" src="https://user-images.githubusercontent.com/110551323/219978308-f0d92548-9a40-48e7-bf0d-0ae41f1319bf.png">
