# ml_weekly_2018.md
https://paper.dropbox.com/doc/UQ-ML-Reading-Group-Schedule-O0e6GrWgdFS7dqZ49wFFZ

## Mar 9, 2018: Model selection
* Structural Risk Minimization (SRM) paradigm
  * While the SRM approach can be useful in some situations, in many practical
    cases the upper bound given in Equation (11.2) is pessimistic.
* Validation:
  * hold out set:
    * Sampling a training set and then sampling an independent validation set is
      equivalent to randomly partitioning our random set of examples into two parts,
      using one part for training and the other one for validation.
  * Validation for Model Selection
    * train different algorithms (or the same algorithm with different parameters) on the given training set. 
    * to choose a single predictor from H we sample a fresh validation set and 
      choose the predictor that minimizes the error over the validation set. 
      In other words, we apply ERMH over the validation set.
  * Model-Selection Curve
    * shows the training error and validation error as a function of the complexity of the model considered. 
  * k-Fold Cross Validation
    * special case k = m, where m is the number of examples, is called leave-one-out (LOO).
    * k-Fold cross validation is often used for model selection (or parameter tuning),
      and once the best parameter is chosen, the algorithm is retrained using this parameter on the entire training set. 
  * Train-Validation-Test Split
    * The first set is used for training our algorithm and 
    * the second is used as a validation set for model selection. 
    * After we select the best model, we test the performance of the output predictor on the third set, 
      which is often called the “test set.”
* What to Do If Learning Fails
  * recall:  ch5: the true error of the learned predictor is decompsed into approximation error and estimation error. 
  * The approximation error of the class does not depend on the sample size or on the algorithm being used
  * consider applying the same hypothesis class but on a different feature representation of the data
  * (LV (hS ) − LS (hS )), is large we say that our algorithm suffers from “overfitting” while 
  * when the empirical risk term, LS (hS ), is large we say that our algorithm suffers from “underfitting.”
  * Learning Curves
    * To produce a learning curve we train the algorithm on prefixes of the data of increasing sizes. 
    * For each prefix we calculate the training error (on the prefix the algorithm is being trained on)
      and the validation error (on a predefined validation set). 
    * If we see that the validation error is starting to decrease then 
      * the best solution is to increase the number of examples (if we can afford to enlarge the data). 
      * Another reasonable solution is to decrease the complexity of the hypothesis class.
    * if we see that the validation error is kept around 1/2 then 
      * we have no evidence that the approximation error of H is good. 
      * It may be the case that increasing the training set size will not help us at all. 
      * Obtaining more data can still help us, as at some point we can see whether 
        the validation error starts to decrease or whether the training error starts to increase.
    * summary: 
      1. If learning involves parameter tuning, plot the model-selection curve to make
         sure that you tuned the parameters appropriately (see Section 11.2.3).
      2. If the training error is excessively large consider enlarging the hypothesis class,
         completely change it, or change the feature representation of the data.
      3. If the training error is small, plot learning curves and try to deduce from them
         whether the problem is estimation error or approximation error.
      4. If the approximation error seems to be small enough, try to obtain more data.
         If this is not possible, consider reducing the complexity of the hypothesis class.
      5. If the approximation error seems to be large as well, try to change the hypothesis class or 
         the feature representation of the data completely.
  
* machine learning from statistics/math vs computerscience perspective
  * in stat/math: we make assumption about underlying distribution
  
## Mar 2, 2018: Boosting (not attended)
* Adaboost algorithm can also be viewed as a “special” form of projected gradient descent, 
  called mirror descent with projection done on the space of probability simplex. 
  This algorithm is also known by another name, i.e., multiplicative weight update.
* See Section 4.3 of https://arxiv.org/pdf/1405.4980.pdf , 
  * the “Simplex setup” where the gradient is done on the negative entropy mirror map followed by simple normalization. 
  * This is identical to Adaboost algorithm in the book on page 135, i.e., 
  x in https://arxiv.org/pdf/1405.4980.pdf is D in the book.

## Feb 23, 2018: Linear Predictors
* $sign(w^t x + b)$
  * b is bias, can be a feature too, so we have $sign(w^t x + b)$
* design matrix
* for separable traning sets linearly, it is a linear programming
* half-space is defined by:
  * a vector w=(w_1, \dots, w_n) and a threshold b as follows:
    if \sum_{i=1}^n w_i x_i > b then \ell(x)=1, else \ell(x)=0
    * https://cs7545.wordpress.com/2015/02/26/notes-0219-learning-halfspace/
  * A half-space is said to be homogeneous if the hyperplane that defines it contains the origin;
    * https://cs.stackexchange.com/questions/50707/what-is-a-homogenous-half-space
  *  The VC dimension of the class of homogenous halfspaces in R^d is d.
* batch perceptron alg
* least square with L2 loss (MSE)
* linear refression for polynomial regression tasks
* cross entropy, CE:
  * In information theory, the cross entropy between two probability distributions {\displaystyle p} p and {\displaystyle q} q over the same underlying set of events measures the average number of bits needed to identify an event drawn from the set, if a coding scheme is used that is optimized for an "unnatural" probability distribution {\displaystyle q} q, rather than the "true" distribution {\displaystyle p} p.

## Feb 16, 2018: Review ch 1 to 6
* understanding ML book:
http://www.cs.huji.ac.il/~shais/UnderstandingMachineLearning/understanding-machine-learning-theory-algorithms.pdf
* diff with classical stat:
learner if blind to D (data distribution) and f (true mapping)
* error, generalization error, risk
* empirical risk minimization (ERM),
  * suffers from over-fitting,
    solution: hypothesis class, H
* estimation error, approximation error (bias)
* realizability assumption:
if the hypothesis class, H, is rich enough, the training error can be zero
* pac learning: probably approx correct
* agnostic pac learning
* multiclass clf: cross-entropy loss
* regression: mean squared err
* bayes optimal predictor, if we know D
* uniform convergence: glivenko-cantalli class
* erm-learnable, pac-learnable
* no free lunch theorem:
no general alg that can generalize to any problem
* bias-complexity tradeoff, overfit-underfit tradeoff
* VC-dimension characterizes PAC-learnability:
https://www.quora.com/Explain-VC-dimension-and-shattering-in-lucid-Way
* non uniform learning
* structural risk minization
* occam's razor: do well as simple as possible
