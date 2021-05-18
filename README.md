The dataset has 10,000 rows and provides the weight, height and gender of the person. I have try to build and train a model on this dataset so it can predict the weight of a person given their gender and height. This is the first project that I'm working on that has a large dataset. 

Step-3:
Before we run any machine learning models, we have to convert all categorical values (text values) to numerical values. In our dataset, we can see that we have one field — “Gender” which is categorical. So we have to convert this field into numerical.

The typical way of converting categorical values to numerical is by using the LabelEncoder class to convert Text to Numbers and then using OneHotEncoder to add dummy variables.
But this is useful only if the categorical field contains more than 2 values — for instance, let’s say we have a field called “City” and it contains more than 2 values like “Houston”, “New York” and “San Francisco”.
In this case, we will first use LabelEncoder to convert the cities to numbers like: “Houston” => 0 and “New York” => 1 and “San Francisco” => 2.
Then we will use OneHotEncoder to add 3 dummy variables one for each city. Finally, we will drop one dummy variable to avoid the dummy variable trap.
