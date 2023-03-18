================= Header ====================
README file for running code for Assignment 2
Student name: Justin Kelley
Student ID: 997351
Subject: COMP30027 (Machine Learning) (Semester 1, 2021)
Assignment: Assignment 2
Date created: 26/04/2021
Date last modified: 15/05/2021
Runtime: About 30-35 minutes.
================= Overview ====================
The Assignment_2_Program.ipynb file contains the main code for the
assignment. This is the code that constructs the models and performs the
analysis for them, which includes providing output related
to the analysis and evaluation in the model and the predictions
made on the test set.

Moreover, the Models.ipynb file contains code to run each final model
individually quickly to get the acccuracy score and confusion matrix
for each one.
=============== Data File Locations ==================
The program uses several data files to access the training and test
data sets from. These files are:
1. recipe_test.csv
2. recipe_train.csv
These two above are located in the main code folder where the program
itself is. They need to be here for the program to run as it searches for
them here.
3. test_ingr_doc2vec50.csv
4. test_name_doc2vec50.csv
5. test_steps_doc2vec50.csv
6. train_ingr_doc2vec50.csv
7. train_name_doc2vec50.csv
8. train_steps_doc2vec50.csv
These six files above are located in the folder "recipe_text_features_doc2vec50",
which is the folder located in the main folder. These files must be located here for the code
to run as it searches for them here.
================= Directory Structure ====================
Assignment_2_Code (folder)
	- .ipynb.checkpoints (folder)
		- Assignment_2_Program-checkpoint.ipynb
		- Models-checkpoint.ipynb
	- recipe_text_features_doc2vec50 (folder)
		- test_ingr_doc2vec50.csv
		- test_name_doc2vec50.csv
		- test_steps_doc2vec50.csv
		- train_ingr_doc2vec50.csv
		- train_name_doc2vec50.csv
		- train_steps_doc2vec50.csv
	- Results (folder)
		- Assignment_2_Program_Results.pdf
		- GNB_Results.pdf
		- KNN_Results.pdf
		- Logistic_Results.pdf
	- Assignment_2_Program.ipynb
	- Models.ipynb
	- README.txt
	- recipe_test.csv
	- recipe_train.csv
	- gaussianPredictions.csv
	- KNNPredictions.csv
	- logisticPredictions.csv

================= Required imports ================================================
Make sure the following Python libraries are installed in order to run code:
1. numpy
2. statsmodels
3. pylab
4. matplotlib
5. pandas
6. datetime
7. scipy
8. sklearn

	
================= How to Run Code (Assignment_2_Program.ipynb) ====================
Each function, the imports and constant definations are each
located in their own code block. In order to run the code all
code blocks must be run in order to initialise all the imports,
constants and function definations. Also, first ensure all the imported
libraries are installed on the computer.

The last code block is used to run the program. This block contains
the defination of the function runProgram(), which will run all the code
and the function call to this function is just below the defination.
Run this code block to run the program.

This function will first process the data into training and test sets
to compute baseline and benchmark scores.

Next, several functions are run to produce output related to the
analysis of the models:
1. baseResults() produces the output of the performance of the three
models at their initial settings.
2. checkAssumptionsGaussianNB() produces output to check the indepedence and
normal distribution assumptions for Gaussian Naive Bayes.
3. studyParametersKNN() produces output to show how the performance changes for
KNN when tuning the hyperparameters.
4. featureSelectionTest() produces output of the performance of all
classifiers when using two subsets of the features.
5. generateLearningCurves() generates learning curves for each model over different
random holdout splits.
6. showResultsForEachModel() outputs the accuracy scores for each model in its
final form using cross validation.

Finally, makePredictions is run, which will use each model to make predictions
for the test set and output this as files in kaggle format.

The results (code output) for this program is located in the Results folder
in Assignment_2_Program_Results.pdf.

================= How to Run Code (Models.ipynb) ====================
This program allows each final model to be run individually to see
their accuracy score and confusion matrix.

In total there are 6 code blocks. The first 3 must be run to initialse imports, contants
and the function to process the data.

The last 3 code blocks are run to run each model. The 4th one runs logistic regression,
the 5th runs GNB and the last one runs KNN. Run any one of these individually, which have
their results located in the results folder in Logistic_Results.pdf, GNB_Results.pdf and
KNN_Results.pdf respectively.