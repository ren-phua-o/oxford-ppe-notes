# Modal Propositional Logic Proof Theory Rough Notes

- Practice on the Sider exercises is necessary and sufficient.

## Method Notes
- When (in general) does it make sense to disabbreviate $\land,\lor\leftrightarrow,\diamond$?
	- In general, it is more convenient to work with abbreviated formulas where there are conjunctive antecedents (use import/export), disjunctive antecedents (use dilemma, i.e. prove by cases), conjunctive consequents (use composition, i.e. prove by cases), bidirectional implications (use bidirectional proof).
	- In general, where the highest-level connective is $\land,\lor$, disabbreviate.
	- In general, suspicious-looking strings like "$\Box\diamond\Box\diamond P\rightarrow\Box\diamond P$ " in B, S4, or S5 are provable without disabbreviation, by direct application of the axioms and $K,K\diamond$ from suitable starting points.
- NEC enables "PL within box".
- Where permitted to suppress PL steps, prove biconditional by proving right-to-left and left-to-right separately.
- Similarly, where permitted to suppress PL steps, prove conjunction by proving each of the conjoined elements.
- This strategy works for conjunctive consequents, disjunctive antecedents.
- Import/export is generally very useful for proving theorems with conjunctive antecedents.
- The general technique for working with disjunctive consequents is to rewrite the disjunctive consequent in terms of negation and material implication.A conditional antecedent can be rewritten as a disjunctive antecedent. $(\phi\rightarrow\psi)\rightarrow\chi\equiv(\lnot\phi\lor\psi)\rightarrow\chi$.
- "Move" negation signs through strings of alternating boxes and diamonds by MN.
- T and PL are useful in conjunction (in some cases) to remove "internal" boxes.
- No possible contradiction in K ($\lnot[P\land\lnot P];\Box\lnot[P\land\lnot P];\lnot\diamond[P\land\lnot P]$), no necessary contradiction in D ($\lnot[P\land\lnot P];\Box\lnot[P\land\lnot P];\lnot\diamond[P\land\lnot P];\Box[P\land\lnot P]\rightarrow\diamond[P\land\lnot P];\lnot\Box[P\land\lnot P]$), no necessary possible contradiction (apply no necessary contradiction to no possible contradiction), and no possibly necessary contradiction (apply no possible contradiction to no necessary contradiction) are useful for proving negations with modus tollens.
- An analogue of Becker, $Becker\diamond$ exists.
- Modal negation is generally useful at "dead ends".
- Using S4 and $K,K\diamond$ in conjunction on a formula like "$\Box(P\rightarrow Q)$" is powerful, and can generate such formulas as "$\Box(\Box\diamond\Box\diamond P\rightarrow\Box\diamond\Box\diamond Q)$", and the internal modal operator chains can be manipulated with $D,T,B,S4,S5$ as required.

## (Bivalent) Propositional Logic

### Axiomatic System
- Definition (Axiomatic Proof from $\Gamma$ in S)
	- An axiomatic proof of S-wff $\phi$ from set of S-wffs $\Gamma=\{\gamma_1,\gamma_2,\ldots,\gamma_n\}$ in S is a finite sequence of wffs $\phi_1,\phi_2,\ldots,\phi_n$, where $\phi_n=\phi$ and each $\phi_i$ (for $i\in\{1,2,\ldots,n\}$) either is an S-axiom, is a member of $\Gamma$, or follows from earlier wffs in the sequence by an S-rule.
	- "$\Gamma\vdash_S\phi$" is equivalent to "an axiomatic proof of $\phi$ from $\Gamma$ in S exists".
	- "$\vdash_S\phi$" abbreviates "$\emptyset\vdash_S\phi$".
	- "$\Gamma_1,\Gamma_2,\ldots,\psi_1,\psi_2,\ldots\vdash_S\phi$" abbreviates "$\Gamma_1\cup\Gamma_2\cup\ldots\cup\psi_1\cup\psi_2\cup\ldots\vdash_S\psi$.
