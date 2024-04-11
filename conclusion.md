# Project_4_Group_9
Project 4

conclusion:

**From the Geomap:**
The more progressive states have a lower percentage diabetes compare to conservative 
-overall, trend for most age groups is positive with the exception of the younger age groups(18-44).
-trend is the people who have less than a high school degree have seen the most increased in diabetes.


**From relationships between variables:**
-Using pairplots on the variables in relation to diabetes, didn't exhibit clear relationships. 
Using a correlation heatmap highlighted a few more-highly correlated.
-Features that were most correlated with Diabetes included GenHlth, HighBP, BMI, and DiffWalk compared to other attributes. Scaling did not influence pairplots or correlation, as expected.

**From Statistical result:**
-Optimization plays a crucial role in machine learning. We were able to retrieve more robust results by utilizing techniques such as 
    1) Balancing Class Distributions (e.g., reducing the number of instances in the majority class) 
    2) Standard Scaling 
    3) Categorical Encoding (e.g., converting diabetes types into binary values).
-The overall accuracy of the model is 0.75, with precision of 0.76 for class 0 and 0.74 for class 1. Recall for class 0 is 0.74, and 0.77 for class 1. F1-score for class 0 is 0.75, and for class 1, it's 0.76.
-The evaluation indicates that the model performs reasonably well in distinguishing between individuals with and without diabetes, with fairly balanced precision and recall for both classes. However, it's essential to note that without additional context, it's challenging to fully assess the model's performance.


**From Supervised Learning:**
random forest has very similar accuracy with logistic regression model, decision tree model has the lowest accuracy among this 3 models. based on importance of features, BMI, High blod pressure, and High cholestrol have the most influences to the random forest model.


**From the neural network:**
3 different type of results,we get about 86% accuracy for analysing the non diabetes , type 1 diabetes and type 2 diabetes.
considering the accuracy the model at the network model is working, however, we still need to predict the actual results in the future.


**compare supervised learning vs neural network:**
supervised learning is more difficult to analyse model with more than 2 results. in this project neural network has easier assessment on the model that more than two results.


Overall,
we have Logistic Regression with 76% accuracy in predicting type-2 diabetes
Also, Random Forest with 75% accuracy in predicting type-2 diabetes.
BMI, High blood pressure and High cholesterol have the most influences in random forest model
and Neural network (Highest Accuracy) with 86% accuracy in predicting type-2 diabetes.
