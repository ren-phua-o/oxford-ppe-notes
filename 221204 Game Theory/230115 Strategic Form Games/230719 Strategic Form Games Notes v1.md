# Strategic Form Games Rough Notes

## Exam Technique
- Be careful to consider domination by mixed strategies.
- Always fully describe strategies.
- Always check second-order conditions.
- Correlated beliefs and correlated mixing are in contrast to product beliefs and independent mixing.
- When constructing a correlated equilibrium, write the state space, the probability distribution, each player's information partition, and each player's strategy as a function of the state.
- The general solution technique to questions similar to the Varian model of sales is to conjecture a symmetric mixed equilibrium, denote the cumulative distribution function of the equilibrium mixed strategy, formulate payoffs in terms of the cumulative distribution function, compute payoffs at the boundaries, and equate to payoffs within the boundaries to derive the cumulative distribution function.
  
## Strategic Form Games
- Definition (Strategic Form Game)
	- A strategic form game is represented by a set of players $N=\{1,\ldots,n\}$, a set of actions $A_i$ available to each player $i\in N$, and a payoff function $u_i(a_i,a_{-i})$ for each player $i\in N$ from action $a_i\in A_i$ and other players' actions $a_{-i}\in\Pi_{j\neq i}A_j$.
- Definition (Strategy)
	- A strategy is a complete contingent (on private information/beliefs in Bayesian games, or on past actions in dynamic games) plan which specifies how the player (whose strategy it is) will act in every distinguishable circumstance in which he might be called upon to act.
- Definition (Pure Strategy)
	- In strategic form games, player $i$'s pure strategies are his actions $a_i\in A_i$.
	- Pure strategies are degenerate mixed strategies, i.e. mixed strategies that assign a probability of $1$ to one action and a probability of $0$ to all other actions.
- Definition (Mixed Strategy)
	- In strategic form games, player $i$'s mixed strategies $\alpha_i$ are probability distributions over $a_i\in A_i$.
	- $\Delta(A_i)$ denotes the set of probability distributions over $A_i$.
- Notation
	- Strategic form games can be represented in matrix (normal) form. Conventionally, player $1$ is the row player, player $2$ is the column player, player $3$ (if there is a third player) is the matrix player, and in each cell, payoff of player $1$ is given first, then player $2$, then player $3$.
	- Strategic form games can be represented in extensive form. Conventionally, player $1$ is the top level, player $2$ is the next level below, and so on.
	- Player $i$'s mixed strategy $\alpha_i$ can be denoted as $\alpha_i=p\times a_i+p'+a_i'+\ldots$ where $p,p',\ldots$ each denotes the probability of player $i$ actually choosing action $a_i,a_i',\ldots$ respectively, and $p,p',\ldots$ sum to $1$. For example, $\frac{1}{2}C+\frac{1}{2}D$ denotes the mixed strategy that consists in playing pure action $C$ with probability $\frac{1}{2}$ and playing pure action $D$ with probability $\frac{1}{2}$.
	- Player $i$'s expected payoff from a mixed strategy $\alpha_i$ given other players' (potentially mixed) strategies $\alpha_{-i}$ is denoted by $v_i(\alpha_i,\alpha_{-i})$. Player $i$'s (potentially expected) payoff from a (potentially mixed) strategy $\alpha_i$ given other players' (potentially mixed) strategies $\alpha_{-i}$ is denoted by $\pi_i(\alpha_i,\alpha_{-i})$. In other words, $\pi$ payoff notation is agnostic between pure and mixed strategies.

