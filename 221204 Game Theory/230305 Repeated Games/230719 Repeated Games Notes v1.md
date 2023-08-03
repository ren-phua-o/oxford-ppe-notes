# Repeated Games Rough Notes

## Exam Technique
- The general solution technique for verifying a subgame-perfect equilibrium is to check for profitable one-shot deviation.
- Common subgame-perfect equilibrium constructions include the following.
	- Grim trigger with Nash reversion.
	- Stick-carrot (potentially for multiple periods). Such a strategy profile can be a subgame-perfect equilibrium even if every player (temporarily) receives payoff lower than his minmax payoff.
	- Deviator-specific grim trigger or deviator-specific stick-carrot.
	- Stick then Nash reversion (180605 Q8)
- When required to derive minmax payoffs, apply the heuristic that some players minmax payoff is the maximum payoff that player can guarantee and the minimum payoff that other (coordinating) players can impose on him.
- The lowest sustainable total payoff in SPE is not simply the sum of minmax payoffs, because minmax payoffs are not necessarily simultaneously feasible. Check the plot of feasible and individually rational payoff vectors for this.

## Nash Equilibrium
- Definition (Repeated Game)
	- A repeated game is a game in which in each period $t\in T$ where $T$ is either finite or infinite, each player $i\in N=\{1,\ldots,n\}$ plays stage-game action $a_i\in A_i$ (where $A_i$ is the set of player $i$'s stage-game actions) and has stage-game payoff $u_i(a_i,a_{-i})$. Player $i$'s stage-game strategy $\alpha_i\in\Delta(A_i)$ is some (potentially degenerate) probability distribution over $A_i$.
	- The action profile at period $t$ is $a^t=(a_1^t,\ldots,a_n^t)$. The history at period $t$ is $h^t=(a^1,\ldots,a^{t-1})$.
	- Player $i$'s repeated game strategy is the function $\alpha_i(h^t)$ from the set of histories to the set of stage-game strategies $\Delta(A_i)$.
	- Player $i$'s repeated game payoff is the discounted sum of stage-game payoffs.
- Definition (Average Discounted Value)
	- The average discounted value $ADV$ of some stream of payoffs with present value $PV$ is given by $ADV=(1-\delta)PV$, where $\delta$ is the discount factor.
	- The average discounted value of some stream of payoffs $\pi^1=v,\ldots,\pi^k=v,\pi^{k+1}=v',\pi^{k+2}=v',\ldots$ is given by $ADV=(1-\delta^k)v+\delta^kv'$.
- Definition (Feasibility)
	- $(v_1,\ldots,v_n)$ is a feasible average discounted payoff vector of the repeated game iff $(v_1,\ldots,v_n)\in co\{(w_1,\ldots,w_n):\exists a\in A:w_i=u_i(a)\}$. In other words, $(v_1,\ldots,v_n)$ is a feasible average discounted payoff vector iff it is achievable as the payoff to some (potentially correlatedly, potentially degenerate) mixed strategy profile of the stage game.
- Definition (Individual Rationality)
	- Average discounted payoff vector $(v_1,\ldots,v_n)$ is individually rational for player $i$ iff $v_i\geq\underline{v_i}=\min_{\alpha_{-i}}\max_{\alpha_i}u_i(\alpha_i,\alpha_{-i})$, it is individually rational iff it is individual for each player $i$.
	- $\underline{v_i}$ is player $i$'s minmax payoff. This is the payoff to player $i$ given that all other players coordinate to minimise $i$'s payoff given that $i$ responds optimally.
	- Player $j$'s payoff from minmaxing player $i$ is potentially less than $\underline{v_j}$. The strategy profile that minmaxes player $i$ is potentially mixed.
	- $V^*$ denotes the set of feasible and individually rational average discounted payoff vectors.
- Theorem (Existence of Nash Equilibrium)
	- For all $v\in V^*$, there exists $\underline{\delta}<1$ such that for all $\delta>\underline{\delta}$, the infinitely repeated game has a Nash equilibrium in which each player $i$'s average discounted payoff is $v_i$.
		- This Nash equilibrium is the strategy profile under which each player, in each period, plays his part of the stage game strategy profile that yields $v$ iff no player previously deviated, and plays his part of the stage game strategy profile that minmaxes player $j$ iff some player previously deviated and $j$ was the first player to deviate.

## Subgame-Perfect Equilibrium
- Motivation (Subgame-Perfect Equilibrium)
	- If some Nash equilibrium of a repeated game is not subgame-perfect, then it involves a non-credible threat.
- Theorem (Existence of Subgame-Perfect Equilibrium, Friedman)
	- For all feasible $v$ such that for all $i$, $v_i$ is greater than $i$'s payoff in some Nash equilibrium of the stage game, for $\delta$ sufficiently close to $1$, there is a subgame-perfect equilibrium of the infinitely repeated game with average discounted payoff vector $v$. In other words, iff each player $i$ is better off under $v$ than under $i$'s Nash-worst-case, then $v$ is achievable at subgame-perfect equilibrium of the infinitely repeated game with $\delta$ sufficiently close to $1$.
- Theorem (One-Shot Deviation Principle)
	- In a repeated game with discounting, a strategy profile $\alpha$ is a subgame-perfect equilibrium iff for all histories $h^t$ (including those off the equilibrium path), for all players $i$, given each other player plays his part of $\alpha$, $i$ has no profitable one-shot deviation (i.e. deviation from $\alpha$ in only $t$ and playing his part of $\alpha$ in every subsequent period).
	- Suppose that some player $i$ has profitable deviation $\alpha_i'$ from $\alpha$ at period $t$ given history $h^t$ . Suppose further for reductio that $i$ has no profitable one-shot deviation. By construction, payoffs realised in an infinitely distant period make an infinitely small contribution to the present value of the payoff stream at $t$. Then, any profitable deviation must yield greater payoff (in present value at $t$) than $\alpha$ in a finite number of periods. Given that actions in later periods do not affect payoffs in earlier periods, any profitable deviation consists in only a finite number of (successive) deviations from $\alpha$.
	- In other words, for all profitable deviations $\alpha_i'$ that yield greater payoff than $\alpha_i$, then there is some finite number of periods $T_{\Delta}$ such that the present value of payoffs from $\alpha_i'$ within these periods exceeds that from $\alpha_i$, then, because actions in periods after $t+T_{\Delta}$ do not affect payoffs in periods $t,\ldots,t+T_{\Delta}$, for all profitable deviations $\alpha_i'$, there is some equally profitable finite deviation $\alpha_i''$ that differs from $\alpha$ in no more than $T_{\Delta}$ periods. So if $i$ has a profitable deviation, $i$ has such a finite profitable deviation.
	- Suppose that $\alpha_i''$ is some arbitrary finite profitable deviation that differs from $\alpha$ only in periods $t,\ldots,t+T_{\Delta}$. Given that there is no profitable one-shot deviation, $\alpha_i''$ is no more profitable than $\alpha_i'''$ that differs from $\alpha_i''$ only in reverting to $\alpha$ one period earlier. Then $\alpha_i'''$ is a profitable deviation from $\alpha$ that differs from $\alpha$ only in periods $t,\ldots,t+T_{\Delta}-1$. By induction, there is some profitable deviation $\alpha_i^1$ that differs from $\alpha$ only in period $t$. By reductio, if some player $i$ has profitable deviation $\alpha_i'$ from $\alpha$ at any period $t$ given any history $h^t$, $i$ has a profitable one-shot deviation.
- Definition (Grim Trigger Strategy)
	- A grim trigger strategy is a strategy under which a player plays one stage game strategy in all periods until triggered by some action profile or history, and plays another stage game strategy in all subsequent periods.
- Definition (Stick-Carrot Strategy)
	- A stick-carrot strategy is a trigger strategy under which a player plays one "cooperative" stage game strategy in all periods until deviation is observed, then the deviating player is punished for a finite number of periods before reversion to "cooperative" play.
- Theorem (Existence of Subgame-Perfect Equilibrium, Fudenberg-Maskin)
	- If $V^*$ is $n$-dimensional, then for all $v\in V^*$, there exists $\underline{\delta}<1$ such that for all $\delta\geq\underline{\delta}$, there is a subgame-perfect equilibrium of the infinitely repeated game with average discounted payoff vector $v$.
	- Informally, if the condition that $V^*$ is $n$-dimensional is not satisfied, deviation cannot be individually punished, so the existence of a subgame-perfect equilibrium is not guaranteed.
	- \[See Eso, 2023 - Lecture on Repeated Games 1, pp. 19-27 for construction of the subgame-perfect equilibrium.\]

## Renegotiation-Proof Subgame-Perfect Equilibrium
- Definition (Weak Renegotiation-Proofness)
	- A subgame perfect equilibrium of a repeated game is weakly renegotiation proof iff no subgame-perfect continuation payoff from any possible history Pareto-dominates the subgame-perfect continuation payoff from any other possible history.
	- Note that the relevant comparison is between subgame-perfect continuation payoffs and not stage game payoffs.
	- Intuitively, if some subgame-perfect continuation payoff dominates another, when the former is subgame-perfect continuation play is triggered, each player has incentive to renegotiate to the latter.
- Theorem (Existence of Renegotiation-Proof Subgame-Perfect Equilibrium)
	- \[See Eso, 2023 - Lecture on Repeated Games 2, p. 5.\]
	- "Possibility of renegotiation necessitates forgiveness such that players will not remain perpetually in a Pareto-suboptimal phase. Punishment must reward the punisher before cooperation can resume."