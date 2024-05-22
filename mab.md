---
layout: archive
author_profile: true
title: MAB
permalink: /mab/
---

### Introduction

{: .text-justify}
*Multi-Armed Bandit (MAB)* is a fundamental framework for sequential decision-making. In this setting, a decision-maker (or player) faces a set of arms, each with an unknown reward distribution. At each time step, the player must choose an arm to pull, receiving a reward drawn from that arm's distribution. The goal is to maximize the cumulative reward over time. MABs are a versatile tool with applications in various fields, including:
- Recommender Systems: Optimizing content recommendations based on user preferences.
- Clinical Trials: Determining the most effective treatment for a disease.
- Online Advertising: Optimizing ad placements to maximize click-through rates.

MAB problems can be categorized based on the nature of the reward process:
- Stochastic MABs: The reward distribution for each arm is stationary and independent over time.
- Adversarial MABs: The rewards are chosen by an adversary, potentially aiming to mislead the player.
- Markovian MABs: The reward distribution depends on the history of past arm selections.
- Contextual MABs: The player receives contextual information at each time step, which can influence the reward distribution.

The MAB problem has attracted significant attention from researchers in various fields, including computer science, mathematics, and statistics. Notable pioneers in the field include:
- Richard Sutton: Known for his work on reinforcement learning, which has strong connections to MABs.
- Peter Auer: A leading researcher in the development of algorithms for stochastic MABs.
- John Langford: Known for his contributions to contextual MABs and online learning.
- Sébastien Bubeck: A prominent researcher in the theoretical analysis of MAB algorithms.
- Lihong Li: Known for his work on bandit algorithms for large-scale applications.
These researchers, along with many others, have contributed to the development of theoretical foundations, algorithms, and applications of MABs. This has made the field an active and growing area of research with ongoing advancements in both theory and practice.


   ![test](https://github.com/jwentong/jwentong.github.io/raw/master/assets/images/mabfig_02.jpg)
   


### Theoretical Parts

####  1. Stochatic MABs

{: .text-justify}
In the problem, each machine provides a random reward from a probability distribution specific to that machine that is not known as apriori. The objective of the gambler is to maximize the sum of rewards earned through a sequence of lever pulls. The crucial tradeoff the gambler faces at each trial is between "exploitation" of the machine that has the highest expected payoff and "exploration" to get more information about the expected payoffs of the other machines. The trade-off between exploration and exploitation is also faced in machine learning. In practice, multi-armed bandits have been used to model problems such as managing research projects in a large organization, like a science foundation or a pharmaceutical company. In early versions of the problem, the gambler begins with no initial knowledge about the machines.


#### 2. Adversarial MABs

{: .text-justify}
The adversarial multi-armed bandit (MAB) is a variation of the classic MAB problem in which an adversary controls the reward distributions for each arm and can change them arbitrarily over time. In other words, the adversary has full control over the rewards that the decision-maker receives at each time step, and their goal is to minimize the total expected reward of the decision-maker.

{: .text-justify}
The adversarial MAB problem is a worst-case scenario in which the decision maker cannot make any assumptions about the reward distributions and must adaptively respond to the adversary's actions. This problem arises in many real-world applications, such as online advertising, where the adversary may manipulate the user's preferences or behavior to reduce the effectiveness of the advertising.

{: .text-justify}
Various algorithms and strategies have been developed to solve the adversarial MAB problem, including the EXP3 (exponential weighting for exploration and exploitation) algorithm, which uses a randomized exploration strategy to avoid exploitation of arms with low rewards, and the follow-the-leader algorithm, which chooses the arm with the highest observed reward in the past.

{: .text-justify}
The adversarial MAB problem is more challenging than the classic MAB problem because it requires the decision maker to adaptively respond to the actions of an intelligent adversary who is actively trying to manipulate the decision maker's choices. However, it is also more relevant to real-world applications where the decision-maker may face strategic opponents who are trying to exploit or deceive them.


#### 3. Markovian MABs

{: .text-justify}
The Markovian multi-armed bandit (MAB) is a variation of the classic MAB problem in which the reward distributions for each arm depend on the state of a Markov decision process (MDP). In an MDP, the system's state evolves over time according to a set of probabilistic transition rules, and the decision maker's actions can influence the transition probabilities and the rewards received at each time step.

{: .text-justify}
In the Markovian MAB problem, the decision maker must learn a policy that maps each state to the best arm to pull at each time step in order to maximize the total expected reward over a sequence of pulls. This problem arises in many real-world applications, such as resource allocation in wireless communication networks, where the decision maker must adaptively allocate resources to different users based on their channel conditions, which can vary over time.

{: .text-justify}
Various algorithms and strategies have been developed to solve the Markovian MAB problem, including the MDP-based bandit algorithm, which uses an MDP model to estimate the expected rewards for each arm in each state, and the Q-learning algorithm, which learns a Q-function that represents the expected total reward for each state-action pair.

{: .text-justify}
The Markovian MAB problem is more complex than the classic MAB problem because it requires the decision-maker to reason about the system's dynamics and how their actions can influence future states and rewards. However, it is also more powerful because it allows the decision-maker to take advantage of the system's temporal structure to improve their decision-making performance.


#### 4. Contextual MABs

{: .text-justify}
The contextual multi-armed bandit (MAB) is an extension of the classic MAB problem in which each arm is associated with a context or set of features that can provide additional information to the decision-maker. In other words, the reward distribution for each arm is dependent on the context or features associated with that arm.

{: .text-justify}
The goal of the contextual MAB problem is to learn a policy that maps each context to the best arm to pull at each time step in order to maximize the total expected reward over a sequence of pulls. This problem arises in many real-world applications, such as online advertising, personalized medicine, and recommendation systems, where the decision-maker has access to contextual information about the user or environment.

{: .text-justify}
Various algorithms and strategies have been developed to solve the contextual MAB problem, including the contextual bandit algorithm, which uses a model of the reward distribution for each arm conditioned on the context, and the contextual Thompson sampling algorithm, which extends the classic Thompson sampling algorithm to incorporate contextual information.

{: .text-justify}
The contextual MAB problem is more challenging than the classic MAB problem because it requires the decision maker to learn a policy that effectively uses contextual information to make informed decisions about which arm to pull at each time step. However, it is also more powerful because it allows the decision-maker to take advantage of additional information to improve their decision-making performance.


---

### Application Parts

#### 1. MAB in Wireless Communications

{: .text-justify} 
Resource management has been a perpetual theme in wireless network design, deployment, and operations. In today’s wireless systems, data demands continue to
grow with a diverse range of applications, from bandwidth-hungry multimedia streaming, delay-sensitive instant messaging, and online gaming to bulk data
transfer. The ever-increasing needs for high-speed ubiquitous network access by mobile users are further aggravated by emerging machine-to-machine communication for home and industrial automation, wide-area sensing and monitoring, autonomous vehicles, etc. Delivery of these rich sets of applications is fundamentally limited by resource scarcity in wireless networks that manifests at various levels. For instance, spectrum scarcity has emerged as a primary problem when trying to launch new wireless services. Vendors and operators are increasingly looking into millimeter radio bands for 5G cellular standard though the spectrum was previously considered unsuitable for wider area applications. Interferences among wireless transceivers in close proximity continue to pose challenges to the delivery of reliable and timely services. Mobile devices are inherently power-constrained, demanding efficient communication schemes and protocols.

{: .text-justify} 
Many resource management solutions in wireless networks operate on the assumption that the decision-makers have complete knowledge of system states and parameters (e.g., channel states, network topology, and user density). When such information is unavailable or incomplete, probing or learning has to be conducted prior to the making of resource management decisions. As an example, in orthogonal frequency-division multiplexing (OFDM) systems, pilot signals are transmitted either along a dedicated set of subcarriers or a specific period across all subcarriers for channel estimation. This allows the adaption of subsequent transmissions to current channel conditions. Sequential learning, in contrast, is a paradigm where learning and decision-making are performed concurrently. The framework is applicable in a variety of scenarios where the utility of resource management resources follows single-parametrized independent and identically distributions, Markovian, or unknown adversarial processes. It is a powerful tool in wireless resource management. Sequential learning and decision-making have been successfully applied to for resource management in cognitive radio networks, wireless LANs, and mesh networks. 

{: .text-justify} 
However, there are significant barriers to the wider adoption of the framework in addressing resource management problems in the wireless community. We believe that this can be attributed to two reasons: First, the sequential learning theory originates from complex stochastic concepts posing a significant learning curve. Effective algorithms often rely on underlying assumptions such as stationary and independent stochastic processes. Identifying a suitable solution to a specific problem can be a tall order for beginners. Second, there is a disconnect between theory and practical constraints in real-world settings. For example, in practice, the timeliness of decision-making often trumps optimality. In contrast, the primary
concerns of sequential learning literature are the convergence rate in the long run and the optimality of the sequence of actions.

{: .text-justify} 
It is the first attempt to bridge the aforementioned gaps. Though the literature on sequential learning is abundant, a comprehensive treatment of its
applications in wireless networks is lacking. In this book, we aim to lay out the theoretical foundation of the so-called multi-armed bandit (MAB) problems and put
it in the context of resource management in wireless networks. Part I of this book presents the formulations, algorithms, and performance of three forms of MAB
problems, namely stochastic, Markov, and adversarial. To the best of our knowledge, this is the first work that covers all three forms of MAB problems. Part II
of this book provides detailed discussions of representative applications of the sequential learning framework in wireless resource management. They serve as case
studies both to illustrate how the theoretical framework and tools in Part I can be applied and also to demonstrate how existing algorithms can be extended to address
practical concerns in operational wireless networks. We believe both the industry
and the wireless research community can benefit from a comprehensive and timely
treatment of these topics.


#### New works related to MAB
{: .text-justify}
* We collected some newly published papers related to MAB in the following link.
  Please ![see](https://abrasive-aletopelta-824.notion.site/Bandit-Paper-From-Recommended-Scholar-c8ca9a7cf3ef4ec1b4b740cd49129165)








