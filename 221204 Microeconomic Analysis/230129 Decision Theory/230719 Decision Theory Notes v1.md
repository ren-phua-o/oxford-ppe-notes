# Decision Theory Notes

## Deterministic Setting

### Preference
- An agent's decision problem is to choose an element from a set of mutually exclusive alternatives $X$. The preference relation approach to decision problems in economics treats preferences as fundamental. On this approach, an agent's choice is derived from his preferences. The choice function approach to decision problems treats choice as fundamental. On this approach, an agent's preferences are inferred from his choices.
- On the preference relation approach, the binary relation weak preference $\succeq$ on $X$ is treated as primitive.
	- It is possible to derive the binary relation of strict preference $\succ$ and indifference $\sim$ from $\succeq$. $\forall x,x'\in X:x\succ x'\Leftrightarrow x\succeq x'\land\lnot x'\succeq x$. $\forall x,x'\in X:x\sim x'\Leftrightarrow x\succeq x'\land x'\succeq x$.
- **$\succeq$ is rational iff it is complete and transitive.**
	- Binary relation $B$ over $X$ is complete (strictly connected) iff $\forall x,x'\in X:xBx'\lor x'Bx$. In words, this is iff there is a $B$-relation between any two elements of $X$.
	- Binary relation $B$ over $X$ is transitive iff $\forall x,x',x''\in X:xBx'\land x'Bx''\rightarrow xBx''$.
- Binary relation $B$ over $X$ is (weakly) connected iff $\forall x\neq x'\in X:xBx'\lor x'Bx$. In words, this is iff there is a $B$-relation between any two distinct elements of $X$.
- Rational $\succeq$ implies that $\succeq$ and $\sim$ are reflexive, $\succ$ is irreflexive, asymmetric, and negative transitive, and $x\succeq x'\land x'\succ x''\rightarrow x\succ x''$.
	- Binary relation $B$ over $X$ is reflexive iff $\forall x\in X:xBx$, it is irreflexive iff it is not reflexive.
	- Binary relation $B$ over $X$ is asymmetric iff $\forall x,x'\in X:\lnot(xBx'\land x'Bx)$.
	- Binary relation $B$ over $X$ is negative transitive iff $\forall x,x',x''\in X:\lnot xBx'\land\lnot x'Bx''\rightarrow\lnot xBx''$.

#### Utility Representation
- **Utility function $u:X\rightarrow\mathbb{R}$ represents preferences $\succeq$ over set $X$ iff $\forall x,x'\in X:u(x)\geq u(x')\Leftrightarrow x\succeq x'$.**
- If $\succeq$ over $X$ is represented by some $u:X\rightarrow\mathbb{R}$, then $\succeq$ is rational. In other words, some preference relation's representability by a utility function implies that preference relation's rationality.
	- For all $x,x'\in X$, by definition of $u$, $u(x),u(x')\in\mathbb{R}$, then by the completeness of $\geq$ over $\mathbb{R}$, $u(x)\geq u(x')$ or $u(x')\geq u(x)$, then by definition of utility representation, $x\succeq x'$ or $x'\succeq x$, then by definition of completeness, $\succeq$ is complete.
	- For all $x,x',x''\in X$ such that $x\succeq x'$ and $x\succeq x''$, by definition of utility representation, $u(x)\geq u(x')$ and $u(x')\geq u(x'')$, then by the transitivity of $\geq$ over $\mathbb{R}$, $u(x)\geq u(x'')$, then by definition of utility representation, $x\succeq x''$.
	- Intuitively, completeness and transitivity are necessary for utility representation because the relation $\geq$ over $\mathbb{R}$ is complete and transitive.
- For **finite or countably infinite** $X$, if $\succeq$ over $X$ is rational, then $\succeq$ is represented by some $u:X\rightarrow\mathbb{R}$. In other words, for finite or countably infinite $X$, some preference relation's rationality implies its representability by a utility function.
	- It is possible to construct an algorithm for assigning utility values to each element in a finite or countably infinite $X$ such that the corresponding utility function represents $\succeq$. \[See Eso, 2023 - Lecture on Preference, Utility, and Choice, p. 14\]
