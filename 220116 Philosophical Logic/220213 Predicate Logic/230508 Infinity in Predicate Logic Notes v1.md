# Infinity in Predicate Logic

- Some set $\Gamma$ of sentences is finitely satisfiable iff each finite subset of $\Gamma$ is satisfiable.

## Natural Numbers
- In predicate logic with identity, the sentence "there is at least one $F$ thing" can be formalised as "$\exists xFx$". The sentence "there are at least two $F$ things" can be formalised as "$\exists x\exists x':(Fx\land Fx'\land x\neq x')$" (where "$x\neq x'$" abbreviates "$\lnot x=x'$"). Similarly, the sentence "there are at least three $F$ things" can be formalised as "$\exists x\exists x'\exists x'':(Fx\land Fx'\land Fx''\land x\neq x'\land x\neq x''\land x'\neq x'')$". This strategy generalises. Let "$\exists_n F$" abbreviate the formalisation of "there are at least $n$ $F$ things".
- $\{\exists_n F:n\in\mathbb{N}\}$ is the set of sentences that formalise "there is at least one $F$ thing", "there are at least two $F$ things", and so on.

## Inequality
- The sentence "there exists a one-to-one mapping from the $F$ things to the $G$ things" can be formalised in second-order logic as
	- "$\begin{aligned}\exists R[&\forall x\forall y (Rxy\rightarrow Fx\land Gy)\\&\land\lnot\exists x\exists y_1\exists y_2(Rxy_1\land Rxy_2\land y_1\neq y_2\land Fx\land Gy_1\land Gy_2)\\&\land\lnot\exists x_1\exists x_2\exists y(Rx_1y\land Rx_2y\land x_1\neq x_2\land Fx_1\land Fx_2\land Gy)]\end{aligned}$".
	- "$\begin{aligned}\exists R[&\forall x\forall y (Rxy\rightarrow Fx\land Gy)\land\forall x(Fx\rightarrow\exists yRxy)\\&\land\lnot\exists x\exists y_1\exists y_2(Rxy_1\land Rxy_2\land y_1\neq y_2)\\&\land\lnot\exists x_1\exists x_2\exists y(Rx_1y\land Rx_2y\land x_1\neq x_2)]\end{aligned}$" seems more accurate.
	- This reads as "there exists binary relation $R$, from $F$ things to $G$ things, whose domain is all the $F$ things, no $F$ thing is mapped to two distinct $G$ things (this relation is functional), and no two distinct $F$ things map to the same $G$ thing (this relation is one-to-one). Let "$F\leq G$" abbreviate the formalisation of "there exists a one-to-one mapping from the $F$ things to the $G$ things".
- The sentence "there are strictly more $F$ things than $G$ things" can be formalised as "$(G\leq F)\land\lnot(F\leq G)$". Let "$F<G$" abbreviate this formalisation.

## Subsets
- The sentence "the $F$ things are a subset of the $G$ things" can be formalised as "$\forall x(Fx\rightarrow Gx)$". Let "$F\subseteq G$" abbreviate this formalisation.
- The sentence "the $F$ things are a strict subset of the $G$ things" can be formalised as "$(F\subseteq G)\land\lnot(G\subseteq F)$". Let $F\subset G$ abbreviate this formalisation.

## Infinity
- The sentence "there are (Dedekind) infinitely many $F$ things" can be formalised as "$\exists F'[F'\subset F\land(F\leq F')\land(F'\leq F)]$". Let "$\infty F$" abbreviate this sentence.
	- Some set $S$ is Dedekind infinite iff there is some proper subset $S'\subset S$ such that $|S|=|S'|$, i.e. $S$ and $S'$ have the same number of elements.
- So, for example, the argument "there are finitely many earthlings, there are infinitely many aliens, so there are more aliens than earthlings" can be formalised as "$\lnot\infty E;\infty A;E<A$".

## Existence in First-Order Logic
- In first-order logic (with identity) the set $\{\exists_n F:n\in\mathbb{N}\}\cup\{\lnot\infty F\}$ is not satisfiable, but is finitely satisfiable. So if "$\lnot\infty F$" exists in first-order logic, then first-order logic is not compact. Given that first-order logic is compact (finite satisfiability implies satisfiability), by reductio, "$\lnot\infty F$" does not exist in first-order logic. Because "$\lnot\infty F$" exists iff "$\infty F$" exists, "$\infty F$" does not exist in first-order logic either.
- In first-order logic (with identity) the set $\{F>G\}\cup\{\exists_n F:n\in\mathbb{N}\}\cup\{\exists_n G:n\in\mathbb{N}\}$ is satisfiable in a model with an uncountably infinite domain, but not in a model with a countably infinite domain, or a model with a finite domain. Given that in first-order logic satisfiability in an uncountably infinite domain implies satisfiability in a countably infinite domain, by reductio, "$F>G$" does not exist in first-order logic.