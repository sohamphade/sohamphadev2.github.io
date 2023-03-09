---
layout: post
title: Lottery-based optimal resource allocation
permalink: /lottery_resource/
excerpt_separator: <!--more-->
tagline: "We develop the theory behind lotteries to incentivize people (eg. flight upgrades and middle-seat lotteries) and invent a lottery-based version of the TCP/IP protocol to design optimal lotteries."
type: project
imagelink: assets/lottery-flight.png
location: front
collaborators: V Anantharam (UC Berkeley)
---

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