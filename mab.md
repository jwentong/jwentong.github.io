---
layout: archive
author_profile: true
title: MAB
permalink: /mab/
---

{: .text-justify}
*Multi-Armed Bandit (MAB)* is a basic framework for the sequential decisionmaking problem, where a decision-maker (or player) must select an arm from a set of arms with unknown distribution at each time round. After that, the player will observe a reward from the environment. According to the rewarding process,
MABs can be roughly classified into stochastic MABs, adversarial MABs, Markovian MABs, and Contextual MABs. 

   ![test](https://github.com/jwentong/jwentong.github.io/raw/master/assets/images/mabfig_02.jpg)

### Theoretical Parts

####  1. Stochatic MABs

{: .text-justify}
In the problem, each machine provides a random reward from a probability distribution specific to that machine, that is not known a-priori. The objective of the gambler is to maximize the sum of rewards earned through a sequence of lever pulls. The crucial tradeoff the gambler faces at each trial is between "exploitation" of the machine that has the highest expected payoff and "exploration" to get more information about the expected payoffs of the other machines. The trade-off between exploration and exploitation is also faced in machine learning. In practice, multi-armed bandits have been used to model problems such as managing research projects in a large organization, like a science foundation or a pharmaceutical company. In early versions of the problem, the gambler begins with no initial knowledge about the machines.


#### 2. Adversarial MABs

{: .text-justify}
Another variant of the multi-armed bandit problem is called the adversarial bandit, first introduced by Auer and Cesa-Bianchi (1998). In this variant, at each iteration, an agent chooses an arm and an adversary simultaneously chooses the payoff structure for each arm. This is one of the strongest generalizations of the bandit problem[53] as it removes all assumptions of the distribution and a solution to the adversarial bandit problem is a generalized solution to the more specific bandit problems.


#### 3. Markovian MABs

{: .text-justify}
Markov MAB problems differ from the stochastic MAB problem discussed in that the reward process of an arm is not IID, instead, follows a Markov process. Furthermore, the evolution of the Markov processes may depend on the player’s decision whether an arm is chosen or not.
In rested Markov MAB problems, the state of an arm changes according to Pi if and only if it is played and remains frozen otherwise. Rested Markov MAB can be used to model job scheduling problems in a single server system. The scheduler needs to decide among K jobs, which one to allocate computing resources to at each time interval. The states of the jobs not scheduled remain unchanged. In contrast, in restless Markov MAB problems, the state of each arm changes regardless of the user’s actions. One application of restless Markov MAB is spectrum sensing and access in cognitive radio networks, which will be discussed in detail in Chap.5.In spectrum sensing and access, the reward of each arm (channel) is a function of the channel occupancy, which may evolve according to a Markov process independent of the user’s action.


#### 4. Contextual MABs

{: .text-justify}
A useful generalization of the multi-armed bandit is the contextual multi-armed bandit. At each iteration an agent still has to choose between arms, but they also see a d-dimensional feature vector, the context vector they can use together with the rewards of the arms played in the past to make the choice of the arm to play. Over time, the learner's aim is to collect enough information about how the context vectors and rewards relate to each other, so that it can predict the next best arm to play by looking at the feature vectors.


---

### Application Parts

#### 1. MAB in Wireless Communications
{: .text-justify}
* IEEE/CIC International Conference on Communications in China (ICCC), 2021


#### 2. MAB in recommend Systems
{: .text-justify}
* Huawei-HKUST Joint Workshop on Theory for Futrue Wireless, 2022








