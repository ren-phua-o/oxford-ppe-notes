# Modal Propositional Logic Metatheory Rough Notes v1

## Propositional Logic

### Proof of Soundness
- Lemma (PL-Validity of PL-Axioms)
	- Proof ($\vDash_{PL}PL1$)
		- Consider some arbitrary PL-interpretation $\mathcal{I}$ and some arbitrary PL-wffs $\phi,\psi$.
		- Suppose for reductio that 
			- (1) $V_{\mathcal{I}}(\phi\rightarrow(\psi\rightarrow\phi))=0$.
		- From (1), by definition of PL-valuation, $\rightarrow$ clause (by $\rightarrow$),
			- (2) $V_{\mathcal{I}}(\phi)=1$,
			- (3) $V_{\mathcal{I}}(\psi\rightarrow\phi)=0$.
		- From (3), by $\rightarrow$,
			- (4) $V_{\mathcal{I}}(\phi)=0$.
		- From (2), (4), by reductio,
			- (5) $V_{\mathcal{I}}(\phi\rightarrow(\psi\rightarrow\phi))=1$.
		- From (5), by generalisation,
			- (6) for all PL-interpretations $\mathcal{I}$, PL-wffs $\phi,\psi$, $V_{\mathcal{I}}(\phi\rightarrow(\psi\rightarrow\phi))=1$.
		- From (6), by definition of PL-validity,
			- (7) for all PL-wffs $\phi,\psi$, $\vDash_{PL}\phi\rightarrow(\psi\rightarrow\phi)$.
		- From (7), by definition of a PL-instance of PL1,
			- (8) every PL-instance of PL1 is PL-valid.
	- Proof ($\vDash_{PL}PL2$)
		- Consider some arbitrary PL-interpretation $\mathcal{I}$ and some arbitrary PL-wffs $\phi,\psi,\chi$.
		- Suppose for reductio that
			- (1) $V_{\mathcal{I}}((\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi)))=0$.
		- From (1), by $\rightarrow$,
			- (2) $V_{\mathcal{I}}(\phi\rightarrow(\psi\rightarrow\chi))=1$,
			- (3) $V_{\mathcal{I}}((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi))=0$.
		- From (3), by $\rightarrow$,
			- (4) $V_{\mathcal{I}}(\phi\rightarrow\psi)=1$,
			- (5) $V_{\mathcal{I}}(\phi\rightarrow\chi)=0$.
		- From (5), by $\rightarrow$,
			- (6) $V_{\mathcal{I}}(\phi)=1$,
			- (7) $V_{\mathcal{I}}(\chi)=0$.
		- From (4), (6), by $\rightarrow$,
			- (8) $V_{\mathcal{I}}(\psi)=1$.
		- From (7), (8), by $\rightarrow$,
			- (9) $V_{\mathcal{I}}(\psi\rightarrow\chi)=0$.
		- From (6), (9), by $\rightarrow$,
			- (10) $V_{\mathcal{I}}(\phi\rightarrow(\psi\rightarrow\chi))=0$.
		- From (2), (10), by reductio,
			- (11) $V_{\mathcal{I}}((\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi)))=1$.
		- From (11), by generalisation,
			- (12) for all PL-interpretations $\mathcal{I}$, PL-wffs $\phi,\psi,\chi$, $V_{\mathcal{I}}((\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi)))=1$.
		- From (12), by definition of PL-validity,
			- (13) for all PL-wffs $\phi,\psi,\chi$, $\vDash_{PL}(\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi))$.
		- From (13), by definition of a PL-instance of PL2,
			- (14) every PL-instance of PL2 is PL-valid.
	- Proof ($\vDash_{PL}PL3$)
		- Consider some arbitrary PL-interpretation $\mathcal{I}$ and some arbitrary PL-wffs $\phi,\psi$.
		- Suppose for reductio that
			- (1) $V_{\mathcal{I}}((\lnot\psi\rightarrow\lnot\phi)\rightarrow((\lnot\psi\rightarrow\phi)\rightarrow\psi))=0$.
		- From (1), by $\rightarrow$,
			- (2) $V_{\mathcal{I}}(\lnot\psi\rightarrow\lnot\phi)=1$,
			- (3) $V_{\mathcal{I}}((\lnot\psi\rightarrow\phi)\rightarrow\psi)=0$,
		- From (3), by $\rightarrow$,
			- (4) $V_{\mathcal{I}}(\lnot\psi\rightarrow\phi)=1$,
			- (5) $V_{\mathcal{I}}(\psi)=0$.
		- From (5), by $\lnot$ clause,
			- (6) $V_{\mathcal{I}}(\lnot\psi)=1$.
		- From (2), (6), by $\rightarrow$,
			- (7) $V_{\mathcal{I}}(\lnot\phi)=1$.
		- From (4), (6), by $\rightarrow$,
			- (8) $V_{\mathcal{I}}(\phi)=1$.
		- From (7), by $\lnot$ clause,
			- (9) $V_{\mathcal{I}}(\phi)=0$.
		- From (8), (9), by reductio,
			- (10) $V_{\mathcal{I}}((\lnot\psi\rightarrow\lnot\phi)\rightarrow((\lnot\psi\rightarrow\phi)\rightarrow\psi))=1$.
		- From (10), by generalisation,
			- (11) for all PL-interpretations $\mathcal{I}$, PL-wffs $\phi,\psi$, $V_{\mathcal{I}}((\lnot\psi\rightarrow\lnot\phi)\rightarrow((\lnot\psi\rightarrow\phi)\rightarrow\psi))=1$.
		- From (11), by definition of PL-validity,
			- (12) for all PL-wffs $\phi,\psi$, $\vDash_{PL}(\lnot\psi\rightarrow\lnot\phi)\rightarrow((\lnot\psi\rightarrow\phi)\rightarrow\psi)$.
		- From (12), by definition of a PL-instance of PL3,
			- every PL-instance of PL3 is PL-valid.
