---
layout: post
title: Three pillars of E-Commerce?
permalink: /gt_ecommerce/
excerpt_separator: <!--more-->
tagline: A theoretical approach with three key stages - personalized recommendations, surge pricing, and data processing.
type: blog
---

E-commerce applications have enabled economic aspects 
-- such as production, distribution, and consumption of goods and services -- 
to permeate our social fabric to an extent never seen before. 
The task ahead is to bring some of the old principles from social sciences like economics and psychology, with suitable modifications, 
into the modern digital world of algorithms and technology. 
In this post, I will expand on a theoretical approach
that I believe can provide new insights in this regard.

E-commerce has not only brought the physical world to our doorstep and into our palms, but it has also vastly expanded the arena for social interactions. 
Think of any platform like Amazon, Facebook, or Youtube. 
You can do almost anything with just a few clicks. You can interact with several other individuals, exchange ideas, 
perform transactions, run your businesses, or cultivate your passions. The possibilities are unlimited.

The smooth functioning of these systems is essential. 
On the systems side, we have tasks such as inventory management and supply chain logistics. 
It requires creating and maintaining the website, platform services, and other operations that would scale as per the need. 
We have extensive infrastructures built for them that have been rapidly evolving over the past few decades. 
On the other hand, we have a massive industry catered towards marketing and maintaining customer relations, 
with a growing trend for using algorithms and social media networks to target customers.

Equally important is the interaction between the system and its users. 
A basic example of such is the search engine. 
Imagine how hard it would be to find some website over the Internet, view a particular video on Youtube, or purchase an item over Amazon without a well-functioning search engine. 

**The first stage** of interaction involves assisting the users to reach their most favorable option(s). 
Let's say each user has a *type* that describes her intent (or maybe, just the fact that there are no intentions and she is open to suggestions). 
(I have purposely used the word "type" here because, later, 
I will put this in the technical framework of mechanism design, where it is common to assume that the players have types.) 
This first stage varies from being passive to aggressive. 
The passiveness comes from it seeking to learn the user's preferences. 
And the aggressiveness comes from it attempting to alter the user's intentions. 
A simple phone directory is an example of a passive search assistant. 
On the other hand, the news feeds on social media or the video recommendations on YouTube are strong influencers and are much more aggressive. 
Usual gadgets like recommendation systems, search suggestions, and advertisements often lie somewhere on this scale based on their design.

No doubt this is a powerful mode of interaction, and we must ask ourselves the following question: 
What are its objectives and what are its effects on the system, and, in particular, on the users of this system? 
It affects the way we think, the things we believe, and the way we behave. 
There is a growing awareness of this effect, 
and many amongst us would agree that we can no more ignore these effects. 
It is time to bring in the lessons learned over centuries through real-world interactions into the world of the web. 
It is a loaded task with several people working on it. 
Studying the purpose and the effect of these systems systematically will help shed some light in this direction. 
It will help improve the design of these systems. 

**The next stage** is to decide who gets what. 
Resources are limited! 
(On a philosophical note, I believe it is one of the defining facts of our lives, 
the underlying reason for why we do most of the things we do the way we do it.) 
Coming back to our e-commerce platforms, consider something like Amazon. 
The number of items available for sale is limited. 
The resources available for shipping are scarce. 
Network bandwidth is bounded. 
Cloud storage and computing resources are limited. 
With these limitations, the system has to allocate resources according to the different preferences of its customers.

To achieve this task, we need to design a protocol for the people to signal how badly they intend to receive the resources. 
When kids fight over an item, the one who makes the most noise generally gets it. 
You make them put in efforts to gauge how badly they need the resources. 
Similarly, for elders, a commonly employed method is to make them pay — the more they are willing to pay, the more they want it. 
Another approach is to make the users put in efforts like waiting in a queue or tolerate being hammered by advertisements.
 
On the topic of advertisements, it is interesting to look at the ad-supported platforms like Youtube, Facebook, or Google in an inverted form. 
Here, the users are the ones who have limited attention spans, and the software is trying to feed them with a maximum number of adverts with the most targeted influence. 
Notice that the advertisers are the customers in this case, who are ready to pay for the limited valuable resource, namely, the users' attention. 

The best way to execute this stage is to provide the customers with their most desired options with varying charges based on the market demand. 
A simple example is that of Uber giving different service options to its customers at varying prices. 
Amazon provides multiple delivery options with varying charges. Just as recommendations were a logical answer for the vastness of search, pricing/effort extraction is a natural way to allocate resources amongst competing entities.

