# death-row-last-words

I used a dataset of the last words of inmates sentenced to death in the state of Florida to categorize certain inmates as claiming to be
innocent up until their death. After reading many statements, I chose to search for certain words and phrases within the dataset that could
determine whether the inmate claimed to be innocent. Examples of terms included in my search terms were: "did not do", "innocent", "did not 
murder", and "truth".

The goal of this project was to find any patterns that could be used to predict whether an inmate claimed to be innocent. The dataset
included information such as the race of the victim, the race of the inmate, the age of the inmate, education level, and previous crimes.

Due to the fact that there was a huge class imbalance between proclaimed innocent inmates and not, I used SMOTE to resample my data and 
create synthetic datapoints. I ran a decision tree after resampling the data using sklearn, then tuned and pruned my tree using a
validation curve, gridsearch, and randomforest. 

To determine the strongest indicators of proclaimed innocence, I used feature selection to score each feature of my model. The number one
feature in both my decision tree and feature selection ended up being whether the victim was white. In addition to this, I ran a correlation
on each of the features in the dataset to compare the most important correlators with innocence, and a feature importance. 

Lastly, I implemented AdaBoost and K Nearest Neighbors to possibly obtain a more accurate model.


