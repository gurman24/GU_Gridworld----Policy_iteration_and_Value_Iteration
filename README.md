# GU_Gridworld----Policy_iteration_and_Value_Iteration


In this blog we will discuss Policy Iteration and Value Iteration using GridWorld as the example. You, the reader, may find the previous blog of interest here: https://github.com/gurman24/GU-GridWorld----Iterative-Policy-Evaluation-and-Policy-Iteration-including-charts-

As discussed before, a **policy** can be defined as: a set of actions you have for a set of states. This is very important because policies dictate how Agents act in Environments when looking to maximize the reward they are looking for. See the following pictures for a deeper explanation: 

- (https://user-images.githubusercontent.com/22970879/42120041-d7145168-7bd1-11e8-8f11-42546269f56e.png), .  

- (https://user-images.githubusercontent.com/22970879/42248842-ea5fcf0c-7ee4-11e8-87de-16cc93b80f42.PNG)

- (https://user-images.githubusercontent.com/22970879/42268306-6577659e-7f38-11e8-9412-2471e7770874.png)

<br/>

This discussion would also be facilitated by having an understanding of States and State-to-State transitions which can be found here:
https://github.com/gurman24/What-are-States-and-State-to-State-Transitions-

<br/>
Now that we have a proper background, the question becomes _ _what is the difference between Policy Iteration and Value Iteration?_ _

- **Policy Iteration** includes: **policy evaluation** + **policy improvement**, and the two are repeated iteratively until policy converges.

- **Value iteration** includes: **finding optimal value function** + one **policy extraction**. There is no repeat of the two because once the value function is optimal, then the policy out of it should also be optimal (i.e. converged). [1]

- value iteration or **backward induction** is essentially a dynamic programming approach. Value iteration finds better policies by construction i.e. finding the best value function by iteratively updating the value function. [2]

- 






[1] = https://stackoverflow.com/questions/37370015/what-is-the-difference-between-value-iteration-and-policy-iteration 

[2] = http://wiki.ubc.ca/Course:CPSC522/Markov_Decision_Process



















