(model-based optimization and how to combine it with learning)[https://www.youtube.com/watch?v=7enj1FGoYwg&t=195s]

# pre
* minimize trials in rl
* real trial err should be safe

# final remark
* im effort to be model-free, RL treats reward as being generated externally.
  This requires an oracle.
  * well, yes, in model-free. it need an oracle, but see model-based
  where there is a reward model that may give immediate rewards along the way,
  see also subfield of inverseRL that tries to recover the reward model.
  what if the reward model is less sparse than the actual reward model?
  also, this is why we also need model-based rl in addition to model free RL

* Brains have elaborate neural mechanism to recognize situations that are good for the organism, and deliver reward internally,
this is likely because the objective external rewards are too sparse (in time) to be useful for learning,
consider a predator chasing prey and only getting rewards upon eating it.
similarly, robots must have the ability to compute rewards themselves.
  * this is exactly model-based rl
  and the question is
  what if the reward model (less sparse) is different enough compared to the actual reward (sparse)?
  how does such less-sparse reward model come from? or how is the less-sparse reward model built, manual or auto?
  or with some heuristic or prior knowledge?

* the internal reward evaluation system requires general-porpuse perception, and
  must be in place before RL starts. so it makes sense to use it for RL,
  instead of doing end-to-end training that effectively reinvent the wheel
  * this seems to be againts deep rl

# his work
* ping pong robot
