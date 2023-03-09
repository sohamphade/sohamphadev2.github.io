---
layout: post
title: Research
---

## Research Themes

1. <a href="#section1">Game Theory and Market Design when Agents have Cumulative Prospect Theory Preferences</a>
2. <a href="#section2">Learning in Repeated Games</a> 
3. <a href="#section3">Optimal Resource Allocation over Networks</a>
4. <a href="#section4">Cooperative games</a>

---

<span class="anchor" id="section1"></span>

## Game Theory and Market Design when Agents have Cumulative Prospect Theory Preferences


In this project, we systematically study game-theoretic settings (in particular, non-cooperative games) when the players' preferences are modeled using [cumulative prospect theory (CPT)](https://en.wikipedia.org/wiki/Cumulative_prospect_theory).
CPT is a generalization of expected utility theory (EUT) and one of the leading decision theories to model human preferences when faced with uncertainty. It was proposed by [Daniel Kahneman](https://en.wikipedia.org/wiki/Daniel_Kahneman) and [Amos Tversky](https://en.wikipedia.org/wiki/Amos_Tversky) for which Kahneman received the [Nobel Memorial Prize in Economic Sciences](https://www.nobelprize.org/prizes/economic-sciences/2002/kahneman/facts/). 
There has been growing discussion concerning the benefits (and limits) of using CPT in game theory and economics. 
In a series of papers, we discover several exciting equilibria related properties by revisiting some of the landmark results in game theory and mechanism design through the CPT lens.

See this [post]({{ '/cptgames/index.html' | absolute_url }}) for further details about this project.

### Papers

- S. Phade and V. Anantharam (2019). “On the Geometry of Nash and Correlated Equilibria with Cumulative Prospect Theoretic Preferences.” *Decision Analysis* 16(2), 142-156.
<a href="https://pubsonline.informs.org/doi/abs/10.1287/deca.2018.0378?casa_token=7J9MUcsbZl4AAAAA:FArUlacTEA378xkYhAZXiy8JU7r78vGt__aQhm0RPs927EnOTR-LC_asRPrDS6ydaQr0yOXNcA" target="_blank">[link]</a>
<a href="https://arxiv.org/abs/1712.00859" target="_blank">[ArXiv]</a>

- S. Phade and V. Anantharam. “Learning in Games with Cumulative Prospect Theoretic Preferences.” <a href="https://arxiv.org/abs/1804.08005" target="_blank">[ArXiv]</a>

- S. Phade and V. Anantharam. “Black-box strategies and Equilibrium in Games with Cumulative Prospect Theory Preferences.” <a href="https://arxiv.org/abs/2004.09592" target="_blank">[ArXiv]</a>

- S. Phade and V. Anantharam. "Mechanism Design for Cumulative Prospect Theory Agents: A General Framework and the Revelation Principle." <a href="https://arxiv.org/abs/2101.08722" target="_blank">[Link]</a>


---


<span class="anchor" id="section2"></span>

## Learning in Repeated Games

The literature on learning in games provides an alternative explanation to equilibrium notions as a long-run outcome in repeated games with mild rationality assumptions on the players. 
It especially important from a behavioral perspective.
We establish several related results when the players have cumulative prospect theory preferences.
In another work, our preliminary analysis brings forth a fundamental trade-off property between the regret rate guarantees of the players and the convergence rates of their mixed-action strategies.
In particular, we show that under certain conditions it is impossible for the mixed-actions of the two players in a game of [matching pennies](https://en.wikipedia.org/wiki/Matching_pennies) to converge almost surely if both the players decide to play optimal no-regret strategies.


### Papers

- S. Phade and V. Anantharam. “Learning in Games with Cumulative Prospect Theoretic Preferences.” <a href="https://arxiv.org/abs/1804.08005" target="_blank">[ArXiv]</a>

- V. Muthukumar, S. Phade, A. Sahai. “On the Impossibility of Convergence of Mixed Strategies with No-Regret Learning.” <a href="https://arxiv.org/abs/2012.02125" target="_blank">[ArXiv]</a>


---


<span class="anchor" id="section3"></span>

## Optimal Resource Allocation over Networks

We consider the problem of congestion management in a network, and resource allocation amongst heterogeneous users, in particular human agents, with varying preferences. It has applications to transportation and telecommunication networks, smart grids, information and financial networks, labor markets, and social networks. Modeling the agents using CPT brings forward the surprising benefits of lottery-based allocations in increasing social welfare as compared to the corresponding EUT-based analysis. This conforms with the observation that lotteries help in influencing the behavior of people, which is backed by several experimental studies. Our work based on CPT analysis not only explains the above phenomenon theoretically but also provides a practical algorithm to design the optimum lottery allocations. It achieves this without actually knowing the CPT preferences of the agents through an
appropriate pricing scheme.


The network resource allocation problem has been studied before. However, CPT-based analysis allows us to capture the user’s behavior towards risk, in particular, the “lure” for a small chance of winning and the “fear” of losing, leading to better [behavior-aware system designs (BASD)]({{ 'basd/index.html' | absolute_url }}). Psychologically this is the same effect observed when people purchase lottery tickets and insurance. Furthermore, working with the general model of CPT preferences, which has inherent non-linearities present in it, requires developing new methods. These are useful more generally in designing algorithms for markets with CPT players, such as job markets, contests, financial services, etc.


<span class="anchor" id="short_video"></span>

<video width="100%" controls poster="{{ 'assets/Short_video_poster.png' | absolute_url }}">
  <source src="http://sohamphade.github.io/files/CPTtalk.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

---

In other related work, we develop similar techniques for optimal resource allocation in a scheduling framework. In particular, we consider the problem of optimal server allocation and scheduling in cloud computing systems. Current popular cloud providers employ fixed-rate pricing schemes that do not account for the delay and risk-sensitivity of the individuals. In contrast, a BASD approach would provide instant service with high certainty to a customer who is in urgent need of his job at a premium price based on the market demand, and delay the jobs of customers with reasonable wait-times with appropriately discounted prices. Our algorithm achieves this in an efficient manner that is practical to implement.



### Papers

- S. Phade and V. Anantharam (2019). “Optimal Resource Allocation over Networks via Lottery-Based Mechanisms.” *International Conference on Game Theory for Networks*, pp. 51–70. Springer, Cham
<a href="https://link.springer.com/chapter/10.1007/978-3-030-16989-3_4" target="_blank">[link]</a>
    <a href="https://arxiv.org/abs/1812.00501" target="_blank">[ArXiv]</a>

- V. Gupta, S. Phade, T. Courtade, K. Ramchandran. “Utility-Based Resource Allocation and Pricing for
Serverless Computing.” <a href="https://arxiv.org/abs/2008.07793" target="_blank">[ArXiv]</a>


---

<span class="anchor" id="section4"></span>

## Cooperative games

We propose a novel solution concept for multi-player cooperative games with characteristics that are the best of both worlds - it always belongs to the core of such games whenever it exists and satisfies certain fairness properties similar to the Shapley value.

### Papers

- S. Phade and V. Anantharam. “A Fair and Stable Solution Concept for Balanced Cooperative Games.” 


---



