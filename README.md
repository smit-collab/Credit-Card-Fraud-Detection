# Credit-Card-Fraud-Detection

### About:
Credit card fraud is when someone uses your credit card or credit account to make a purchase you didn't authorize. Credit card fraud is a fraud committed using a payment card, such as a credit card  as a fraudulent source of funds in a transaction.

### Dataset:
The dataset is obtained from the kaggle.Total transactions given in the data are 284807 and we have to predict which ones are fraudelent. So we will only take 50% of the data to save on time and computation.

### Summary:
Mainly I have important algorithms to find the accuracy of the model:
a.) local outlier factor to calculate anomaly scores
b.) isolation algorithms.

There are total 31 columns and V1 to V28 are result of PCA dimensonality reduction which is ued to protect sensitive info of the card in the dataset so the identity,location dosen't get exposed of the user. Class 0 means valid normal card transaction and if class is 1 then it means fraudelent transaction.
While describing the data we also observe that the min is 0 and mean is close to 0 meaning we have more valid transactions compared to fraudlent ones which is shown in the chart of transaction class distribution.



The libraries used are :
 sys
 numpy 
 pandas 
 matplotlib.pyplot 
 seaborn 
 scipy
 sklearn


### Observations:
1. from the chart of histograms we can observe that most of the V's are clustered near 0 with some of the outliers present or no outliers. If we observe the class chart we can see there many valid transactions and very few fraudulent ones.

2. A number of fraud cases from the dataset are 147 and the number of valid Cases is 85295 and the outlier fraction is 17.

3. Furthermore observing the correlation chart we can see that most of the V's are unrelated and we have a lot of values close to the zero. Carefully observing the class we can see that there are some variations in the parameter and the lighter ones are positive correlation and darker ones are negative correlation. So v17 is a stronger negative correlation and like that we can observe other correlation coefficients. Also, there isn't any strong correlation btw amounts and whether or not it was fraudulence or time.

4. in In isolation forest we had 99.6% accuracy and 191 errors and precision of 35% which is a lot better.so only 35% actually    fraudulent cases were identified. So 35% of the time we can find out if the transaction was fraudulent or not.

5. So we observe that the local outlier factor classifier gave 293 errors and 99.66% accuracy. 
When we look at the precision, recall and f1 score we see that for class 0 we had the precision of 100%  but for class 1 we had really bad precision meaning actual fraudulent cases were not being labeled as we thought so. Meaning false positive and false negative were not good at all.
