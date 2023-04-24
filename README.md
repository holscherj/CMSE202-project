# Crash Course: Predicting Accident Severity with Machine Learning Models
## Authors: Jack Holscher, Susan Lin
## CMSE202-004 SS23 


## Abstract
### In this project, we aim to answer the following question: Can we predict the severity of a car accident given various factors such as time day, weather conditions, location, and more?

### We set out to answer this question armed with resources from a number of different python modules, such as pandas, numpy, matplotlib, seaborn, sklearn, statsmodels, and more.

### We construct two different machine learning models, an ordinary least squares regression model, and a support vector machine

### Each designed with the same goal in mind, we compare the two and their various performance metrics such as precision, recall, and accuracy in order to find the most efficient model for answering our question.


## Contributions
### Susan and I both worked very diligently on this project. We worked together very well and communicated every step of the way. In my opinion, I think we divided up the overall workload pretty effectively.

### Jack: Personally, I worked on the bulk of cleaning the data, and building and evaluating the models. I also wrote this markdown file and contributed to the presentation.

### Susan: Susan carried all the work visualizing and analyzing the data and some initial features that were of interest. She also completed the bulk of our presentation.


## Instructions for Running the Notebook

### Disclaimer: The dataset that we worked with for the regression model is very large. After we dropped 2 of the 7 years it contained, it still sits at just over 1 GB of information. Running the entire notebook in one go takes an estimated 10-15 minutes. Cells that take a particularly large amount of time will indicated here and in the comments of the cell.

### Run the cells from top to bottom, starting with the necessary imports. From there it is pretty self-explanatory.

### The first cell that's going to take a minute or two to run is the second one. This cell is responsible for dropping the two oldest years in the dataset, and writing the results to a new CSV file. I had to do this with python since the dataset is too large to open in a CSV editor like Excel.

### The next cell that is a little slower is the following one, cell number three. This is just reading the dataset into a DataFrame object, and shouldn't take as long as cell two.

### The rest of the cells for cleaning, visualizing, and building the regression model should run quickly. The next cell of interest is number twenty-nine. This is where we perform the GridSearch to tune the hyperparameters for the SVM model. Right now, it is completely commented out since it really only needed to be run once in order to obtain the parameters. Upon running it the first time, it gave me the following results: C= 0.01, gamma = 0.01, kernel = 'linear.' Feel free to run the cell yourself to see the results, it should take around 5-7 minutes

### The last time-consuming cell is number thirty-two. This is the cell that fits the model and evaluates it 100 different times. It is most likely the most time-consuming cell in the notebook, so feel free to lower the number of iterations for testing purposes. This is easily done by lower the 225 in line 65 (... in range(124, 225))  to something along the lines of 150
