
## My Journey in Data Science
### *WORK IN PROGRESS: NOT ALL PROJECTS HAVE BEEN UPLOADED*
## Academic Projects:
As part of the cirriculum for Data Science at the Barcelona School of Economics, I have completed a few machine learning assignments. The details and links to the repositories are below.

# 1. [Housing Prices Prediction using Linear Models](https://github.com/gnlmano/Housing-Prices-Prediction)
![](/images/housing.jpeg)
1. This is my first data science project. For this assignment, I had to use linear models to predict housing prices in 3 counties of California.
2. Coming from an Economics background, it was interesting to see the paradigm shift between Economics and Data Science. In Economics, we are highly concerned with ensuring that the assumptions of linear regression hold up. But in Data Science, the primary focus is on the predictive power of the model.
3. EDA took up most of the work. Many features seem to follow a linear relationship with the target. I polynomial-transform the data to take into account non-linearities.
4. Longitude and latitude are not linear features; doesn't make sense to use them in a linear model. I used a clustering algorithm to feed them into the model.
5. Simple models using minimal features perform best on the test set. Feature engineering to create new features and adding more features degrades performance.
6. Regarding feature importance, the best performing features are non-linear making interpretation obscure. 

---

# 2. [Forest Cover Prediction Using Logistic Regression](https://github.com/gnlmano/Forest-Cover-Prediction-Logistic-Regression) 
![](/images/header.png)
1. In this project, we were tasked with predicting the class of forest cover (the predominant kind of tree cover) from strictly cartographic and environment variables.
2. There are 2 parts to this assignment. First is a binary prediction task and the second is a multi-class prediction.
3. The logistic regression classifer works well for the binary prediction problem but over-fits in the multi-class prediction.

---

# 3. [Probability of Death Prediction using K-Nearest Neighbours](https://github.com/gnlmano/Probability-of-Death-KNN)
![](/images/mimic.png)
1.  In this project, we have to predict the probability of death of a patient that is entering an Intensive Care Unit, using K-Nearest Neighbor models.
2. The vitals of a patient are provided and additional data on comorbidities are given. Using the comorbidities data, I target encode each comorbidity to create a mortality proxy. 
3. The KNN algorithm overfits on the training data achieving a perfect classification. However, the test-sample performance is poor at around 80%. 
4. GridSearching for optimal value of K is redundant in this case as using $K = \sqrt{N}$ without tuning yields an almost perfect classifier. As KNN is a lazy algorithm, it doesn't make sense to search wide ranges of K.
5. To overcome over-fitting, I try removing redundant and highly correlated features. But this does not improve the classification. I hypothesize that the KNN algorith is not well-suited for this dataset. Using a SVM classifier without any tuning on the same pipeline yields a test-set accuracy aboe 90% (SVM repo will be uploaded soon).



