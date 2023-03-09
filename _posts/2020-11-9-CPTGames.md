---
layout: post
title: Game Theory and Market Design when Agents have Cumulative Prospect Theory Preferences
permalink: /cptgames/
excerpt_separator: <!--more-->
tagline: Cumulative prospect theory, which has enjoyed great empirical success, is an equally powerful tool when it comes to making theoretical advancements in behavioral game theory and mechanism design.
type: blog
---


In this project, we systematically study game-theoretic settings (in particular, non-cooperative games) when the players' preferences are modeled using [cumulative prospect theory (CPT)](https://en.wikipedia.org/wiki/Cumulative_prospect_theory).
CPT is a generalization of expected utility theory (EUT) and one of the leading decision theories to model human preferences when faced with uncertainty. It was proposed by [Daniel Kahneman](https://en.wikipedia.org/wiki/Daniel_Kahneman) and [Amos Tversky](https://en.wikipedia.org/wiki/Amos_Tversky) for which Kahneman received the [Nobel Memorial Prize in Economic Sciences](https://www.nobelprize.org/prizes/economic-sciences/2002/kahneman/facts/). 
There has been a growing discussion concerning the benefits (and limits) of using CPT in game theory and economics. 
In fact, in the [paper](https://authors.library.caltech.edu/80314/) "Prospect theory in the wild: Evidence from the field", [Colin F. Camerer](https://en.wikipedia.org/wiki/Colin_Camerer) concludes:

> "there is no good scientific reason why it (prospect theory) should not replace expected utility in current research, and be given prominent space in economics textbooks."


What better place to begin this endeavor than to study the notions of equilibrium that have been central to game theory and economic analysis!
In our [paper](https://pubsonline.informs.org/doi/abs/10.1287/deca.2018.0378?casa_token=VFyCgbBb3GUAAAAA:_ZSTZZMeUPrjrEpwSSAuQ-OT_ujm2xyDzaM_XApEUKUQX2MYZMbu4Xxlw7M18VG8ityON1PeXQ) titled "On the Geometry of Nash and Correlated Equilibria with CPT Preferences", we take the notions of CPT Nash equilibrium and CPT correlated equilibrium defined by [Kerim Keskin](https://sites.google.com/site/kerimkeskin) as our starting point and establish several geometric properties of these equilibrium notions. 
We explore questions such as the convexity and the connectivity properties of the correlated equilibria set, and the relation between the Nash equilibria and the correlated equilibria. 
For example, under EUT, it was known that the set of all correlated equilibria is a convex polytope. 
Keskin (2016) showed that this property need not hold under CPT. 
We prove that it can, in fact, be disconnected (if you are curious, check out the construction of an example in section 4 of the [paper](https://pubsonline.informs.org/doi/abs/10.1287/deca.2018.0378?casa_token=VFyCgbBb3GUAAAAA:_ZSTZZMeUPrjrEpwSSAuQ-OT_ujm2xyDzaM_XApEUKUQX2MYZMbu4Xxlw7M18VG8ityON1PeXQ)).
Nonetheless, certain properties like the Nash equilibria all lying on the boundary of the correlated equilibria set (proved by Nau et al. (2004)) continues to hold true,
although they require new proof techniques.


These new theoretical phenomena bring out some of the important distinctions resulting from CPT modeling.
They have practical implications for the design of experiments for learning the unknown game structures.
For example, in modern online advertising, the internal working of the ad-placement algorithms is typically unknown to the customers. 
Knowledge about the structure of the equilibria, especially under presumably more accurate behavioral models, would benefit the design of experiments and simulations.
They can also help in suggesting system improvements or policy changes such as advertising strategies, cybersecurity, or military tactics -- *like [WOPR from WarGames](https://en.wikipedia.org/wiki/WarGame)!*

<!-- 
| ![wargames movie image]({{'/assets/wargames.jpg' | absolute_url}}) | 
|:--:| 
| *Space* |
--->


<!--
<figure>
  <img src="{{'/assets/wargames.jpg' | absolute_url}}" alt="my alt text"/>
  <figcaption>The fictional US military supercomputer, War Operation Plan Response (WOPR), was programmed to simulate the possible outcomes of a nuclear war.</figcaption>
</figure>
--->




Building on this, we consider the setting of learning in repeated games in the [paper](https://arxiv.org/abs/1804.08005) "Learning in Games with Cumulative Prospect Theoretic Players". 
The literature on learning in games provides an alternative explanation to the equilibrium notions as a long-run outcome in repeated games with mild rationality assumptions on the players. 
They are especially important from a behavioral perspective where players have limited computational powers.
We consider the [celebrated theorem](https://www.amazon.science/latest-news/amazon-economist-test-of-time-award-acm-conference-economics-computation) of [Rakesh Vohra and Dean Foster](https://www.sciencedirect.com/science/article/abs/pii/S0899825697905959) on the convergence of the empirical average of the action play to the set of correlated equilibria when players make calibrated forecasts and respond with myopically optimal actions.
One soon realizes that the notion of CPT correlated equilibrium, as defined by Keskin, is not enough to capture this result.
But instead, we need an appropriate convexification of this set that we call the mediated CPT correlated equilibrium.


In a correlated equilibrium, the mediator is assumed to recommend an action to each player to play.
We introduce the notion of mediated games in which the mediator is allowed to send signals from more general sets.
This is a specific type of game with communication as introduced by [Myerson](https://en.wikipedia.org/wiki/Roger_Myerson).
The mediated CPT correlated equilibria are then the Bayes-Nash equilibria of this mediated game.
Since the mediated CPT correlated equilibria are more general than the CPT correlated equilibria we get that the revelation principle in the context of correlated equilibria does not hold under CPT preferences.


Calibrated learning is one form of learning in games.
More generally, the result on the convergence to correlated equilibria is closely related to the notion of no-regret learning in games.
We prove that the set of CPT correlated equilibria is not approachable in the Blackwell approachability sense.
These results strongly suggest that the notion of mediated CPT correlated equilibrium is the appropriate notion to consider in this context.


A major revelation in the previous study is that: **The Revelation Principle Fails under CPT!**
A natural question is what happens in mechanism design where the revelation principle has played a fundamental role.
As suspected we observe that the revelation principle fails in mechanism design when agents have CPT preferences.
In the [paper](https://arxiv.org/abs/2101.08722) "Mechanism Design for CPT Agents: A General Framework and the Revelation Principle", we develop an appropriate framework that we call mediated mechanism design that allows us to recover the revelation principle under certain settings.


The premise of a typical mechanism design scenario comprises a bunch of agents each having a private type consisting of their private information and preferences over the outcomes.
There is a system operator (or a principal) who controls the implementations in the system but cannot directly observe the private types of players.
To achieve optimal implementations conditioned on the types of the players, the system operator designs a communication protocol where the players can interact strategically in the resulting game.
This allows the system operator to elicit information about the private types of the players.
As an example, think of auctions.
The [second-price sealed-bid auctions](https://en.wikipedia.org/wiki/Vickrey_auction) incentivize the players to reveal their private values truthfully, and the item is allocated to the player with the highest value at the second-highest bid.


For a modern application, consider ride-hailing services such as Uber or Lyft.
These apps present the customers with several options such as premium rides, shared rides, economy rides, etc.
The purpose of these options is to elicit the preferences of the customers and provide optimal services.
These systems have inherent uncertainties, and it is essential to account for the customers' behavior towards such uncertainties.
The CPT-based analysis reveals that if we add a stage where each customer is sent a private message before she makes her option selection, then we can get improved results.
For example, these messages could take the form of selecting a customer at random to receive priority service or discounted pricing.
Such messages play the role of nudges that help in aligning the beliefs of the players for optimal service provisioning.


We already observe such [nudges](https://en.wikipedia.org/wiki/Nudge_theory) and incentives being used around us. 
But a theory explaining these practices is still in an infant stage.
Our mediated mechanism design framework is a very promising direction at explaining these observations theoretically and improving the design of these systems.
Mechanism design is commonly referred to as the engineering side of game theory. These theoretical and methodological results can have substantial implications for the design of [behavior-aware systems]({{ '/basd/index.html' | absolute_url }}) such as online marketplaces and social networks.


There is an important common thread that runs through each of the above studies.
CPT preferences do not satisfy something called the betweenness property.
To understand this, let us consider a thought experiment.


> Suppose you are presented with two lotteries:
> 
> 1. You win $20,000 with a 34% chance and nothing with a 66% chance.
>
> 2. You win $30,000 with a 17% chance and nothing with an 83% chance.
>
>	Which lottery would you choose? 
>
>	Now consider the following third lottery:
>
> 3. You win $30,000 with a 1% chance, $20,000 with a 32% chance, and nothing with a 67% chance.
>
>	Would you prefer this lottery over the previous two lotteries?


Most people strictly prefer lottery 1 over lottery 2. But when asked about lottery 3, they choose it over the previous two lotteries. Now notice that lottery 3 can be thought of as a compound lottery of lottery 1 and lottery 2. Suppose you receive lottery 1 with a 16 in 17 chance and lottery 2 with a 1 in 17 chance. Then the compound lottery, if reduced to a single lottery, is exactly lottery 3.
Thus we observe that people might prefer to actively randomize over their options.
In the above setting, lottery 1 is a less risky gamble with a lower reward, and lottery 2 is a more risky gamble with a higher reward.
A risk-averse person would typically thus prefer lottery 1 over lottery 2.
However, when considering lottery 3, this person still perceives it to be low risk but is lured towards the 1% chance of winning a higher reward.
This explains the desire to go for lottery 3.


The nice thing about CPT preferences is that it neatly captures this effect through the probability weighting functions that overweight small percentages.
Building upon the idea that the players might prefer to actively randomize over their actions, we consider mixed strategies in non-cooperative games from a new perspective.
We refer to such actively mixed-strategies as black-box strategies.


Traditionally, mixed actions have been considered from two viewpoints, especially in the context of mixed-action Nash equilibrium. According to the first viewpoint, these are conscious randomizations by the players – each player only knows her mixed-action and not its pure realization. The notion of black-box strategies captures this interpretation of mixed-actions. According to the other viewpoint, players do not randomize, and each player chooses some definite action. 
But the other players need not know which one and the mixture represents their uncertainty, i.e., their conjecture about her choice. 

Under CPT, these two interpretations get nicely untangled, and we get four different concepts of Nash equilibria depending on whether we allow randomization in each of the interpretations.
In the [paper](https://arxiv.org/abs/2004.09592) titled "Black-box Strategies and Equilibrium for CPT Players", we develop these four notions and study their properties such as existence and relation to each other.


Cumulative Prospect Theory has several insights to offer. We must explore these theoretical ideas along with the experimental advances in behavioral game theory. 
We are at a fascinating juncture in this field, where theory and practice can assist each other in achieving something remarkable!



### Further Reading

- Camerer, C. F. (1998). Prospect theory in the wild: Evidence from the field.

- Keskin K (2016) Equilibrium notions for agents with cumulative prospect theory preferences. *Decision Analysis*. 13(3):192-208.

- Phade, S. R., & Anantharam, V. (2019). On the geometry of Nash and correlated equilibria with cumulative prospect theoretic preferences. *Decision Analysis*, 16(2), 142-156.

- Nau R, Canovas SG, Hansen P (2004) On the Geometry of Nash equilibria and correlated equilibria. *Internat. J. Game Theory* 32(4):443-453.

- Foster, D. P., & Vohra, R. V. (1997). Calibrated learning and correlated equilibrium. *Games and Economic Behavior*, 21(1-2), 40.

- Hart, S., & Mas‐Colell, A. (2000). A simple adaptive procedure leading to correlated equilibrium. *Econometrica*, 68(5), 1127-1150.

- Fudenberg, D., Drew, F., Levine, D. K., & Levine, D. K. (1998). *The theory of learning in games* (Vol. 2). MIT press.

- Phade, S. R., & Anantharam, V. (2018). Learning in Games with Cumulative Prospect Theoretic Preferences. *arXiv preprint* arXiv:1804.08005.

- Myerson, R. B. (2013). *Game theory*. Harvard university press.

- Aumann, R., & Brandenburger, A. (1995). Epistemic conditions for Nash equilibrium. *Econometrica: Journal of the Econometric Society*, 1161-1180.

- Phade, S. R., & Anantharam, V. (2020). Black-Box Strategies and Equilibrium for Games with Cumulative Prospect Theoretic Players. *arXiv preprint* arXiv:2004.09592.

