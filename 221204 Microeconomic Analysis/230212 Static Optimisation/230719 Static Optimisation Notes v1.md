# Static Optimisation Notes

## Exam Technique
- In general, it is possible to simplify a constraint of the form $\underline{x}\leq x\leq\bar{x}$ to a single quadratic constraint. For example, $-1\leq x\leq 3$ simplifies to $(x-1)^2\leq 4$.
- Be careful to note which positivity constraints can be neglected, it is not always the case that all can be neglected.
- If an additional constraint is imposed, and solutions to the original problem are known, for the new Lagrangian, it is only necessary to check cases where the additional constraint binds.
- It is always necessary to argue for the necessity/sufficiency of the FOCs. In the case where the optimisation problem is concave or convex this is trivial. In the case where it is not (because, for example, the constraint set is not convex), check the constraint qualification and appeal to the Weierstrass extreme value theorem.

## Unconstrained Optimisation
- $\mathbf{\overrightarrow{x}}\in S$ is a global maximum of $C^2$ (i.e. twice-continuously differentiable) $f:\mathbb{R}^n\rightarrow\mathbb{R}$ on $S\subseteq\mathbb{R}^n$ iff $f(\mathbf{\overrightarrow{x}})\geq f(\mathbf{\overrightarrow{x'}})$ for all $\mathbf{\overrightarrow{x'}}\in S$.
- $\mathbf{\overrightarrow{x}}\in S$ is a local maximum of $C^2$ $f:\mathbb{R}^n\rightarrow\mathbb{R}$ on $S\subseteq\mathbb{R}^n$ iff $f(\mathbf{\overrightarrow{x}})\geq f(\mathbf{\overrightarrow{x'}})$ for all $\mathbf{\overrightarrow{x'}}$ in some neighbourhood of $\mathbf{\overrightarrow{x}}$.
	- These are strict maxima iff the inequalities are strict for $\mathbf{\overrightarrow{x}}\neq\mathbf{\overrightarrow{x'}}$.
	- An interior maximum occurs at an interior point of $S$, a constrained optimum occurs on the boundary of $S$.

### First-Order Condition
- An optimisation problem is unconstrained iff $S=\mathbb{R}^n$, then there are no constrained optima.
- The first-order condition for an unconstrained optimum is $Df(\mathbf{\overrightarrow{x}})=\mathbf{\overrightarrow{0}}$. This is necessary but not sufficient for an unconstrained optimum.

### Second-Order Conditions
- The second-order sufficient conditions for an unconstrained optimum are as follows. If $D^2f(\mathbf{\overrightarrow{x^*}})$ is negative definite, then $\mathbf{\overrightarrow{x^*}}$ is a strict local maximum, if $D^2f(\mathbf{\overrightarrow{x^*}})$ is positive definite, then $\mathbf{\overrightarrow{x^*}}$ is a strict local minimum, and if $D^2f(\mathbf{\overrightarrow{x^*}})$ is indefinite, then $\mathbf{\overrightarrow{x^*}}$ is a saddle point, where $\mathbf{\overrightarrow{x^*}}$ satisfies the first-order condition.
- The second-order necessary conditions for an unconstrained optimum are as follows. Only if $D^2f(\mathbf{\overrightarrow{x^*}})$ is negative semi-definite, then $\mathbf{\overrightarrow{x^*}}$ is a local maximum, only if $D^2f(\mathbf{\overrightarrow{x^*}})$ is positive semi-definite, then $\mathbf{\overrightarrow{x^*}}$ is a local minimum.

#### Definiteness
- A $n$-square symmetric matrix $A$ is positive definite iff $\forall \mathbf{\overrightarrow{x}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n:\mathbf{\overrightarrow{x^T}}A\mathbf{\overrightarrow{x}}>0$.
	- The intuition for the relevance of definiteness to optimisation is as follows. Consider the second-order Taylor expansion of $f$ around candidate optimum $\mathbf{\overrightarrow{x^*}}$, $f(\mathbf{\overrightarrow{x^*}}+\mathbf{\overrightarrow{a}})\approx f(\mathbf{\overrightarrow{x^*}})+Df(\mathbf{\overrightarrow{x^*}})\mathbf{\overrightarrow{a}}+\frac{1}{2}\mathbf{\overrightarrow{a^T}}D^2f(\mathbf{\overrightarrow{x^*}})\mathbf{\overrightarrow{a}}$. Given that (by the first-order condition) $Df(\mathbf{\overrightarrow{x^*}})=0$, the approximation reduces to $f(\mathbf{\overrightarrow{x^*}}+\mathbf{\overrightarrow{a}})\approx f(\mathbf{\overrightarrow{x^*}})+\frac{1}{2}\mathbf{\overrightarrow{a^T}}D^2f(\mathbf{\overrightarrow{x^*}})\mathbf{\overrightarrow{a}}$. So, informally, all $\mathbf{\overrightarrow{x}}$ in a neighbourhood of $\mathbf{\overrightarrow{x^*}}$ are such that $f(\mathbf{\overrightarrow{x}})>f(\mathbf{\overrightarrow{x^*}})$, i.e. $\mathbf{\overrightarrow{x^*}}$ is a local minimum iff $\forall\mathbf{\overrightarrow{a}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n:\mathbf{\overrightarrow{a^T}}D^2f(\mathbf{\overrightarrow{x^*}})\mathbf{\overrightarrow{a}}>0$.
- A $n$-square symmetric matrix $A$ is negative definite iff $\forall \mathbf{\overrightarrow{x}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n:\mathbf{\overrightarrow{x^T}}A\mathbf{\overrightarrow{x}}<0$. The conditions for semi-definiteness are identical except in replacing the strict inequalities with weak inequalities. A $n$-square symmetric matrix $A$ is indefinite iff it is neither positive semi-definite nor negative semi-definite.
- The following table summarises the tests for definiteness.

|Definiteness|$\mathbf{\overrightarrow{x^T}}A\mathbf{\overrightarrow{x}}$ Test|Eigenvalue Test|Determinant Test|
|---|---|---|---|
|Positive Definite|$\forall\mathbf{\overrightarrow{x}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n:\mathbf{\overrightarrow{x}}^TA\mathbf{\overrightarrow{x}}>0$|$\forall\lambda>0$|$\forall k:\det A_k>0$|
|Positive Semi-Definite|$\forall\mathbf{\overrightarrow{x}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n:\mathbf{\overrightarrow{x}}^TA\mathbf{\overrightarrow{x}}\geq0$|$\forall\lambda\geq0$|Complicated|
|Negative Definite|$\forall\mathbf{\overrightarrow{x}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n:\mathbf{\overrightarrow{x}}^TA\mathbf{\overrightarrow{x}}<0$|$\forall\lambda<0$|$\forall k:(-1)^k\det A_k>0$|
|Negative Semi-Definite|$\forall\mathbf{\overrightarrow{x}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n:\mathbf{\overrightarrow{x}}^TA\mathbf{\overrightarrow{x}}\leq0$|$\forall\lambda\leq0$|Complicated|
|Indefinite|Otherwise|Otherwise|Otherwise|

- Where $|A_k|$ is the $k^{th}$ leading principal minor of $A$, i.e. the determinant of the $k$-square submatrix of $A$ that retains only the first $k$ rows and first $k$ columns.
- For a $2\times2$ matrix, the signs of the eigenvalues can be inferred from the determinant and trace of the matrix. The determinant of a $2\times2$ matrix is equal to the product of its eigenvalues, and the trace is equal to the sum of its eigenvalues.

## Optimisation with Equality Constraints
- The generic optimisation problem with equality constraints is $\max_{\mathbf{\overrightarrow{x}}}f(\mathbf{\overrightarrow{x}})\text{ s.t. }\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x}})=\mathbf{\overrightarrow{a}}$, where $f:\mathbb{R}^n\rightarrow\mathbb{R}$ is the $C^2$ objective function, $\mathbf{\overrightarrow{h}}:\mathbb{R}^n\rightarrow\mathbb{R}^m$ is $C^2$, and $\mathbf{\overrightarrow{a}}\in\mathbb{R}^m$.
	- In this representation, there are $n$ variables and $m$ constraints. In what follows, let $i$ index the variables and $j$ index the constraints.
	- The constraint set is $\{\mathbf{\overrightarrow{x}}:\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x}})=\mathbf{\overrightarrow{a}}\}$.

### Weierstrass Extreme Value Theorem
- If the objective function is continuous and the constraint set is compact (closed and bounded), then by the Weierstrass extreme value theorem, then a global (constrained) maximum (of the objective function) and a global minimum exist. If a maximum and a minimum exist, it is not necessary to verify the second order conditions at stationary points, and the global maximum and global minimum can be found by evaluating the objective function at the stationary points.
	- The constraint set is closed, informally, if the constraints are weak inequality constraints, and/or if the boundaries of the constraint set are in the constraint set. Formally, the constraint set is closed iff any sequence of points, each in the constraint set, converges to some point in the constraint set.
	- The constraint set is bounded iff there exists some ball that contains that set. A necessary condition for boundedness is that there exists some upper bound and some lower bound on each variable.

### Lagrangian Optimisation
- The Lagrangian function $L(\mathbf{\overrightarrow{x}};\mathbf{\overrightarrow{\lambda}})\equiv f(\mathbf{\overrightarrow{x}})-\sum_{j=1}^m\lambda_j(h_j(\mathbf{\overrightarrow{x}})-a_j)$ is the objective function less some weighted sum of the $m$ constraints.
- The constraint qualification is the condition that $D\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x}})$ is full rank. If the constraint qualification holds at some point $\mathbf{\overrightarrow{x}}$, the Lagrangian first-order conditions are necessary for an optimum at $\mathbf{\overrightarrow{x}}$.
	- This follows from Lagrange's Theorem, which states that  if $\mathbf{\overrightarrow{x^*}}$ is a local maximum of $f$ subject to the constraint $\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x}})=\mathbf{\overrightarrow{a}}$, and the constraint qualification is satisfied, then there exists $\mathbf{\overrightarrow{\lambda^*}}=(\lambda^1,\ldots,\lambda^m)$ such that $D_{\mathbf{\overrightarrow{x}}}L(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})=\mathbf{\overrightarrow{0}}$.
	- At points where the constraint qualification is not satisfied, the Lagrangian first-order conditions are not necessary for an optimum. Evaluate the objective function at these points and compare against the value of the objective function at the stationary points to determine the optimum.

#### Lagrangian First-Order Conditions
- The Lagrangian first-order conditions are:
	- $D_{\mathbf{\overrightarrow{x}}}L(\mathbf{\overrightarrow{x}};\mathbf{\overrightarrow{\lambda}})=Df(\mathbf{\overrightarrow{x}})-\sum_{j=1}^m\lambda_j(Dh_j(\mathbf{\overrightarrow{x}}))=\mathbf{\overrightarrow{0}}$.
	- $\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x}})=\mathbf{\overrightarrow{a}}$.
	- In words, the derivative of the Lagrangian function with respect to each variable is zero, and all constraints are satisfied.
