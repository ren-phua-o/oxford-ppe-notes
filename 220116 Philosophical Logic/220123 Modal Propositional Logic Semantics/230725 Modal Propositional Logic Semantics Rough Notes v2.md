# Modal Propositional Logic Semantics Rough Notes

## Modal Propositional Logic
- Motivation (Non-Truth-Functionality)
	- Non-truth-functional English (natural language) connectives cannot be represented in propositional logic. A logic is truth-functional iff the truth-value of a complex wff is a function of the truth-value of its immediate subformulas. \[See Studd, 2020 - Notes on Modal Propositional Logic Semantics, p. 1 for examples.\]

### Syntax
- Definition (MPL-wff)
	- The definition of a MPL-wff is identical to the definition of a PL-wff except in including the unary connective $\Box$ which is syntactically similar to $\lnot$.
	- Each sentence letter $\alpha\in\{P,Q,R,P_1,Q_1,R_1,P_2,\ldots\}$ is a MPL-wff.
	- If each of $\phi$ and $\psi$ is a MPL-wff, then each of $\lnot\phi$, $(\phi\rightarrow\psi)$, and $\Box\phi$ is a MPL-wff.
	- Only strings that can be shown to be MPL-wffs by the above rules are MPL-wffs.
- Abbreviations
	- The abbreviations for MPL are identical to the abbreviations for PL except in including the abbreviation $\diamond\phi$ for $\lnot\Box\lnot\phi$.
	- "$\phi\land\psi$" abbreviates "$\lnot(\phi\rightarrow\lnot\psi)$".
	- "$\phi\lor\psi$" abbreviates "$(\lnot\phi\rightarrow\psi)$".
	- "$\phi\leftrightarrow\psi$" abbreviates "$((\phi\rightarrow\psi)\land(\psi\rightarrow\psi))$".
	- "$\diamond\phi$" abbreviates "$\lnot\Box\lnot\phi$".
	- The familiar bracketing conventions apply.

## Simplified Modal Propositional Logic

### Semantics
- Definition (SMPL-Model)
	- A SMPL-model $\mathcal{M}$ is a pair $\langle\mathcal{W},\mathcal{I}\rangle$, where:
		- $\mathcal{W}$ is a non-empty set, the set of possible worlds, and
		- $\mathcal{I}$ is a function from the set of sentence letter-world pairs $\{\langle\alpha,w\rangle:\alpha\in\{P,Q,R,P_1,Q_1,R_1,P_2,\ldots\},w\in\mathcal{W}\}$ to the set of truth values $\{0,1\}$, the interpretation function.
- Definition (SMPL-Valuation)
	- The SMPL-valuation $V_{\mathcal{M}}$ for a given SMPL-model $\mathcal{M}=\langle\mathcal{W},\mathcal{I}\rangle$ is the unique function from the set of MPL-wffs to the set of truth values $\{0,1\}$ for each world $w\in\mathcal{W}$ such that:
		- for all sentence letters $\alpha$, $V_{\mathcal{M}}(\alpha,w)=\mathcal{I}(\alpha,w)$,
		- $V_{\mathcal{M}}(\lnot\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,w)=0$,
		- $V_{\mathcal{M}}(\phi\rightarrow\psi,w)=0\text{ iff }V_{\mathcal{M}}(\phi,w)=1\text{ and }V_{\mathcal{M}}(\psi,w)=0$.
		- and $V_{\mathcal{M}}(\Box\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,v)=1\text{ for all }v\in\mathcal{W}$.
	- The definition of SMPL-valuation and $\diamond\phi$ together imply $V_{\mathcal{M}}(\diamond\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,v)=1\text{ for some }v\in\mathcal{W}$.
- Definition (SMPL-Validity)
	- MPL-wff $\phi$ is SMPL-valid iff $\phi$ is valid in every SMPL-model.
	- "$\vDash_{SMPL}\phi$" is equivalent to "$\phi$ is SMPL-valid".
