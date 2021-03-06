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

![Project2Kmeans](https://user-images.githubusercontent.com/103547154/178723546-d2fb5334-bd83-4eda-9d62-dc0d9e2a0915.png)


This KMeans bar graph of mean values of our clusters shows that there are very little differences in the averages of our analytical columns. With the knowledge that this data set is synthetic, it's not too surprising but, with the context of our Kernal Density plot above, we can see that some values are more prevalent, such as the distribution of the "Sulfates" column. 

## Modeling Method Decision
Based on my observations of the metrics for our models, and knowing that our data is slightly unbalanced in the favor of Non-Potable water, I honestly would not be able to faithfully put any of these models into real world production. With that said, if I was forced to choose, I would chose our "Tuned KNN" model, without PCA, to put into production. I choose this based off of two general factors. Firstly, it had the highest accuracy when it came to predicting our testing data, at 66% correctly predicted values. Secondly, it had the best precision score at 0.61, which is the highest of our other precision scores. The reason I choose to base off of both accuracy and precision is due to the fact that, we need our model to be accurate, and while 66% isn't really the best, it is the highest performing of the other models. Also, with precision being a score that shows how accurately we can predict our true values while punishing false positives, and the nature of our data being very important to human health, we want to punish false positives as much as possible (as people can be seriously harmed by drinking tainted water). For reference we were able to bring our precentage of false positives down to 11% with 66% accuracy.

As a note, it's very possible that with further feature engineering, or maybe datetime data or location data these models could potentially be extremely good! Going forward I would recommend to anyone collecting water samples for potability testing to also include that type of information as well. As depending on where/when these water samples were collected the values may vary wildly. That way we may find more connections between these features and make better recommendations for how we might combat the problem of clean water across the globe.


## Contact
All feedback on my code is appreciated. Feel free to reach out to me at: a.cottle1031@gmail.com 