- Debreu's theorem states that if $\succeq$ over $X\subseteq\mathbb{R}^n$ is rational **and continuous**, then $\succeq$ is represented by some continuous $u:X\rightarrow\mathbb{R}$.
	- $\succeq$ on $X\subseteq\mathbb{R}^n$ is continuous iff (1) for all sequences $\mathbf{\overrightarrow{x_1}},\mathbf{\overrightarrow{x_2}},\ldots$ that converge to $\mathbf{\overrightarrow{x_{\infty}}}$, and (2) for all $k\in1,2,\ldots$ $\mathbf{\overrightarrow{x_k}}\succeq\mathbf{\overrightarrow{x'}}$, then (3) $\mathbf{\overrightarrow{x_{\infty}}}\succeq\mathbf{\overrightarrow{x'}}$. Intuitively, this is iff indifference curves are continuous. Equivalently, this is iff the set of all $\mathbf{\overrightarrow{x'}}$ such that $\mathbf{\overrightarrow{x'}}\succeq\mathbf{\overrightarrow{x}}$ is a closed set.
- The **uniform consumption equivalent $\hat{x}$ of $\mathbf{\overrightarrow{x}}$ is such that $u(\mathbf{\overrightarrow{x}})=u((\hat{x},\hat{x},\ldots))$.**
- Lexicographic preferences are rational but not continuous, and do not have a utility representation.
- Any monotonic (i.e. strictly increasing) transformation $f:\mathbb{R}\rightarrow\mathbb{R}$ of a utility function $u:X\rightarrow\mathbb{R}$ represents the same preferences.
	- For all $x,x'\in X$ such that $x\succeq x'$, by definition of utility representation, $u(x)\geq u(x')$, then by strict monotonicity of $f$, $f(u(x))\geq f(u(x'))$, then by definition of utility representation, $f\circ u$ represents $\succ$.

#### Derived Choice
- For finite $X$, rational $\succeq$ over $X$ yields a maximal element.
- For (potentially infinite) compact $X$, rational and continuous $\succeq$ yields a maximal element.
	- Since $\succeq$ is rational and continuous, it can be represented by continuous $u$. Then, by the Weierstrass extreme value theorem, since $X$ is compact, a maximum exists.

### Choice
- An agent's decision problem is to choose an element from a set of mutually exclusive alternatives $X$. A choice problem or menu $A$ is some subset of $X$. Let $\Delta=\{A_1,A_2,\ldots\}$ denote some set of menus. Then a choice function is some $c:\Delta\rightarrow X$ such that for all $A\in\Delta$, $c(A)\in A$. In other words, a choice function is some function that selects an element of each menu. $\mathcal{X}$ denotes the set of all subsets of $X$. $\mathcal{B}$ denotes the set of all pairs of elements in $X$.
- Choice data is a collection of menus and elements chosen from each menu.
	- Universal choice data is a collection of menus $\mathcal{X}$ and elements chosen from each menu.
	- Binary choice data is a collection of menus $\mathcal{B}$ and elements chosen from each menu.
	- Bundle consumption choice data is a collection of menus and elements chosen from each menu corresponding, where each pair corresponds to some consumption problem $\max_{x_1,x_2,\ldots}u(x_1,x_2,\ldots)\text{ s.t. }p_1x_1+p_2x_2+\ldots\leq m$.
- If $A$ is a finite menu and $\succ$ is rational, then $c(A,\succ)$ is defined as the maximal element of $A$ according to $\succ$.
	- **$c(A,\succ)$ satisfies Nash's Independence of Irrelevant Alternatives axiom (or Sen's alpha, or Chernoff's Postulate 6), which states that $\forall A'\subseteq A:c(A,\succ)\in A'\rightarrow c(A',\succ)=c(A,\succ)$. In words, if a rational agent chooses some element $a$ from $A$, and $a$ is available in $A'\subseteq A$, then that rational agent chooses $a$ from $A'$ too.**
- If $X$ is finite, $c(A,\succ)$ is on $\mathcal{X}$, and $c(A,\succ)$ satisfies Nash's Independence of Irrelevant Alternatives axiom, then $\succ$ is rational.
	- (See Eso, 2023 - Lecture on Preferences, Utility, and Choice, p. 28.)
