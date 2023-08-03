# Propositional Logic Rough Notes

## Exam Technique
- Answers to parts of a question often draw on earlier results.
- It is necessary to argue that counterexamples succeed.
- In general, a useful tactic for proving a conditional is to prove that the negation of the consequent implies the negation of the antecedent. For example, prove $\vDash_{SV}\phi\Rightarrow\vDash_{PL}\phi$ by proving $\cancel{\vDash}_{PL}\phi\Rightarrow\cancel{\vDash}_{SV}\phi$.
- When given some abbreviation, it is sometimes expedient to construct truth tables or write a derived rule which is then applied or referred to in semantic arguments, rather than disabbreviating within semantic arguments.
	- For example, it is expedient to construct the truth tables for $\Delta\phi=\lnot(\phi\rightarrow\lnot\phi)$ and $\nabla\phi=\lnot\Delta\lnot\phi$ and refer to those in a semantic argument.

## Bivalent Propositional Logic

### Syntax
- Definition (PL-wff)
	- Each sentence letter $\alpha\in\{P,Q,R,P_1,Q_1,R_1,P_2,\ldots\}$ is a PL-wff.
	- If each of $\phi$ and $\psi$ is a PL-wff, then each of $\lnot\phi$ and $(\phi\rightarrow\psi)$ is a PL-wff.
	- Only strings that can be shown to be PL-wffs by the above rules are PL-wffs.
- Abbreviations
	- "$\phi\land\psi$" abbreviates "$\lnot(\phi\rightarrow\lnot\psi)$".
	- "$\phi\lor\psi$" abbreviates "$(\lnot\phi\rightarrow\psi)$".
	- "$\phi\leftrightarrow\psi$" abbreviates "$((\phi\rightarrow\psi)\land(\psi\rightarrow\psi))$".
	- The familiar bracketing conventions apply.

### Semantics
- Definition (PL-Interpretation)
	- A PL-interpretation (bivalent interpretation) $\mathcal{I}$ is a function from the set of sentence letters $\{P,Q,R,P_1,Q_1,R_1,P_2,\ldots\}$ to the set of truth values $\{0,1\}$.
- Definition (PL-Valuation)
	- The PL-valuation $V_{\mathcal{I}}$ for a given PL-interpretation $\mathcal{I}$ is the unique function from the set of PL-wffs to the set of truth values $\{0,1\}$ such that:
		- for all sentence letters $\alpha$, $V_{\mathcal{I}}(\alpha)=\mathcal{I}(\alpha)$,
		- $V_{\mathcal{I}}(\lnot\phi)=1\text{ iff }V_{\mathcal{I}}(\phi)=0$,
		- and $V_{\mathcal{I}}(\phi\rightarrow\psi)=0\text{ iff }V_{\mathcal{I}}(\phi)=1\text{ and }V_{\mathcal{I}}(\psi)=0$.
- Definition (PL-Validity)
	- PL-wff $\phi$ is PL-valid iff for all PL-interpretations $\mathcal{I}$, $V_{\mathcal{I}}(\phi)=1$.
	- "$\vDash_{PL}\phi$" is equivalent to "$\phi$ is PL-valid".
- Definition (PL-Semantic Consequence)
	- PL-wff $\phi$ is a PL-semantic consequence of set of PL-wffs $\Gamma=\{\gamma_1,\gamma_2,\ldots\}$ iff for all PL-interpretations $\mathcal{I}$, if for all $\gamma_i\in\Gamma$, $V_{\mathcal{I}}(\gamma_i)=1$, then $V_{\mathcal{I}}(\phi)=1$.
	- "$\Gamma\vDash_{PL}\phi$" is equivalent to "$\phi$ is a PL-semantic consequence of $\Gamma$".

## Trivalent Propositional Logic
- Motivation (Bivalence Failure)
	- Presupposition failure, vagueness, and indeterminacy yield prima facie bivalence failure in natural language. \[See Studd, 2020, Notes on Propositional Logic, p. 4 for examples.\]

### Syntax
- Definition (Trivalent wff)
	- Each sentence letter $\alpha\in\{P,Q,R,P_1,Q_1,R_1,P_2,\ldots\}$ is a trivalent wff.
	- If each of $\phi$ and $\psi$ is a trivalent wff, then each of $\lnot\phi$, $(\phi\rightarrow\psi)$, $(\phi\land\psi)$, and $(\phi\lor\psi)$ is a trivalent wff.
	- Only strings that can be shown to be trivalent wffs by the above rules are trivalent wffs.