## Nash Equilibrium
- Definition (Best Response)
	- Player $i$'s best response $B_i(\alpha_{-i})=\{\alpha_i\in \Delta(A_i):\forall \alpha_i'\in \Delta(A_i):u_i(\alpha_i,\alpha_{-i})\geq u_i(\alpha_i',\alpha_{-i})\}$. In other words, each element $\alpha_i\in B_i(\alpha_{-i})$ weakly maximises $u_i(\alpha_i,\alpha_{-i})$.
- Discussion
	- Nash equilibrium can be understood as a stability concept. At Nash equilibrium, no player has incentive to deviate. The concept of Nash equilibrium does not explain how this equilibrium is reached.
	- Nash equilibrium can also be understood as a self-fulfilling outcome, in the sense that if each player anticipates the same equilibrium, each player (rationally) will play his part of that equilibrium.
	- Common knowledge of rationality does not imply Nash equilibrium results because players could have false beliefs (about what the other is expected to play) where there are multiple Nash equilibria.
	- A Nash equilibrium is either pure, mixed, or hybrid.
	- A Nash equilibrium is a strict Nash equilibrium iff each player is strictly worse off if he deviates.

### Pure Strategy Nash Equilibrium
- Definition (Pure Strategy Nash Equilibrium)
	- A pure strategy Nash equilibrium is an action profile $a^*=\{a_1^*,\ldots,a_n^*\}$ such that $\forall i:\forall a_i:u_i(a_i^*,a_{-i}^*)\geq u_i(a_i,a_{-i}^*)$. In other words, no player has incentive to deviate given that each other player plays his Nash equilibrium action.
- Relationship: the action profile $a^*$ is a pure strategy Nash equilibrium iff $\forall i:a_i^*\in B_i(a_{-i}^*)$.
	- Suppose that $\forall i:a_i^*\in B_i(a_{-i}^*)$, then by definition of $B_i$, $\forall i:\forall a_i:u_i(a_i^*,a_{-i}^*)\geq u_i(a_i,a_{-i}^*)$, then by definition of pure strategy Nash equilibrium, $a_i^*$ is a pure strategy Nash equilibrium.
	- Suppose that $a_i^*$ is a pure strategy Nash equilibrium, then by definition of pure strategy Nash equilibrium, $\forall i:\forall a_i:u_i(a_i^*,a_{-i}^*)\geq u_i(a_i,a_{-i}^*)$, then by definition of $B_i$, $\forall i:a_i^*\in B_i(a_{-i}^*)$.
- Relationship: if a single action profile $a^*$ survives IESDS, that action profile is the unique Nash equilibrium.
	- Suppose for reductio that a single action profile $a^*$ survives IESDS and it is not a Nash equilibrium. Then, by definition of Nash equilibrium, some player $i$ can profitably deviate from $a^*$. Then, for this player, the maximally profitable deviation $a_i'$ is not strictly dominated, this strategy, and the corresponding strategy profile $a'$ survive IESDS. So, by reductio, if a single action profile $a^*$ survives IESDS, it is a Nash equilibrium.
	- Suppose for reductio that a Nash equilibrium $a^*$ does not survive IESDS. Then, by definition of IESDS, some player's action at $a^*$ is strictly dominated. Then, by definition of Nash equilibrium, $a^*$ is not a Nash equilibrium. So, by reductio, all Nash equilibrium survive IESDS.
	- So if only one action profile survives IESDS, it is a Nash equilibrium and there are no other Nash equilibria.
- Technique: pure strategy Nash equilibria can be found by finding mutual best responses.
- Technique: pure strategy Nash equilibria can be found by "guess and check".
	- "Equilibrium candidate … fails to deviation by …."

### Mixed Strategy Nash Equilibrium
- Definition (Mixed Strategy Nash Equilibrium)
	- A mixed strategy Nash equilibrium is a strategy profile $\alpha^*=\{\alpha_1^*,\ldots,\alpha_n^*\}$ such that $\forall i:\forall \alpha_i\in\Delta( A_i):\pi_i(\alpha_i^*,\alpha_{-i}^*)\geq\pi_i(\alpha_i,\alpha_{-i}^*)$. In other words, no player has incentive to deviate given that each other player plays his Nash equilibrium action.
- Relationship: the strategy profile $\alpha^*$ is a mixed strategy Nash equilibrium iff $\forall i:\alpha_i^*\in B_i(\alpha_{-i}^*)$.
- Technique: mixed strategy Nash equilibria can be found by finding mutual best responses.
- Technique: mixed strategy Nash equilibria can be found by applying the indifference principle.
	- The mixed strategy profile $\alpha^*$ is a mixed strategy Nash equilibrium iff $\forall i:\forall a_i\in A_i$ such that $p_{\alpha_i}(a_i)=0$ $:\pi_i(a_i,\alpha_{-i}^*)<\pi_i(\alpha_i^*,\alpha_{-i}^*)$, and $\forall i:\nexists a_i\in A_i:\pi_i(a_i,\alpha_{-i}^*)>\pi_i(\alpha_i^*,\alpha_{-i}^*)$. In other words, iff each player $i$'s strategy $\alpha_i^*$ assigns zero weight to any action $a_i$ that yields a lower payoff than $\alpha_i^*$ given $\alpha_{-i}^*$, and each player $i$ has no action $a_i$ that yields a higher payoff than $\alpha_i^*$ given $\alpha_{-i}^*$.
	- The mixed strategy profile $\alpha^*$ is a mixed strategy Nash equilibrium only if $\forall i:\forall a_i\in\{a_i\in A_i:p_{\alpha_i^*}(a_i)\neq0\}:\pi_i(a_i,\alpha_i^*)=c$ where $c$ is some constant. In other words, only if each player's expected payoff from each action $a_i$ assigned positive probability by $\alpha_i^*$ is the same.
- Discussion
	- Interpretation of mixed strategy Nash equilibrium is problematic because each player who plays a mixed strategy has no incentive to randomise in any specific way over the actions in the support of the mixed strategy since each of these actions yields the same expected payoff.
	- One interpretation of mixed strategy Nash equilibrium is as a stable social configuration of actions.
	- Another interpretation of mixed strategy Nash equilibrium is as a description of other players' beliefs about each player's actions.

## Dominance
- Definition (Strictly Dominated Strategy)
	- Player $i$'s strategy $\alpha_i$ is strictly dominated iff $\exists \alpha_i'\in\Delta(A_i):\forall a_{-i}\in\Pi_{j\neq i}A_j:u_i(\alpha_i',a_{-i})>u_i(\alpha_i,a_{-i})$. In other words, iff player $i$ has some other strategy $\alpha_i'$ that yields a strictly higher payoff given any strategies $a_{-i}$ of other players.
	- Strict dominance can be defined in relation to only other players' pure strategies without loss of generality.
- Definition (Strictly Dominant Strategy)
	- Player $i$'s strategy $\alpha_i$ is strictly dominant iff $\nexists a_i'\in A_i:\exists a_{-i}\in\Pi_{j\neq i}A_j:\pi(a_i',a_{-i})\geq\pi(a_i,a_{-i})$. In other words, iff player $i$ has no other strategy $a_i'$ that yields a weakly higher payoff given some strategies $a_{-i}$ of other players.
- Definition (Belief)
	- Player $i$'s belief is denoted by $p_i(\cdot)$ where $p_i(a_{-i})$ is player $i$'s assessment of the probability that other players' play $a_{-i}$ and $\sum_{a_{-i}\in\Pi_{j\neq i}A_j}p_i(a_{-i})=1$.
- Definition (Rationality)
	- Player $i$ is rational iff player $i$ maximises $\pi_i$ given $p_i(\cdot)$.
- Relationship: a rational player never plays a strictly dominated strategy.
	- Suppose for reductio that rational player $i$ plays strategy $\alpha_i$ which is strictly dominated by $\alpha_i'$.
	- Then, $E_{p_i}(a_i)=\sum_{a_{-i}\in\Pi_{j\neq i}A_j}p_i(a_{-i})u_i(a_i,a_{-i})<\sum_{a_{-i}\in\Pi_{j\neq i}A_j}p_i(a_{-i})u_i(a_i',a_{-i})=E_{p_i}(a_i')$, where $E_{p_i}(a_i)$ denotes player $i$'s expected payoff given belief $p_i(\cdot)$, and where the inequality holds since $u_i(a_i,a_{-i})<u_i(a_i',a_{-i})$ for all $a_{-i}$ by definition of strict dominance.

### Iterated Elimination of Strictly Dominated Strategies
- Formalisation
	- Let $R_i^0=A_i$ for all players $i$.
	- Let $R_i^k\subseteq R_i^{k-1}$ be the subset of undominated actions, i.e. $R_i^k=\{a_i\in R_i^{k-1}:\nexists\alpha_i\in\Delta(R_i^{k-1}):\forall a_{-i}\in\Pi_{j\neq i}R_j^{k-1}:u(\alpha_i,a_{-i})>u(a_i,a_{-i})\}$, i.e. $R_i^k$ is the set of pure strategies in $R_i^{k-1}$ which are not strictly dominated by some (potentially mixed) strategy from $R_i^k$.
	-  Let $R_i^\infty=\bigcap_kR_i^k$ denote the set of pure strategies which survive iterated elimination of strictly dominated strategies.
	- If $R_i^\infty$ is a singleton for all $i$, the game is dominance-solvable.
- Discussion
	- For finite games, iterated elimination of strictly dominated strategies terminates in a finite number of steps.
	- For finite games, $R_i^\infty$ is independent of the order of elimination.
	- Games are not necessarily dominance-solvable, since $R_i^\infty$ is not necessarily a singleton.

### Iterated Elimination of Weakly Dominated Strategies
- Definition (Weakly Dominated Strategy)
	- Player $i$'s strategy $\alpha_i$ is weakly dominated iff $\exists \alpha_i'\in\Delta(A_i)$ such that $\forall a_{-i}\in\Pi_{j\neq i}A_j:u_i(\alpha_i',a_{-i})\geq u_i(\alpha_i,a_{-i})$ and $\exists a_{-i}''\in\Pi_{j\neq i}A_j:u_i(\alpha_i',a_{-i}'')> u_i(\alpha_i,a_{-i}'')$. In other words, iff player $i$ has some other strategy $\alpha_i'$ that yields a weakly higher payoff given any strategies $a_{-i}$ of other players, and a strictly higher payoff given some strategies $a_{-i}'$ of other players.
- Definition (Weakly Dominant Strategy)
	- Player $i$'s strategy $\alpha_i$ is weakly dominant iff it weakly dominates all other strategies $\alpha_i'$.
- Discussion
	- The strategies that survive iterated elimination of weakly dominated strategies depends on the order of elimination for some even finite, "nice" games.
	- Nash equilibria do not necessarily survive iterated elimination of weakly dominant strategies.

## Rationalisability
- Definition (Rationalisability)
	- Player $i$'s action $a_i$ is rationalisable iff it is a best response to some potentially correlated mix of other players' rationalisable actions.
	- Formally, let $Z_i\subseteq A_i$ denote the subset of player $i$'s actions that contains only rationalisable actions. Let $Z=\{Z_1,\ldots,Z_n\}$. For each player $i$, each $a_i\in Z_i$ maximises $i$'s expected payoff given some (potentially correlated) belief $p_i(\cdot)$ which assigns positive probability only to $\alpha_{-i}\in\Delta(Z_{-i})$, i.e. some potentially correlated mix of other players' rationalisable actions.
	- Equivalently, player $i$'s action $a_i$ is not rationalisable if it is not a best response to any potentially correlated mix of other players' actions. All and only rationalisable actions survive iterated elimination of unrationalisable actions.
- Relationship: all and only (correlatedly) rationalisable strategies survive iterated elimination of strictly dominated strategies.
	- Pearce's Lemma: In a two-player finite game a pure strategy is strictly dominated by another pure or mixed strategy if and only if it is not a best reply against any pure or mixed strategy of the opponent.
	- Then, by definition of rationalisability, in a two-player finite game, all and only rationalisable strategies survive iterated elimination of strictly dominated strategies.
	- Given correlated mixing, in three or more-player games, it is as if each player faces a single other player. So in any finite game, all and only rationalisable strategies survive iterated elimination of strictly dominated strategies.
- Relationship: if some player $i$'s action $a_i$ is a strictly dominant strategy, then $a_i$ is $i$'s only rationalisable action.
- Discussion
	- It is reasonable to consider an action rationalisable if it is a best response to some potentially correlated mix of other players' rationalisable actions (rather than only if it is a best response to some independent mix of other players' rationalisable actions) because players may have correlated beliefs about the mix of other players' actions for innocuous reasons. For example, one player may believe two other players are likely to choose the same action because those two attended the same business school.

## Correlated Equilibrium
- Definition (Correlated Equilibrium)
	- Let $P$ denote a joint distribution over the set of all action profiles $A=\Pi_iA_i$ and $P(a_{-i}|a_i)$ denote the probability that $a_{-i}$ is drawn from this distribution given that $a_i$ is drawn from this distribution. Then $P$ is a correlated equilibrium iff $\forall i:\forall a_i,a_i'\in A_i:\sum_{a_{-i}}P(a_{-i}|a_i)u(a_i,a_{-i})\geq\sum_{a_{-i}}P(a_{-i}|a_i)u(a_i',a_{-i})$, i.e. for each player $i$, $a_i$ (weakly) maximises $i$'s expected payoff given that each $a_{-i}$ occurs with probability $P(a_{-i}|a_i)$. In other words, iff it is weakly optimal for each player to play the action drawn from $P$ given that he believes other players' do the same.
	- An equivalent definition of a correlated equilibrium is as consisting of a set of states, a probability distribution over this set of states, for each player an information partition over the set of states, and for each player a strategy corresponding to each part of the partition.
- Technique: correlated equilibria can be found by writing the incentive constraints for each action of each player and solving simultaneously. (See Eso, 2023 - Notes on Strategic Form Games.)
- Relationship: any weighted average of two Nash equilibria is a correlated equilibrium.
- Relationship: strictly dominated strategies are played with zero probability in correlated equilibria because these are not incentive compatible.