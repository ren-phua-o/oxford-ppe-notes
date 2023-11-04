# Counterfactuals Rough Notes

## Stalnaker's Conditional
- Motivation
	- Counterfactual conditionals are conditionals of the form "if it were the case that $\phi$ (although it is not in fact the case), then it would be the case that $\psi$."
	- Two candidate formalisations of counterfactual conditionals in MPL are "$\phi\rightarrow\psi$" (material conditional) and "$\Box(\phi\rightarrow\psi)$" (strict conditional).
	- The material conditional is unsatisfactory as a formalisation of counterfactual conditionals because it obeys the false antecedent inference pattern (i.e. $\lnot\phi\vDash_K\phi\rightarrow\psi$) and it obeys the true consequent inference pattern (i.e. $\psi\vDash_K\phi\rightarrow\psi$). Natural language counterfactual conditionals apparently do not obey these inference patterns. For example, in natural language, we do not infer from "it is not snowing" that "if it is snowing, the Philosophical Logic exam would be cancelled", and we do not infer from "the lecture is on Monday" that "if the lecture is rescheduled to Thursday, then the lecture is on Monday".
	- Both the material conditional and the strict conditional are unsatisfactory because each obeys both augmentation (strengthening the antecedent) and contraposition (i.e. $\phi\rightarrow\psi\vDash_K\phi\land\psi\rightarrow\chi$, $\phi\rightarrow\psi\vDash_K\lnot\psi\rightarrow\phi$, $\Box(\phi\rightarrow\psi)\vDash_K\Box(\phi\land\chi)\rightarrow\psi$, $\Box(\phi\rightarrow\psi)\vDash_K\Box(\lnot\psi\rightarrow\lnot\phi)$). Natural language counterfactual conditionals apparently do not obey these inference patterns. For example, in natural language, we do not infer from "if the switch was flipped, then the light would be on" that "if the switch was flipped, and if the bulb had been removed, then the light would be on", and from "if it rained, it would not rain heavily" that "if it rained heavily, it would not rain".

### Syntax
- Definition (SC-wff)
	- $\lnot,\rightarrow,\Box,\Box\!\!\rightarrow$ are the SC-connectives, $P,Q,R,P_1,Q_1,R_1,P_2,\ldots$ are the SC-sentence letters.
	- Each sentence letter $\alpha$ is a SC-wff.
	- If each of $\phi$ and $\psi$ is a SC-wff, then each of $\lnot\phi$, $(\phi\rightarrow\psi)$, $\Box\phi$, and $\phi\Box\!\!\rightarrow\psi$ is a SC-wff.
	- Only strings that can be shown to be SC-wffs by the above clauses are SC-wffs.

### Semantics
- Definition (Preorder)
	- A binary relation $\preceq$ is a (weak) preorder of set $A$ iff $\preceq$ is reflexive and transitive on $A$.
- Definition (Linear Preorder)
	- A binary relation $\preceq$ is a linear preorder of set $A$ iff $\preceq$ is reflexive, transitive, and connected (for all $x\neq y$, $Rxy$ or $Ryx$) on $A$.
- Definition (Partial Order)
	- A binary relation $\preceq$ is a (weak) partial order of set $A$ iff $\preceq$ is reflexive, transitive, and antisymmetric on $A$.
- Definition (Linear Order)
	- A binary relation $\preceq$ is a linear order of set $A$ iff $\preceq$ is reflexive, transitive, antisymmetric, and connected on $A$.
	- A heuristic for the above is that a (partial) order is reflexive, transitive, and antisymmetric. "Adding" linearity adds connectedness. "Adding" "pre" removes asymmetry.
- Definition (Least Element)
	- Suppose $\preceq$ is a partial order on $A$ and $B\subseteq A$, then the least element $b_0$ in $B$ with respect to $\preceq$ is such that $b_0\in B$ and for all $b\in B$, $b_0\preceq b$. If $b_0$ exists, it is unique.
- Definition ($w$-Closest $\phi$-World)
	- Under the SC-model $\mathcal{M}=\langle\mathcal{W},\preceq,\mathcal{I}\rangle$, where $w\in\mathcal{W}$, the $w$-closest $\phi$-world, if it exists, is the world $u\in\mathcal{W}$ such that:
		- $V_{\mathcal{M}}(\phi,u)=1$, and
		- for all $u'\in\mathcal{W}$ such that $V_{\mathcal{M}}(\phi,u')=1$:
			- $u\preceq_wu'$.
- Definition (SC-Model)
	- A SC-model $\mathcal{M}$ is a triple $\langle\mathcal{W},\preceq,\mathcal{I}\rangle$ such that:
		- $\mathcal{W}$ is a non-empty set, the set of possible worlds,
		- $\preceq$ is a three-place relation on $\mathcal{W}$, the nearness relation, such that for each $w\in\mathcal{W}$:
			- $\preceq_w=\{\langle u,v\rangle:\langle u,v,w\rangle\in\preceq\}$ is a linear order on $\mathcal{W}$,
			- $w\preceq_wu$ for every $u\in\mathcal{W}$ (the base assumption),
			- Heuristically, the base assumption is the assumption that $w$ is weakly nearer to $w$ than all $u$ (hence, by antisymmetry, strictly nearer for all $u\neq w$).
		- $\mathcal{I}$ is a two-place function from sentence letters $\alpha$ and worlds $w$ to the set of truth values $\{0,1\}$, the interpretation function, such that:
			- If there exists $v\in\mathcal{W}$ such that $V_{\mathcal{M}}(\phi,v)=1$, then for all $w\in\mathcal{W}$, there exists $u\in\mathcal{W}$ such that $V_{\mathcal{M}}(\phi,u)=1$ and for all $u'$ such that $V_{\mathcal{M}}(\phi,u')=1$, $u\preceq_wu'$, i.e. if some $\phi$-world $v$, exists, then for each world $w$, there is a $w$-closest $\phi$-world $u$ (the limit assumption).
