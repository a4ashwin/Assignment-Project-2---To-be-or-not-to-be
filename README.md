# Assignment-Project-2---To-be-or-not-to-be
 2nd assignment of EECS 731 Intro to Data Science - To be or not to be

 Prerequisites
 Anaconda, Python 3.7.3, Jupyter Notebook, Pandas Library

 Introduction:
 In this project, we are going to transform the dataset of dialogues in Shakespeare's plays by using feature engineering. We are going to transform the dataset into a new dataset that has the meaningful data to make predictions using different model. We are going to predict the player in the dataset using the rest of the columns. The process includes dropping of features, changing the datatypes, concatenating features, training the models, testing the models, printing the overall accuracy and precision etc. We have Dataline, Line, ActSceneLine, PlayerLinenumber and PlayerLine as features in the dataset.

 Idea:
 To predict the player as an output from the dataset, we need to transform the dataset into a meaningful one for the same. Firstly, we drop the rows with empty values as it they won't help in predicting the player. we split the feature ActSceneLine in 3 different features viz Act, Scene and Line because Act and Scene are important in predicting the player but Line doesn't matter as it is not fixed that which line is given to which player. After that we drop columns- Dataline, Line, ActSceneLine, PlayerLinenumber and PlayerLine because these columns are not providing any relevant information regarding the player. Dataline has the indexes only, Line and PlayerLinenumber are not creating any pattern, ActSceneLine has been splitted and PlayerLines are all different as there is negligible possibility that a character in a play says same line in same play or another play. Now we Concatenate Play, Act and Scene as a single feature because a player has high chance of saying lines in the same scene of an act of a play then saying it in different plays in same act or scene. Then we convert this column into dummy numerical values to feed in to the model and evaluate it.

 Process:
 - Download the data from www.Kaggle.com
 - Load the dataset into Pandas dataframe
 - Splitted ActSceneLine into 3 columns i.e. Act, Scene and ActSceneLine
 - Drop Dataline, Line, ActSceneLine, PlayerLinenumber and PlayerLine
 - Convert Act and Scene to string
 - Concatenate Play, Act and Scene in single column and drop the individual columns
 - Encode the PlayActScene in to numbers using LabelEncoder
 - Split the dataset in training and test data for 10-fold cross validation
 - Train the models
 - Predict the output
 - Compare with original output
 - Print Accuracy, precision and other paramaters of predictions

 Result:
 For Naive Bayes classification model, before using feature engineering and exploratory data analysis, we were getting an accuracy of around 19% and precsion of 19.5% and after transforming the data, we got accuracy and precision around 17% which is a decrease in the prediction. However, while using KNeighbors classification model, before using feature engineering and exploratory data analysis, we were getting an accuracy of around 19% and precsion of 19% and after transforming the data, we got accuracy and precision around 37% in the prediction which is almost double.


 Built With:
 Jupyter Notebook
 Python 3.7.3
 Pandas

 Authors:
 Ashwin Rathore

 License:
 This project is created for Course EECS 731 Assignment for University of Kansas.

 Acknowledgments
 https://www.kaggle.com/kingburrito666/shakespeare-plays