- Definition (Axiomatic System for PL)
	- Every PL-instance of Modus Ponens (MP) is a PL-rule. $MP:\phi,\phi\rightarrow\psi\Rightarrow\psi$.
	- Every PL-instance of each of the following axiom schemas is a PL-axiom. $PL1:\phi\rightarrow(\psi\rightarrow\phi)$, $PL2:(\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi))$, $PL3:(\lnot\psi\rightarrow\lnot\phi)\rightarrow((\lnot\psi\rightarrow\phi)\rightarrow\psi)$.
	- The characteristic inference of PL2 is "modus ponens within the consequent".
- Definition (PL-Instance of a Schema)
	- A PL-instance of a given schema is the result of uniformly substituting each schematic letter ($\phi,\psi,\ldots$) in the schema with a PL-wff.
	- Note that an axiomatic proof schema and an axiomatic proof are different.
- Theorem (Cut1)
	- If $\Gamma\vdash_S\delta$ and $\Sigma,\delta\vdash_S\phi$, then $\Sigma,\Gamma\vdash_S\phi$.
	- In other words, the "intermediate premise" $\delta$ can be substituted by the "basic premises" $\Gamma$.
- Theorem (Cut)
	- If $\Gamma_1\vdash_S\delta_1,~\Gamma_2\vdash_S\delta_2,~\ldots,~\Gamma_n\vdash_S\delta_n$ and $\Sigma,\delta_1,\delta_2,\ldots,\delta_n\vdash_S\phi$, then $\Sigma,\Gamma_1,\Gamma_2,\ldots,\Gamma_n\vdash_S\phi$.
	- In other words, the "intermediate premises" $\delta_1,\delta_2,\ldots,\delta_n$ can be substituted by the "basic premises" $\Gamma_1,\Gamma_2,\ldots,\Gamma_n$.
- Theorem (Deduction Theorem)
	- If $\Gamma,\phi\vdash_S\psi$ then $\Gamma\vdash_S\phi\rightarrow\psi$.

### Common Proof Schemas
- Axiomatic Proof Schema (Excluded Middle)
	1. $\phi\lor\lnot\phi\Leftrightarrow\lnot\phi\rightarrow\lnot\phi$ (Reflexivity of Material Implication)
- Axiomatic Proof Schema (Reflexivity of Material Implication)
	1. $(\phi\rightarrow\phi)\rightarrow(\phi\rightarrow(\phi\rightarrow\phi))$ (PL1)
	2. $((\phi\rightarrow\phi)\rightarrow(\phi\rightarrow(\phi\rightarrow\phi)))\rightarrow((\phi\rightarrow(\phi\rightarrow\phi))\rightarrow(\phi\rightarrow\phi))$ (PL2)
	3. $(\phi\rightarrow(\phi\rightarrow\phi))\rightarrow(\phi\rightarrow\phi)$ (1, 2, MP)
	4. $(\phi\rightarrow(\phi\rightarrow\phi))$ (PL1)
	5. $\phi\rightarrow\phi$ (3, 4, MP)
- Axiomatic Proof Schema (Modus Ponens within the Consequent)
	1. $\phi\rightarrow(\psi\rightarrow\chi)$ (premise)
	2. $\phi\rightarrow\psi$ (premise)
	3. $(\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi))$ (PL2)
	4. $(\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi)$ (1, 3, MP)
	5. $\phi\rightarrow\chi$ (2, 4, MP)
- Axiomatic Proof Schema (Hypothetical Syllogism)
	1. $\phi\rightarrow\psi$ (premise)
	2. $\psi\rightarrow\chi$ (premise)
	3. $(\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi))$ (PL2)
	4. $(\psi\rightarrow\chi)\rightarrow(\phi\rightarrow(\psi\rightarrow\chi))$ (PL1)
	5. $(\phi\rightarrow(\psi\rightarrow\chi))$ (2, 4, MP)
	6. $(\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi)$ (3, 5, MP)
	7. $\phi\rightarrow\chi$ (1, 6, MP)
- Axiomatic Proof Schema (Contained Hypothetical Syllogism)
	1. Repeated DT (on Axiomatic Proof Schema of Hypothetical Syllogism)
	3. $(\phi\rightarrow\psi)\rightarrow((\psi\rightarrow\chi)\rightarrow(\phi\rightarrow\chi))$