- **If $X$ is finite and $\succ$ is rational, then $c(A,\succ)$ satisfies the Weak Axiom of Revealed Preference, which states that if $x,x'\in A,A'$ then not both $c(A,\succ)=x$ and $c(A',\succ)=x'$.**

#### Revealed Preference
- $x$ is **directly revealed preferred** to $x'$ by choice function $c$ iff $\exists A:x,x'\in A\land c(A)=x$. In words, $x$ is directly revealed preferred to $x'$ by choice function $c$ iff the agent whose choice function it is chooses $x$ from $A$ in which $x'$ is also available.
	- Universal choice data and binary choice data are each sufficient for direct revelation of an agent's preferences (rational or not).
- $x$ is **indirectly revealed preferred** to $x'$ by choice function $c$ iff $x\succ x'$ can be inferred from directly revealed preferences and the transitivity of $\succ$.

#### Dynamic Choice
- A model of a dynamic decision problem consists of a set of periods $T=\{1,2,\ldots,\bar{t}\}$, a set $Z_t$ of possible outcomes at each period $t$, a menu $A_t(c_1,\ldots,c_{t-1})\subseteq Z_t$ at each period $t$ contingent on outcomes chosen $c_1,\ldots,c_{t-1}$ in earlier periods.
- In the two-period model of a dynamic decision problem, the agent at $t=0$ chooses some pair $x_0=(c_0,A_1(c_0))$ from $X_0=\{(c_0,A_1(c_0)):c_0\in Z_0\}$ and at $t=1$ chooses some outcome $x_1=c_1$ from $X_1=A_1(c_0)\subseteq Z_1$.
- An agent's dynamic choice is rational only if it satisfies consequentialism, time separability, and dynamic consistency.
	- An agent's dynamic choice satisfies consequentialism iff $c_t$ is independent of the outcomes not chosen $Z_{t-\Delta t}\setminus\{c_{t-\Delta t}\}$ in earlier periods $t-\Delta t$.
	- An agent's dynamic choice satisfies time separability iff $c_t(A_t,c_0,\ldots,c_{t-1})=c_t(A_t,c_0',\ldots,c_{t-1}')$ for all $c_0,\ldots,c_{t-1},c_0',\ldots,c_{t-1}'$ such that $A_t(c_0,\ldots,c_{t-1})=A_t(c_0',\ldots,c_{t-1}')$. In words, an agent's dynamic choice satisfies time separability iff his choice at $t$ is dependent only on his menu at $t$ and not on his earlier choices (except insofar as they affect his menu at $t$).
	- An agent's dynamic choice satisfies dynamic consistency (in the two-period decision problem where the agent at $t=0$ chooses $A_1$ and at $t=1$ chooses $c_1\in A_1$) iff his preferences can be represented by utility functions $u_0,u_1$ such that for all $A_1$, $u_0(A_1)=\max_{z_1\in A_1}u_1(z_1)$.
- An agent's preferences $\succeq$ over dated consumption levels $X=\{(c_t,t):c_t\in\mathbb{R},t=0,1,\ldots\}$ can be represented by a discounted utility function iff there exists some $u$ such that $\forall c,c'\in\mathbb{R},t,t'\in\{0,1,\ldots\}:(c,t)\succeq(c',t')\Leftrightarrow\delta^tu(c)\geq\delta^{t'}u(c')$.
	- If $\succeq$ is complete, transitive, continuous, monotone (i.e. strictly increasing in $c_t$) and stationary, then $\succeq$ can be represented by a discounted utility function, where $u$ is continuous and strictly increasing.
	- $\succeq$ is stationary iff $\forall c,c'\in\mathbb{R},t,t'\in\{0,1,\ldots\},\Delta t\in\mathbb{Z}:(c,t)\succeq(c',t')\Leftrightarrow(c,t+\Delta t)\succeq(c',t'+\Delta t)$. In words, this is iff preferences are invariant to displacement in time.

## Stochastic Setting

### Lotteries
- A simple lottery $L=[p_1,\ldots,p_k;x_1,\ldots,x_k]$ is a probability distribution over a fixed set of outcomes.
- A compound lottery $L=[p_1,\ldots,p_k;L_1,\ldots,L_k]$ is a probability distribution over lotteries or outcomes.
- We assume that agents consider compound lotteries in their reduced form.
- (See Eso, 2023 - Lecture on Expected Utility 1, pp. 5-6 for discussion of graphical representation of lotteries.)

#### Lotteries as Cumulative Distribution Functions
- The cumulative distribution function $F_X(x)$ of a random variable $x$ is the function such that $\forall x:F_X(x)=P(X\leq x)$.
- If an agent has expected utility preferences, utility $U(F_X)$ of lottery $X$ with cumulative distribution function $F_X$ is defined by $U(X)=\int_{-\infty}^{\infty}u(x)F_X'(x)dx$.
- The expected value $EV(X)$ of $X$ with $F_X$ is defined by $\int_{\infty}^{\infty}xF'(x)dx$.
- The certainty equivalent $CE(X)$ of $X$ with $F_X$ is defined in the intuitive way.
- An agent with expected utility preferences invests non-zero amount in any risky asset with positive expected returns, and a more risk-averse agent with such preferences invests less.

### Expected Utility
- The expected value $EV(L)$ of a (simple or reduced) lottery $L=[p_1,\ldots,p_k;x_1,\ldots,x_k]$ is given by $\sum_{i=1}^kp_ix_i$.
- If an agent's preferences $\succeq$ over lotteries is complete, transitive, and continuous, then by Debreu's theorem, there is a utility representation $U$ of $\succeq$ such that $L\succeq L'\Leftrightarrow U(L)\geq U(L')$.
	- Preferences $\succeq$ over lotteries is complete iff $\forall L,L':(L\succeq L')\lor(L'\succeq L)$.
	- Preferences $\succeq$ over lotteries is transitive iff $\forall L,L',L'':L\succeq L'\land L'\succeq L''\rightarrow L\succeq L''$.
	- **Preferences $\succeq$ over lotteries is continuous iff $\forall L\succeq L'\succeq L'':\exists p\in[0,1]:[p,1-p;L,L'']\sim L'$.**
- The **expected utility theorem states that if $\succeq$ over lotteries $\mathcal{L}$ is complete, transitive, continuous, and satisfies the independence axiom, then there exists some Bernoulli utility function $u(x)$ such that $U(L)=\sum_{i=1}^kp_iu(x_i)$.**
	- **The independence axiom states that for all $L,L',L''$ and $L_1=[p,1-p;L,L']$, $L_2=[p,1-p;L,L'']$, $L_1\succeq L_2$ iff $L'\succeq L''$. In words, agents do not consider counterfactuals.**
	- The EU hypothesis states that preferences are complete, transitive, continuous, and satisfy the independence axiom.
	- \[See Eso, 2023 - Lecture on Expected Utility 1, pp. 12-13 for sketch proof\]
	- \[See Eso, 2023 - Lecture on Expected Utility 1, pp. 14-16 for evaluation\]