- Definition (SC-Valuation)
	- The SC-valuation $V_{\mathcal{M}}$ given model $\mathcal{M}=\langle\mathcal{W},\preceq,\mathcal{I}\rangle$ is the unique function from the set of wffs to the set of truth values $\{0,1\}$ for each world $w\in\mathcal{W}$ such that:
		- for all sentence letters $\alpha$, $V_{\mathcal{M}}(\alpha,w)=\mathcal{I}(\alpha,w)$,
		- $V_{\mathcal{M}}(\lnot\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,w)=0$,
		- $V_{\mathcal{M}}(\phi\rightarrow\psi,w)=0\text{ iff }V_{\mathcal{M}}(\phi,w)=1\text{ and }V_{\mathcal{M}}(\psi,w)=0$,
		- $V_{\mathcal{M}}(\Box\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,v)=1\text{ for all }v\in\mathcal{W}$,
		- $V_M(\phi\Box\!\!\rightarrow\psi,w)=1$ iff $V_{\mathcal{M}}(\psi,u)=1$ where $u$ is the closest $\phi$-world to $w$.
- Definition (SC-Validity)
	- SC-wff $\phi$ is SC-valid iff for all SC-models $\mathcal{M}=\langle\mathcal{W},\preceq,\mathcal{I}\rangle$, for all worlds $w\in\mathcal{W}$, $V_{\mathcal{M}}(\phi,w)=1$.
- Definition (SC-Semantic Consequence)
	- SC-wff $\phi$ is a SC-semantic consequence of $\Gamma=\{\gamma_1,\gamma_2,\ldots\}$ iff for all SC-models $\mathcal{M}=\langle\mathcal{W},\preceq,\mathcal{I}\rangle$, for all worlds $w\in\mathcal{W}$:
		- if $\forall\gamma_i\in\Gamma:V_{\mathcal{M}}(\gamma_i)=1$ then $V_{\mathcal{M}}(\phi)=1$.

## Lewis's Conditional
- Motivation
	- The semantics of SC imply that for all models $\mathcal{M}=\langle\mathcal{W},\preceq,\mathcal{I}\rangle$, for all worlds $w\in\mathcal{W}$, for all wffs $\phi$ if there exists some $v\in\mathcal{W}$ such that $V_{\mathcal{M}}(\phi,v)=1$, then there exists a $w$-closest $\phi$ world. There seems to be no reason to think that in reality, if there exists some world in which some proposition is true, there exists some unique closest world in which that proposition is true. It is conceivable that instead there are two or more equally close worlds in which that proposition is true. So it is not clear that SC models a plausible reality. It is also conceivable that there is a sequence of ever closer worlds in which that proposition is true, with no closest such world.

### Syntax
- The syntax of LC is identical to that of SC.

### Semantics
- Definition (LC-Model)
	- A LC-model $\mathcal{M}$ is a triple $\langle\mathcal{W},\preceq,\mathcal{I}\rangle$ such that:
		- $\mathcal{W}$ is a non-empty set, the set of possible worlds,
		- $\preceq$ is a three-place relation on $\mathcal{W}$, the nearness relation, such that for each $w\in\mathcal{W}$:
			- $\preceq_w=\{\langle u,v\rangle:\langle u,v,w\rangle\in\preceq\}$ is a linear **preorder** on $\mathcal{W}$,
			- if $u\preceq_ww$ then $u=w$ for all $u\in\mathcal{W}$ (the modified base assumption),
			- Heuristically, the modified base assumption is the assumption that no $u\neq w$ is weakly nearer to $w$ than $w$.
		- $\mathcal{I}$ is a two-place function from sentence letters $\alpha$ and worlds $w$ to the set of truth values $\{0,1\}$, the interpretation function.
	- The definition of LC-model is obtained from the definition of SC-model by abandoning the antisymmetry of $\preceq$ and the limit assumption (that if some $\phi$-world exists, then for all $w$, there exists a unique $w$-closest $\phi$-world). The base assumption is modified such that it remains possible to infer that any given world $w$ is closer to $w$ than any other world is. This inference from the base assumption in SC relied on the antisymmetry of $\preceq_w$.
- Definition (LC-Valuation)
	- The LC-valuation $V_{\mathcal{M}}$ given model $\mathcal{M}=\langle\mathcal{W},\preceq,\mathcal{I}\rangle$ is the unique function from the set of wffs to the set of truth values $\{0,1\}$ for each world $w\in\mathcal{W}$ such that:
		- for all sentence letters $\alpha$, $V_{\mathcal{M}}(\alpha,w)=\mathcal{I}(\alpha,w)$,
		- $V_{\mathcal{M}}(\lnot\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,w)=0$,
		- $V_{\mathcal{M}}(\phi\rightarrow\psi,w)=0\text{ iff }V_{\mathcal{M}}(\phi,w)=1\text{ and }V_{\mathcal{M}}(\psi,w)=0$,
		- $V_{\mathcal{M}}(\Box\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,v)=1\text{ for all }v\in\mathcal{W}$,
		- $V_M(\phi\Box\!\!\rightarrow\psi,w)=1$ iff either (1) there is no $\phi$-world, or (2) there is some $\phi$-world $u$ such that for every world $v$ closer to $w$ than $u$, $V_{\mathcal{M}}(\phi\rightarrow\psi,v)=1$.