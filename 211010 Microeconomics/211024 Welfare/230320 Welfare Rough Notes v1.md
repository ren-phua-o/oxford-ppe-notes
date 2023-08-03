# Welfare Rough Notes

## Summary
- 1FWT: **If $(\mathbf{\overrightarrow{x^*}},\mathbf{\overrightarrow{p^*}})$ is a competitive equilibrium in the exchange economy, then $\mathbf{\overrightarrow{x^*}}$ is Pareto-efficient.**
- 2FWT: **If $\mathbf{\overrightarrow{x^*}}$ is a Pareto-efficient allocation in the exchange economy, then (supposing that preferences are continuous, monotonic, and convex) for some endowment $\mathbf{\overrightarrow{w}}$, the competitive equilibrium is $(\mathbf{\overrightarrow{x^*}},\mathbf{\overrightarrow{p^*}})$ for some $\mathbf{\overrightarrow{p^*}}$.**

## Social Welfare
- Definition (Pareto-Dominance)
	- Allocation $\mathbf{\overrightarrow{x}}$ Pareto-dominates allocation $\mathbf{\overrightarrow{x'}}$ iff for each agent $i$, $\mathbf{\overrightarrow{x}}\succeq_i\mathbf{\overrightarrow{x'}}$ and for some agent $j$, $\mathbf{\overrightarrow{x}}\succ_j\mathbf{\overrightarrow{x'}}$. In other words, every agent weakly prefers $\mathbf{\overrightarrow{x'}}$ to $\mathbf{\overrightarrow{x}}$ and some agent strictly prefers $\mathbf{\overrightarrow{x}}$ to $\mathbf{\overrightarrow{x'}}$.
	- Note that the relation of Pareto-dominance is not complete.
- Definition (Pareto-Efficiency)
	- Allocation $\mathbf{\overrightarrow{x}}$ is Pareto-efficient iff there is no allocation $\mathbf{\overrightarrow{x'}}$ that Pareto-dominates $\mathbf{\overrightarrow{x}}$. Informally, allocation $\mathbf{\overrightarrow{x}}$ is Pareto-efficient iff no agent can be made (strictly) better off without making some agent (strictly) worse off.
- Definition (Utility Possibility Frontier)
	- The utility possibility frontier given some endowment $\mathbf{\overrightarrow{w}}$, supposing that preferences are well-behaved, is $U=\{\mathbf{\overrightarrow{u}}(\mathbf{\overrightarrow{x}}):\sum_ix_i=\sum_iw_i\}$.
- Definition (Rawlsian Social Welfare Function)
	- The Rawlsian social welfare function is $W(\mathbf{\overrightarrow{u}})=\min_iu_i(\mathbf{\overrightarrow{x}})$.
- Definition (Utilitarian Social Welfare Function)
	- The utilitarian social welfare function is $W(\mathbf{\overrightarrow{u}})=\sum_iu_i(\mathbf{\overrightarrow{x}})$.
- Definition (Atkinsonian Social Welfare Function)
	- The Atkinsonian social welfare function is $W(\mathbf{\overrightarrow{u}})=\Pi_iu_i(\mathbf{\overrightarrow{x}})^{\alpha_i}$ where $\sum_i\alpha_i=1$.
- Theorem
	- Supposing that the utility possibility frontier is concave, every Pareto-optimal allocation maximises some well-behaved social welfare function. Precisely, for all utility allocations $\mathbf{\overrightarrow{u}}$ such that $\mathbf{\overrightarrow{u}}\in U$, where $U$ is concave, there exists some $W(\mathbf{\overrightarrow{u}})=\sum_i\alpha_iu_i(\mathbf{\overrightarrow{x}})$ such that $\mathbf{\overrightarrow{u}}=\max_{\mathbf{\overrightarrow{u}}}W(\mathbf{\overrightarrow{u}})\text{ s.t. }\mathbf{\overrightarrow{u}}\in U$.
- Theorem (First Fundamental Welfare Theorem)
	- If $(\mathbf{\overrightarrow{x^*}},\mathbf{\overrightarrow{p^*}})$ is a competitive equilibrium in the exchange economy, then $\mathbf{\overrightarrow{x^*}}$ is Pareto-efficient.
	- This follows from the monotonicity of preferences. By the monotonicity of preferences, the budget constraint for each agent binds at equilibrium. By the optimality of each agent $i$'s equilibrium consumption bundle $\mathbf{\overrightarrow{x_i^*}}$, if $i$ strictly prefers some consumption bundle $\mathbf{\overrightarrow{x_i'}}$ to $\mathbf{\overrightarrow{x_i^*}}$, then $\mathbf{\overrightarrow{x_i'}}$ does not satisfy $i$'s budget constraint at equilibrium prices. By the optimality of each agent $j$'s equilibrium consumption bundle $\mathbf{\overrightarrow{x_j^*}}$, the monotonicity of preferences, and the linearity of budget constraints, if $j$ weakly prefers $\mathbf{\overrightarrow{x_j'}}$ to $\mathbf{\overrightarrow{x_j^*}}$, then $\mathbf{\overrightarrow{x_j'}}$ either violates or just satisfies $j$'s budget constraint at equilibrium prices. Then any Pareto-dominant $\mathbf{\overrightarrow{x'}}$ is such that the total value of the allocation exceeds the total value of the endowment at $\mathbf{\overrightarrow{p^*}}$ and is not feasible.
- Theorem (Second Fundamental Welfare Theorem)
	- If $\mathbf{\overrightarrow{x^*}}$ is a Pareto-efficient allocation in the exchange economy, then (supposing that preferences are continuous, monotonic, and convex) for some endowment $\mathbf{\overrightarrow{w}}$, the competitive equilibrium is $(\mathbf{\overrightarrow{x^*}},\mathbf{\overrightarrow{p^*}})$ for some $\mathbf{\overrightarrow{p^*}}$.
	- \[See Cowan, 2022 - Lecture on Welfare 1, p. 27 for graphical representation.\]
	- ![[Cowan, 2022 - Lecture on Welfare 1.pdf#page=27]]
	- The second fundamental welfare theorem implies that any Pareto-efficient allocation can be implemented as a market outcome by lump sum redistribution.

## Preference Aggregation
- Definition (Preference Aggregation Rule)
	- Suppose that there is a set of social states $X=\{\mathbf{\overrightarrow{x_1}},\mathbf{\overrightarrow{x_2}},\ldots\}$, a set of agents $N=\{1,\ldots,n\}$, and each agent $i$ has rational (complete and transitive) preferences $\succeq_i$ over $X$. Then a preference aggregation rule of preference profile $(\succeq_1,\ldots\succeq_n)$ on $X$ is the function $F$ from $(\succeq_1,\ldots,\succeq_n)$ to some preference $\succeq^*$.

### Common Preference Aggregation Rules
- Definition (Dictatorial Rule)
	- Every preference aggregation rule $F(\mathbf{\overrightarrow{\succeq}})=\succeq^*$ such that $\succeq^*=\succeq_i$ for some $i\in N$ is a dictatorial rule.
- Definition (Majority Rule)
	- Majority rule is defined in the intuitive way. Formally, preference aggregation rule $\succeq^*$ is a majority rule iff $\mathbf{\overrightarrow{x}}\succeq^*\mathbf{\overrightarrow{x'}}\Leftrightarrow|\{i\in N:\mathbf{\overrightarrow{x}}\succeq_i\mathbf{\overrightarrow{x'}}\}|\geq|\{i\in N:\mathbf{\overrightarrow{x}}\succeq_i\mathbf{\overrightarrow{x'}}\}|$.
- Definition (Scoring Rule)
	- Every preference aggregation rule $F(\mathbf{\overrightarrow{\succeq}})=\succeq^*$ such that $\mathbf{\overrightarrow{x}}\succeq^*\mathbf{\overrightarrow{x'}}\Leftrightarrow\sum_ip(K(\succeq_i,\mathbf{\overrightarrow{x}}))\geq\sum_ip(K(\succeq_i,\mathbf{\overrightarrow{x'}}))$ where $K(\succeq_i,\mathbf{\overrightarrow{x}})$ is equal to the position of $\mathbf{\overrightarrow{x}}$ in the ranking corresponding to $\succeq_i$ and $p:\mathbb{R}\rightarrow\mathbb{R}$ is a decreasing function.

### Arrow's Impossibility Theorem
- Definition (Rationality)
	- Preference relation $\succeq$ is rational iff it is complete and transitive.
- Definition (Unrestricted Domain)
	- Preference aggregation rule $F$ has an unrestricted domain iff $F(\mathbf{\overrightarrow{\succeq}})$ is defined for all $\mathbf{\overrightarrow{\succeq}}$.
- Definition (Pareto Principle)
	- Preference aggregation rule $F$ satisfies the Pareto principle iff $(\forall i:\mathbf{\overrightarrow{x}}\succeq_i\mathbf{\overrightarrow{x'}})\Rightarrow \mathbf{\overrightarrow{x}}\succeq^*\mathbf{\overrightarrow{x'}}$.
- Definition (Non-Dictatorship)
	- Preference aggregation rule $F$ satisfies non-dictatorship iff $\nexists i\in N:(\mathbf{\overrightarrow{x}}\succeq_i\mathbf{\overrightarrow{x'}}\Leftrightarrow\mathbf{\overrightarrow{x}}\succeq^*\mathbf{\overrightarrow{x'}})$.
- Definition (Independence of Irrelevant Alternatives)
	- Preference aggregation rule $F$ satisfies independence of irrelevant alternatives iff social ordering over any $\mathbf{\overrightarrow{x}},\mathbf{\overrightarrow{x'}}\in X$ depends only on individual preferences over $\mathbf{\overrightarrow{x}},\mathbf{\overrightarrow{x'}}$, and not on individual preferences over other alternatives.
- Theorem (Arrow's Impossibility Theorem)
	- Suppose that $|X|\geq3$, then there is no $F$ that satisfies unrestricted domain, Pareto principle, non-dictatorship, and independence of irrelevant alternatives, and yields rational $\succeq^*$ for all $\mathbf{\overrightarrow{\succeq}}$.
- Definition (Single-Peaked Preferences)
	- Agents' preferences over some choice set are singled-peaked iff there exists some ordering over the choice set such that for each person there is a bliss point such that this bliss point is the maximal element in the choice set according to his preferences and for every two points in the same direction from the bliss point, the further point is less preferred.

### Sen's Impossibility Theorem
- Definition (Liberalism)
	- Preference aggregation rule $F$ satisfies Liberalism iff for each $i$ there exists $\mathbf{\overrightarrow{x}},\mathbf{\overrightarrow{x'}}\in X$ such that $\mathbf{\overrightarrow{x}}\succeq^*\mathbf{\overrightarrow{x'}}\Leftrightarrow\mathbf{\overrightarrow{x}}\succeq_i\mathbf{\overrightarrow{x'}}$.
- Theorem (Sen's Impossibility Theorem)
	- Suppose that $|X|\geq3$, then there is no $F$ that satisfies unrestricted domain, Pareto principle, and Liberalism.

### Median Voter Theorem
- Definition (Single-Peakedness)
	- Agent $i$'s preference relation $\succeq_i$ over $S\subseteq\mathbb{R}$ is single-peaked iff there exists bliss point $b_i$ such that $\forall x,x'\leq b_i:x\succeq x'\Leftrightarrow(b_i-x)\leq(b_i-x')$ and $\forall x,x'\geq b_i:x\succeq x'\Leftrightarrow(x-b_i)\leq(x'-b_i)$.
- Theorem (Median Voter Theorem)
	- If voters' preferences are single-peaked, each of two candidates chooses policy equal to the bliss point of the median voter in equilibrium.

### Gibbard's Impossibility Theorem
- Definition (Strategy-Proofness)
	- Preference aggregation rule $F$ satisfies strategy-proofness iff truth-telling is a dominant strategy for each agent.
- Definition (Sovereignty)
	- Preference aggregation rule $F$ satisfies Sovereignty iff every possible $\succeq^*$ over $X$ is in the range of $F$.
- Theorem (Gibbard's Impossibility Theorem)
	- Suppose that $|X|\geq3$, then there is no $F$ that satisfies strategy-proofness and Sovereignty.