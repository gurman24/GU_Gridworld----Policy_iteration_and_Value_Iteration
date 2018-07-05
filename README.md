# GU_Gridworld----Policy_iteration_and_Value_Iteration

_ _see footnotes at the bottom for website sources_ _

In this blog we will discuss Policy Iteration and Value Iteration using GridWorld as the example. You, the reader, may find the previous blog of interest here: https://github.com/gurman24/GU-GridWorld----Iterative-Policy-Evaluation-and-Policy-Iteration-including-charts-

As discussed before, a **policy** can be defined as: a set of actions you have for a set of states. This is very important because policies dictate how Agents act in Environments when looking to maximize the reward they are looking for. See the following pictures for a deeper explanation: 

- (https://user-images.githubusercontent.com/22970879/42120041-d7145168-7bd1-11e8-8f11-42546269f56e.png)  

- (https://user-images.githubusercontent.com/22970879/42248842-ea5fcf0c-7ee4-11e8-87de-16cc93b80f42.PNG)

- (https://user-images.githubusercontent.com/22970879/42268306-6577659e-7f38-11e8-9412-2471e7770874.png)

<br/>

This discussion would also be facilitated by having an understanding of States and State-to-State transitions which can be found here:
https://github.com/gurman24/What-are-States-and-State-to-State-Transitions-

<br/>
Now that we have a proper background, the question becomes _ _what is the difference between Policy Iteration and Value Iteration_ _ ?

- **Policy Iteration** includes: **policy evaluation** + **policy improvement**, and the two are repeated iteratively until policy converges.

- **Value iteration** includes: **finding optimal value function** + one **policy extraction**. There is no repeat of the two because once the value function is optimal, then the policy out of it should also be optimal (i.e. converged). [1]

- value iteration or **backward induction** is essentially a dynamic programming approach. Value iteration finds better policies by construction i.e. finding the best value function by iteratively updating the value function. ... Value Iteration is moderately expensive. [time and resource consuming][2]

- Advantages:
  - Complexity of each iteration is [smaller than Policy Iteration]
  - Will converge towards optimal values
  - Value iteration is good for a small set of states because we will avoid computing very deep expectimax trees which run in exponential time

- Disadvantages:
  - Value iteration has to touch every state in every iteration and so if we have a large number of total states, value iteration suffers
  - It is slow because we have to consider all actions at every node, and often, there are many actions
  - The "max" at a state rarely changes. This means that the relative size of the Q values converge well before the values converge

- Details:
  - Value iteration does the same thing as policy iteration, that is, they take an MDP [Markov Decision Process, google that separately to make better sense of this conversation] as input and outputs an optimal policy as an output [3]

- Value iteration computes the optimal state value function by iteratively improving the estimate of V(s) [value function]. The algorithm initialize V(s) to arbitrary random values. It repeatedly updates the Q(s, a) [optimal Q-function, googling that further would be helpful] and V(s) values until they converges. Value iteration is guranteed to converge to the optimal values. [4]

- Value iteration starts at the "end" and then works backward, refining an estimate of either Q* [Q-Function] or V* [Value Function]. There is really no end, so it uses an arbitrary end point.[5]


_ _How then does all the above relate to GridWorld_ _? 

let us look at how to run the GridWorld problem in terms of how to actually _ _win the game_ _ :






<br/>
[1] = https://stackoverflow.com/questions/37370015/what-is-the-difference-between-value-iteration-and-policy-iteration 

[2] = http://wiki.ubc.ca/Course:CPSC522/Markov_Decision_Process

[3] = http://cs188ai.wikia.com/wiki/Value_Iteration

[4] = https://medium.com/@m.alzantot/deep-reinforcement-learning-demysitifed-episode-2-policy-iteration-value-iteration-and-q-978f9e89ddaa

[5] = http://artint.info/html/ArtInt_227.html















