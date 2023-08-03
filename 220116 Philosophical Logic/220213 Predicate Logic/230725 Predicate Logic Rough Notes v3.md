# Predicate Logic Rough Notes

## Exam Technique
- For "impossible" questions, reasonable credit will be awarded for some attempt. For example, by testing notable cases like the empty set or the universal relation.
- For semantic proofs in second-order logic, "it is acceptable to use words once in the set-theoretic part of the proof, but the form of the proof is otherwise similar to the form of proofs in PL, MPL, PC, SC, LC".
- The ancestral relation $R^*ab$ abbreviates $\forall X[\forall x(Rax\rightarrow Xx)\land\forall y_1\forall y_2(Xy_1\land Ry_1y_2\rightarrow Xy_2)\rightarrow Xb]$.

## Classical Predicate Logic

### Syntax
- Definition (PC-Term)
	- $\lnot,\rightarrow,\forall$ are the PC-connectives, $x,y,x_1,y_1,x_2,\ldots$ are the PC-variables, $F,G,F_1,G_1,F_2,\ldots$ are the $n$-place PC-predicates, $a,b,a_1,b_1,a_2,\ldots$ are the PC-constants. If $\alpha$ is a PC-variable or a PC-constant, then $\alpha$ is a PC-term.
- Definition (PC-wff)
	- If $\Pi$ is a $n$-place PC-predicate, and each of $\alpha_1,\ldots,\alpha_n$ is a PC-term, then $\Pi\alpha_1\ldots\alpha_n$ is a PC-wff.
	- If each of $\phi,\psi$ is a PC-wff, and $\alpha$ is a PC-variable, then each of $\lnot\phi$, $(\phi\rightarrow\psi)$, and $\forall\alpha\phi$ is a PC-wff.
	- Only strings that can be shown to be PC-wffs by the above clauses are PC-wffs.
	- PC-term and PC-wff are defined simultaneously and recursively.
- Abbreviations
	- "$\exists\alpha\phi$" abbreviates "$\lnot\forall\alpha\lnot\phi$.
	- Abbreviations for "$\phi\land\psi$", "$\phi\lor\psi$", and "$\phi\leftrightarrow\psi$" are introduced in the familiar way.
	- The familiar bracketing conventions apply.
- Definition (Free Variable Occurrence)
	- An occurrence of PC-variable $\alpha$ in PC-wff $\phi$ is bound iff it occurs in a subformula of the form $\forall\alpha\psi$, an occurrence of $\alpha$ is free otherwise.

### Semantics
- Definition (PC-Model)
	- A PC-model $\mathcal{M}$ is a pair $\langle\mathcal{D},\mathcal{I}\rangle$ such that:
		- $\mathcal{D}$ is a non-empty set, the domain, and
		- $\mathcal{I}$ is a function on the set of constants and predicates, the interpretation function, such that:
			- for all constants $\alpha$, $\mathcal{I}(\alpha)\in\mathcal{D}$, and
			- for all $n$-place predicates $\Pi$, $\mathcal{I}(\Pi)$ is some $n$-place relation over $\mathcal{D}$.
- Definition (PC-Variable Assignment)
	- A PC-variable assignment $g$ for model $\mathcal{M}=\langle\mathcal{D},\mathcal{I}\rangle$ is a function on the set of variables such that for all variables $\alpha$, $g(\alpha)\in\mathcal{D}$.
- Definition (PC-Variant Assignment)
	- A PC-variant assignment $g_u^\alpha$, where $\alpha$ is some variable and $u\in\mathcal{D}$, of variable assignment $g$ for model $\mathcal{M}=\langle\mathcal{D},\mathcal{I}\rangle$ is the variable assignment such that $g_u^\alpha(\beta)=\begin{cases}u&\text{ if }\beta=\alpha\\g(\beta)&\text{ otherwise}\end{cases}$. In words, $g_u^{\alpha}$ is the variable assignment that differs from $g$ only in assigning $u$ to $\alpha$.
- Definition (PC-Term Denotation)
	- The PC-term denotation $[\alpha]_{\mathcal{M},g}$ of term $\alpha$ for model $\mathcal{M}$ and variable assignment $g$ for $\mathcal{M}$ is such that $[\alpha]_{\mathcal{M},g}=\begin{cases}\mathcal{I}(\alpha)&\text{ if }\alpha\text{ is a constant}\\g(\alpha)&\text{ if }\alpha\text{ is a variable}\end{cases}$.
