# Agent-based-Modeling

### What is it ?
Agent-based models are computer simulations that are used to investigate the interactions between different elements, such as people, objects, places, and time.

These models are constructed from the bottom up, meaning that individual agents (often people in the field of epidemiology) are given specific attributes.
The agents are programmed to behave and interact with each other and their environment in certain ways, and these interactions can lead to emergent effects that may differ from the effects of individual agents.

### Advantages
Agent-based modeling differs from traditional methods, such as regression analysis, in that it allows for the study of complex systems that exhibit non-independence among individuals and feedback loops in causal mechanisms.
Unlike traditional methods, agent-based modeling is not limited to observed data and can be used to model counterfactual situations or experiments that may be impossible or unethical to conduct in the real world.

### Limits
However, agent-based modeling has some limitations, such as the difficulty in finding data parameters (such as the reproductive rate for infectious diseases) in the literature and the difficulty in assessing the validity of the model, especially when modeling unobserved associations.

### Conclusion
Agent-based modeling is a useful tool for evaluating the impacts of exposures on outcomes, particularly when interrelatedness, reciprocity, and feedback loops are known or suspected to exist or when real-world experiments are not possible.

# My agent-based model

### How to test it ?

1. Download the free NetLogo software from https://ccl.northwestern.edu/netlogo/index.shtml
2. Download the file [Word of Mouth Game.nlogo](https://github.com/timdgn/Agent-based-Modeling/blob/main/Word%20of%20Mouth%20Game.nlogo) from this repository
3. Open the file with NetLogo and play with the parameters to simulate the population

### Why this model ?

This idea of this simple model came in my mind because of a smartphone game named Homescapes (a Candy-Crush-like) I played a lot.

### How it works

This model describes a population of smartphone owners of any age (No, not only 50 years old women play candy-crush-like games in public transportation).

A basis of gamers can talk about the game to the others they meet and convert them to be gamers too.
The gamers can be bored by the game, so they stop playing it for some days.
Bored people can then play it again, if a good friend convinces them to do so !

### How to use it

- "number-of-persons" sets the number of persons in the population.
- "proba-initial-gamers" sets the percentage of the population who play the game at the beginning of the simulation.
- "proba-convert-to-gaming" sets the probability that someone convinces someone else to play the game.
- "proba-to-be-bored" sets the probability for someone to be bored by the game.
- "time-to-be-bored" is the days to pass after which a gamer gets bored of the game, if "proba-to-be-bored" lets him be bored.
- "bored-period" sets the days after which a bored person stops to be bored, and can be convinced again to play the game.

A live update of the % of gamers and bored persons is shown.

### Things to notice

The model stops after 2'000 days, or if:

- There is no more susceptible gamers (blue)
OR
- There is no more gamers (green) AND bored gamers (red)

### Things to try

A pretty much realistic configuration is the following:

- "number-of-persons" = 500
- "proba-initial-gamers" = 0.05
- "proba-convert-to-gaming" = 0.10
- "proba-to-be-bored" = 0.50
- "time-to-be-bored" = 30
- "bored-period" = 20

We can see that the % of gamers flows between 10 and 20%, which is exactly around the official user retention of the game Homescapes after 1 month:
"Most importantly, after one month, Homescapes retains 14% of players. That’s outstanding. The average 30-day retention for the top 2% of casual games is 13%."

Source:
https://www.blog.udonis.co/mobile-marketing/mobile-games/homescapes-analysis#fromHistory

### What can be enhanced

- The faster the gamers are bored by the game, the lower is their probability of playing the game again, and the same for the probability of convincing other people.

- A not-fully-connected friendship network can be built: Close friends and friend-of-a-friend (with strong links in the network) would have a better chance to convince each other to be gamers. The days during which a gamer plays the game should be randomly set, and if a player plays the game only 1 day, it ends any existing relationship with the person who told him about the game (he's blaming the person for the bad recommandation).
