# Industrial Organisation Supplementary Notes

## Miscellaneous Notes
- Take care to note in asymmetric cases that quantities have a lower bound at zero, so "edge" solutions exist. Cournot best response functions extend indefinitely in the direction of increasing competitor output because best response functions are defined for all competitor actions.
- Comment on the slope and intercept of the best response functions.
- Tack on in the conclusion of an essay that oligopoly theory is not entirely helpful because competition authorities in practice are also (increasingly) concerned with dynamic (to do with innovation), environmental, and political effects of merger.
- Always evaluate and offer case studies where relevant.

## Market Definition
- Definition
	- A market is the minimal set of products over which a hypothetical monopolist would find it profitable to raise price.
- Discussion
	- The small but significant and non-transitory increase in price (SSNIP) test is a non-arbitrary method of market definition. This test was first applied by the EU competition authority in the 1992 Nestle/Perrier case.
	- The procedure for applying the SSNIP test to define the market for some product $A$ is as follows. Compute the own-price elasticity of demand $\epsilon_A$ for $A$. Then, if demand is price inelastic, then an increase in price on $A$ is profitable and the relevant market is $A$. If demand is price elastic, then determine if an increase in price on $A$ is profitable. If such an increase in price is profitable, then the relevant market is $A$. If not, compute the own-price elasticity of demand $\epsilon_{A+B}$ for the bundle $A+B$, where $B$ is a close substitute for $A$. Then repeat the above for this bundle. This procedure identifies the minimal set of products (including $A$) over which a hypothetical monopolist would find it profitable to raise price.

## Vertical Merger
- Parameters
	- Pre-merger, a single upstream monopolist manufacturer $U$ produces an intermediate good at constant marginal cost $c$ and chooses wholesale price $w$ at which to sell to a single downstream monopolist retailer $D$. $D$ produces a final good at constant marginal cost $w$ (which it takes as given) and chooses retail price $p$ at which to sell to consumers. Demand in the retail market is $Q(p)=a-p$, with inverse demand $P=a-Q$. Demand in the wholesale market is derived from (equal to) demand in the retail market. $D$ chooses $p$ to maximise $\pi^D=(p-w)Q(p)$, $U$ chooses $w$ to maximise $\pi^U=(w-c)Q(p)$.
	- Post-merger, a single integrated firm $I$ produces a final good at constant marginal cost $c$ and chooses retail price $p$ to maximise profit $\pi^I=(p-c)Q(p)$.
- Analysis
	- Solve for the pre-merger equilibrium by backward induction. First-order condition on $p$ for maximisation of $\pi^D$ ($FOC_D$): $(p-w)Q'(p)+Q(p)=0\Leftrightarrow (p-w)(-1)+(a-p)=0\Leftrightarrow p=\frac{a+w}{2}$. Second-order condition ($SOC_D$): $-2<0$. $\pi^D$ is a maximum at $p=\frac{a+w}{2}$. Then, $Q(p)=a-p=\frac{a-w}{2}$. First-order condition on $w$ for maximisation of $\pi^U$ ($FOC_U$): $(w-c)(-\frac{1}{2})+\frac{a-w}{2}=0\Leftrightarrow w=\frac{a+c}{2}$. Second-order condition ($SOC_U)$: $-1<0$. $\pi^U$ is a maximum at $w=\frac{a+c}{2}$. Then, $p=\frac{3a+c}{4}$, $Q(p)=\frac{a-c}{4}$.
	- Solve for the post-merger equilibrium by solving the first-order condition on $p$ for maximisation of $\pi^I$. $FOC_I:(p-c)Q'(p)+Q(p)=0\Leftrightarrow (p-c)(-1)+(a-p)=0\Leftrightarrow p=\frac{a+c}{2}$. Second-order condition ($SOC_I$): $-2<0$. $\pi^I$ is a maximum at $p=\frac{a+c}{2}$. Then $Q(p)=\frac{a-c}{2}$.
- Result (Double Marginalisation)
	- Post-merger, compared to pre-merger, retail price $p$ is lower, quantity $Q(p)$ is higher, then consumer surplus is larger and aggregate welfare is higher.
	- Intuitively, this is because the upstream firm has strict incentive to choose wholesale price greater than marginal cost (it otherwise has zero profit). This increases marginal cost for the downstream firm, which finds it optimal to reduce output and (partially) pass on the increase in cost to consumers as an increase in retail price. The negative externality imposed by the upstream firm on the downstream firm in choosing price above marginal cost is internalised post merger.