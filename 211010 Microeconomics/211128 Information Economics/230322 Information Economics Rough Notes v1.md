# Information Economics Rough Notes
- These notes are incomplete. The sections of this topic that have been excluded from these notes are made redundant by the Information Economics topic from Microeconomic Analysis.

## Miscellaneous Notes
- The equilibrium concept in the Akerlof model of adverse selection is general equilibrium. This entails that aggregate demand is zero at the equilibrium prices. Then, if, for example, there are two buyers with common valuation greater than the valuation of the one seller, then equilibrium price equal to the buyers' common valuation such that buyers are indifferent.
- In the Akerlof model, the market unravels from the top, so consider prices in decreasing order, with the first price being such that the highest quality (and the rest) are sold, the second price being such that the second highest quality (and worse qualities) are sold, and so on.
- An outcome in the Akerlof model is some allocation, and does not include any description of prices or transactions.
- Agency cost is equal to the risk premium associated with the lottery faced by an agent who exerts high effort.
- A principal incurs an agency cost in inducing high effort because a variable wage scheme is required to induce high effort (by the incentive constraint), then the risk-averse agent bears some risk and must be compensated for risk-bearing by a higher expected wage (such that the participation constraint continues to hold). This increase in the expected wage is the risk premium of the lottery associated with high effort, this is the agency cost.
- In principal-agent problems, both the participation constraint and the incentive constraint bind. Any contract such that the participation constraint does not bind fails to deviation by reducing payoff in the unfavourable outcome. If the incentive constraint does not bind, the principal can reduce both risk and expected wage such that the participation constraint remains satisfied.

## Adverse Selection
- Definition (Adverse Selection)
	- Adverse selection describes a situation of asymmetric information where informed participants selectively participate in exchanges.

### Adverse Selection in Goods Markets (Akerlof)
- Parameters
	- A single seller $S$ has a single unit of good of quality $q$ which is randomly distributed, a single buyer $B$ has valuation $v=mq$, where $m>1$ is some multiple, for a unit of quality $q$. If trade occurs at price $p$, $S$'s payoff is $p-q$ and $B$'s payoff is $v-p$. If trade does not occur, each player's payoff is normalised to $0$. Suppose for simplicity that $q\sim U(0,1)$ and that $m=1.5$.
- Analysis
	- Suppose that $S$ accepts some price $p$, then by common knowledge of rationality, $B$ knows $q\leq p$, then given $q\sim U(0,1)$, $E(q|q\leq p)=\frac{p}{2}$, then $B$'s expected payoff from buying at $p$ is $mE(q|p\leq q)-p=-\frac{p}{4}$ and $B$ does not buy.
- Result
	- No trade occurs.
- Discussion
	- Generally, markets where adverse selection occurs unravel from the top. There may be multiple equilibria. Equilibrium price within a range lies at the top of the range if buyers outnumber sellers (hence sellers have "bargaining power") and at the bottom of the range if sellers outnumber buyers.

### Adverse Selection in Insurance Markets
- Parameters (Homogenous Agents)
	- Each of a large number of homogenous agents has wealth $w$ and faces monetary loss $K$ with probability $p$. Each agent is offered insurance at premium $\pi$ and chooses coverage $Q$. The agent pays cost $\pi Q$ to the insurer, and in the event that the monetary loss occurs, the insurer pays $Q$ to the agent. Each agent has risk-averse expected utility preferences.
	- Suppose that the market for insurance is competitive and insurers are risk-neutral, then (by the Bertrand result), each insurer offers each agent actuarially fair insurance, i.e.  $\pi=p$.
- Analysis
	- Formulate each agent's final wealth as a $Q$-contingent lottery $L(Q)$. Then formulate each agent's expected utility as a function of $Q$, $U(L(Q))$ and maximise with respect to $Q$.
- Result
	- Each agent fully insures, i.e. $Q^*=K$. If $\pi>p$, then it can be shown graphically that $Q^*<K$. \[See Eso, 2022 - Lecture on Information Economics 1, p. 11\]
