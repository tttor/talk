hanna_reading_2018: Deep RL

# 2018 01 19: Hanna
* Silver, David, et al. "The predictron: End-to-end learning and planning." arXiv preprint arXiv:1612.08810 (2016).
* Tamar, Aviv, et al. "Value iteration networks." Advances in Neural Information Processing Systems. 2016.

## VIN (best in nips 2016)
* problem
  * most recent deep RL works [21, 18, 9] employed NN architectures that are very similar to
    the standard networksused in supervised learning tasks,
    which typically consist of CNNs for feature extraction, and fully
    connected layers that map the features to a probability distribution over actions.
  * Such networks are inherently reactive, and in particular, lack explicit planning computation.
    The success of reactive policies in sequential problems is due to the learning algorithm, which
    essentially trains a reactive policy to select actions that
    have good long-term consequences in its training domain.
  * as we show in our experiments, while standard CNN-based networks can be easily
    trained to solve a set of such maps, they do not generalize well to new tasks outside this set,
    because they do not understand the goal-directed nature of the behavior.
* idea
  * a value-iteration network (VIN), has a differentiable "planning program" embedded
    within the NN structure.
  * an observation that the classic value-iteration (VI) planning algorithm [1, 2] may be
    represented by a specific type of CNN.
  * the effects of modelling errors in VINs can be mitigated by training the network end-to-end
  * CNNs can implement a particular form of planning computation similar to the value iteration algorithm,
    which can then be used as a policy for RL or IL

* result
  * on discrete and continuous path-planning domains,
  * on a natural-language based search task.
