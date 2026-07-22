MDP REPRESENTATION
AIM:
To model the food delivery process as a Markov Decision Process (MDP) and analyze the states, actions, and rewards involved in completing the delivery efficiently.

PROBLEM STATEMENT:
Problem Description
An agent (delivery person) is assigned to deliver food from a restaurant to a customer. The goal is to complete the delivery quickly while minimizing delays and effort. The agent chooses actions such as picking up food, moving, or delivering based on the current state.

State Space
The state space represents all possible stages of the delivery process:

D0 → Order Not Picked D1 → Food Picked D2 → Delivered (Goal State)

Sample State
"Food is picked and the agent is on the way to the customer" (D2)

Action Space
The possible actions available to the agent:

->Pick Up Food ->Start Delivery ->Continue Moving ->Deliver Food

Sample Action
"Continue Moving"

Reward Function
The reward function guides the agent: +10 → Successfully picking up food +20 → Delivering food to customer (goal achieved) -2 → Delay in movement -5 → Wrong action or unnecessary delay

Graphical Representation
image
PYTHON REPRESENTATION:
P = {
  0: {
    0: [(1.0, 0, -2.0, False)],
    1: [(1.0, 1, +10.0, False)],
    2: [(1.0, 0, -3.0, False)],
    3: [(1.0, 0, -3.0, False)]
  },
  1: {
    0: [(1.0, 1, -3.0, False)],
    1: [(1.0, 1, -2.0, False)],
    2: [(1.0, 2, +20.0, True)],
    3: [(1.0, 1, -3.0, False)]
  },
  2: {
    0: [(1.0, 2, 0, True)],
    1: [(1.0, 2, 0, True)],
    2: [(1.0, 2, 0, True)],
    3: [(1.0, 2, 0, True)]
  }
}
OUTPUT:
image
RESULT:
Thus, the food delivery process problem is successfully represented in MDP form.