- Axiomatic Proof Schema (Ex Falso Quodlibet)
	1. $\phi$ (premise)
	2. $\lnot\phi$ (premise)
	3. $\phi\rightarrow(\lnot\psi\rightarrow\phi)$ (PL1)
	4. $\lnot\phi\rightarrow(\lnot\psi\rightarrow\lnot\phi)$ (PL1)
	5. $(\lnot\psi\rightarrow\phi)$ (1, 3, MP)
	6. $(\lnot\psi\rightarrow\lnot\phi)$ (2, 4, MP)
	7. $(\lnot\psi\rightarrow\lnot\phi)\rightarrow((\lnot\psi\rightarrow\phi)\rightarrow\psi)$ (PL3)
	8. $(\lnot\psi\rightarrow\phi)\rightarrow\psi$ (6, 7, MP)
	9. $\psi$ (5, 8, MP)
- Axiomatic Proof Schema (Contained Ex Falso Quodlibet)
	1. $\lnot\phi\rightarrow\lnot\phi$ (Reflexivity of Material Implication)
	2. $(\lnot\phi\rightarrow\lnot\phi)\rightarrow((\lnot\phi\rightarrow\phi)\rightarrow\phi)$ (PL3)
	3. $(\lnot\phi\rightarrow\phi)\rightarrow\phi$ (1, 2, MP)
- Axiomatic Proof Schema (Modus Tollens)
	1. $\phi\rightarrow\psi$ (premise)
	2. $\lnot\psi$ (premise)
	3. \[Double Negation introduction and Reverse Modus Tollens\]
- Axiomatic Proof Schema (Reverse Modus Tollens)
	1. $\lnot\phi\rightarrow\lnot\psi$ (premise)
	2. $\psi$ (premise)
	3. $\psi\rightarrow(\lnot\phi\rightarrow\psi)$ (PL1)
	4. $\lnot\phi\rightarrow\psi$ (2, 3, MP)
	5. $(\lnot\phi\rightarrow\lnot\psi)\rightarrow((\lnot\phi\rightarrow\psi)\rightarrow\phi)$ (PL3)
	6. $(\lnot\phi\rightarrow\psi)\rightarrow\phi$ (1, 5, MP)
	7. $\phi$ (4, 6, MP))
- Axiomatic Proof Schema (Negated Conditional)
	1. $\lnot(\phi\rightarrow\psi)$ (premise)
	2. $\psi\rightarrow(\phi\rightarrow\psi)$ (PL1)
	3. $\psi\rightarrow\lnot(\phi\rightarrow\psi)$ (PL1, 1, MP)
	4. $\lnot\lnot\psi\rightarrow\psi$ (DNE, DT)
	5. $\lnot\psi$ (PL3, 3, MP, 2, MP)
- Axiomatic Proof Schema (Weakening the Consequent)
	1. $[\phi\rightarrow(\psi\rightarrow(\chi\rightarrow\psi))]\rightarrow[(\phi\rightarrow\psi)\rightarrow(\phi\rightarrow(\chi\rightarrow\psi))]$ (PL2)
	2. $\psi\rightarrow(\chi\rightarrow\psi)$ (PL1)
	3. $(\psi\rightarrow(\chi\rightarrow\psi))\rightarrow[\phi\rightarrow(\psi\rightarrow(\chi\rightarrow\psi))]$ (PL1)
	4. $[\phi\rightarrow(\psi\rightarrow(\chi\rightarrow\psi))]$ (2, 3, MP)
	5. $(\phi\rightarrow\psi)\rightarrow(\phi\rightarrow(\chi\rightarrow\psi))$ (1, 4, MP)