- Definition (Validity in SMPL-Model $\mathcal{M}$)
	- MPL-wff $\phi$ is valid in SMPL-model $\mathcal{M}=\langle\mathcal{W},\mathcal{I}\rangle$ iff $V_{\mathcal{M}}(\phi,w)=1$ for all $w\in\mathcal{W}$.

### Interpretation
- Discussion
	- The connective $\Box$ in MPL can be taken to represent each of the connectives in natural language "is necessary", "has always been", "will always be", "is known by S", "is obligatory". These connectives in natural language are in some sense ["intensional" (as opposed to "extensional"](https://en.wikipedia.org/wiki/Extensionality). These connectives correspond to different [modalities](https://dictionary.cambridge.org/us/dictionary/english/modal).
	- The following table summarises interpretations of $\Box$.

|Modality|$\Box\phi$|$\diamond\phi$|$\mathcal{W}$|
|---|---|---|---|
|Metaphysical|Necessarily $\phi$|Possibly $\phi$|The set of metaphysically possible worlds|
|Temporal|Has always been $\phi$|Was $\phi$|The set of times|
|Temporal|Will always be $\phi$|Will be $\phi$|The set of times|
|Epistemic|S knows $\phi$|For all S knows, it could be that $\phi$|The set of worlds consistent with what $S$ knows|
|Deontic|$\phi$ is obligatory|$\phi$ is permissible|The set of morally permissible worlds|

## Modal Propositional Logic
- Motivation (Counterexamples to SMPL)
	- Consider the following MPL-wff schemas.
		- $D:\Box\phi\rightarrow\diamond\phi$.
		- $T:\Box\phi\rightarrow\phi$.
		- $B:\phi\rightarrow\Box\diamond\phi$.
		- $4:\Box\phi\rightarrow\Box\Box\phi$.
		- $5:\diamond\phi\rightarrow\Box\diamond\phi$.
	- On the metaphysical interpretation of $\Box$, $4$ and $5$ are controversial. On the (strict, i.e. excluding the present moment) temporal interpretation, $T$, $B$, and $5$ are clearly false. On the epistemic interpretation, $4$ and $5$ are controversial.
	- The apparent cause of the problematic validities is the SMPL truth condition for $\Box$.

### Semantics
- Definition (MPL-Model)
	- The definition of an MPL-model is identical to the definition of an SMPL-model except in including the accessibility relation $\mathcal{R}$.
	- A MPL-model $\mathcal{M}$ is a triple $\langle\mathcal{W},\mathcal{R},\mathcal{I}\rangle$, where:
		- $\mathcal{W}$ is a non-empty set, the set of possible worlds,
		- $\mathcal{R}$ is a binary relation over $\mathcal{W}$, the accessibility relation.
		- and $\mathcal{I}$ is a function from the set of sentence letter-world pairs $\{\langle\alpha,w\rangle:\alpha\in\{P,Q,R,P_1,Q_1,R_1,P_2,\ldots\},w\in\mathcal{W}\}$ to the set of truth values $\{0,1\}$, the interpretation function.
- Definition (MPL-Valuation)
	- The definition of MPL-valuation is identical to the definition of SMPL-valuation except in the clause for $\Box\phi$.
	- The MPL-valuation $V_{\mathcal{M}}$ given MPL-model $\mathcal{M}=\langle\mathcal{W},\mathcal{R},\mathcal{I}\rangle$ is the unique function from the set of MPL-wffs to the set of truth values $\{0,1\}$ for each world $w\in\mathcal{W}$ such that:
		- for all sentence letters $\alpha$, $V_{\mathcal{M}}(\alpha,w)=\mathcal{I}(\alpha,w)$,
		- $V_{\mathcal{M}}(\lnot\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,w)=0$,
		- $V_{\mathcal{M}}(\phi\rightarrow\psi,w)=0\text{ iff }V_{\mathcal{M}}(\phi,w)=1\text{ and }V_{\mathcal{M}}(\psi,w)=0$,
		- and $V_{\mathcal{M}}(\Box\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,v)=1\text{ for all }v\in\mathcal{W}\text{ such that }\mathcal{R}wv$.
	- The definition of MPL-valuation and $\diamond\phi$ together imply $V_{\mathcal{M}}(\diamond\phi,w)=1\text{ iff }V_{\mathcal{M}}(\phi,v)=1\text{ for some }v\in\mathcal{W}\text{ such that }\mathcal{R}wv$.
- Definition (S-Validity)
	- MPL-wff $\phi$ is S-valid iff $\phi$ is valid in every S-model.
	- "$\vDash_{S}\phi$" is equivalent to "$\phi$ is S-valid".
- Definition (Validity in S-Model $\mathcal{M}$)
	- MPL-wff $\phi$ is valid in S-model $\mathcal{M}=\langle\mathcal{W},\mathcal{R},\mathcal{I}\rangle$ iff $V_{\mathcal{M}}(\phi,w)=1$ for all $w\in\mathcal{W}$.
- Definition (S-Model)
	- MPL-model $\mathcal{M}=\langle\mathcal{W},\mathcal{R},\mathcal{I}\rangle$ is a
		- $D$-model iff $\mathcal{R}$ is serial on $\mathcal{W}$ (i.e. $\forall w\in\mathcal{W}:\exists v\in\mathcal{W}:\mathcal{R}wv$, i.e. each world sees some world),
		- $T$-model iff $\mathcal{R}$ is reflexive on $\mathcal{W}$ (i.e. each world sees itself),
		- $B$-model iff $\mathcal{R}$ is reflexive and symmetric on $\mathcal{W}$,
		- $S4$-model iff $\mathcal{R}$ is reflexive and transitive on $\mathcal{W}$,
		- $S5$-model iff $\mathcal{R}$ is reflexive, symmetric, and transitive on $\mathcal{W}$.
	- Every MPL-model is a $K$-model.
	- The definition of S-validity and the definitions of $K,D,T,B,S4,S5$ models together imply that:
		- validity in $K$ implies validity in $D,T,B,S4,S5$,
		- validity in $D$ implies validity in $T,B,S4,S5$,
		- validity in $T$ implies validity in $B,S4,S5$,
		- validity in $B$ (or $S4$) implies validity in $S5$.
	- Invalidity implications are the reverse.
- The following table summarises the above.

|Model|Condition on $\mathcal{R}$|Characteristic Validity|Remarks|
|---|---|---|---|
|K||||
|D|$\mathcal{R}$ is serial on $\mathcal{W}$|$\Box\phi\rightarrow\diamond\phi$||
|T|$\mathcal{R}$ is reflexive on $\mathcal{W}$|$\Box\phi\rightarrow\phi$|$\phi$ is a "stronger" condition than $\diamond\phi$|
|B|$\mathcal{R}$ is reflexive and symmetric on $\mathcal{W}$|$\phi\rightarrow\Box\diamond\phi$|The characteristic validity is implied by symmetry|
|S4|$\mathcal{R}$ is reflexive and transitive on $\mathcal{W}$|$\Box\phi\rightarrow\Box\Box\phi$|The characteristic validity is implied by transitivity|
|S5|$\mathcal{R}$ is reflexive, symmetric, and transitive on $\mathcal{W}$|$\diamond\phi\rightarrow\Box\diamond\phi$|The intuition for the characteristic validity is "every world w sees sees every world w sees"|

### Methods
- Method (Establish Validity)
	- To establish $\vDash_S\phi$, suppose $\cancel{\vDash}_S\phi$ and show that this supposition yields a contradiction.
- Method (Establish Invalidity)
	- \[See Sider, 2010 - Logic for Philosophy, pp. 187-202.\]