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
   
{: .text-justify} 
Resource management has been a perpetual theme in wireless network design, deployment, and operations. In today’s wireless systems, data demands continue to
grow with a diverse range of applications from bandwidth-hungry multimedia streaming, delay-sensitive instant messaging, and online gaming to bulk data
transfer. The ever-increasing needs for high-speed ubiquitous network access by mobile users are further aggravated by emerging machine-to-machine communication for home and industrial automation, wide-area sensing and monitoring, autonomous vehicles, etc. Delivery of these rich sets of applications is fundamentally limited by resource scarcity in wireless networks that manifests at various levels. For instance, spectrum scarcity has emerged as a primary problem when trying to launch new wireless services. Vendors and operators are increasingly looking into millimeter radio bands for 5G cellular standard though the spectrum was previously considered unsuitable for wider area applications. Interferences among wireless transceivers in close proximity continue to pose challenges to the delivery of reliable and timely services. Mobile devices are inherently power-constrained, demanding efficient communication schemes and protocols.

Many resource management solutions in wireless networks operate on the assumption that the decision makers have the complete knowledge of system states and parameters (e.g., channel states, network topology, and user density). When such information is unavailable or incomplete, probing or learning has to be conducted prior to the making of resource management decisions. As an example, in orthogonal frequency-division multiplexing (OFDM) systems, pilot signals are transmitted either along a dedicated set of subcarriers or a specific period across all subcarriers for channel estimation. This allows the adaption of subsequent transmissions to current channel conditions. Sequential learning, in contrast, is a paradigm where learning and decision-making are performed concurrently. The framework is applicable in a variety of scenarios where the utility of resource management resources follows single-parametrized independent and identically distributions, Markovian or unknown adversarial processes. It is a powerful tool in wireless resource management. Sequential learning and decision-making have been successfully applied to for resource management in cognitive radio networks, wireless LANs, and mesh networks. 

However, there are significant barriers in the wider adoption of the framework in addressing resource management problems in the wireless community. We believe that this can be attributed to two reasons: First, the sequential learning theory originates from complex stochastic concepts posing a significant learning curve. Effective algorithms often rely on underlying assumptions such as stationary and independent stochastic processes. Identifying a suitable solution to a specific problem can be a tall order for beginners. Second, there is a disconnect between theory and practical constraints in real-world settings. For example, in practice, the timeliness of decision-making often trumps optimality. In contrast, the primary
concerns of sequential learning literature are the convergence rate in a long run and the optimality of the sequence of actions.

It is the first attempt to bridge the aforementioned gaps. Though the literature on sequential learning is abundant, a comprehensive treatment of its
applications in wireless networks is lacking. In this book, we aim to lay out the theoretical foundation of the so-called multi-armed bandit (MAB) problems and put
it in the context of resource management in wireless networks. Part I of this book presents the formulations, algorithms, and performance of three forms of MAB
problems, namely stochastic, Markov, and adversarial. To the best of our knowledge, this is the first work that covers all the three forms of MAB problems. Part II
of this book provides detailed discussions of representative applications of the sequential learning framework in wireless resource management. They serve as case
studies both to illustrate how the theoretical framework and tools in Part I can be applied and also to demonstrate how existing algorithms can be extended to address
practical concerns in operational wireless networks. We believe both the industry
and the wireless research community can benefit from a comprehensive and timely
treatment of these topics.

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


#### 2. MAB in Recommend Systems
{: .text-justify}
* Huawei-HKUST Joint Workshop on Theory for Futrue Wireless, 2022








