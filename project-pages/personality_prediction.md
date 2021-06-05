## MBTI Personality Type Prediction Project
## Course: MA415/CSSE415 - Machine Learning
*Completed in Spring 2020-21*

**Please note that I cannot share the source code for this course project due to academic integrity regulations at Rose-Hulman.**

### Project Description
The Myers-Briggs Type Indicator (MBTI) is a personality test designed to categorize human personalities along 4 distinct dimensions. This test has been widely used by company HR divisions, marketers & advertisers, teambuilders and leaders, and many others to gauge people’s personality type and resulting interaction style. Therefore, because this personality type classification has so many practical applications, there is great value in accurately predicting the personality type of a team member, a product consumer, or a potential job hire. 

Social media posts are one common form of information that is readily available and may contain hints as to which personality type a specific person falls under. These posts can then be converted into features for training machine learning models and can be used to train models such as random forest classifiers, K nearest neighbors classifiers, gradient boosting classifiers, and more. In this project, various data preprocessing techniques (TF-IDF, word embeddings, PCA, balancing) and machine learning models are used to turn social media posts from the website Personality Cafe into predictors of the poster's MBTI personality type. 

The full project report, including visualizations, main results, and discussion about relevant literature, can be found here: https://docs.google.com/document/d/1u8Iz6o_5lyCMQ3q4EyRMeesOFM6iRW4vZpbn8MYmI08/edit?usp=sharing

### My Contribution
For this project, I worked on the majority of the data pre-processing stages after the data were converted from raw post text to TF-IDF and word embeddings. Specifically, I performed Principal Component Analysis (PCA) on both sets of extracted features to select only the most relevant ones. I also balanced the dataset, which was heavily skewed due to the uneven distribution of personality types, by randomly selecting a subset of all data rows for each personality type such that each type ended up with the same number of corresponding rows as the least common personality type (which still provided nearly 20,000 rows for each of 16 personality types, due to the size of the dataset). I chose to select a subset instead of bootstrapping the less common types due to the size of the dataset; training time was a significant cost due to the very large size of the dataset and our limited access to computing resources, meaning that we were willing to sacrifice some data in exchange for a large increase in efficiency. 

I also trained and evaluated many different machine learning models. Specifically, I trained the logistic regressor, random forest, and gradient boosting trees models. I also optimized for hyper-parameters where applicable; for example, I determined the optimal tree depth and number of trees for the random forest, and the optimal learning rate and number of trees for the gradient boosting trees, by using grid search cross-validation on the training dataset. 

Finally, I also helped to write a large portion of the final report (linked in the project description), including the introduction, model descriptions, reporting results, and discussion. I also reviewed external papers (cited at the end of the final report) which described recent research in similar areas related to personality type prediction and feature extraction from social media posts. 

### Technical Architecture and Tools Used
*Programming Languages and Tools* <br>
Python - All code was written using Python in Jupyter Notebooks. Many Python libraries were used for data exploration & preprocessing and machine learning model implementations, including Pandas, Scikit-Learn, and Matplotlib. <br>
Jupyter Notebooks - All code was written in Python using Jupyter Notebooks. The notebooks were mostly run on remote servers, due to the high demands on computation power required to handle a dataset as large as ours (tens of gigabytes).
