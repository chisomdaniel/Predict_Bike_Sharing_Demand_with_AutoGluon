# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Chinweze Chukwusom Daniel

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
While trying to submit my prediction, it was noted that kaggle doesn't accept scores less than zero, so I had to write a few code lines to change any negatuve value in the output to 0.

### What was the top ranked model that performed?
The top ranking model was WeightedEnsemble_L2

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
After performing a little analysis on the data, I found that the `seasons` ans `weather` column were both of int datatypes, but in reality they are int representations of a category, so in a bid to add more features, I converted the two tables to have a datatype of `category`. I also converted the datetime column to a `datetime` datatype and separated each `day`, `month`, `year`, `second`, `minute`, `hour`

### How much better did your model preform after adding additional features and why do you think that is?
After adding additional features, the model performance increased by almost 40%, and I think this is because the addition of new features increased the training parameters and in turn giving the model a wider scope to learn from

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
In trying different parameters, there was just a little difference in the model's performance

### If you were given more time with this dataset, where do you think you would spend more time?
I would spend more time understanding how each hyperparameter significantly affect the performance of the model and tuning the model to different hyperparameter condition.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|Default|Default|Default|1.79306|
|add_features|Default|Default|Default|0.68128|
|hpo|eta=0.1|max_depth=12|no_of_tress=Default|0.55895|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](model_test_score.png)

## Summary
Overall, this project was a good guide to put into practice the skill and knowledge I've gotten so far in this course.
