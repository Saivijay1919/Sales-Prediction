# Sales-Prediction
Supermarket has several outlets around the world&amp; we want to predict the sales.

Prediction✍ of Sales📊🌟

    UNDERSTANDING OF THE PROBLEM STATEMENT:
•	According to the quote, "Success in sales is the sum of small efforts, repeated day in & day out"
•	Let us consider a supermarket has several outlets or several stores around the world & they want us to predict the sales which they can expect.
    APPLICATION OF PREDICTING THE SALES:
•	We can tell the company what are all the challenges they may face
•	What are the brands or products which is sold the most & other such kind of things
•	This helps sales team to understand which product to sell & which product to promote & other such kind of things
•	They can also make several marketing plans(let's say that a particular product in a particular store is getting sold the most & we may find some insights from it - as of why this product is getting sold the most & this helps the company to make better marketing decisions)
    Dataset
we are having 8523 different products with 12 features.
Item_Outlet_Sales is the target variable which we are going to predict & the remaining are the feature variables.

    Categorical Features:
•	Item_Identifier : categories of different products
•	Item_Fat_Content : It tells us whether it has high fat content or low fat content or regular fat content
•	Item_Type : It tells us whether it has meat or soft drink & such kind of things
•	Outlet_Identifier : It tells us the unique ID of the outlet
•	Outlet_Size : it tells us whether it is medium,high or small in size
•	Outlet_Location_Type : It tells us whether it is tier 1 or tier 2 & such kind of things
•	Outlet_Type : It tells us whether it is supermarket or grocerry store


    Data preprocessing:
We can observe that we are having 1463 missing values in the Item_Weight column & we are having about 2410 missing values in the Outlet_Size column

IN ORDER TO DEAL WITH THE MISSING VALUES

Mean --> average
•	The Mean value of a dataset is the average value i.e. a number around which a whole data is spread out. All values used in calculating the average are weighted equally when defining the Mean
•	In this case, in order to convert the missing values in the numerical column, we use mean of that particular column
Mode --> most repeated value
•	The mode is the value that appears most frequently in a data set. A set of data may have one mode, more than one mode, or no mode at all.The mode can be the same value as the mean and/or median, but this is usually not the case.
•	In this case, in order to convert the missing values in the categorical feature, we use the mode of that particular column
•	# filling the missing values in "Outlet_Size" column with Mode
•	#Here we take Outlet_Size column & Outlet_Type column since they are correlated

From the above pivot table, we can observe that
•	If the outlet type is Grocery Store in most of the cases the outlet size(mode) is Small
•	If the outlet type is Supermarket Type1 in most of the cases the outlet size(mode) is Small
•	If the outlet type is Supermarket Type2 in most of the cases the outlet size(mode) is Medium
•	If the outlet type is Supermarket Type3 in most of the cases the outlet size(mode) is Medium.

    DATA VISUALIZATION
•	Data visualization is the graphical representation of information and data.
•	It enables decision makers to see analytics presented visually, so they can grasp difficult concepts or identify new patterns.

    Data Pre-processing:
In Item_Fat_Content feature having similar meaning words  LF/low fat == Low Fat. Reg== Regular.  Ex: Low Fat 5089 Regular 2889 LF 316 reg 117 low fat 112


    LABEL ENCODING:
•	Label Encoding refers to the convertion of the labels into a numeric form so as to convert them into the machine-readable form. Machine learning algorithms can then decide in a better way how those labels must be operated. It is an important pre-processing step for the structured dataset in supervised learning.
•	In simple terms, taking all the categorical values & transforming them into some numerical values.

    MACHINE LEARNING MODEL

SUPERVISED LEARNING:
•	It is defined by its use of labeled datasets to train algorithms that to classify data or predict outcomes accurately.
•	Basically supervised learning is when we teach or train the machine using data that is well labeled.
•	In this particular project, the labels are the target which is more precise.
•	In this case the targets are sales amount
REGRESSION:
•	Regression means predicting a particular value especially continuous value (i.e.sales)
•	MACHINE LEARNING MODEL TRAINING - XGBoost Regressor
•	Extreme Gradient Boosting (XGBoost) is an open-source library that provides an efficient and effective implementation of the gradient boosting algorithm.XGBoost is an efficient implementation of gradient boosting that can be used for regression predictive modeling.

    EVALUATION
•	The R2 score is a very important metric that is used to evaluate the performance of a regression-based machine learning model. It is pronounced as R squared and is also known as the coefficient of determination. It works by measuring the amount of variance in the predictions explained by the dataset.