- The Lagrangian multiplier $\lambda_j$ is a measure of the sensitivity of the objective function to a relaxation of constraint $j$. $\lambda_j=\frac{\partial f(\mathbf{\overrightarrow{x}}^*(\mathbf{\overrightarrow{a}}))}{\partial a_j}$.

#### Lagrangian Second-Order Conditions
- It is only necessary to evaluate the Lagrangian second-order conditions iff it is not known that an optimum exists (or if required by the question).
	- If the objective function is continuous and the constraint set is closed and bounded, then by the Weierstrass extreme value theorem, an optimum exists. If the constraint qualification is satisfied at all points, then the first-order conditions are necessary. Then the only candidate optima are those that satisfy the first-order conditions. The global optima can be found by evaluating the objective function at these points and comparing.
- The Lagrangian second-order conditions are (these are never directly applied):
	- If $\forall\mathbf{\overrightarrow{v}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n$ such that $D\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x^*}})\mathbf{\overrightarrow{v}}=0$, $\mathbf{\overrightarrow{v^T}}D_{\mathbf{\overrightarrow{x}}}^2L(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})\mathbf{\overrightarrow{v}}<0$, then $(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})$ is a strict local maximum, where $(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})$ satisfies the constraint qualification and the first-order conditions.
	- If $\forall\mathbf{\overrightarrow{v}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n$ such that $D\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x^*}})\mathbf{\overrightarrow{v}}=0$, $\mathbf{\overrightarrow{v^T}}D_{\mathbf{\overrightarrow{x}}}^2L(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})\mathbf{\overrightarrow{v}}>0$, then $(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})$ is a strict local minimum, where $(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})$ satisfies the constraint qualification and the first-order conditions.
