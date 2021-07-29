## Ensembles and Random Forests

An <i>Ensemble</i> is a group of classifiers and we aggregate the predictions of these classifiers. This technique is called <i>Ensemble learning</i>. First, individual classifiers make their predictions, then the class is predicted that gets the most votes.

A <i>Random Forest</i> is an Ensemble of Decision Tree Classifiers.

<b>Hard Voting</b>: Aggregating the predictions of each classifier and predict the class that gets the most votes.

#### Bagging, Pasting:
Same training algorithm is used for every predictor and train them on different random subsets of the training set. If sampling is performed with replacement, this method is called <i>Bagging</i> and if the sampling is performed without, it is called <i>Pasting</i>.

#### Random Forests:
A Random Forest is an ensemble of Decision Trees, generally trained via the bagging method, with maximum sample size equal to size of training set.

#### Boosting:
AdaBoost is an Ensemble method that combines several weak learners into a strong learner. The predictors are trained sequentially where each predictor tries to correct its predecessors. <i>AdaBoost</i> (Adaptive Boosting) and <i>Gradient Boosting</i> are two of the boosting methods.
The first classifier gets many instances wrong, so their weights get boosted. The second classifier therefore does a better job on these instances and so on. Once all predictors are trained, the ensemble makes predictions like <i> bagging</i> or <i>pasting</i>.

##### AdaBoost:
AdaBoost works by sequentially adding predictors to an ensemble. This algorithm first trains a base classifier and uses to make prediction on the training set. It then increases the relative weight of misclassifed training instances. Then it trains a second classifier, using the updated weights, and again makes predictions on the training set, updates the instance weights, and so on.

##### Gradient Boosting:
Gradient Boosting works by sequentially adding predictors to an ensemble, each one correcting its predecessor. However, instead of tweaking the weights at every iteration like AdaBoost, it tries to fit the new predictor to the residual errors made by the previous predictor.