- Axiomatic Proof Schema (Double Negation Elimination)
	1. $\lnot\lnot\phi$ (premise)
	2. $(\lnot\phi\rightarrow\lnot\lnot\phi)\rightarrow((\lnot\phi\rightarrow\lnot\phi)\rightarrow\phi)$ (PL3)
	3. $\lnot\lnot\phi\rightarrow(\lnot\phi\rightarrow\lnot\lnot\phi)$ (PL1)
	4. $\lnot\phi\rightarrow\lnot\lnot\phi$ (1, 3, MP)
	5. $(\lnot\phi\rightarrow\lnot\phi)\rightarrow\phi$ (2, 4, MP)
	6. $\lnot\phi\rightarrow\lnot\phi$ (Reflexivity of Material Implication)
	7. $\phi$ (5, 7, MP)
- Axiomatic Proof Schema (Contained Double Negation Elimination)
	1. $(\lnot\phi\rightarrow\lnot\lnot\phi)\rightarrow((\lnot\phi\rightarrow\lnot\phi)\rightarrow\phi)$ (PL3)
		- From Double Negation Elimination
	2. $\lnot\lnot\phi\rightarrow(\lnot\phi\rightarrow\lnot\lnot\phi)$ (PL1)
		- Apply Modus Ponens within the Consequent throughout
	3. $\lnot\lnot\phi\rightarrow((\lnot\phi\rightarrow\lnot\phi)\rightarrow\phi)$ (1, 2, Hypothetical Syllogism)
	4. $\lnot\phi\rightarrow\lnot\phi$ (Reflexivity of Material Implication)
	5. $(\lnot\phi\rightarrow\lnot\phi)\rightarrow(\lnot\lnot\phi\rightarrow(\lnot\phi\rightarrow\lnot\phi))$ (PL1)
	6. $\lnot\lnot\phi\rightarrow(\lnot\phi\rightarrow\lnot\phi)$ (4, 5, MP)
	7. $[\lnot\lnot\phi\rightarrow((\lnot\phi\rightarrow\lnot\phi)\rightarrow\phi)]\rightarrow[(\lnot\lnot\phi\rightarrow(\lnot\phi\rightarrow\lnot\phi))\rightarrow(\lnot\lnot\phi\rightarrow\phi)]$ (PL1)
	8. $(\lnot\lnot\phi\rightarrow(\lnot\phi\rightarrow\lnot\phi))\rightarrow(\lnot\lnot\phi\rightarrow\phi)$ (3, 7, MP)
	9. $\lnot\lnot\phi\rightarrow\phi$ (6, 8, MP)
- Axiomatic Proof Schema (Double Negation Introduction)
	1. $\phi$ (premise)
	2. $(\lnot\lnot\lnot\phi\rightarrow\lnot\lnot\phi)\rightarrow((\lnot\lnot\lnot\phi\rightarrow\lnot\phi)\rightarrow\lnot\lnot\phi)$ (PL3)
	3. ?
- Axiomatic Proof Schema (Excluded Middle Modus Ponens)
	1. $\phi\rightarrow\psi$ (premise)
	2. $\lnot\phi\rightarrow\psi$ (premise)
	3. $\lnot\psi\rightarrow\lnot\phi$ (1, MT, DT)
	4. $\lnot\psi\rightarrow\phi$ (2, MT, DT)
	5. $\psi$ (PL3, 3, MP, 4, MP)

## Modal Propositional Logic

### Axiomatic System
- Definition (Axiomatic Proof in S)
	- An axiomatic proof of S-wff $\phi$ in S is a finite sequence of wffs $\phi_1,\phi_2,\ldots,\phi_n$, where $\phi_n=\phi$ and each $\phi_i$ either is an S-axiom, or follows from earlier wffs in the sequence by an S-rule.
- Definition (Axiomatic System for K)
	- The axiomatic system for K is identical to the axiomatic system for PL except in including the rule schema NEC and the axiom schema K, and in defining rules and axioms as MPL-instances (rather than PL-instances) of rule schemas and axiom schemas respectively. $NEC:\phi\Rightarrow\Box\phi$. $K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$.
	- Every MPL-instance of Modus Ponens (MP) is a K-rule. $MP:\phi,\phi\rightarrow\psi\Rightarrow\psi$.
	- Every MPL-instance of each of the following axiom schemas is a K-axiom. $PL1:\phi\rightarrow(\psi\rightarrow\phi)$, $PL2:(\phi\rightarrow(\psi\rightarrow\chi))\rightarrow((\phi\rightarrow\psi)\rightarrow(\phi\rightarrow\chi))$, $PL3:(\lnot\psi\rightarrow\lnot\phi)\rightarrow((\lnot\psi\rightarrow\phi)\rightarrow\psi)$.
	- Every MPL-instance of NEC is a K-rule. $NEC:\phi\Rightarrow\Box\phi$.
	- Every MPL-instance of K is a K-axiom. $K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$.
	- \[Intuition\]
