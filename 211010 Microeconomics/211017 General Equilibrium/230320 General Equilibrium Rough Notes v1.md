# General Equilibrium Rough Notes

## Exam Technique
- Always check second-order conditions.
- Read questions and sub-questions carefully, answer every part.
- Very readily use acronyms in the exam.
- Comment on each intermediate result, even in part A.
- A part A answer is usually 1-2 messy pages. A part B answer is usually 2-3 messy pages.
- An essay is usually 6 messy pages.

## Miscellaneous Notes
- Competitive equilibrium in Robinson Crusoe economy requires that firms maximise profit, households maximise utility, profits are distributed to households, and all markets clear.
- $-\frac{p_1}{p_2}=MRS=-\frac{MU_1}{MU_2}$.
- Pareto efficiency requires exhausted endowment, equal MRS (except in corner cases). Rawlsian solution additionally requires equal utility.
- Rawlsian solution will be Pareto efficient because if both players can be made better off, then the worst off player can be made better off.
- Solve consumption problems by either (1) equating MRS with price ratio, (2) solving the constrained optimisation problem, or (3) recognising the form of the utility function. Always comment on the form of the utility function.
- Lagrangian optimisation has the first-order conditions for each variable, and for the Lagrangian coefficient.
- Draw multiple indifference curves.
- For Cobb-Douglas utility functions of the form $x_1^ax_2^b\ldots$, take logarithms to simplify
- Technically, an agent has convex preferences iff, for all bundles $\mathbf{\overrightarrow{x}}$, the set of bundles weakly preferred to $\mathbf{\overrightarrow{x}}$ is a convex set, equivalently, this is iff indifference curves are convex (curving upward). If preferences are continuous, monotonic, and convex, then by the Arrow-Debreu theorem, a competitive equilibrium exists.

## Trade Notes
- Solve for optimum capital to labour ratio by $MRTS=\frac{MPL}{MPK}=\frac{w}{r}$. Then use this to find $Y$ and $C$ in terms of one input, and minimise. Or, more simply, argue that there are constant returns to scale and compute the average cost.
- In the two-goods case, because the optimal capital to labour ratio is fixed in each industry by relative factor prices, given some endowment, the equations can be solved simultaneously to find the equilibrium factor employment in each industry.
- At the competitive equilibrium, price equals marginal cost in each industry.
- Rybczynski Theorem: **if relative factor prices are constant and both goods continue to be produced, an increase in the supply of one factor $X$ leads to an increase in the output of the $X$-intensive good, and a decrease in the output of the other.**
- Stolper-Samuelson Theorem: **if there are constant returns to scale, and both goods continue to be produced, then an increase in the relative price of the $X$-intensive good leads to an increase in the relative return to $X$, and a decrease in the relative return to the other factor.**

## Game Theory Miscellaneous Notes
- For full marks, draw the game tree when solving for SPE.
- When explaining SPE, refer to credibility of threats and time-consistency of strategies.

## Exchange Economy
- Parameters
	- Each $X$ of two agents $A,B$ has endowment $\mathbf{\overrightarrow{w}}_X=(w_X^1,w_X^2)$ of two goods $1,2$ and chooses consumption $\mathbf{\overrightarrow{x}}_X=(x_X^1,x_X^2)$ to maximise utility $u_X(x_X^1,x_X^2)$ subject to budget constraint $p^1x_X^1+p^2x_X^2\leq p^1w_X^1+p^2w_X^2$. Concisely, consumer $X$'s optimisation problem is $\max_{\mathbf{\overrightarrow{x_X}}}u_X(\mathbf{\overrightarrow{x_X}})\text{ s.t. }\mathbf{\overrightarrow{p}}\cdot\mathbf{\overrightarrow{x_X}}\leq\mathbf{\overrightarrow{p}}\cdot\mathbf{\overrightarrow{w_X}}$ This characterises the situation where there are no distortions and each consumer takes prices as given.
	- Suppose that each $u_X$ represents continuous, monotonic, and convex preference, i.e. utility functions are well-behaved (i.e. continuous, monotonic, and convex).
- Analysis
	- The exchange economy can be represented by an Edgeworth box. \[See Cowan, 2022 - Lecture on General Equilibrium 1, pp. 14-20.\]
- Definition (Excess Demand)
	- Excess demand $z_X^i(\mathbf{\overrightarrow{p}})$ of consumer $X$ for good $i$ given price vector $\mathbf{\overrightarrow{p}}$ is defined by $z_X^i(\mathbf{\overrightarrow{p}})=x_X^i(\mathbf{\overrightarrow{p}})-w_X^i$. Aggregate excess demand $z^i(\mathbf{\overrightarrow{p}})$ for good $i$ given price vector $\mathbf{\overrightarrow{p}}$ is defined by $z^i(\mathbf{\overrightarrow{p}})=\sum_Xz_X^i(\mathbf{\overrightarrow{p}})$. Excess demand vector $\mathbf{\overrightarrow{z}}(\mathbf{\overrightarrow{p}})=(z^1(\mathbf{\overrightarrow{p}}),\ldots,z^n(\mathbf{\overrightarrow{p}}))$.
- Intermediate Result (Excess Demands are Homogenous of Degree Zero)
	- Excess demands (and demands) are homogenous of degree zero, i.e. invariant to a uniform scaling of the price vector.
