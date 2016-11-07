# Project 2: Supervised Learning
## Notes on each classifier

### Why?

We are asked to chose three learning models from scikit-learn that might help us classify students as failing or not.
The list of potential choices is as follows.

- Gaussian Naive Bayes (GaussianNB)
- Decision Trees
- Ensemble Methods (Bagging, AdaBoost, Random Forest, Gradient Boosting)
- K-Nearest Neighbors (KNeighbors)
- Stochastic Gradient Descent (SGDC)
- Support Vector Machines (SVM)
- Logistic Regression

I will take notes on the pros/cons of each of these in relation to our data set so I can properly chose.

### The Dataset

Some info on the dataset:

- Total number of students: 395
- Number of features: 30
- Number of students who passed: 265
- Number of students who failed: 130
- Graduation rate of the class: 67.09%

We are constricted to samples of 100, 200, and 300 students by the setup of the problem.

In general we can say this dataset is fairly small and has a high number of features relative to the amount of data. The total count and this ratio will be important in our decision making.

## The Classifiers/Learners

Drop some links/decision trees here as needed.
1. http://scikit-learn.org/stable/tutorial/machine_learning_map/
2. http://scikit-learn.org/stable/auto_examples/classification/plot_classifier_comparison.html#sphx-glr-auto-examples-classification-plot-classifier-comparison-py


## Gaussian Naive Bayes (GaussianNB)







## Decision Trees
  - http://scikit-learn.org/stable/modules/tree.html
  - PROS:
    - simple and can be visualized/interpreted
    - data doesn't have to be normalized as often
    - cost of using is low (unimportant for us)
    - handles multiple types of data
  - CONS:
    - prone to overfit at times
    - can be unstable because small data variations can cause very different trees to come out
      - using an ensemble method protects against this

  in general this seems like a solid approach. it worked well for titanic data which was bigger but only one order of magnitude away. potentially using the ensemble method would be nice?


## Ensemble Methods (Bagging, AdaBoost, Random Forest, Gradient Boosting)

  - http://scikit-learn.org/stable/modules/ensemble.html

  What is each of these? Brief explainer:
  - Bagging:
    - averaging the outputs of various models
      to create a new output with low variance and
      low overfitting
  - Random Forest:
    - Bagging with a bunch of decision trees
    - Each tree will cast a vote for a model
  - Gradient Boosting:
    -
  - Adaptive Boosting (AdaBoost):
    - iteratively re-fit submodules (boosting !== bagging)

  PROS:
    - max_features can cut down our dimensionality
    - big advantage not overfitting... but we dont really
      need to run on tons of data sinc our N is low
  CONS:






## K-Nearest Neighbors (KNeighbors)
  - http://scikit-learn.org/stable/modules/neighbors.html
  - http://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html
  - https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm

  PROS:
    - simple
    - should be good with a low N
  CONS:
    - needs to remember data: unimportant in this case
    - The accuracy of the k-NN algorithm can be severely degraded by the presence of noisy or irrelevant features (from wikipedia)
      - would probably need some dimensionality reduction in our case

## Stochastic Gradient Descent (SGDC)

  - http://scikit-learn.org/stable/modules/sgd.html
  - PROS:
    - Efficiency (unimportant for us)
    - Ease if implementation
  - CONS:
    - needs a number of hyperparameters
    - sensitive to feature scaling (we'd need to play with our data more, and this would introduce more chances for error_

  This probably isn't great because simplicity and efficiency are the two best features, but we don't seem to need these at this scale.





## Support Vector Machines (SVM/SVC)

Link one above immediately points us in the direction of Linear SVC for small sample sizes (under 100K).
It tries to fall back onto K Nearest Neighbors then SVC with emsemble learning if that fails.





## Logistic Regression

