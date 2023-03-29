---
layout: post
title: Reinforcement Learning for Economic Policymaking
permalink: /rl_econ/
excerpt_separator: <!--more-->
tagline: "Deep reinforcement learning has shown promising results in games with a limited number of agents such as Chess, Go, Poker, etc. We develop methods to go beyond few agent settings and apply it to microeconomic simulations for finding general equilibria and optimal agent policies."
type: project
imagelink: assets/ev-charging.png
location: front
collaborators: Stephan Zheng, Sunil Srinivasa, Stefano Ermon (Salesforce Research)
---

Several situations encountered in social and economic settings can be modeled as a game between multiple players. Multi-agent reinforcement learning (MARL) is a promising technique to simulate these situations and gain novel insights for improved policy-making and assisting individual decision-making. In this project, we develop a parallel computing framework and propose a new algorithm to scale MARL to millions of agents. Sample applications: planning of EV charging infrastructure, transportation networks, supply-chain networks, financial networks, economic networks, digital networks.

**AI for Global Climate Change Cooperation.**
This project was a collaboration between Yoshua Bengio's group at MILA - Quebec AI Institute and the AI Economist team at Salesforce (which I was a part of). We developed a simulator environment with multiple regions (countries) modeled as independent decision making agents who interact with each other through actions such as countries production, capital investments, international trade and tariffs, climate change mitigation investments. We developed this simulator by extending the [RICE simulator](https://williamnordhaus.com/dicerice-models) designed by William Nordhaus. We used multi-agent reinforcement learning to train the decision policies of each agent for its own best interests.

We launched a [competition](https://www.ai4climatecoop.org/) where participants use this simulation environment to design their own negotiation protocols such as bilateral agreements, climate clubs, etc. The simulated agents interact in this modified environment and observe its effect on the global production and temperature change across 100 years.

A key challenge in this project was to conceptualize a modular framework that would allow the implementation of any general negotiation protocol by fixing the core actions and their effect on the production and climate outcomes and a bridge between the negotiation agreements and core actions through action masking (not allowing certain actions). We coded this simulator in pytorch (and a faster version using CUDA WarpDrive). The details can be found in this workshop [paper](https://arxiv.org/pdf/2208.07004.pdf). 


**Scalable Multi-Agent Reinforcement Learning to Solve Markov Decision Processes with Network Constraints.**
Several economic and business situations can be modeled as Markov decision processes with network constraints. Example: Urban electric vehicle (EV) charging. Each EV owner makes decisions regarding when to travel, where to charge, how long to charge, which type of charger to use, etc. This results in a Markov process for each EV owner but these processes are coupled because they share common resources such as public EV charging stations. The wait times at these stations depend on the demand at these stations resulting from other agents' decisions.

We explored previous methods using rule-based simulations (e.g. [MATSim](https://www.matsim.org/)) and analytical approximations for this problem. These methods are often either restricted to a narrow set of decision policies or a small number or independent decision making agents or both. We developed a multi-agent reinforcement learning framework to simulate such environments. We can guarantee convergence to approximate optimal allocations in these network economic problems. A key difficulty was training a large number of simulated agents in parallel. We developed efficient methods to resolve this problem by leveraging the similarity between agents and training them in parallel on GPUs.