- Definition (MPL-Instance of a Schema)
	- A MPL-instance of a schema is the result of uniformly substituting each schematic letter in the schema with a MPL-wff.
- Theorem (Soundness)
	- If $\vdash_S\phi$ then $\vDash_S\phi$.
	- Soundness holds for PL and K (and D, T, B, S4, and S5).
- Theorem (Strong Soundness)
	- If $\Gamma\vdash_S\phi$ then $\Gamma\vDash_S\phi$.
	- Strong soundness holds for PL but not for K (and not for D, T, B, S4, S5).
- Abbreviations (PL)
	- In an abbreviated proof (in an MPL system), every MPL-tautology abbreviates the proof of that MPL-tautology. Then, any MPL-tautology can be written in an axiomatic proof in MPL as if it were an axiom.
	- In an abbreviated proof (in an MPL system), if $\phi_1\rightarrow(\phi_2\rightarrow\ldots(\phi_n\rightarrow\psi)\ldots)$ is an MPL-tautology, then $\psi$ can be written as if $\phi_1,\phi_2,\ldots,\phi_n\Rightarrow\psi$ were a rule.
- Definition (MPL-tautology)
	- An MPL-tautology $\phi$ is the result of uniformly substituting sentence letters in a PL-valid PL-wff by MPL-wffs.
	- For example, $\Box P\lor\lnot\Box P$, $\lnot(\Box P\land\lnot\Box P)$, $\Box P\rightarrow\lnot\lnot\Box P$ are MPL-tautologies.
- Abbreviation (Becker)
	- Becker: $\phi\rightarrow\psi\Rightarrow\Box\phi\rightarrow\Box\psi$. Writing $\Box\phi\rightarrow\Box\psi$ as if Becker were a rule abbreviates writing $\Box(\phi\rightarrow\psi),\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi),\Box\phi\rightarrow\Box\psi$.
- Definition (Axiomatic System for D)
	- The axiomatic system for D is identical to the axiomatic system for K except in including the axiom schema D. $D:\Box\phi\rightarrow\diamond\phi$.
- Definition (Axiomatic System for T)
	- The axiomatic system for T is identical to the axiomatic system for K except in including the axiom schema T. $T:\Box\phi\rightarrow\phi$.
- Definition (Axiomatic System for B)
	- The axiomatic system for B is identical to the axiomatic system for T except in including the axiom schema B. $B:\diamond\Box\phi\rightarrow\phi$.
- Definition (Axiomatic System for S4)
	- The axiomatic system for S4 is identical to the axiomatic system for T except in including the axiom schema S4. $S4:\Box\phi\rightarrow\Box\Box\phi$.
- Definition (Axiomatic System for S5)
	- The axiomatic system for S5 is identical to the axiomatic system for T except in including the axiom schema S5. $S5:\diamond\Box\phi\rightarrow\Box\phi$.
- The following table summarises the above.

