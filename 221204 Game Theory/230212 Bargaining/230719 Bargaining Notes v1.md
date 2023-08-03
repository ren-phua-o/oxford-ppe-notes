# Bargaining Notes

## Cooperative Game Theory of Bargaining
- Definition (Bargaining Problem)
	- A bargaining problem is a pair $(U,d)$, where $U$ is the set of possible agreement payoff vectors, and $d$ is the disagreement payoff vector. $U=\{(u_1(\mathbf{\overrightarrow{x}}),\ldots,u_n(\mathbf{\overrightarrow{x}}):\mathbf{\overrightarrow{x}}\in X\}$ where $X$ is the set of possible agreements. $\mathbf{\overrightarrow{d}}=(d_1\equiv u_1(\mathbf{\overrightarrow{D}}),\ldots,d_n\equiv u_n(\mathbf{\overrightarrow{D}}))$ where $\mathbf{\overrightarrow{D}}$ is the disagreement.
	- It is common to suppose that $\mathbf{\overrightarrow{D}}\in X\Leftrightarrow\mathbf{\overrightarrow{d}}\in U$, i.e. it is possible to "agree to disagree", $\exists\mathbf{\overrightarrow{v}}\in U:\forall i:v_i>d_i$, i.e. some agreement Pareto-dominates disagreement, and $U$ is convex, closed, and bounded, i.e. $\forall\mathbf{\overrightarrow{v_1}},\mathbf{\overrightarrow{v_2}}\in U:\forall\alpha\in[0,1]:\alpha\mathbf{\overrightarrow{v_1}}+(1-\alpha)\mathbf{\overrightarrow{v_2}}\in U$ and $\forall\{\mathbf{\overrightarrow{v_i}}\}_{i=1}^{\infty}:(\forall i:\mathbf{\overrightarrow{v_i}}\in U)\Rightarrow\mathbf{\overrightarrow{v_{\infty}}}\in U$ and $\nexists\mathbf{\overrightarrow{u}}\in U:\exists i:u_i=\infty\lor u_i=-\infty$ , i.e. if $\mathbf{\overrightarrow{v_1}},\mathbf{\overrightarrow{v_2}}\in U$ then any weighted average of the two elements is also an element of $U$, and if all members of a sequence are in $U$ then the limit of that sequence is also in $U$, and there is a finite upper bound and a finite lower bound on each dimension of $U$.
- Definition (Bargaining Solution)
	- A bargaining solution is a function $F(U,\mathbf{\overrightarrow{d}})$ from bargaining problems $(U,\mathbf{\overrightarrow{d}})$ to agreements $\mathbf{\overrightarrow{u}}\in U$.

## Nash Bargaining Theorem
- Definition (Weak Pareto Efficiency)
	- Suppose that $F(U,\mathbf{\overrightarrow{d}})=\mathbf{\overrightarrow{u}}$, then $\nexists\mathbf{\overrightarrow{v}}\in U:\forall i:v_i>u_i$, i.e. there is no agreement that strictly Pareto-dominates $\mathbf{\overrightarrow{u}}$.
- Definition (Symmetry)
	- Consider $n=2$. Bargaining problem $(U,\mathbf{\overrightarrow{d}}\equiv(d_1,d_2))$ is symmetric iff $d_1=d_2$ and $\forall(u_1,u_2)\in U:(u_2,u_1)\in U$. Suppose that $F(U,\mathbf{\overrightarrow{d}})=\mathbf{\overrightarrow{u}}\equiv(u_1,u_2)$, then $u_1=u_2$, i.e. if a bargaining problem is symmetric, then its solution is also symmetric.
- Definition (Invariance to Equivalent Payoff Representations)
	- Let $f_i(u_i)=\alpha_iu_i+\beta_i$ where $\alpha_i>0$ for all $i\in\{1,\ldots,n\}$. Let $U'=\{(f_1(u_1),\ldots,f_n(u_n)):(u_1,\ldots,u_n)\in U\}$, $\mathbf{\overrightarrow{d'}}=(f_1(d_1),\ldots,f_n(d_n))$, and $\mathbf{\overrightarrow{u'}}=(f_1(u_1),\ldots,f_n(u_n))$. Suppose that $F(U,\mathbf{\overrightarrow{d}})=\mathbf{\overrightarrow{u}}$ then $F(U',\mathbf{\overrightarrow{d}}')=\mathbf{\overrightarrow{u}}'$, i.e. if one bargaining problem is a linear transformation of another, then the solution of the former is obtained by applying the same transformation to the solution of the latter.
- Definition (Independence of Irrelevant Alternatives)
	- Suppose that $U'\subseteq U$ and $\mathbf{\overrightarrow{d'}}=\mathbf{\overrightarrow{d}}$ and $F(U,\mathbf{\overrightarrow{d}})\subseteq U'$, then $F(U',\mathbf{\overrightarrow{d'}})=F(U,\mathbf{\overrightarrow{d}})$, i.e. removal of non-solution possible agreements does not affect the solution.
- Nash Bargaining Theorem
	- $F(U,\mathbf{\overrightarrow{d}})=\mathbf{\overrightarrow{u^*}}\equiv(u_1^*,\ldots,u_n^*)\equiv\arg\max_{(u_1,\ldots,u_n)}\Pi_{i=1}^n(u_i-d_i)$ subject to $(u_1,\ldots,u_n)\in U$ and $\forall i:u_i\geq d_i$ uniquely satisfies the Nash bargaining axioms.
- Definition (Kalai Smorodinsky Bargainign Solution)
	- The Kalai-Smorodinsky bargaining solution is the point on the Pareto frontier $(u_1^*,u_2^*)$ such that $\frac{u_1^*-d_1}{u_2^*-d_2}=\frac{\max u_1-d_1}{\max u_2-d_2}$.

## Non-Cooperative Game Theory of Bargaining
- Relationship (Cooperative and Non-Cooperative Game Theory of Bargaining)
	- In the infinite repetition offer-counteroffer game, as the probability $\alpha$ of breakdown converges to zero, the subgame perfect equilibrium allocation converges to the Nash bargaining solution.
- At the stationary equilibrium of the infinite repetition offer-counteroffer game, each player makes the same offer every time, and each player is indifferent between accepting and rejecting each offer.
	- If some player strictly prefers accepting, then the offering player has a strictly profitable deviation to a less generous but still acceptable offer.
	- If some player $A$ strictly prefers rejecting, then this is only because $A$ has greater payoff from rejecting and making an acceptable counteroffer. This counteroffer is less generous to the initial offering player $B$ than $B$'s initial offer. So $B$ has strictly profitable deviation to a more generous, acceptable offer.
	- The general algebraic solution to such a game is as follows.
		- $x_2^1=(1-\alpha)x_2^2$,
		- $x_1^2=(1-\alpha)x_1^1\Rightarrow (1-x_2^2)=(1-\alpha)(1-x_2^1)$.
	- The result of this Rubinstein model converges to the Nash bargaining solution as the probability of breakdown converges to zero.