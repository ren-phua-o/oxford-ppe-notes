# Dynamic Games Notes

## Exam Technique
- In dynamic Bayesian games, each candidate pure equilibrium is either a separating equilibrium or a pooling equilibrium. Each pooling equilibrium is a pooling equilibrium on some strategy. In general, upon conjecturing that an equilibrium is a separating equilibrium or a pooling equilibrium on some strategy, the details of the equilibrium can be "filled in" by sequential rationality and Bayesian beliefs.
- When drawing a game in extensive form, if there is a commitment type, draw the nodes of the commitment type (even though the commitment type has only one available action). Do not "bypass" or "omit" the node where the commitment type is called upon to act.
- In signalling games, low value types imitate high value types with probability less than $1$ because perfect imitation undermines the signal, and the signal is rewarded with probability less than $1$ because a certain reward creates strict incentive for imitation.

## Extensive Form Games
- Definition (Extensive Form Game)
	- An extensive form game is represented by a set of players $N=\{1,\ldots,n\}$, a set of histories $H$, a set of possible actions $A(h)$ at each history $h\in H$, a player assignment function $P(h):H\setminus Z\rightarrow N$ where $Z=\{h\in H:A(h)\neq\emptyset\}$ is the set of terminal histories, an information partition $\mathcal{I}$ of $H$ such that $\forall h,h'\in I\in\mathcal{I}:P(h)=P(h')\land A(h)=A(h')$, i.e. all histories in each information set $I$ in the partition $\mathcal{I}$ are assigned to the same player, and are indistinguishable to this player, and a set of payoff functions $\{u_i(z):Z\rightarrow\mathbb{R}\}_{i=1}^N$, each from the set of terminal histories to the set of rational numbers.
- Representation
	- An extensive form game can be represented by an augmented game tree. An augmented game tree is a directed graph consisting of nodes which each represent some history $h\in H$ and are each labelled with the assigned player $P(h)$, arrows which represent history-action pairs $(h,a\in A(h))$ from the node $h$ to the node $h\frown a=(h_1,\ldots,h_n,a)$, dashed lines between all nodes corresponding to histories in the same information set, i.e. $\forall h,h':\exists I\in\mathcal{I}:h,h'\in I$, and probabilities on arrows denoting prior probabilities of actions by Nature. This representation is lossless.
	- An extensive form game can be represented in strategic form. For each player, each strategy assigns an action to every information set of this player. This representation is lossy, information about the sequence of moves is lost in this representation.
	- The strategic form representation of an extensive form game can be reduced iff there are two or more equivalent strategies. This reduction is lossless.
- Relationship (Information Sets, Actions, and Strategies)
	- Each player $i$ has $\Pi_{I\in\mathcal{I}:P(h\in I)=i}|A(h\in I)|$ strategies. In other words, the number of strategies each player $i$ has is equal to the product of the number of strategies player $i$ has at each of player $i$'s information sets.

## Subgame-Perfect Equilibrium
- Motivation
	- Since an extensive form game can be represented in strategic form, and each (finite) strategic form game has a (potentially mixed) Nash equilibrium, each (finite) extensive form game has a Nash equilibrium. But Nash equilibria of extensive form games may be time inconsistent, i.e. some player's strategy, prescribed by Nash equilibrium, could be sub-optimal at some history that is off the equilibrium path.
- Definition (Subgame)
	- A subgame of some extensive form game consists of a subset $H'$ of histories of the game, where one history in this subset is the root of this subgame, and each other history in this subset is a direct or indirect successor of the root, and if history $h$ is in this subset of histories, then $\forall h':(\exists I\in\mathcal{I}:h,h'\in I)\rightarrow h'\in H'$, i.e. no information sets are only partially contained in $H'$.
- Definition (Subgame-Perfect Equilibrium)
	- A subgame-perfect equilibrium of a game is a strategy profile that induces a Nash equilibrium in every subgame.
- Kuhn's (1953) Theorem
	- Every finite extensive game with perfect information has a subgame-perfect equilibrium, obtained by backward induction.

## Perfect Bayesian Equilibrium
- Motivation
	- Some extensive form games have no subgames, so all Nash equilibria are subgame-perfect equilibria, but some such subgame-perfect equilibria are unreasonable.
- Definition (Beliefs)
	- A set of beliefs is a set of probability distributions, each corresponding to an information set, over the histories within that information set.
- Definition (Perfect Bayesian Equilibrium)
	- A perfect Bayesian equilibrium is an assessment $(\sigma,\mu)$ that consists of a strategy profile $\sigma$ and a belief system $\mu$ that satisfies sequential rationality, i.e. each player $i$'s strategy $\sigma_i$ is optimal against the strategy profile $\sigma_{-i}$ given player $i$'s beliefs, and satisfies Bayesian beliefs, i.e. at each information set, the assigned player's beliefs are consistent with Bayes' rule, prior probabilities, observed actions, and equilibrium strategies. Bayesian beliefs does not have implications for beliefs at off-equilibrium paths.
- Fudenberg and Tirole (1991) Theorem
	- Every finite extensive game has a perfect Bayesian equilibrium.

## Forward Induction
- Intuition
	- The idea of forward induction is, roughly, that at some non-singleton information set, the assigned player has some information about other players' actions (namely, the assigned player knows that other players' actions are such that the history is one of those in the information set). So the assigned player could infer something like "the other players would so choose only if they expect greater payoff from so choosing than is guaranteed by their outside option, so the histories that yield lower expected payoffs for them are implausible."

## Intuitive Criterion
- Definition (Intuitive Criterion)
	- In assigning beliefs to off-equilibrium path histories, assign zero probability to all types whose equilibrium payoff exceeds the maximum possible deviation payoff.
	- If there are no off-equilibrium-path beliefs, then the equilibrium satisfies the Intuitive Criterion.

## Divinity D1
- Definition (Divinity D1)
	- In assigning beliefs to off-equilibrium path histories $h,h',\ldots\in H$, assign zero probability to all types such that there is another type for whom there is a larger set of strategies of the assigned player $P(h)$ such that this deviation is profitable.