|Model|Semantic Condition on $\mathcal{R}$|Characteristic Validity|Axiom Schemas|Rule Schemas|
|---|---|---|---|---|
|K|||$PL1,PL2,PL3$<br>$K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$|$MP$<br>$NEC:\phi\Rightarrow\Box\phi$|
|D|Serial|$\Box\phi\rightarrow\diamond\phi$|$PL1,PL2,PL3$<br>$K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$<br>$D:\Box\phi\rightarrow\diamond\phi$|$MP$<br>$NEC:\phi\Rightarrow\Box\phi$|
|T|Reflexive|$\Box\phi\rightarrow\phi$|$PL1,PL2,PL3$<br>$K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$<br>$T:\Box\phi\rightarrow\phi$|$MP$<br>$NEC:\phi\Rightarrow\Box\phi$|
|B|Reflexive, Symmetric|$\phi\rightarrow\Box\diamond\phi$|$PL1,PL2,PL3$<br>$K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$<br>$T:\Box\phi\rightarrow\phi$<br>$\textcolor{yellow}{B:\diamond\Box\phi\rightarrow\phi}$|$MP$<br>$NEC:\phi\Rightarrow\Box\phi$|
|S4|Reflexive, Transitive|$\Box\phi\rightarrow\Box\Box\phi$|$PL1,PL2,PL3$<br>$K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$<br>$T:\Box\phi\rightarrow\phi$<br>$S4:\Box\phi\rightarrow\Box\Box\phi$|$MP$<br>$NEC:\phi\Rightarrow\Box\phi$|
|S5|Reflexive, Symmetric, Transitive|$\diamond\phi\rightarrow\Box\diamond\phi$|$PL1,PL2,PL3$<br>$K:\Box(\phi\rightarrow\psi)\rightarrow(\Box\phi\rightarrow\Box\psi)$<br>$T:\Box\phi\rightarrow\phi$<br>$\textcolor{yellow}{S5:\diamond\Box\phi\rightarrow\Box\phi}$|$MP$<br>$NEC:\phi\Rightarrow\Box\phi$|

### Common Proof Schemas
- \[See Sider, 2010 - Logic for Philosophy, pp. 207-213\]
- "Diamond" Axioms
	- $K\diamond:\Box(\phi\rightarrow\psi)\rightarrow(\diamond\phi\rightarrow\diamond\psi)$
	- $T\diamond:\phi\rightarrow\diamond\phi$
	- $B\diamond:\phi\rightarrow\Box\diamond\phi$
		- This is the characteristic validity.
	- $S4\diamond:\diamond\diamond\phi\rightarrow\diamond\phi$
	- $S5\diamond:\diamond\phi\rightarrow\Box\diamond\phi$
		- This is the characteristic validity.
- Axiomatic Proof Schema (Becker)
	1. $\phi\rightarrow\psi$ (PL)
	2. $\Box(\phi\rightarrow\psi)$ (1, NEC)
	3. $\Box\phi\rightarrow\Box\psi$ (2, K, MP)
- Axiomatic Proof Schema (No Possible Contradiction in K)
	1. $\lnot(P\land\lnot P)$ (PL)
	2. $\Box\lnot(P\land\lnot P)$ (1, NEC)
	3. $\lnot\diamond(P\land\lnot P)$ (2, PL DNI)
- Axiomatic Proof Schema ($K\diamond:\Box(\phi\rightarrow\psi)\rightarrow(\diamond\phi\rightarrow\diamond\psi)$)
	1. $(\phi\rightarrow\psi)\rightarrow(\lnot\psi\rightarrow\lnot\phi)$ (PL contraposition)
	2. $\Box(\phi\rightarrow\psi)\rightarrow\Box(\lnot\psi\rightarrow\lnot\phi)$ (1, NEC, K, MP)
	3. $\Box(\lnot\psi\rightarrow\lnot\phi)\rightarrow(\Box\lnot\psi\rightarrow\Box\lnot\phi)$ (K)
	4. $(\Box\lnot\psi\rightarrow\Box\lnot\phi)\rightarrow(\lnot\Box\lnot\phi\rightarrow\lnot\Box\lnot\psi)$ (PL contraposition)
	5. $\Box(\phi\rightarrow\psi)\rightarrow(\diamond\phi\rightarrow\diamond\psi)$ (2, 3, 4, PL syllogism)
