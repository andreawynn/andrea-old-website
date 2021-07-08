## Stock Market Prediction - Independent Data Science Project
*Note: This project is still undergoing ongoing improvements. All project code and files can be found <a href="https://github.com/andrea-00/stock-market-prediction">here</a>.*

### Project Description
The stock market is highly volatile, with billions of dollars made and lost each day through trades. The stock market can be highly lucrative to those who can predict it well; however, predicting the price of a stock is an exceptionally challenging problem. <br>

In this independent project, I decided to apply my knowledge of machine learning and data science techniques to train models for predicting the prices of a few specific stocks. Notes on the specific techniques I used can be found in the section below. <br>

All source code for this project can be found <a href="https://github.com/andrea-00/stock-market-prediction">here</a> on GitHub. 

### Tools and Techniques Used
*Version Control* <br>
I posted all code for this project <a href="https://github.com/andrea-00/stock-market-prediction">in this GitHub repository</a> with regular commits after every major change. I am the sole contributor for this project. 

*Programming Languages and Tools* <br>
Python - I used Python and various Python libraries (listed below) to write all the code for the project. <br>
Jupyter Notebooks - I used Jupyter Notebooks for all coding throughout this project. All code files are in the .ipynb format (Jupyter Notebooks / Google Colab). <br>

*Libraries Used* <br>
Pandas & NumPy - I used Pandas and NumPy for storing and manipulating data, as well as for providing data to models for training. <br>
plotly - I used plotly for data visualization after performing predictions, to visualize the accuracy of my results as compared to the true stock prices. <br>
sklearn (Scikit-Learn) - I used Scikit-Learn for all the machine learning models and a number of data processing tools that I used throughout the project. <br>
yfinance (Yahoo Finance) - I used the yfinance package for pulling data on various stocks to use for training and validation data. <br>
fastai, ta - I used the fastai and ta libraries to process and add some features to the dataset. <br>

*Data Processing Techniques* <br>
Scaling - Used StandardScaler to scale training data to have a mean of 0 and standard deviation 1. Applied same scaling to both training and validation features.

*Machine Learning Models* <br>
Linear Regression - Used linear regression (from Scikit-Learn) to establish a baseline accuracy against which other models would be compared. R^2 value for predictions 1 day out was approximately 0.9873 for AMZN stock. <br>
Artificial Neural Network - Trained a neural network (MLPRegressor from Scikit-Learn) using the identity activation function, hidden layer size 100, adaptive learning rate, and 10000 maximum iterations. R^2 value for predictions 10 days out was approximately -58.231 for AMZN stock (this was the highest R^2 of the shifts tested). 

### Ideas for Continued Improvement
Following is a non-exhaustive running list of potential improvements and new things to try in the project. 
- Add Lasso or Ridge regularization
- Add Principal Component Analysis
- Test predictions on a wider variety of different stocks
- Test models on post-COVID stocks
- Implement a floor on model predictions that prevents predictions from going negative
- Hyper-parameter optimization, using GridSearchCV, RandomSearchCV, or some other method
- Try additional ML models: decision trees, random forests, gradient boosting, support vector machines (SVM)
