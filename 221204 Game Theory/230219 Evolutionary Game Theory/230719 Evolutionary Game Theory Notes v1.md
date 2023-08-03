# Evolutionary Game Theory Rough Notes

## Exam Technique
- The replicator equation can be given without proof.
- When giving a payoff table for a repeated game, if the game is symmetric, it is sufficient to give only the Row player's payoffs, but it is important to note this, and to note whether the payoffs are given in terms of present value or average discounted value.
- For differentiation of a complex term such as $p(1-p)q(1-q)$ with respect to time, apply chain rule. Let $x=\ln[p(1-p)q(1-q)]=\ln p+\ln(1-p)+\ln q+\ln(1-q)$, then differentiate $x$ with respect to time. Then $\frac{d}{dt}p(1-p)q(1-q)=\frac{de^x}{dx}\frac{dx}{dt}$. This is useful for evaluating the long run properties of a population under replicator dynamics.

## Evolutionarily Stable Strategy
- Definition (Evolutionarily Stable Strategy)
	- An evolutionarily stable strategy $\alpha^*$ of a symmetric two-player game with common payoff function $u$ is the strategy in this game such that $(\alpha^*,\alpha^*)$ is a symmetric Nash equilibrium of this game, and for all strategies of this game $\alpha'\neq\alpha^*$, if $\alpha'$ is a best response against $\alpha^*$, then $u(\alpha^*,\alpha')>u(\alpha',\alpha')$.
	- In other words, an evolutionarily stable strategy $\alpha^*$ of a symmetric two-player game with common payoff function $u$ is the strategy such that the corresponding symmetric strategy profile is a Nash equilibrium of this game, and there is no other strategy $\alpha'$ that both (1) does as well as $\alpha^*$ against $\alpha^*$ and (2) does better than $\alpha^*$ against $\alpha'$.
- Motivation (Evolutionarily Stable Strategy)
	- The concept of evolutionarily stable strategy is motivated by the phenomenon of evolution in biology. The definition captures the idea that some strategy $\alpha^*$ is evolutionarily stable if no member of a population of $\alpha^*$ players has evolutionary pressure to deviate (because some other strategy does better than $\alpha^*$ against the population), and if the population cannot be invaded by mutant $\alpha'$ players who do as well as $\alpha^*$ against $\alpha^*$ and (weakly) better than $\alpha^*$ against $\alpha'$ and so fare better than $\alpha^*$ on average.
- Relationship (Strict Nash Equilibrium and Evolutionarily Stable Strategy)
	- If $(\alpha^*,\alpha^*)$ is a strict Nash equilibrium (i.e. a Nash equilibrium at which players play mutual strict best responses), then $\alpha^*$ is a pure strategy and an evolutionarily stable strategy.
	- By definition of a strict best response, there is no $\alpha'$ that does as well as $\alpha^*$ against $\alpha^*$, then $\alpha^*$ is an evolutionarily stable strategy.
	- Suppose that $\alpha^*$ is a strict best response against $\alpha^*$. Suppose further for reductio that $\alpha^*$ is a mixed strategy. Then by definition of best response, there is no profitable deviation from $\alpha^*$, then each of the pure actions $\alpha^*$ assigns non-zero probability to has equal payoff. Then $\alpha^*$ is not a strict best response. By reductio and by generalisation, if $\alpha^*$ is a strict best response against $\alpha^*$, then $\alpha^*$ is a pure strategy.
- Result (Potential Non-Existence of Evolutionarily Stable Strategy)
	- Some symmetric games have no evolutionarily stable strategy.
- Relationship (Strict Nash Equilibrium and Evolutionarily Stable Strategy in Asymmetric Games)
	- Suppose that $G$ is an asymmetric two-player game, with players $N=\{1,2\}$, actions $A_1,A_2$, and payoff functions $u_1(a_1,a_2),u_2(a_2,a_1)$. Let $G'$ be the Bayesian game with two players $A,B$ in which with $\frac{1}{2}$ probability, $A,B$ play $G$ with $A$ as $1$ and $B$ as $2$ (where each of $A,B$ knows his role) and with $\frac{1}{2}$ probability, $A,B$ play $G$ with the roles reversed. Then, each player's strategy in $G'$ is a role-contingent strategy, and $G'$ is a symmetric two-player game.
	- Then, role-contingent strategy $(\sigma_1,\sigma_2)$ is an evolutionarily stable strategy of $G'$ iff strategy profile $(\sigma_1,\sigma_2)$ is a strict (hence pure) Nash equilibrium of $G$.

## Replicator Dynamics
- Parameters (Replicator Dynamics)
	- Suppose that $G$ is a symmetric two-player game where each player $i$ has finite number $m$ of actions $A_i=\{1,\ldots,m\}$. Define $A_{m\times m}$ as the payoff matrix such that the value $a_{ij}$ in the $i^{th}$ row and the $j^{th}$ column is the payoff $u(i,j)$, where $u$ is the common payoff function.
	- In period $t\in T=1,2,\ldots$, the number of $i$-players in the population is denoted as $n_i(t)\in\mathbb{R}$, the population size is $n(t)=\sum_{i=1}^mn_i(t)$, the proportion of $i$-players in the population is $p_i(t)=\frac{n_i(t)}{n(t)}$, and the average payoff to an $i$-playing member of the population is $\pi_i(t)=\sum_{j=1}^mp_j(t)a_{ij}$.
	- The replicator dynamic is $n_i(t+1)=n_i(t)[1+\lambda\pi_i(t)]$, where $\lambda$ is some scale factor. In words, between periods $t$ and $t+1$, the number of $i$-players increases at a rate directly proportionate to the average payoff to $i$ at period $t$.
- Analysis (Replicator Dynamics)
	- $Ap(t)$ is the $m\times1$ column matrix where the value in row $i$ is the average payoff to $i$-players at period $t$. $p(t)Ap(t)$ is the $1\times 1$ matrix where the single value is the average payoff in the population. Then, from period $t$ to period $t+1$, the growth rate of $i$-players is $\lambda[Ap(t)]_i$ and the growth rate of the population is $\lambda p(t)Ap(t)$.
	- $n_i(t+1)=n_i(t)(1+\lambda[Ap(t)]_i)$.
	- $n(t+1)=n(t)(1+\lambda p(t)Ap(t))$.
	- $p_i(t+1)=\frac{n_i(t+1)}{n(t+1)}=\frac{n_i(t)(1+\lambda[Ap(t)]_i)}{n(t)(1+\lambda p(t)Ap(t))}\approx p_i(t)[1+\lambda([Ap(t)]_i-p(t)Ap(t))]$.
- Result (Replicator Equation)
	- $\dot{p_i}=\frac{dp_i(t)}{dt}\approx p_i(t+1)-p_i(t)=\lambda p_i(t)([Ap(t)]_i-p(t)Ap(t))$.
	- In words, the proportion of $i$ players increases at a rate proportionate to (1) scale factor $\lambda$, (2) the prevailing proportion $p_i(t)$, and (3) the difference between the average payoff to $i$ and the average payoff in the population $[Ap(t)]_i-p(t)Ap(t)$.
	- In zero-sum games, average payoff is zero, so the replicator equation simplifies to $\dot{p}_X=p_X[Ap]_X$, where $X$ is some strategy and $A$ is the payoff matrix.
- Result (Replicator Equation with Two Strategies)
	- Where $m=2$, $\dot{p_i}=p_i(t)(1-p_i(t))([Ap(t)]_1-[Ap(t)]_2)$, supposing $\lambda=1$.
	- Intuitively, the proportion of $i$-players increases iff $i$-players do better than $j$-players.
- Definition (Basin of Attraction)
	- The basin of attraction of some distribution within a population is the set of distributions that converge to that distribution under the replicator (or other) dynamic.
- Relationship (Nash Equilibrium and Replicator Dynamic)
	- Each Nash equilibrium corresponds to an absorbing state (from which, when there are no shocks or errors the population does not evolve away from).
- Relationship (Evolutionarily Stable Strategy and Replicator Dynamic)
	- Each evolutionarily stable strategy corresponds to a stable absorbing state under the replicator dynamic. An absorbing state is stable iff it is restored after a small shock, and (equivalently) has a non-singleton (e.g. $[0.1,0.2]$) basin of attraction.
- Relationship (Risk Dominance and Replicator Dynamic)
	- The risk dominant evolutionarily stable strategy corresponds to the absorbing state with the largest basin of attraction under the replicator dynamic.
- Interpretation (Replicator Dynamics)
	- The evolutionary interpretation of the replicator dynamic maps payoffs to reproductive fitness. The economic interpretation maps replication to imitation and exit.
- Definition (Monomorphic Population)
	- A monomorphic population is a population in which all members play the same (potentially mixed) strategy.
- Definition (Polymorphic Population)
	- A polymorphic population is a population in which members play different strategies.

## Best Response Dynamics
- Parameters
	- In each period, a randomly selected player updates his strategy to best respond to the distribution of strategies in the population.
- Definition (Absorbing State)
	- An absorbing state is a distribution of strategies in a population such that, under the best response (or other) dynamic, if realised in period $t$, is maintained in all subsequent periods.
	- It is not natural to consider absorbing states under the replicator dynamic since such "stable" distributions are never (precisely) realised but merely approached.
- Relationship (Absorbing State and Nash Equilibrium)
	- All and only absorbing states under deterministic best response dynamics correspond to a pure Nash equilibrium of symmetric game played. Mixed (or hybrid) Nash equilibrium do not correspond to absorbing states because each player is indifferent between the strategies mixed over, so with non-zero probability, the updating player changes his strategy hence the state changes from one period to the next.

### Stochastic Best Response Dynamics
- Parameters
	- In each period, a randomly selected player, with probability $1-\epsilon$ updates his strategy to best respond to the distribution of strategies in the population, and with probability $\epsilon$ updates his strategy to one that is not such a best response.
- Result (Long Run Probabilities)
	- In the long run, the probability that $n$ players play $a$ in any period converges to a constant probability.
	- In the long run, the proportion of periods in which $n$ players play $a$ converges to a constant proportion.
	- In the long run, populations remain at or near absorbing states under deterministic best response dynamics, and occasionally move between absorbing states as a result of "mistakes". Absorbing states with "larger" basins of attraction require more mistakes to "escape", hence populations remain at such absorbing states longer than they remain at those with "smaller" basins of attraction. The system remains at or around the risk-dominant ESS in the vast majority of periods.
	- Long run behaviour is independent of the initial conditions.
- Definition (Stochastic Stability)
	- The absorbing state under deterministic best response dynamics for which the minimum number of "mistakes" is necessary to "escape (to another absorbing state)" is the greatest is the unique stochastically stable equilibrium.
- Relationship (Risk Dominance and Stochastic Stability)
	- If some symmetric pure strategy Nash equilibrium is risk dominant, then the corresponding strategy is the unique stochastically stable equilibrium under stochastic best response dynamics given a sufficiently large population.
- Evaluation (Risk Dominance)
	- It is not clear that risk-dominance is appropriate in economic contexts rather than Pareto-dominance. Nor that stochastic best response dynamics are a better justification for risk-dominant equilibrium play than global games.