- Parameters (Heterogenous Agents with Private Types)
	- Suppose instead that agents are heterogenous. Each agent is either type $L$ or type $H$. Type $L$ agents face this loss with probability $p_L$ and type $H$ agents face this loss with probability $p_H$, where $p_H>p_L$. The proportion of type $L$ agents is $\lambda$. Each agent's type is privately known and not observable by insurers.
- Result
	- Insurance at $\pi_L=p_L$ and $\pi_H=p_H$ cannot be sustained in equilibrium. It can be shown graphically that each type $H$ agent is strictly better off choosing to insure at $\pi_L$ and that profit from such insurance is negative.

### Screening
- Definition (Screening)
	- Screening describes action taken by uninformed market participants to improve efficiency in a market where adverse selection occurs.
- Parameters (Rothschild-Stiglitz)
	- Each of a large number of heterogenous agents has wealth $w$ and faces monetary loss $K$, and is either type $L$ or type $H$. Type $L$ agents face this loss with probability $p_L$ and type $H$ agents face this loss with probability $p_H$, where $p_H>p_L$. The proportion of type $L$ agents is $\lambda$. Each agent's type is privately known and not observable by insurers. Each agent has risk-averse expected utility preferences.
	- Suppose that the market for insurance is perfectly competitive and insurers are risk-neutral.
	- Each insurer offers each agent a menu of policies which are premium-amount pairs (equivalently, final wealth lotteries). Then, each agent chooses a policy from the menus offered.
- Analysis
	- At the subgame equilibrium, each agent optimally chooses a policy. At the subgame perfect equilibrium, each insurer maximises expected profit, perfectly anticipating each agent's strategy and each other insurer's strategy.
	- Given that insurers are risk-neutral and the market for insurance is competitive, by the Bertrand result, each insurer insures each agent only at an actuarially fair premium, and each insurer has zero expected profit.
- Preliminary Result (Single-Crossing Property)
	- In $(w_N,w_A)$ (wealth in the event that no loss occurs, wealth in the event that loss (accident) occurs) space, at any point, the indifference curve of type $L$ agents is steeper than that of type $H$ agents.
	- This result can be established by differentiating expected utility of each type of agent with respect to $w_N$ and with respect to $w_A$.
- Definition (Pooling Equilibrium)
	- In this context, a pooling equilibrium is an equilibrium such that the firm offers a single policy that is accepted by each agent of either type.
	- Given that insurers are risk-neutral and the market for insurance is competitive, at any pooling equilibrium, insurance is offered at $\bar{\pi}=\lambda p_L+(1-\lambda)p_H$.
- Definition (Separating Equilibrium)
	- In this context, a separating equilibrium is an equilibrium such that insurers offer two policies, $(\pi_L,Q_L),(\pi_H,Q_H)$ and each type $L$ agent chooses the former and each type $H$ agent chooses the latter.
- Intermediate Result (No Pooling Equilibrium)
	- No pooling equilibrium exists. Suppose for reductio that a pooling equilibrium exists. Then given that insurers are risk-neutral and the market for insurance is competitive, insurance is offered at $\bar{\pi}=\lambda p_L+(1-\lambda)p_H$. Then, by the single-crossing property, there exists some alternative policy that would be chosen by only type $L$ agents. Deviation to offering only this policy is profitable since every type $H$ agent continues to choose the original policy offered by every other insurer, and only type $L$ agents choose the new policy, which lies below the zero-profit line for type $L$ agents. By reductio, no pooling equilibrium exists.