- If $\succeq$ can be represented by some Bernoulli utility function $u$, it can also be represented by some Bernoulli function $v$ where $v(x)\equiv a+bu(x)$.

### Risk Aversion
- An agent with $\succeq$ is risk-averse iff $[1;EV(L)]\succ L$ for all non-degenerate $L$.
	- An agent with $\succeq$ is risk-neutral iff $[1;EV(L)]\sim L$ for all $L$.
	- An agent with $\succeq$ is risk-loving iff $[1;EV(L)]\prec L$ for all $L$.
	- Equivalently, an agent with $\succeq$ is risk-averse iff $RP_{\succeq}(L)>0$ for all $L$.
	- Equivalently, an agent with $\succeq$ represented by $u$ is risk-averse iff $u''<0$, i.e. $u$ is strictly concave.
		- Strict concavity of $u$ is equivalent to $\forall p\in(0,1),x,x'\in\mathbb{R}:pu(x)+(1-p)u(x')<u(px+(1-p)x')$.
- The certainty equivalent $CE(L)$ of $L$ is such that $[1;CE(L)]\sim L$. In words, $CE(L)$ is the certain outcome that the agent finds exactly as good as $L$.
	- If $\succeq$ can be represented by $u$, then $CE(L)$ is such that $u(CE(L))=\sum p_iu(x_i)$.
- The risk premium $RP(L)$ of $L$ is defined by $RP(L)=EV(L)-CE(L)$.

#### Arrow-Pratt Measures of Risk Aversion
- Arrow-Pratt measure of risk aversion $A(x)=-\frac{u''(x)}{u'(x)}$.
	- $A(x)$ is proportional to the risk premium of a small zero mean lottery.
	- $\uparrow A(x)\Leftrightarrow\uparrow\text{ risk aversion }\Leftrightarrow\uparrow\text{ concavity of u }\Leftrightarrow\uparrow\text{ risk premium of any given L}$.
- An agent with constant absolute risk aversion $CARA(a)$ has preferences represented by $u$ such that $\forall x:A(x)\equiv-\frac{u''(x))}{u'(x)}=a$, where $a$ is some constant. $CARA(a)$ implies $u(x)=-e^{-ax}$.
	- An agent with $CARA(a)$ accepts the same lotteries at any initial wealth level.
	- Suppose $L$ is some lottery where outcomes are normally distributed with mean $\mu$ and variance $\sigma^2$, then for an agent with $CARA(a)$, $CE(L)=\mu-\frac{a}{2}\sigma^2$.
- An agent with $DARA$ has preferences represented by $u$ such that $A(x)$ is decreasing in $x$.
	- An agent with $DARA$ becomes less risk-averse as initial wealth increases.
- An agent with constant relative risk aversion $CRRA(r)$ has preferences represented by $u$ such that $\forall x:A(x)x\equiv-\frac{u''(x)x}{u'(x)}=r$, where $r$ is some constant. $CRRA(r)$ implies $u(x)=x^{1-r}$ for $r\in(0,1)$ and $u(x)=\ln x$ for $r=1$.

#### Prudence
- A risk-averse agent with expected utility preferences is prudent iff $u'''>0$.
	- $DARA$ implies prudence.

### Stochastic Dominance
- $L\succ_{FOSD}L'$ iff $\textcolor{red}{\forall x:F_L(x)\leq F_{L'}(x)}$, where $F_L$ and $F_{L'}$ are the respective cumulative distribution functions. **Graphically, the plot of $F_L(x)$ against $x$ remains weakly below the plot of $F_{L'}(x)$ against $x$ for all $x$.** Informally, $L$ assigns greater probabilities to higher values (and, necessarily, lower probabilities to lower payoffs) than $L'$.
	- $L\succ_{FOSD}L'$ iff any expected utility preference $\succeq$ with strictly increasing $u$ is such that $L\succ L'$.
- Suppose that $EV(L)=EV(L')$, then $L\succ_{SOSD}L'$ iff $\textcolor{red}{\forall a:\int_{-\infty}^a F_L(x)dx\leq\int_{-\infty}^a F_{L'}(x)dx}$, where $F_L$ and $F_{L'}$ are the respective cumulative distribution functions. **Graphically, (a sufficient condition for $L\succ_{SOSD}L'$ is that) the plot of $F_L(x)$ against $x$ crosses the plot of $F_{L'}(x)$ against $x$ once from the bottom.** Informally, $L$ is a mean-preserving spread of $L'$.
	- $EV(L)=EV(L')$ and $L\succ_{SOSD}L'$ iff any expected utility preference $\succeq$ with strictly increasing and strictly concave $u$ is such that $L\succ L'$.
	- A mean-preserving spread of $L$ is any $L'$ that can be constructed by spreading out one or more portions of $L$'s probability density (mass) function while preserving the mean, without requiring that all or most of the probability mass is moved toward the mean. [An example here.](https://en.wikipedia.org/wiki/Mean-preserving_spread#Example)
- $L$ LR-dominates $L'$ on the domain $[a,b]$ iff $\frac{f_L(x)}{f_{L'}(x)}$ is weakly increasing in $x\in[a,b]$.
	- $L\succ_{LR}L'\Rightarrow L\succ_{FOSD}L'$. In words, likelihood ratio dominance implies first order stochastic dominance.

### Knightian Uncertainty
- In some decision problems, agents face Knightian uncertainty, where probabilities are not quantified.
- A model of a decision problem under Knightian uncertainty consists of a set of states $S$, a set of outcomes $Z$, a set of acts $\mathcal{F}$ such that each $f\in\mathcal{F}$ is some function from $S$ to $Z$, and a preference relation $\succeq$ over $\mathcal{F}$.
- $\succeq$ has a **subjective** expected utility representation iff there exists some probability distribution $P$ on $S$ and some utility function $u$ on $Z$ such that $f\succeq f'\Leftrightarrow\int uf(s)P(s)ds\geq\int uf'(s)P(s)ds$.