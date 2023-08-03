# Mechanism Design Notes

## First Price Auction
- Result (Under-Reporting Valuations at Nash Equilibrium)
	- In a first price auction, bidders have incentive to shade their bids below their valuations. The trade off that each bidder faces is between a higher probability of winning the auction and a lower surplus in the event of winning the auction. A bid equal to valuation wins the auction with relatively high probability, but yields zero surplus in the event of winning (and in the event of losing). A lower bid wins the auction with lower probability, but yields positive surplus in the event of winning.

## Vickrey-Clarke-Groves Mechanism
- Definition (Social Decision Problem)
	- Suppose that there is a set $X$ of social outcomes $x$, there is a set of agents $N=\{1,\ldots,N\}$, and each agent $i$ has utility in monetary terms $u_i(x,\theta_i)+p_i$, where $\theta_i\in\Theta_i$ is the private type of agent $i$ and $p_i$ is the transfer received by agent $i$. Then a social decision problem is the problem $\max_{x\in X}\sum_{i\in N}u_i(x,\theta_i)$.
- Definition (Socially Efficient Decision Rule)
	- The socially efficient decision rule is the function $x^*$ that maps each state $\theta=(\theta_1,\ldots,\theta_n)$ to some social outcome $x$ such that $x^*(\theta)=\arg\max_{x\in X}\sum_{i\in N}u_i(x,\theta_i)$.
- Definition (Efficient Mechanism Design)
	- An efficient mechanism under is a mechanism for implementing the socially efficient decision rule without directly observing the state $\theta$.
- Definition (Private Values)
	- Agents have private values iff for each agent $i$, $u_i$ is a function of $x$ and $\theta_i$ only (and not a function of $\theta_j$ for $j\neq i$). If for some agent $i$, $u_i$ is a function of $\theta_j$ for $j\neq i$, then agents have interdependent values.
- Definition (Vickrey-Clarke-Groves Mechanism)
	- The Vickrey-Clarke-Groves mechanism is the following. Each agent $i$ reports a type $\hat{\theta_i}$. Denote $\hat{\theta}=(\hat{\theta_1},\ldots,\hat{\theta_n})$. Choose $x=x^*(\hat{\theta})$ and for each player $i$ set $p_i=p_i^*(\hat{\theta})=\sum_{j\neq i}u_j(x^*(\hat{\theta}),\hat{\theta_j})-\pi_i(\hat{\theta_{-i}})$, where $\pi_i$ is any function of $\hat{\theta_{-i}}$, i.e. of each other player's reported type.
	- In other words, each player receives a transfer equal to the total gross utility of other players at the socially efficient outcome given the reported state less some amount that is independent of that player's action.
- Theorem (Truthful Reporting is Weakly Dominant Under Any Vickrey-Clarke-Groves Mechanism)
	- Under the Vickrey-Clark-Groves mechanism, each player $i$'s payoff is equal to the sum of (1) $i$'s gross utility $u_i(x^*(\hat{\theta}),\theta_i)$, (2) the total gross utility of other players at the socially efficient outcome given the reported state $\sum_{j\neq i}u_j(x^*(\hat{\theta}),\hat{\theta_j})$, and (3) some amount that is independent of player $i$'s action $\pi_i(\hat{\theta_{-i}})$. Then, each player's maximisation problem reduces to $\max_{\hat{\theta_i}}u_i(x^*(\hat{\theta}),\theta_i)+\sum_{j\neq i}u_j(x^*(\hat{\theta}),\hat{\theta_j})$.
	- By definition of $x^*$, for all $\theta_i,\hat{\theta_{-i}},x$, $u_i(x^*(\theta_i,\hat{\theta_{-i}}),\theta_i)+\sum_{j\neq i}u_j(x^*(\theta_i,\hat{\theta_{-i}}),\hat{\theta_j})\geq u_i(x,\theta_i)+\sum_{j\neq i}u_j(x,\hat{\theta_j})$. In other words, for all types $\theta_i$ of player $i$, reports $\hat{\theta_{-i}}$ of other players, $x^*(\theta_i,\hat{\theta_{-i}})$ weakly maximises total gross payoff given state $(\theta_i,\hat{\theta_{-i}})$.
	- Then $\hat{\theta_i}=\theta_i$ solves player $i$'s optimisation problem. Truthful reporting is weakly dominant.
- Definition (Pivot Mechanism)
	- The pivot mechanism is the instance of the Vickrey-Clarke-Groves mechanism where $\pi_i(\hat{\theta_{-i}})=\max_{x\in X}\sum_{j\neq i}u_j(x,\hat{\theta_j})$, i.e. the maximum total gross utility of other players given the reported state. Then, each player pays an amount equal to the maximum total gross utility of other players given the reported state less the actual total utility of other players given the reported state. Informally, this is the externality that the presence of each player imposes on all other players.

## Matching
- Definition (Stable Pairing)
	- A stable pairing is a pairing of participants such that there is no participant on one side of the market $a_i$ (paired with $b_i$) who would prefer some other participant $b_{j\neq i}$ (paired with $a_j$ on the other side who also prefers $a_i$.
- Definition (Gale-Shapley Deferred Acceptance Algorithm)
	- One side of the market $A$ is selected to make initial demands. Each participant $a_i$ on this side of the market chooses his most preferred participant $b$ on the other side $B$. Then, each participant $b_i$ on side $B$ chosen by multiple $a$ provisionally chooses one of these participants (and rejects the rest). Then each rejected $a$ chooses his most preferred $b$ from those that have not yet rejected him. Repeat $B$-choosing and rejected-$A$-choosing until a complete pairing is obtained.
- Results (Gale-Shapely Deferred Acceptance Algorithm)
	- Truthful reporting yields the stable pairing that is optimal for the side that makes the initial demands.
	- Truthful reporting is strictly dominant for the side that makes the initial demands.
	- Manipulation by the side that receives the initial demands is possible.
	- If there are multiple stable pairings, there is no stable pairing algorithm that is strategy-proof.