- The Lagrangian second-order conditions can be evaluated by the bordered Hessian test.
	- The relevant bordered Hessian matrix is $BH=\begin{bmatrix}\mathbf{0}_{m\times m}&D\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x^*}})\\D\mathbf{\overrightarrow{h}}(\mathbf{\overrightarrow{x^*}})^T&D_{\mathbf{\overrightarrow{x}}}^2L(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})\end{bmatrix}$. The bordered Hessian matrix is constructed from the Jacobian matrix of the binding constraints and the Hessian matrix of the Lagrangian function.
	- **Let $|BH_r|$ denote the $(m+r)^{th}$ leading principal minor (i.e. the determinant of the top-left sub-matrix with $m+r$ rows and $m+r$ columns).** 
	- **$(\mathbf{\overrightarrow{x^*}},\mathbf{\overrightarrow{\lambda^*}})$ is a strict local minimum iff $\forall r\in\{m+1,\ldots,n\}:sign(|BH_r|)=(-1)^m$, which implies that all such $|BH_r|$ have the same sign.**
	- **$(\mathbf{\overrightarrow{x^*}},\mathbf{\overrightarrow{\lambda^*}})$ is a strict local maximum iff $\forall r\in\{m+1,\ldots,n\}:sign(|BH_r|)=(-1)^r$, i.e. $|BH_r|$ alternates in sign, and $|BH_n|=|BH|$ has sign $(-1)^n$.**
	- **There are $n-m$ determinants to be evaluated. This is the number of degrees of freedom at the stationary point $\mathbf{\overrightarrow{x}}$, which is the number of variables less the number of binding constraints at this point.**

