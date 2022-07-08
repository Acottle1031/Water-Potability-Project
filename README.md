# **Water-Potability-Project**
## Attempting to predict potability of water

**Author**: Austin Cottle

### **Business problem**:

My goal here is to do my best to create a model capable of accurately predicting the potability (whether or not water is drinkable) of water samples. 


### Data 
Source: https://www.kaggle.com/datasets/adityakadiwal/water-potability

This data set includes information regarding the present values of different elements in our water. Including Ph, Hardness, Solids, Chloramines, Sulfates, Conductivity, Organic Carbon, and Trihalomethanes. Also including our target feature, Potability. Descriptions of all features available in Data Dictionary.

## Analysis

#### Distribution of Potability in data

![image](https://user-images.githubusercontent.com/103547154/177974125-423da11a-c696-414a-b60d-fb1dcf331436.png)

This histogram shows us the distribution of "Potable" vs "Non-Potable" water. We can see that we have 2000 values in favor of "Non-Potable" and 1300 values in favor of "Potable" which shows us that our data is slightly unbalanced in favor of "Non-Potable" values. 


#### Distribution of Features by "Potability" 
![download](https://user-images.githubusercontent.com/103547154/177975361-318f70a5-533e-4470-8cba-4350293454e7.png)

This Kernel Density Plot shows us that our "Non-Potable" water shares very similar values in it's features as our "Potable" water. With this being the case, I'd assume we'll have little luck determining meaningful relationships between features to our potability.


#### How Our Features Interact:

**note:** I have a parallel coordinates plot via plotly in my code but am having issues figuring out how get this to upload as an interactive chart, I will do my best to research and submit ASAP, just so you're able to see if you'd like, if the code is opened in an .ipynb file it should be available. 

## Modeling Method Decision
Based on my observations of the metrics for our models, and knowing that our data is slightly unbalanced in the favor of Non-Potable water, I honestly would not be able to faithfully put any of these models into real world production. With that said, if I was forced to choose, I would chose our "Tuned KNN" model, without PCA, to put into production. I choose this based off of two general factors. Firstly, it had the highest accuracy when it came to predicting our testing data, at 66% correctly predicted values. Secondly, it had the best precision score at 0.61, which is the highest of our other precision scores. The reason I choose to base off of both accuracy and precision is due to the fact that, we need our model to be accurate, and while 66% isn't really the best, it is the highest performing of the other models. Also, with precision being a score that shows how accurately we can predict our true values while punishing false positives, and the nature of our data being very important to human health, we want to punish false positives as much as possible (as people can be seriously harmed by drinking tainted water). For reference we were able to bring our precentage of false positives down to 11% with 66% accuracy.

As a note, it's very possible that with further feature engineering, or maybe datetime data or location data these models could potentially be extremely good! Going forward I would recommend to anyone collecting water samples for potability testing to also include that type of information as well. As depending on where/when these water samples were collected the values may vary wildly. That way we may find more connections between these features and make better recommendations for how we might combat the problem of clean water across the globe.