### Semantics
- Definition (Trivalent Interpretation)
	- A trivalent interpretation $\mathcal{I}$ is a function from the set of sentence letters $\{P,Q,R,P_1,Q_1,R_1,P_2,\ldots\}$ to the set of truth values $\{0,1,\#\}$.
- Definition (Weak Kleene-Valuation)
	- The weak Kleene-valuation $WV_{\mathcal{I}}$ for a given trivalent interpretation $\mathcal{I}$ is the unique function from the set of trivalent wffs to the set of truth values $\{0,1,\#\}$ such that:
		- for all sentence letters $\alpha$, $WV_{\mathcal{I}}(\alpha)=\mathcal{I}(\alpha)$,
		- $WV_{\mathcal{I}}(\lnot\phi)=\#\text{ iff }WV_{\mathcal{I}}(\phi)=\#$,
		- for all $\circ\in\{\land,\lor,\rightarrow\}$, $WV_{\mathcal{I}}(\phi\circ\psi)=\#\text{ iff }WV_{\mathcal{I}}(\phi)=\#\text{ or }WV_{\mathcal{I}}(\psi)=\#$,
		- and $WV_{\mathcal{I}}$ coincides with $V_{\mathcal{I}}$ for all other $WV_{\mathcal{I}}(\phi)$ and $WV_{\mathcal{I}}(\psi)$.
- Discussion (Weak Kleene-Valuation)
	- Weak Kleene-valuation is plausible if we take $\#$ to indicate "meaningless" and suppose that any sentence with a meaningless component is thereby also meaningless.
- Definition (Kleene-Valuation)
	- The (strong) Kleene-valuation $KV_{\mathcal{I}}$ for a given trivalent interpretation $\mathcal{I}$ is the unique function from the set of trivalent wffs to the set of truth values $\{0,1,\#\}$ such that:
		- for all sentence letters $\alpha$, $KV_{\mathcal{I}}(\alpha)=\mathcal{I}(\alpha)$,
		- and for all trivalent wffs $\phi,\psi$ and $\circ\in\{\land,\lor,\rightarrow\}$, $KV_{\mathcal{I}}(\phi\circ\psi)=1$ iff (with some violence to notation) $KV_{\mathcal{I}}^*(\phi)\circ KV_{\mathcal{I}}^*(\psi)=1$ for all $KV_{\mathcal{I}}^*$ that differ from $KV_{\mathcal{I}}$ only in assigning $0$ or $1$ instead of $\#$, $KV_{\mathcal{I}}(\phi\circ\psi)=0$ iff $KV_{\mathcal{I}}^*(\phi)\circ KV_{\mathcal{I}}^*(\psi)=0$ for all $KV_{\mathcal{I}}^*$ that differ from $KV_{\mathcal{I}}$ only in assigning $0$ or $1$ instead of $\#$, and $KV_{\mathcal{I}}(\phi\circ\psi)=\#$ otherwise.
- Definition (Lukasiewicz-Valuation)
	- The Lukasiewicz-valuation $LV_{\mathcal{I}}$ for a given trivalent interpretation $\mathcal{I}$ is the unique function from the set of trivalent wffs to the set of truth values $\{0,1,\#\}$ that differs from $KV_{\mathcal{I}}$ only in that $LV_{\mathcal{I}}(\phi\rightarrow\psi)=1$ if $LV_{\mathcal{I}}(\phi)=\#$ and $LV_{\mathcal{I}}(\psi)=\#$.

- Definition (Kleene-Validity)
	- Trivalent wff $\phi$ is Kleene-valid iff for all trivalent interpretations $\mathcal{I}$, $KV_{\mathcal{I}}(\phi)=1$.
	- "$\vDash_K\phi$" is equivalent to "$\phi$ is Kleene-valid".
- Definition (Kleene-Semantic Consequence)
	- Trivalent wff $\phi$ is a Kleene-semantic consequence of set of trivalent wffs $\Gamma=\{\gamma_1,\gamma_2,\ldots\}$ iff for all trivalent interpretations $\mathcal{I}$, if for all $\gamma_i\in\Gamma$, $KV_{\mathcal{I}}(\gamma_i)=1$, then $KV_{\mathcal{I}}(\phi)=1$.
	- "$\Gamma\vDash_K\phi$" is equivalent to "$\phi$ is a Kleene-semantic consequence of $\Gamma$".
- Definition (Lukasiewicz-Validity)
	- Trivalent wff $\phi$ is Lukasiewicz-valid iff for all trivalent interpretations $\mathcal{I}$, $LV_{\mathcal{I}}(\phi)=1$.
	- "$\vDash_L\phi$" is equivalent to "$\phi$ is Lukasiewicz-valid".
- Definition (Lukasiewicz-Semantic Consequence)
	- Trivalent wff $\phi$ is a Lukasiewicz-semantic consequence of set of trivalent wffs $\Gamma=\{\gamma_1,\gamma_2,\ldots\}$ iff for all trivalent interpretations $\mathcal{I}$, if for all $\gamma_i\in\Gamma$, $LV_{\mathcal{I}}(\gamma_i)=1$, then $LV_{\mathcal{I}}(\phi)=1$.
	- "$\Gamma\vDash_L\phi$" is equivalent to "$\phi$ is a Lukasiewicz-semantic consequence of $\Gamma$".
- Definition (LP-Validity)
	- Trivalent wff $\phi$ is LP-valid iff for all trivalent interpretations $\mathcal{I}$, $KV_{\mathcal{I}}(\phi)\in\{1,\#\}$.
	- "$\vDash_{LP}\phi$" is equivalent to "$\phi$ is LP-valid".
- Definition (LP-Semantic Consequence)
	- Trivalent wff $\phi$ is a LP-semantic consequence of set of trivalent wffs $\Gamma=\{\gamma_1,\gamma_2,\ldots\}$ iff for all trivalent interpretations $\mathcal{I}$, if for all $\gamma_i\in\Gamma$, $KV_{\mathcal{I}}(\gamma_i)\in\{1,\#\}$, then $KV_{\mathcal{I}}(\phi)\in\{1,\#\}$.
	- "$\Gamma\vDash_LP\phi$" is equivalent to "$\phi$ is a LP-semantic consequence of $\Gamma$".
- The following table summarises the above definitions.

|System|Valuation|Designated Values|
|---|---|---|
|Kleene|Kleene|1|
|Lukasiewicz|Lukasiewicz|1|
|LP (Logic of Paradox)|Kleene|1,#|

- Motivation (Supervaluation)
	- Penumbral (i.e. indefinite, marginal, "shadowy") connections (of sentences) yield prima facie counterexamples to Kleene-valuation. A penumbral connection is a logical connection between indefinite (neither definitely true nor definitely false) sentences. $\mathcal{I}(P)=\#\Rightarrow KV_{\mathcal{I}}(P\land\lnot P)=\#,KV_{\mathcal{I}}(P\lor\lnot P)=\#$. Suppose $P$ represents the sentence "Henry is tall" and Henry is a borderline case, so Henry is not (unqualifiedly) tall but also not (unqualifiedly) not tall, hence we construct $\mathcal{I}$ such that $\mathcal{I}(P)\neq0,1$. Intuitively, we think that $P\land\lnot P$ should evaluate as (simply) false, and $P\lor\lnot P$ should evaluate as (simply) true.
- Definition (Supervaluation)
	- The supervaluation $SV_{\mathcal{I}}$ for a given trivalent interpretation $\mathcal{I}$ is the unique function from the set of trivalent wffs to the set of truth values $\{0,1,\#\}$ such that:
		- $SV_{\mathcal{I}}(\phi)=1$ iff for all precisifications $\mathcal{I}^+$ of $\mathcal{I}$, $V_{\mathcal{I}^+}(\phi)=1$,
		- $SV_{\mathcal{I}}(\phi)=0$ iff for all precisifications $\mathcal{I}^+$ of $\mathcal{I}$, $V_{\mathcal{I}^+}(\phi)=0$,
		- $SV_{\mathcal{I}}(\phi)=\#$ otherwise.
- Definition (Refinement)
	- A trivalent interpretation $\mathcal{I}^+$ is a refinement of trivalent interpretation $\mathcal{I}$ iff for all sentence letters $\alpha$, if $\mathcal{I}(\alpha)=1$ then $\mathcal{I}^+(\alpha)=1$, and if $\mathcal{I}(\alpha)=0$ then $\mathcal{I}^+(\alpha)=0$.
- Definition (Precisification)
	- A bivalent interpretation $\mathcal{I}^+$ is a precisification of trivalent interpretation $\mathcal{I}$ iff for all sentence letters $\alpha$, if $\mathcal{I}(\alpha)=1$ then $\mathcal{I}^+(\alpha)=1$, and if $\mathcal{I}(\alpha)=0$ then $\mathcal{I}^+(\alpha)=0$.
- Definition (SV-Validity)
	- Trivalent wff $\phi$ is SV-valid iff for all trivalent interpretations $\mathcal{I}$, $SV_{\mathcal{I}}(\phi)=1$.
	- "$\vDash_{SV}\phi$" is equivalent to "$\phi$ is SV-valid".
- Definition (SV-Semantic Consequence)
	- Trivalent wff $\phi$ is a SV-semantic consequence of set of trivalent wffs $\Gamma=\{\gamma_1,\gamma_2,\ldots\}$ iff for all trivalent interpretations $\mathcal{I}$, if for all $\gamma_i\in\Gamma$, $SV_{\mathcal{I}}(\gamma_i)=1$, then $SV_{\mathcal{I}}(\phi)=1$.
	- "$\Gamma\vDash_{SV}\phi$" is equivalent to "$\phi$ is a SV-semantic consequence of $\Gamma$".
- Relationship (SV-Semantic Consequence and PL-Semantic Consequence)
	- $\Gamma\vDash_{SV}\phi\text{ iff }\Gamma\vDash_{PL}\phi$.
- Discussion (Truth-Functionality)
	- Supervaluationist connectives are not truth-functional (whereas PL, Kleene, and Lukasiewicz connectives are) in the sense that $SV_{\mathcal{I}}(\phi\circ\psi)$ is not (simply) a function of $SV_{\mathcal{I}}(\phi)$ and $SV_{\mathcal{I}}(\psi)$ for all connectives $\circ\in\{\land,\lor,\rightarrow\}$.
- Discussion (Non-Classical Logics)
	- In general non-classical logics "scale back classical logic's set of logical truths and logical consequences". Intuitionists want to reject the law of excluded middle (as a logical truth), paraconsistent logicians want to reject ex falso quodlibet (as a logical consequence). (See 210611 Philosophical Logic Paper Q1.)