## Optimisation with Inequality Constraints
- The generic optimisation problem with inequality constraints is $\max_{\mathbf{\overrightarrow{x}}}f(\mathbf{\overrightarrow{x}})\text{ s.t. }\mathbf{\overrightarrow{g}}(\mathbf{\overrightarrow{x}})\leq\mathbf{\overrightarrow{b}}$, where $f:\mathbb{R}^n\rightarrow\mathbb{R}$ is the $C^2$ objective function, $\mathbf{\overrightarrow{g}}:\mathbb{R}^n\rightarrow\mathbb{R}^m$ is $C^2$ and $\mathbf{\overrightarrow{b}}\in\mathbb{R}^m$.
	- The constraint set is defined analogously to optimisation with equality constraints.

### Kuhn-Tucker Optimisation
- The Lagrangian function is defined analogously to optimisation with equality constraints.
	- The sign on each $\lambda_j(g_j(\mathbf{\overrightarrow{x}})-b_j)$ term depends on whether the optimisation problem is a maximisation problem or a minimisation problem and whether the inequality constraint is a $\geq$ constraint or a $\leq$ constraint. Intuitively, this term "penalises" violation of the constraint. So for example, for a maximisation problem and a $\leq$ constraint, the relevant $\lambda_j(g_j(\mathbf{\overrightarrow{x}})-b_j)$ term will be positive when the constraint is violated, so the $\lambda_j(g_j(\mathbf{\overrightarrow{x}})-b_j)$ term should have a negative sign that "acts against" maximisation.
