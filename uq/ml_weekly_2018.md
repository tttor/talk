# ml_weekly_2018.md
link: https://paper.dropbox.com/doc/UQ-ML-Reading-Group-Schedule-O0e6GrWgdFS7dqZ49wFFZ

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

## Feb 16, 2018: Fred Roosta
* understanding ML book:
http://www.cs.huji.ac.il/~shais/UnderstandingMachineLearning/understanding-machine-learning-theory-algorithms.pdf
* ch 1 to 6 (review)
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