- Lemma (PL-Rules Preserve PL-Validity)
	- Proof (MP Preserves PL-Validity)
		- Suppose that
			- (1) $\vDash_{PL}\phi$,
			- (2) $\vDash_{PL}\phi\rightarrow\psi$.
		- From (1), by definition of PL-validity,
			- (3) for all PL-interpretations $\mathcal{I}$, $V_{\mathcal{I}}(\phi)=1$.
		- From (2), by definition of PL-validity,
			- (4) for all PL-interpretations $\mathcal{I}$, $V_{\mathcal{I}}(\phi\rightarrow\psi)=1$.
		- Consider some arbitrary PL-interpretation $\mathcal{I}$.
		- From (3),
			- (5) $V_{\mathcal{I}}(\phi)=1$.
		- From (4),
			- (6) $V_{\mathcal{I}}(\phi\rightarrow\psi)=1$
		- From (5), (6), by $\rightarrow$,
			- (7) $V_{\mathcal{I}}(\psi)=1$.
		- From (7), by generalisation,
			- (8) for all PL-interpretations $\mathcal{I}$, $V_{\mathcal{I}}(\psi)=1$.
		- From (8), by definition of PL-validity,
			- (9) $\vDash_{PL}\psi$.
		- From the above, by conditional proof,
			- (10) if (1), (2), then (9), i.e. MP preserves PL-validity.
- Base Case
	- Suppose that there is an axiomatic proof (from $\emptyset$) in PL of arbitrary PL-wff $\phi$ which is a sequence of $n=1$ PL-wffs. Then, by definition of an axiomatic proof in PL, this proof is the sequence $\phi$ and $\phi$ is a PL-axiom. Then, by the PL-validity of PL-axioms, $\vDash_{PL}\phi$. From the above, by conditional proof, if there is an axiomatic proof in PL of arbitrary PL-wff $\phi$ which is a sequence of $n=1$ PL-wffs, then $\vDash_{PL}\phi$.
- Induction Hypothesis
	- Given $n$, suppose that for all $m<n$, if there is an axiomatic proof in PL of arbitrary PL-wff $\phi$ which is a sequence of $m$ PL-wffs, then $\vDash_{PL}\phi$.
- Induction Step
	- Suppose that there is an axiomatic proof in PL of arbitrary PL-wff $\phi$ which is a sequence of $n$ PL-wffs. Then, by definition of an axiomatic proof in PL, either $\phi$ is a PL-axiom, or $\phi$ follows from earlier wffs $\psi,\chi$ by a PL-rule.
	- Suppose that $\phi$ is a PL-axiom, then by the PL-validity of PL-axioms, $\vDash_{PL}\phi$.
	- Suppose that $\phi$ follows from earlier wffs $\psi,\chi$ by a PL-rule, then by the lemma that PL-rules preserve PL-validity, if $\vDash_{PL}\psi$ and $\vDash_{PL}\chi$, then $\vDash_{PL}\phi$. By definition of an axiomatic proof in PL, there is an axiomatic proof in PL of $\psi$ which is a sequence of $m<n$ PL-wffs, namely the sequence obtained by eliminating all PL-wffs after $\psi$ in the proof of $\phi$. Then, by the Induction Hypothesis, $\vDash_{PL}\psi$. By an analogous argument, $\vDash_{PL}\chi$. Then $\vDash_{PL}\phi$.
	- By cases, if there is an axiomatic proof in PL of arbitrary PL-wff $\phi$ which is a sequence of $n$ PL-wffs, $\vDash_{PL}\phi$.
	- By strong induction over the length of the axiomatic proof of $\phi$, if there is an axiomatic proof of $\phi$, then $\vDash_{PL}\phi$.

### Proof of Cut
- \[See Sider, 2010 - Logic for Philosophy, pp. 73-74\]
- The rough idea of the (informal) proof is that the required (axiomatic) proof can be constructed by concatenating the given (axiomatic) proofs.

### Proof of Deduction Theorem
- (See Sider, 2010 - Logic for Philosophy, pp. 74-76.)

## Modal Propositional Logic

### Proof of Soundness
- The proof of soundness in MPL can be adapted from the proof of soundness in PL.

## Mathematical Methods
- Method (Conditional Proof)
	- Suppose $A$. Then $B$. By conditional proof, if $A$ then $B$.
- Method (Biconditional Proof)
	- Suppose $A$. Then $B$. Suppose $B$. Then $A$. By biconditional proof, $A$ iff $B$.
- Method (Proof by Cases)
	- Suppose $A$. Then $C$. Suppose $B$. Then $C$. By cases, if $A$ or $B$ then $C$.
- Method (Proof by Reductio)
	- Suppose $A$. Then $B$ and not $B$. By reductio, not $A$.
- Method (Proof by Generalisation)
	- Consider arbitrary $X$, $x$. $x$ has $P$. By generalisation, all $X$ have $P$.