These pricing strategies affect the revenue of the company. 
They also determine the customer-company relations. 
A better understanding of the customers' behavioral responses will go a long way in designing these systems. 
Several answers to this study will come from economics and game theory. 
(See [Behavior-Aware System Design]({{ '/basd/index.html' | absolute_url }}) post for further discussion on this.)

**The final stage** is that of incorporating feedback. 
It includes operations like keeping track of user actions, choices, responses, and ratings; collecting and processing this data. 
The digital revolution and the emergence of companies with billions of users have made it possible to collect this data at relatively low costs. If used correctly, we can certainly benefit from it. 
It will help improve the effectiveness of the previous two stages.

<figure>
  <img src="{{'/assets/3_pillars.png' | absolute_url}}" alt="3_pillars_of_ecommerce"/>
</figure>


All this might sound similar to several articles over the Internet trumpeting cool ideas in the form of mantras or principles. 
But the question that I am interested in is whether we can translate these ideas into a proper working model that can be analyzed mathematically.


Why should we do this? Although intuition and ideas are great, they are often just the first step. 
Consider the example of constructing a bridge. 
Maybe we can build a small one across a creek using intuition and ideas. 
But to create something magnificent like the Golden Gate Bridge, we need some serious engineering tools based on concrete mathematical theories. 
We need to account for several factors such as the strength requirements, the weather conditions, 
and the soil composition to determine the materials to be used, the building's architecture, and the construction method.



The same holds for any engineering task. 
As the scale grows, the task becomes more and more complicated, and it becomes imperative to have a well-established set of assumptions and objectives to execute these tasks. 
For example, once we know what we expect from the bridge, like the amount of traffic that is supposed to pass every day, the kind of maintenance that is feasible, and the expected life span of the bridge, then, 
using mathematical models that are based on scientific laws, we can build a working model to proceed.

Theory alone certainly cannot answer everything. Here is an excerpt from Roth and Peranson (1999) that wonderfully explains this:


> Consider the design of suspension bridges. The Newtonian physics they embody is beautiful both in mathematics and in steel, and college students can be taught to derive the curves that describe the shape of the supporting cables. But no bridge could be built based only on this elegant theoretical treatment, in which the only force is gravity, and all beams are perfectly rigid. Real bridges are built of steel and rest on rock and soil and water, and so bridge design also concerns metal fatigue, soil mechanics, and the forces of waves and wind. Many design questions concerning these real-world complications cannot be answered analytically but, instead, must be explored using physical or computational models. Often these involve estimating magnitudes of phenomena missing from the simple Newtonian model, some of which are small enough to be of little consequence, while others will cause the bridge to fall down if not adequately addressed. Just as no suspension bridges could be built without an understanding of the underlying physics, neither could any be built without understanding many additional features, also physical in nature, but more varied and complex than addressed by the simple model. These additional features, and how they are related to and interact with that part of the physics captured by the simple model, are the concern of the scientific literature of engineering. Some of this is less elegant than the Newtonian model, but it is what makes bridges stand. Just as important, it allows bridges designed on the same basic Newtonian model to be built longer, stronger, and lighter over time, as the complexities and how to deal with them become better understood.

For our task of building reliable e-commerce applications, 
we have sophisticated models to study some of the components of this system. 
Thanks to the engineering sciences, we know a lot about the software and the hardware side of the problem. 
However, we are still missing a vital component, namely the human aspect. 
In all these applications, human interaction with the platform is a prime factor. It not only affects the future of that e-commerce application but also has a significant impact on society. Any theory-based approach towards designing these systems must be qualified to account for it.

<figure>
    <blockquote>
        <p>"Game theory can be defined as the study of mathematical models of conflict and cooperation between intelligent rational decision-makers." </p>
    </blockquote>
    <figcaption>—Roger B. Myerson, <cite>Game Theory - Analysis of Conflict</cite></figcaption>
</figure>

This is where game theory and economics come into the picture.  
**Mechanism design**, which is often called the engineering side of game theory, is just what we need. 
To give a very crude description of the basic premise of mechanism design, say you have some participants. 
Think of them as the users for whom we are designing the system. Each of these participants is assumed to have a specific type that describes their needs, behavior, and intentions. 
The system operator has a bunch of options that it can execute given the resource constraints. 
However, it does not know the individual types of participants. It can set up a game scenario, where the participants interact strategically with each other resulting in an equilibrium outcome depending on the appropriate equilibrium notion. 
The mechanism designer's objective is to produce the equilibrium outcome that satisfies some desired characteristics conditioned on the types of the participants, even without directly observing the types of the participants.