- Theorem (Walras' Law)
	- For all price vectors $\mathbf{\overrightarrow{p}}$, $\mathbf{\overrightarrow{p}}\cdot\mathbf{\overrightarrow{z}}(\mathbf{\overrightarrow{p}})=0$. In other words, the values of excess demand sum to zero. Walras's law follows from the result that each consumer's budget constraint binds.
	- Walras' Law implies that if each market $i\neq j$ clears (i.e. $\forall i\neq j:z_i=0$) then market $j$ clears (i.e. $z_j=0$).
- Definition (Competitive (Walrasian) Equilibrium)
	- Competitive equilibrium is the pair of consumption and price vectors $(\mathbf{\overrightarrow{x^*}},\mathbf{\overrightarrow{p^*}})$ such that every market clears (i.e. $\forall i:z_i(\mathbf{\overrightarrow{p^*}})=0)$
- Result (Existence of Competitive Equilibrium)
	- Suppose $\mathbf{\overrightarrow{w}}>\mathbf{\overrightarrow{0}}$, then competitive equilibrium exists.

## Robinson Crusoe Economy
- Parameters
	- One consumer $C$ has endowment of leisure (recreation) $R^w=1$ and chooses consumption $x$ and labour (supply) $L$ to maximise utility $u(x,R)$ subject to $px\leq wL+\pi$ where $p$ is the price of consumption, $w$ is the wage, and $\pi$ is the profit of the one firm $F$ (which is fully owned by $C$). Firm $F$ has production function $f(L)$ and chooses labour (demand) $L$ and production $x$ to maximise profit $\pi=px-wL$ subject to $x\leq f(L)$. $C$ and $F$ each take $p$ and $w$ as given.
- Analysis
	- The Robinson Crusoe economy can be represented in $R,x$ space. \[See Cowan, 2022 - Lecture on General Equilibrium, pp. 30-33.\]
- Result (Existence of Competitive Equilibrium)
	- Given some conditions including non-increasing returns to scale, competitive equilibrium exists.

## Production Economy
- Parameters
	- Consider an economy with two industries, one for good $X$ and one for good $Y$, and two inputs, capital $K$ and labour $L$. Denote the production function for each good $Z$ as $F_Z(K_Z,L_Z)$. In industry $Z$, each firm $i$'s optimisation problem is $\min_{K_i,L_i}wL_i+rK_i\text{ s.t. }q_i\leq F_Z(K_i,L_i)$.
	- Suppose that the production of $X$ is more labour-intensive than the production of $Y$, i.e. for any wage $w$ and rental rate of capital $r$, the optimal ratio $\frac{K}{L}$ is higher for $Y$ than for $X$.
	- Suppose that (1) there are constant returns to scale in each industry, (2) there are decreasing marginal returns to each factor, (3) factors are perfectly mobile across industries (i.e. $w_X=w_Y=w,r_X=r_Y=r$), and (4) input markets are perfectly competitive (hence at equilibrium, $w=MPL_X=MPL_Y,r=MPK_X=MPK_Y$).
- Analysis
	- In each industry $Z$, given some $w,r$, for all levels of total output $Q_Z$, (supposing each firm $i$ chooses optimal $K_i,L_i$,) $\frac{K_Z}{L_Z}$ is constant. This follows from (1).
	- Then, in the economy, the general equilibrium, given some $w,r$ and some perfectly inelastic capital supply and labour supply $\bar{K},\bar{L}$, is such that in each industry $Z$, $\frac{K_Z}{L_Z}$ is equal to the above constant ratio. \[See Cowan, 2022 - Lecture on General Equilibrium 2, pp. 4-5 for graphical representation.\]
	- ![[Cowan, 2022 - Lecture on General Equilibrium 2 (International Trade).pdf#page=4]]
- Result (Rybczynski Theorem)
	- Suppose that relative input prices remain unchanged and each good continues to be produced. Then an increase in the supply of one factor $\bar{J}$ (i.e. an increase in either $\bar{K}$ or $\bar{L}$) causes an increase in the output of the $J$-intensive good and a decrease in the output of the other good. \[See Cowan, Lecture on General Equilibrium 2, pp. 6 for graphical representation.\]
- Result (Stolper-Samuelson Theorem)
	- Suppose that each good continues to be produced (and continue to suppose that there are constant returns to scale), then an increase in the relative price of the $J$-intensive good causes an increase in the real return to $J$ and a decrease in the real return to the other factor.
	- Intuitively, an increase in the price $p_{Z_J}$ of the $J$-intensive good, $Z_J$ causes industry $Z_J$ to expand, which causes an increase in relative (to the other factor $-J$) aggregate demand for $J$, which causes an increase in the relative input price of $J$. Analytically, the change in relative input prices causes a change in each industry $Z$'s optimal $\frac{K_Z}{L_Z}$. Graphically, it can be shown that output of $Z_J$ increases and output of $Z_{-J}$ decreases, and each good is produced with relatively higher $J$.

## International Trade
- Analysis is largely graphical. \[See Cowan, 2022 - Lecture on General Equilibrium 2, pp. 15-27.\]
- ![[Cowan, 2022 - Lecture on General Equilibrium 2 (International Trade).pdf#page=15]]
- Gains from trade can be decomposed into gains from exchange (increase in consumer welfare due to trade at world prices from autarky production) and gains from specialisation (further increase in consumer welfare from optimisation of production given trade at world prices).