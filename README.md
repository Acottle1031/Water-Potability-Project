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


