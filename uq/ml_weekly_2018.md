# ml_weekly_2018.md
link: https://paper.dropbox.com/doc/UQ-ML-Reading-Group-Schedule-O0e6GrWgdFS7dqZ49wFFZ

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