- Definition (PC-Valuation)
	- The PC-valuation $V_{\mathcal{M},g}$ for model $\mathcal{M}=\langle\mathcal{D},\mathcal{I}\rangle$ and variable assignment $g$ for $\mathcal{M}$ is the unique function from the set of PC-wffs to the set of truth values $\{0,1\}$ such that:
		- $V_{\mathcal{M},g}(\Pi\alpha_1\ldots\alpha_n)=1$ iff $\langle[\alpha_1]_{\mathcal{M},g},\ldots,[\alpha_n]_{\mathcal{M},g}\rangle\in\mathcal{I}(\Pi)$, for all $n$-place predicates $\Pi$ and terms $\alpha_1,\ldots,\alpha_n$,
		- $V_{\mathcal{M},g}(\forall\alpha\phi)=1$ iff for all $u\in\mathcal{D}$, $V_{\mathcal{M},g_u^{\alpha}}(\phi)=1$, for all variables $\alpha$ and PC-wffs $\phi$,
		- $V_{\mathcal{M},g}(\lnot\phi)=1$ iff $V_{\mathcal{M},g}(\phi)=0$, and
		- $V_{\mathcal{M},g}(\phi\rightarrow\psi)=1$ iff $V_{\mathcal{M},g}(\phi)=0$ or $V_{\mathcal{M},g}(\psi)=1$.
	- The definition of PC-valuation and the definition of $\exists\alpha\phi$ together imply $V_{\mathcal{M},g}(\exists\alpha\phi)=1$ iff for some $u\in\mathcal{D}$, $V_{\mathcal{M},g_u^{\alpha}}(\phi)=1$, for all variables $\alpha$ and PC-wffs $\phi$.
- Definition (PC-Validity)
	- PC-wff $\phi$ is valid iff for all models $\mathcal{M}$ for all variable assignments $g$ for $\mathcal{M}$, $V_{\mathcal{M},g}(\phi)=1$.
- Definition (PC-Semantic Consequence)
	- PC-wff $\phi$ is a PC-semantic consequence of set of wffs $\Gamma=\{\gamma_1,\gamma_2,\ldots\}$ iff for all models $\mathcal{M}$ for all variable assignments $g$ for $\mathcal{M}$, if for all $\gamma\in\Gamma$, $V_{\mathcal{M},g}(\gamma)=1$, then $V_{\mathcal{M},g}(\phi)=1$.

## Predicate Logic with Identity

### Syntax
- The syntax of $PC_{=}$ is exactly analogous to that of $PC$ except in:
	- including the connective $=$,
	- including the additional clause in the definition of a wff:
		- if each of $\alpha,\beta$ is a term, then $\alpha=\beta$ is a wff.

### Semantics
- Definition ($PC_=$-Valuation)
	- The definition of $PC_{=}$-valuation is exactly analogous to that of $PC$-valuation except in including the additional clause:
		- $V_{\mathcal{M},g}(\alpha=\beta)=1$ iff $[\alpha]_{\mathcal{M},g}=[\beta]_{\mathcal{M},g}$, for all terms $\alpha,\beta$.

## Predicate Logic with Complex Terms

### Syntax
- The syntax of $PC_{\iota}$ is exactly analogous to that of $PC$ except in:
	- including the connective $\iota$,
	- including the additional clause in the definition of a term:
		- if $\alpha$ is a variable and $\phi$ is a wff, then $\iota\alpha\phi$ is a term.
- Note that $PC_{\iota}$-term and $PC_{\iota}$-wff are defined simultaneously and recursively, in the (non-trivial) sense that the definition of $PC_{\iota}$-term refers to $PC_{\iota}$-wffs and the definition of $PC_{\iota}$-wff refers to $PC_{\iota}$-terms.

### Semantics
- Definition ($PC_{\iota}$-Term Denotation)
	- The definition of $PC_{\iota}$-term denotation is exactly analogous to that of $PC$-term denotation except in including the additional case:
		- $[\iota\alpha\phi]_{\mathcal{M},g}=\begin{cases}\text{the unique }u\in\mathcal{D}\text{ such that }V_{\mathcal{M},g_u^{\alpha}}(\phi)=1&\text{if such }u\text{ exists}\\\text{undefined}&\text{otherwise}\end{cases}$.
- Definition ($PC_{\iota}$-Valuation)
	- The definition of $PC_{\iota}$-valuation is exactly analogous to that of $PC$-valuation except in modifying the clause for elementary wffs as follows:
		- $V_{\mathcal{M},g}(\Pi\alpha_1\ldots\alpha_n)=1$ iff each of $[\alpha_1]_{\mathcal{M},g},\ldots,[\alpha_n]_{\mathcal{M},g}$ is defined and $\langle[\alpha_1]_{\mathcal{M},g},\ldots,[\alpha_n]_{\mathcal{M},g}\rangle\in\mathcal{I}(\Pi)$, for all $n$-place predicates $\Pi$ and terms $\alpha_1,\ldots,\alpha_n$.
	- This modification is simply to account for instances of undefined complex terms.
