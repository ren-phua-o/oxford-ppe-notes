# Bayesian Games Notes

## Exam Technique
- Eliminate strictly dominated strategies (for each player-type) to simplify the payoff table when finding Bayesian Nash equilibria.
- For Harsanyi purification, the general solution technique is to solve for the payoffs to each action, find the threshold, and impose symmetry. (See 160606 Game Theory Paper Q1d.)_
- A general strategy for constructing a Bayesian Nash equilibrium in Bayesian games with a continuum of types is to conjecture that equilibrium strategies have a particular functional form, then solve for one player's best response. (See 160606 Game Theory Paper Q3f.)
- The simplest method to determine dominance in interim and/or ex ante payoffs is to inspect the respective payoff matrices.

## Bayesian Games
- Definition (Bayesian Game)
	- A Bayesian game (static game of incomplete information) is represented by a set of players $N=\{1,\ldots,n\}$, a set of states (or a set of type profiles) $\Omega$, and for each player $i\in N$, a set of actions $A_i$, a set of signals $T_i=\{t_i^1,\ldots\}$, a signal function $\tau_i$ from $\Omega$ to $T_i$, a set of beliefs $P_i=\{p_i^1,\ldots\}$ where each belief is some probability distribution over $\Omega$ associated with some signal, and a payoff function $u_i(a=\{a_1,\ldots,a_n\},\omega\in\Omega)$.
- Discussion (Bayesian Game)
	- A Bayesian game so represented can be understood as follows. First, a state $\omega\in\Omega$ is realised, then each player $i$ receives signal $t_i=\tau_i(\omega),t_i\in T_i$, then each player $i$ adjusts some prior belief, by Bayes' rule, given $t_i$, to form posterior belief $p_i$, then each player $i$ computes expected payoffs given $p_i$.
- Discussion (Signal)
	- A signal $t_i$ received by player $i$ is perfectly informative iff given this signal, player $i$ knows the state $\omega$, i.e. $\tau_i(\omega)=t_i$ and $\tau_i(\omega')\neq t_i$ for all $\omega'\in\Omega$ and $\omega'\neq\omega$.
	- A signal $t_i$ received by player $i$ is perfectly uninformative iff given this signal, player $i$ knows nothing about the state $\omega$, i.e. $\tau_i(\omega)=t_i$ for all $\omega\in\Omega$.
	- Each player's signal function is not necessarily deterministic.
	- Each player's types may be discrete or continuous, i.e. a player may have a finite number of types (signals) or an infinite number of types (signals).
- Discussion (Strategy)
	- Since, by definition, a strategy is a complete contingent plan which specifies how the player (whose strategy it is) will act in every distinguishable circumstance in which he might be called to act, a strategy in Bayesian games is signal-contingent.
	- So player $i$'s strategy in a Bayesian game can be represented as $\sigma_i(t_i)$.

## Bayes-Nash Equilibrium
- Definition (Bayes-Nash Equilibrium)
	- A Bayes-Nash equilibrium of a Bayesian game is a Nash equilibrium of the strategic form game where the set of players is $N'=\{(i,t_i):i\in N,t_i\in T_i\}$ , i.e. each player in the strategic form game is a player-type pair of the Bayesian game, the set of actions $A_{(i,t_i)}'$ of each player $(i,t_i)$ is $A_i$, and the payoff function of each player $(i,t_i)$, $u_{(i,t_i)}'(a'_{(i,t_i)},a_{-(i,t_i)}')=\int_{\omega\in\Omega}P(\omega|t_i)u_i(a_i=a'_{(i,t_i)},\sigma_{-i}(\tau_{-i}(\omega)),\omega)d\omega$, i.e. the payoff of each player $(i,t_i)$ in the strategic form game is the expected payoff of the player $i$ in the Bayesian game given his interim beliefs based on his signal $t_i$.
	- Equivalently, a Bayes-Nash equilibrium is a strategy profile of a Bayesian game $\sigma^*=(\sigma_1^*,\ldots,\sigma_n^*)$ such that $E[u_i(\sigma_i^*,\sigma_{-i}^*;t_i,t_{-i})|t_i=t_i^j]\geq E[u_i(\sigma_i',\sigma_{-i}^*;t_i,t_{-i})|t_i=t_i^j]$ for all strategies $\sigma_i'$ of player $i$ and all types $t_i^j$ of player $i$.

## Purification
- Proposition (Harsanyi Purification)
	- The probability distributions over strategies induced by the pure (Bayesian Nash) equilibria of the perturbed game converge to the distribution of the (mixed Nash) equilibrium of the unperturbed game.
- Informal Discussion
	- Let $G$ denote some strategic form game with set of $n$ players $N$, actions $A$, and payoffs $u$. Let $G'$ be the Bayesian game with set of players $N'=N$, set of states $\Omega=\{(\epsilon_1,\ldots,\epsilon_n):\epsilon_1,\ldots,\epsilon_n\in[0,x]\}$, actions $A'=A$, signals $\tau_i(\omega=(\epsilon_1,\ldots,\epsilon_n))=\epsilon_i$, prior beliefs $\epsilon_1,\ldots,\epsilon_n\sim U(0,x)$ independently, and payoffs "perturbed" by $\epsilon$. Then suppose that each player $i$ plays a pure strategy $s_i(t_i=\epsilon_i)$ where he plays one action if $\epsilon_i$ is below some threshold and another action otherwise. Then, for each player, for each action, the ex ante probability that he plays that action in the Bayesian game converges to the probability that he plays that action in the mixed Nash Equilibrium of the strategic form game.

## Global Games
- Discussion (from Eso, 2023 - Notes on Bayesian Games)
	- Suppose that the payoffs in a game are determined by a random draw from a class of games, and each player observes a noisy signal concerning which game is selected. This defines an incomplete-information game, called a global game, in which each player’s type is their received signal. Types are correlated because each signal concerns the same underlying state of nature, i.e., which game is played. In certain games, in particular, $2\times 2$ coordination games, as the noise in the player’s signals vanishes, iterated strict dominance on interim payoffs in the global game forces players to play a specific pure-strategy equilibrium — the so-called risk-dominant equilibrium, to be defined below. This is an interesting and powerful argument for selecting among multiple Nash equilibria in coordination games.
- Definition (Risk Dominant Strategy)
	- In a $2\times 2$ game an equilibrium is called risk dominant if the product of the players’ deviation losses is greater than in any other equilibrium.
	- A player’s deviation loss at a given equilibrium is the size of the decrease in his or her payoff as he or she unilaterally deviates from that equilibrium.