- Axiomatic Proof Schema (Application of $K\diamond$)
	1. $\phi_1\rightarrow(\phi_2\rightarrow(\phi_3\rightarrow\psi))$ (PL)
	2. $\Box\phi_1\rightarrow\Box(\phi_2\rightarrow(\phi_3\rightarrow\psi))$ (1, NEC, K, MP)
	3. $\Box(\phi_2\rightarrow(\phi_3\rightarrow\psi))\rightarrow(\Box\phi_2\rightarrow\Box(\phi_3\rightarrow\psi)$ (K)
	4. $\Box(\phi_3\rightarrow\psi)\rightarrow(\diamond\phi_3\rightarrow\diamond\psi)$ ($K\diamond$)
	5. $\Box\phi_1\rightarrow(\Box\phi_2\rightarrow(\diamond\phi_3\rightarrow\diamond\psi))$ (2, 3, 4, PL syllogism)
	6. $\diamond\phi_3\rightarrow(\Box\phi_1\rightarrow(\Box\phi_2\rightarrow\diamond\psi))$ (5, PL import/export)
		- Other combinations are possible in the final step using import/export.
- Axiomatic Proof Schema (Application of $D$)
	1. $\phi$ (PL)
	2. $\Box\phi$ (1, NEC)
	3. $\diamond\phi$ (2, D, MP)
- Axiomatic Proof Schema (No Possibly Necessary Contradiction in D)
	1. $\lnot(P\land\lnot P)$ (PL)
	2. $\Box\lnot(P\land\lnot P)$ (1, NEC)
	3. $\lnot\diamond(P\land\lnot P)$ (2, PL DNI)
	4. $\Box(P\land\lnot P)\rightarrow\diamond(P\land\lnot P)$ (D)
	5. $\lnot\Box(P\land\lnot P)$ (3, 4, PL MT)
	6. $\Box\lnot\Box(P\land\lnot P)$ (5, NEC)
	7. $\lnot\diamond\Box(P\land\lnot P)$ (6, PL DNI)
- Axiomatic Proof Schema ($T\diamond:\phi\rightarrow\diamond\phi$)
	1. $\Box\lnot\phi\rightarrow\lnot\phi$ (T)
	2. $\phi\rightarrow\diamond\phi$ (1, PL contraposition, double negation elimination)
- Axiomatic Proof Schema ($B\diamond:\phi\rightarrow\Box\diamond\phi$)
	1. $\diamond\Box\lnot\phi\rightarrow\lnot\phi$ (B)
	2. $\phi\rightarrow\Box\diamond\phi$ (1, PL contraposition, double negation elimination)
- Axiomatic Proof Schema ($S4\diamond:\diamond\diamond\phi\rightarrow\diamond\phi$)
	1. $\Box\lnot\phi\rightarrow\Box\Box\lnot\phi$ (S4)
	2. $\Box\lnot\phi\rightarrow\lnot\lnot\Box\lnot\phi$ (PL double negation introduction)
	3. $\Box\Box\lnot\phi\rightarrow\Box\lnot\lnot\Box\lnot\phi$ (2, NEC, K, MP)
	4. $\Box\lnot\phi\rightarrow\Box\lnot\lnot\Box\lnot\phi$ (1, 3, PL syllogism)
	5. $\diamond\diamond\phi\rightarrow\diamond\phi$ (4, PL contraposition)
- Axiomatic Proof Schema ($S5\diamond:\diamond\phi\rightarrow\Box\diamond\phi$)
	1. $\diamond\Box\lnot\phi\rightarrow\Box\lnot\phi$ (S5)
	2. $\diamond\phi\rightarrow\Box\diamond\phi$ (1, PL contraposition)
- Axiomatic Proof Schema (B in S5)
	1. $\diamond\Box\phi\rightarrow\Box\phi$ (S5)
	2. $\Box\phi\rightarrow\phi$ (T)
	3. $\diamond\Box\phi\rightarrow\phi$ (1, 2, PL syllogism)
- Axiomatic Proof Schema (B in S5)
	1. $\Box\phi\rightarrow\Box\diamond\Box\phi$ ($B\diamond$)
	2. $\diamond\Box\phi\rightarrow\Box\phi$ (S5)
	3. $\Box\diamond\Box\phi\rightarrow\Box\Box\phi$ (2, NEC, K, MP)
	4. $\Box\phi\rightarrow\Box\Box\phi$ (1, 2, 3, PL syllogism)