- Result (High Risk Types Offered Full Insurance)
	- In equilibrium, type $H$ agents are offered (and choose) full insurance $Q_H=K$ at premium $\pi_H=p_H$. \[See Eso, 2022 - Lecture on Information Economics 1 (Adverse Selection and Screening), p. 25 for graphical proof.\]
	- ![[Eso, 2022 - Lecture on Information Economics 1 (Adverse Selection and Screening, Annotated).pdf#page=25]]
- Result (Low Risk Types Offered Partial Insurance)
	- In equilibrium, type $L$ agents are offered (and choose) partial insurance $Q_L<K$ at premium $\pi_L=p_L$ where the incentive compatibility constraint binds. \[See Eso, 2022 - Lecture on Information Economics, p. 27 for graphical proof.\]
- Result (Potential Non-Existence)
	- Suppose that $\lambda$ is sufficiently high such that some segment of the pooling zero profit line lies above the indifference curves at the separating equilibrium, then there exists a profitable deviation from the separating equilibrium, so there is no separating equilibrium. By the earlier argument, there is no pooling equilibrium. Then, the Rothschild-Stiglitz model of screening in insurance has no equilibrium.

### Signalling
- Definition (Signalling)
	- Signalling describes action taken by informed market participants to improve efficiency in markets where adverse selection occurs by distinguishing between types.
- Parameters
	- In the first stage of a three stage Bayesian game, a worker $W$ with type (ability) $\theta\in\{\theta_L,\theta_H\}$ observes $\theta$ and chooses education level $e\geq0$. In the second stage, firms competitively observe $e$ and choose wage $w$. (It is without loss of generality to suppose that firms choose common $w$ given that firms so choose competitively) In the third stage, the worker chooses whether to accept $w$. $W$'s payoff is $w-\frac{e}{\theta}$ if he accepts and $0$ otherwise. A firm $F$ has payoff $\theta-w$ if its offer is accepted and $0$ otherwise. $W$ is type $H$ with probability $\lambda$.
- Definition (Pooling Equilibrium)
	- In this context, a pooling equilibrium is an equilibrium such that both types of $W$ choose common $e$, i.e. $e(\theta_H)=e(\theta_L)$.
	- Then, given that firms are competitive hence each firm has expected payoff $0$, at a pooling equilibrium, each firm's strategy is such that $w(e_H=e_L)=\lambda\theta_H+(1-\lambda)\theta_L$.
- Definition (Separating Equilibrium)
	- In this context, a separating equilibrium is an equilibrium such that both types of $W$ choose different $e$.
	- Then, given that firms are competitive hence each firm has expected payoff $0$, at a separating equilibrium, each firm's strategy is such that $w(e_H)=\theta_H,w(e_L)=\theta_L$.
- Analysis
	- Let $\bar{\theta}=\lambda\theta_H+(1-\lambda)\theta_L$.
	- $W$'s strategy is some function $e(\theta)$ and some rule for choosing whether to accept an offer. $F$'s strategy is some function $w(e)$. Given that firms are competitive, $F$ has expected payoff $0$, hence $w(e)=E(\theta|e)$.
	- For all $e^*\in[0,\bar{\theta}]$, there exists a pooling equilibrium such that $e(\theta)=e^*$ for all $\theta$ and $w(e)=\begin{cases}\bar{\theta}&\text{if }e=e^*\\\theta_L&\text{otherwise}\end{cases}$. It can be verified that no player has incentive to deviate.
	- For all $e_H\in[(\theta_H-\theta_L)\theta_L,(\theta_H-\theta_L)\theta_H]$, there exists a separating equilibrium such that $e(\theta_H)=e_H$ and $e(\theta_L)=0$, and $w(e_H)=\theta_H$ and $w(e)=\theta_L$ for all other $e$.
	- There is a plurality of equilibria. "Robustness considerations" eliminate all but the minimum cost separating equilibrium, i.e. the separating equilibrium such that $e_H$ is a minimum.
	- \[See Eso, 2022 - Lecture on Information Economics 2 for graphical argument.\]
	- ![[Eso, 2022 - Lecture on Information Economics 2 (Signalling, Annotated).pdf#page=20]]

## Moral Hazard (Grossman-Hart)
- Definition (Moral Hazard)
	- Moral hazard describes a situation of asymmetric information where an agent can take a costly action that is beneficial to but not observable by a principal.
- Analysis
	- Analysis of moral hazard problems is familiar from Microeconomic Analysis.