- Note that $PC_{\iota}$-term denotation and $PC_{\iota}$ are defined simultaneously and recursively in a non-trivial sense.

## Predicate Logic with Complex Predicates

### Syntax
- The syntax of $PC_{\lambda}$ is exactly analogous to that of $PC$ except in:
	- including the additional clause in the definition of a $n$-place predicate:
		- if $\alpha$ is a variable and $\phi$ is a wff, then $\lambda\alpha\phi$ is a $1$-place predicate.

### Semantics
- Definition (Extension of a Complex Predicate)
	- The extension $\phi^{\mathcal{M},g,\alpha}$ of a complex predicate $\lambda\alpha\phi$ is given by $\phi^{\mathcal{M},g,\alpha}=\{u\in\mathcal{D}:V_{\mathcal{M},g_u^{\alpha}}(\phi)=1\}$.
- Definition ($PC_{\lambda}$-Valuation)
	- The definition of $PC_{\lambda}$-valuation is exactly analogous to that of $PC$-valuation except in:
		- modifying the clause for elementary wffs as follows:
			- $V_{\mathcal{M},g}(\Pi\alpha_1\ldots\alpha_n)=1$ iff $\langle[\alpha_1]_{\mathcal{M},g},\ldots,[\alpha_n]_{\mathcal{M},g}\rangle\in\mathcal{I}(\Pi)$, for all $n$-place simple predicates $\Pi$ and terms $\alpha_1,\ldots,\alpha_n$,
		- including the additional clause:
			- $V_{\mathcal{M},g}((\lambda\alpha\phi)(\beta))=1$ iff $[\beta]_{\mathcal{M},g}\in\phi^{\mathcal{M},g,\alpha}$ for all variables $\alpha$, terms $\beta$, and wffs $\phi$.

## Second-Order Logic

### Syntax
- The syntax of SOL is exactly analogous to that of PC except in:
	- including the following definition of predicate variables:
		- $X,Y,X_1,Y_1,X_2,\ldots$ are the SOL-predicate variables,
	- including the additional clauses in the definition of a SOL-wff:
		- if $\pi$ is a $n$-place predicate variable, and each of $\alpha_1,\ldots,\alpha_n$ is a term, then $\pi\alpha_1\ldots\alpha_n$ is a wff,
		- if $\pi$ is a $n$-place predicate variable and $\phi$ is a wff, then $\forall\pi\phi$ is a wff.

### Semantics
- Definition (SOL-Model)
	- Th definition of a SOL model is identical to that of a PC model.
- Definition (SOL-Variable Assignment)
	- A SOL-variable assignment $g$ for model $\mathcal{M}=\langle\mathcal{D},\mathcal{I}\rangle$ is a function on the set of variables and predicate variables such that for each variable $\alpha$, $g(\alpha)\in\mathcal{D}$ and for each $n$-place predicate variable $\pi$, $g(\pi)$ is a $n$-place relation over $\mathcal{D}$.
- Definition (SOL-Variant Assignment)
	- A SOL-variant assignment $g_u^\alpha$, where $\alpha$ is some variable and $u\in\mathcal{D}$, of variable assignment $g$ for model $\mathcal{M}=\langle\mathcal{D},\mathcal{I}\rangle$ is the variable assignment such that $g_u^\alpha(\beta)=\begin{cases}u&\text{ if }\beta=\alpha\\g(\beta)&\text{ otherwise}\end{cases}$. In words, $g_u^{\alpha}$ is the variable assignment that differs from $g$ only in assigning $u$ to $\alpha$.
	- A SOL-variant assignment $g_U^\pi$, where $\pi$ is some $n$-place predicate variable and $U$ is some $n$-place relation over $\mathcal{D}$, of variable assignment $g$ for model $\mathcal{M}=\langle\mathcal{D},\mathcal{I}\rangle$ is the variable assignment such that $g_U^\pi(\rho)=\begin{cases}U&\text{ if }\rho=\pi\\g(\rho)&\text{ otherwise}\end{cases}$. In words, $g_U^{\pi}$ is the variable assignment that differs from $g$ only in assigning $U$ to $\pi$.
- Definition (SOL-Valuation)
	- The definition of SOL-valuation is exactly analogous to that of PC-valuation except in including the additional clauses:
		- $V_{\mathcal{M},g}(\pi\alpha_1\ldots\alpha_n)=1$ iff $\langle[\alpha_1]_{\mathcal{M},g},\ldots,[\alpha_n]_{\mathcal{M},g}\rangle\in g(\pi)$,
		- $V_{\mathcal{M},g}(\forall\pi\phi)=1$ iff for every $n$-place relation $U$ over $\mathcal{D}$, $V_{\mathcal{M},g_U^{\pi}}(\phi)=1$.