- The constraint qualification is the condition that the Jacobian matrix of the binding constraints is full rank. If the constraint qualification holds, the Kuhn-Tucker first-order conditions are necessary for an optimum.
	- This follows from the Kuhn-Tucker theorem, which states that if $\mathbf{\overrightarrow{x^*}}$ is a local maximum of $f$ subject to the constraints $\mathbf{\overrightarrow{g}}(\mathbf{\overrightarrow{x}})\leq\mathbf{\overrightarrow{b}}$, and the constraint qualification is satisfied, then there exists $\mathbf{\overrightarrow{\lambda^*}}$ such that $D_{\mathbf{\overrightarrow{x}}}L(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})=\mathbf{\overrightarrow{0}}$ (i.e. the Lagrangian first-order conditions hold) and for all $j\in\{1,\ldots,m\}$, $\lambda_j^*\geq0$, $g_j(\mathbf{\overrightarrow{x^*}})-b_j\leq0$ and $\lambda_j(g_j(\mathbf{\overrightarrow{x^*}})-b_j)=0$ (i.e. each Lagrangian multiplier is non-negative, each constraint is satisfied, and each "penalty term" is zero).

#### Kuhn-Tucker First-Order Conditions
- The Kuhn-Tucker first-order conditions are:
	- $D_{\mathbf{\overrightarrow{x}}}L(\mathbf{\overrightarrow{x}};\mathbf{\overrightarrow{\lambda}})=Df(\mathbf{\overrightarrow{x}})-\sum_{j=1}^m\lambda_j(Dh_j(\mathbf{\overrightarrow{x}}))=\mathbf{\overrightarrow{0}}$.
		- This is identical to the Lagrangian first-order conditions.
	- $\forall j\in\{1,\ldots,m\}:\lambda_j^*\geq0\land g_j(\mathbf{\overrightarrow{x^*}})\leq b_j\land\lambda_j^*(g_j(\mathbf{\overrightarrow{x^*}})-b_j)=0$. In words, each Kuhn-Tucker multiplier is non-negative, each constraint is satisfied, and each "penalty term" is zero.
		- These are the complementary slackness conditions.
- The Kuhn-Tucker multiplier $\lambda_j$ is a measure of the sensitivity of the objective function to a relaxation of the constraint $j$.

#### Kuhn-Tucker Second-Order Conditions
- It is again only necessary to evaluate the Kuhn-Tucker second-order conditions iff it is not known that an optimum exists (or if required by the question).
- The Kuhn-Tucker second-order conditions are:
	- If $e\neq0$ (i.e. some constraints bind at $\mathbf{\overrightarrow{x^*}}$) and $\forall\mathbf{\overrightarrow{v}}\neq\mathbf{\overrightarrow{0}}\in\mathbb{R}^n$ such that $D\mathbf{\overrightarrow{g_E}}(\mathbf{\overrightarrow{x^*}})\mathbf{\overrightarrow{v}}=0$, $\mathbf{\overrightarrow{v^T}}D_{\mathbf{\overrightarrow{x}}}^2L(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})\mathbf{\overrightarrow{v}}<0$, then $(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})$ is a strict local maximum, where $(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})$ satisfies the constraint qualification and the first-order conditions.
		-  This is analogous to the Lagrangian second-order conditions.
	- If $e=0$ (i.e. no constraints bind at $\mathbf{\overrightarrow{x^*}}$) and $D^2f(\mathbf{\overrightarrow{x^*}})$ is positive definite, then $\mathbf{\overrightarrow{x^*}}$ is a strict local maximum, where $(\mathbf{\overrightarrow{x^*}};\mathbf{\overrightarrow{\lambda^*}})$ satisfies the constraint qualification and the first-order conditions.
		- This is identical to the unconstrained second-order conditions.
