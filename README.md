
by Gregory Urman

www.linkedin.com/in/gregoryurman  

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

- Advantages of Value Iteration:
  - Complexity of each iteration is [smaller than Policy Iteration]
  - Will converge towards optimal values
  - Value iteration is good for a small set of states because we will avoid computing very deep expectimax trees which run in exponential time

- Disadvantages of Value Iteration:
  - Value iteration has to touch every state in every iteration and so if we have a large number of total states, value iteration suffers
  - It is slow because we have to consider all actions at every node, and often, there are many actions
  - The "max" at a state rarely changes. This means that the relative size of the Q values converge well before the values converge

- Details:
  - Value iteration does the same thing as policy iteration, that is, they take an MDP [Markov Decision Process, google that separately to make better sense of this conversation] as input and outputs an optimal policy as an output [3]

- Value iteration computes the optimal state value function by iteratively improving the estimate of V(s) [value function]. The algorithm initialize V(s) to arbitrary random values. It repeatedly updates the Q(s, a) [optimal Q-function, googling that further would be helpful] and V(s) values until they converges. Value iteration is guranteed to converge to the optimal values. [4]

- Value iteration starts at the "end" and then works backward, refining an estimate of either Q* [Q-Function] or V* [Value Function]. There is really no end, so it uses an arbitrary end point.[5]


_ _How then does all the above relate to GridWorld_ _? 

let us look at how to run the GridWorld problem in terms of how to actually _ _win the game_ _ :

![grid world plus directions](https://user-images.githubusercontent.com/22970879/42313209-65c09134-7fff-11e8-9e06-2b0f66338aa4.png)


In short: Value Iteration helps us come up with a better value estimate of how to get to the goal value A.K.A _terminal state_ we a looking for. [Paraphrase] [6] :-) :-) :-) 

![value iteration in number form](https://user-images.githubusercontent.com/22970879/42315362-803e7346-8004-11e8-86fa-781ad911d8e5.png)

Above, that path is expressed in terms of decimals
-------------------------------------------------------------------------------------------------------------------------------

# Conclusion: 

- Both Policy Iteration and Value Iteration help is find the Optimum Value Function

- In terms of Grid World, that means the Optimum Path for winning the game, moving from one square to the next

- Value Iteration works backwards, just like many other processes, especially Dynamic Programming.


- as someone I know said it before: 
  - **Value Iteration** = one iteration of policy evaluation followed by policy update, only! (like a mini-policy-evaluation to policy-iteration process) (Dr. Hart, Regis University, Denver CO)

-------------------------------------------------------------------------------------------------------------------------------




<br/>
[1] = https://stackoverflow.com/questions/37370015/what-is-the-difference-between-value-iteration-and-policy-iteration 

[2] = http://wiki.ubc.ca/Course:CPSC522/Markov_Decision_Process

[3] = http://cs188ai.wikia.com/wiki/Value_Iteration

[4] = https://medium.com/@m.alzantot/deep-reinforcement-learning-demysitifed-episode-2-policy-iteration-value-iteration-and-q-978f9e89ddaa

[5] = http://artint.info/html/ArtInt_227.html

[6] = https://www.youtube.com/watch?v=glHKJ359Cnc

<br/>

_ _Thank you very much for reading this blog. I hope you found it useful for learning more about Reinforcement Learning as part of Machine Learning. Onward and upward!_ _



Gregory Urman

www.linkedin.com/in/gregoryurman
