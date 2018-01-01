[RI Seminar: Dmitry Berenson : What Matters for Deformable Object Manipulation](https://www.youtube.com/watch?v=7Rc3cxN_cus&t=1021s)

# pre
* hardware for manip in unstructured env is already there
* focus: diverse, collaborative, unstructured env

# his work
* constrained manip planning
* collaborative manip
* compliant manip (now)

# source of compliant manip:
* deformatble object: clothes (table clothing), carbon fiber, cables, agriculture crops
compliant robot body

# deformable obj
* uncertainty, expensive to simulate
* hi dim space
* hyper underactuated

# question: representation of deformable obj
* existing:
spring, mesh less model, fem simulation
* rel work
motion planning for deformable obj
* approach:
reduced model for a certain task
model can be useful even if not accurate
model selection as multi arm bandit problem: KalmanFilter MAB for non-stationary distribution

# approach
* multiple models for control
* interleaving planing and control
* note: focus on eef planning, becuase we already know how to move the arm

# comments
* tools for deformable objects,
  * ironing to fold clothes
* questions in using tools
  * which tools
  * how to grasp tools
  * how to use tools