- **The Kuhn-Tucker second-order conditions can be evaluated by the bordered Hessian test.**
	- The relevant bordered Hessian is constructed analogous to the bordered Hessian in the Lagrangian case from the Hessian matrix of the Lagrangian function and the Jacobian matrix of the binding constraints.

## Convexity and Concavity
- Function $f:S\rightarrow\mathbb{R}$, where $S$ is a convex set, is (weakly) convex iff $\forall\mathbf{\overrightarrow{x}},\mathbf{\overrightarrow{x'}}\in S:\forall t\in(0,1):f(t\mathbf{\overrightarrow{x}}+(1-t)\mathbf{\overrightarrow{x'}})\leq tf(\mathbf{\overrightarrow{x}})+(1-t)f(\mathbf{\overrightarrow{x'}})$. $f$ is (weakly) concave iff $\forall\mathbf{\overrightarrow{x}},\mathbf{\overrightarrow{x'}}\in S:\forall t\in(0,1):f(t\mathbf{\overrightarrow{x}}+(1-t)\mathbf{\overrightarrow{x'}})\geq tf(\mathbf{\overrightarrow{x}})+(1-t)f(\mathbf{\overrightarrow{x'}})$. The properties are strict if the inequalities are strict.
	- Set $S$ is convex iff $\forall\mathbf{\overrightarrow{x}},\mathbf{\overrightarrow{x'}}\in S:\forall t\in(0,1):t\mathbf{\overrightarrow{x}}+(1-t)\mathbf{\overrightarrow{x'}}\in S$.
- The convexity/concavity of a function can be evaluated by the definiteness of its Hessian.
	- $\forall x\in S:D^2f(x)\text{ is negative semi-definite}\Leftrightarrow f\text{ is concave.}$
		- Supposing that $f$ is $C^2$ and $S$ is convex.
	- $\forall x\in S:D^2f(x)\text{ is negative definite}\Rightarrow f\text{ is strictly concave.}$
	- $\forall x\in S:D^2f(x)\text{ is positive semi-definite}\Leftrightarrow f\text{ is convex.}$
	- $\forall x\in S:D^2f(x)\text{ is positive definite}\Rightarrow f\text{ is strictly convex.}$
	- The intuition for these relationships can be drawn from the one-dimensional case where, for example, a negative second derivative implies concavity.
- If $f$ is convex, then the stationary point $\mathbf{\overrightarrow{x_0}}$ such that $Df(\mathbf{\overrightarrow{x_0}})=\mathbf{\overrightarrow{0}}$ (if it exists) is a global minimum. If $f$ is concave, then the stationary point $\mathbf{\overrightarrow{x_0}}$ such that $Df(\mathbf{\overrightarrow{x_0}})=\mathbf{\overrightarrow{0}}$ (if it exists) is a global maximum.
	- If $f$ is strictly convex/concave, these optima are strict optima.
- An optimisation problem is convex iff it is a minimisation problem with a convex objective function and concave $\leq$ constraints. An optimisation problem is concave iff it is a maximisation problem with a concave objective function and convex $\geq$ constraints.
- If an optimisation problem is convex, the Kuhn-Tucker first-order conditions are sufficient for a maximum. If an optimisation problem is concave, the Kuhn-Tucker first-order conditions are sufficient for a minimum.
	- If an optimisation problem is convex/concave, and additionally the constraint set has a non-empty interior (or if the constraint qualification holds), then the first-order conditions are also necessary for a global maximum/minimum. The constraint set has non-empty interior iff there is some point that satisfies all constraints with strict inequality.
		- A set has non-empty interior iff there is some point in that set such that there is some open ball around that point that is entirely within that set.