The most commonly known example of mechanism design is an auction. Imagine an auction house. 
Different participants have different valuations for the art piece. 
This valuation information is a part of their types. You wish to assign the item to the person who values it the most and subsequently extract the maximum possible price. 
The mechanism design that achieves such a task is the bidding protocol. 
Making the participates bid strategically to win the item at the lowest possible price not only makes them reveal information about their valuations but also allows the auctioneer to sell the item to the bidder who values it the most and correspondingly get a better price for the item. 

Different bidding protocols have different features. 
The mechanism design framework allows us to study these features systematically. 
For example, if we have certain beliefs about the valuations of the participants, then [Myerson’s optimal auction](https://pubsonline.informs.org/doi/abs/10.1287/moor.6.1.58) provides a way to design a mechanism that maximizes the revenue. 
If you want each participant to report her valuation truthfully and assign the item to the highest bidder, then one must use the [Vickrey-Clarke-Groves auction](https://en.wikipedia.org/wiki/Vickrey–Clarke–Groves_auction), which takes the form of a second-price sealed-bid auction in this case. 
Dutch auction and English auction are other examples. 
The 2020 Economics Nobel Memorial Prize was awarded to Robert B. Wilson and Paul Milgrom for their work on auction theory. It played a crucial role in the design of F.C.C. spectrum auctions.

Let us look at another example. 
Imagine a car riding service like Uber. 
Different riders have different requirements depending on their preferences and purpose of travel. 
For someone who is going to the airport to catch a flight, she will assign a lot of importance to her arrival time. 
Someone else who is not in a hurry might want the cheapest option and be ready to share her ride. 
Let us club all these preferences into the different types of users. 
Now the platform’s task is to assign rides to different users along with the routes to satisfy certain goals. 
These goals could be something like getting each individual the best service possible depending on her preferences, raising the maximum revenue possible, allocating resources in an environment-friendly manner allowing for maximum sharing as possible, or some combination of these different goals. 

Intuitively, we know that we should show multiple options to the riders with corresponding prices and let them select what they like. 
This constitutes the first two stages. 
In the first stage, you present the best options available based on the information provided by each customer, like destination, estimated time of arrival, number of passengers, etc. 
Then, in the second stage, you identify how badly each individual wants their preferences to be satisfied by asking them to pay for the services accordingly.
Having realized this, is there some way we can construct these options systematically and then based on the users’ selections assign appropriate resources? 
Can theory help us answer this question and subsequently design algorithms with some quantitative guarantees?

To some extent, the role of any mechanism is to provide a communication protocol through which the users' choices and actions can be coordinated. 
Now, in general, one could imagine a countless number of different communication schemes. 
So, where does one start to search for the so-called optimal mechanism? Fortunately, the theory of mechanism design offers some reassurance.

**Revelation principle**, one of the most fascinating results from mechanism design, roughly says that if you can design a communication protocol that has certain features under strategic play, 
then there exists an equivalent direct mechanism, where you ask each user to simply state its type and allocate resources so that the resulting protocol under strategic play has the same features. 
Think of the second-price sealed-bid auction. 
Each person submits a sealed bid for the auction item, and the person with the highest bid wins the item and pays the amount equal to the second-highest bid. 
The nice feature about this protocol is that it is in the best interest of each person to report her true valuation. 
All direct mechanisms have this property. 
The revelation principle says that you can restrict your attention to such direct mechanisms without loss of generality.

To put this in the context of our three-stage structure, it seems that a direct mechanism only consists of the second stage, 
where each user is presented with a list of options, one corresponding to each of her types, with corresponding outcomes and prices, and the user chooses one amongst them that best suits her. 
This is the one that corresponds to her type. So the revelation principle seems to suggest that it is enough to construct platforms with just the second stage.
But there are several problems with this reasoning as you might have guessed.

For instance, the number of possible types could be very large, and it is not feasible to present each user with an option corresponding to each type. 
In the case of Amazon, this would mean presenting each customer with all the items available to shop on the platform. 
This suggests why we need the first stage. 
But this is not the only reason. 
It turns out that there are certain other benefits in executing the first stage, especially when the users display human-like characteristics in their decision-making.

The revelation principle holds under fairly general settings provided that the participants' preferences follow the predictions of expected utility theory. 
It is common to employ the concept of utility functions, central to economics theory, to capture the notion of preferences for the users. 
Expected utility theory extends these preferences to account for uncertainties, coming possibly from beliefs or other intrinsic sources of randomness present in the system. 

It has been observed that human beings often do not behave according to expected utility theory. 
They often exhibit systematic deviations in their behavior and decision-making. 
Behavioral economics seeks to provide a better understanding of this phenomenon. 
Several books and articles have been written that cover the descriptive and prescriptive nature of human behavior.  
It is especially important in the context of e-commerce applications, where people interact with the platform as part of their day-to-day lives. 
As a result, they tend to show more behavioral traits in such interactions.

From a theory point of view, [cumulative prospect theory](https://en.wikipedia.org/wiki/Cumulative_prospect_theory), a leading theory for decision-making under uncertainty (another Nobel prize winning work), proposed by Daniel Kahneman and Amos Tversky, is especially useful. It has a nice mathematical formulation and accounts for several behavioral aspects in a unified form. 
It tells you how each person evaluates different outcome scenarios under uncertainty.

Working on mechanism design with cumulative prospect theory instead of expected utility theory, one quickly realizes that the revelation principle does not hold anymore. 
This is a big deal. 
There are several reasons why we want something like the revelation principle to hold. 
One of the reasons as mentioned earlier was to simplify the search over all the possible communication protocols. 
Another reason is that the direct mechanisms are inherently nice from a strategic behavior point of view. 
In particular, the optimal strategy for each person is simple — report her type. This is important because many times the participants do not have a complete picture of the system at their disposal. 
Even if they have access to it, they do not possess the necessary computation power. 
This is typical of the e-commerce platforms that we are interested in. 
The participants come in all sizes varying in their computational power. 
The nice thing about direct mechanisms is that it is easy for the small participants to act optimally (although they might not understand completely why it is optimal), and the large participants even with all their extra abilities cannot do any better.

In our paper, we establish that by introducing a stage similar to the first stage above, we can recover a form of the revelation principle even under the behavioral setting of cumulative prospect theory. 
In this stage, the system oprator acts as a mediator and sends signals to all the participating agents.
These signals perform two main functions: it allows us to simplify the options shown to the users and it also allows us to align the participants beliefs. 
These properties come up naturally from our framework that we call the **mediated mechanism design**. (See [this](https://arxiv.org/abs/2101.08722), for further details.)

The first property concerns the operability of the system. Since the interacting agents are human beings, we want to make the communication protocol in the first two stages as accessible as possible.
Just like driving a car is made accessible by giving as few controls to the driver as possible, but still maintaining a strong and complex engine, the first stage allows us to construct e-commerce applications similarly. Namely, we want a strong theory that will enable us to build a robust mechanism, and at the same time make it accessible without losing its integral parts. 

The second property is closely related to the [nudge theory](https://en.wikipedia.org/wiki/Nudge_theory) (yet another incredible contribution to behavioral economics that won the Nobel prize). It is important to realize that the first stage has the power to influence the beliefs of the user and also her type. This is the aggressive part of the first stage. 

Is it a bad thing? That depends on what is the purpose of the nudge. 
To make it clear, the sort of nudge we are interested in our paper is restricted to be truthful in nature.
Even then it is quite a powerful tool.
Although some might consider using misinformation, it often creates more problems than it intends to solve.
With a behavioral model at our disposal, we can better understand its influence and tell when something is harmful and not acceptable. 
It could suggest ways to improve the design of these mechanisms, both qualitatively and quantitatively. 
In my opinion, that is the purpose of any theory. 
Certainly, it will not be able to answer everything, but it is like the bridge example I mentioned above. 
Once we have a strong starting model to discuss and analyze the problem, we can start incorporating other more complex effects.

This brings us to the last stage, which takes the previous implementations of the mechanism and tries to improve it for the future. 
Most of the user interactions with the platform are of a repeated nature. 
This makes it possible to learn from previous interactions and improve the performance of the mechanism. 
These include several popular approaches from machine learning and reinforcement learning. 
Once we have decided the structure of our mechanism, like to sort of communications to employ, based on a better understanding of the underlying assumptions and objectives, we can then use data-driven techniques to optimize these designs.

Most of the technological developments that we see today are dominated by this third stage. 
The design of the first two stages is often taken for granted by assuming them to be something either observed, or seemingly intuitive, or based on trial and error. This approach is fast and often gets the job done. 
However, if we want to answer questions like the objectives and impacts of these mechanisms such as social impact, fairness, sustainability, environment-friendliness, and health-related concerns in a concrete manner, approaches based on well-defined theories stand a better chance of doing it.

Incorporating game theory in the design of e-commerce applications would allow us to give guarantees about the structure of our mechanism, systematically study its purpose and effects on society, and thus build better long-lasting systems.














