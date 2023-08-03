# Oligopoly Outline

## Oligopoly
- Static Models
	- Static Bertrand Model
	- Sequential Bertrand Model
	- Static Cournot Model
	- Stackelberg Model
	- Kreps-Scheinkman Model
- Dynamic Models
	- Dynamic Cournot Model
	- Dynamic Bertrand Model
	- Rotemberg-Saloner Model
	- Green-Porter Model
- Facilitating Practices
	- Retrospective Most-Favoured Nation Clause
	- Contemporaneous Most-Favoured Nation Clause
	- Meeting Competition Clause
	- Meet-or-Release Clause
	- Pricing Conventions
- Multimarket Contact
	- Symmetric Markets
	- Asymmetric Costs
	- Asymmetric Market Shares

## Static Bertrand Model
- Parameters: Standard Bertrand model.
- Analysis: Show no profitable deviation from $p=c$.
- Result: Allocative and productive efficiency.
	- Analytically, all and only units such that $v>c$ are produced and consumed, and all units are produced at minimum cost. Under asymmetric competition, where cost differences are small, allocative inefficiency is small.
- Result: Positive incentive to collude.
	- Intuitively, Bertrand competition has the structure of Prisoner's Dilemma, and there are mutual negative externalities.
- Evaluation: Unrealistic result that Bertrand competition between two firms yields the perfectly competitive outcome.
- Evaluation: Unrealistic assumptions that products are homogenous, there are no capacity constraints, and competition is static.
- Case Study (Nynex): In 1987, Nynex (monopolist) sold telephone directories on CD (relatively homogenous product) for USD 10,000 (monopoly price). Following the entry of competitor, Pro CD, price for telephone directories on CD fell to <USD 1,000 (much closer to marginal cost).
- Case Study (Nintendo): In 1999, Nintendo cut prices for its game console to match Sony within an hour of the Sony price cut.

## Sequential Bertrand Model
- Parameters: Standard Bertrand model with a first-mover.
- Analysis: Show no profitable deviation from $p_1=p^M,p_2=p_1-\epsilon$.
- Evaluation: Unrealistic assumption that there is a first-mover since prices are easily adjusted.

## Static Cournot Model
- Parameters: Standard Cournot model.
- Analysis: Find reaction function by taking FOC, then solve by imposing symmetry.
- Result: Allocative and productive inefficiency.
	- Analytically, since $p>c$, at the margin $v>c$, then $\uparrow Q\Rightarrow\uparrow W$, and $\cancel{\max}W$. Under asymmetric competition, $q_2\neq 0$ unless $DD$ small or $c_1\ll c_2$.
- Result: Allocative and productive efficiency as $n\rightarrow\infty$
	- Analytically, by inspection, $n\rightarrow\infty\Rightarrow Q^*\rightarrow Q^o,p^*\rightarrow p^o,\Pi\rightarrow 0$.
- Result: Positive incentive to collude.
	- Intuitively, Cournot competition has the structure of Prisoner's Dilemma, and there are mutual negative externalities.
	- Analytically, $q=\frac{q^M}{n}\Rightarrow\pi=\frac{\pi^M}{n}>\pi^*$.
- Result: Size differences reflect efficiency differences.
	- Analytically, by inspection, $\downarrow c_i\Rightarrow\uparrow q_i^*$.
	- Intuitively, $\downarrow c_i\Rightarrow(p-c_i)\Rightarrow$ incentive to $\uparrow q_i$.
- Result: Price-cost margin $\propto$ quantity share.
	- Analytically, $q_i^*=-\frac{P(Q^*)-c_i}{P'(Q^*)}$, then $\frac{q_i^*}{Q^*}\frac{Q^*}{P(Q^*)}=-\frac{P(Q^*)-c_i}{P(Q^*)P'(Q^*)}$, then $\frac{q_i^*}{Q^*}|\frac{Q^*P'(Q^*)}{P(Q^*)}|=\frac{P(Q^*)-c_i}{P(Q^*)}$, then $L_i\equiv\frac{p-c_i}{p}=\frac{s_i}{|\epsilon|}$.
	- Intuitively, $\downarrow c_i\Rightarrow(p-c_i)\Rightarrow$ incentive to $\uparrow q_i$.
- Result: Average price-cost margin $\propto$ Herfindahl index of concentration.
	- Analytically, $L\equiv\sum_{i=1}^ns_iL_i=\sum_{i=1}^n\frac{s_i^2}{|\epsilon|}=\frac{H}{|\epsilon|}$.
- Evaluation: Realistic result that oligopoly outcomes are intermediate between monopoly outcomes and perfectly competitive outcomes.
- Evaluation: Unrealistic assumption that prices necessarily clear the market since firms choose prices.

## Stackelberg Model
- Parameters: Standard Cournot model with a first-mover.
- Analysis: Find second-mover reaction function by taking FOC, substitute to get first-mover profit function, solve by taking FOC.
- Result: First-mover advantage.
	- Analytically, at Cournot quantities, $\uparrow q_1$ has no direct effect on $\pi_1$ since FOC holds, but has a positive strategic effect.
- Evaluation: Unrealistic assumption that firms choose quantities sequentially.

## Kreps-Scheinkman Model
- Parameters: Firms each choose $\bar{q_i}$ at cost $c\bar{q_1}$, then choose $p_i$ to maximise $\pi_i=p_iq_i-c\bar{q_i}$ subject to $q_i\leq\bar{q_i}$. Consumers buy at the lowest price. Suppose $P(Q)=1-Q$ and demand is efficiently rationed.
- Analysis: Show $\frac{\partial\pi_i}{\partial q_i}>0$ for small $\bar{q_1},\bar{q_2}$, then show no profitable deviation from $p=P(\bar{q_1}+\bar{q_2})$ in second stage, then show $\pi_i^*=[P(\bar{q_i}+\bar{q_j})-c]\bar{q_i}$.
- Result: Reduced-form profit function coincides with Cournot profit function where quantities are interpreted as capacities.
	- Intuitively, each firm faces downward-sloping, less than perfectly elastic residual demand since other firms are capacity-constrained, hence can increase prices.
- Evaluation: Assumption that $\sum_i\bar{q_i}\ll DD$ more likely where $c$ is high relative to $\max_qqP(q)$ since $\pi\geq0$.
- Evaluation: Assumption that demand is efficiently rationed is not necessarily realistic. For example, many goods are rationed by queueing.
- Discussion: Capacity constraints are an extreme case of increasing marginal cost, the result generalises to less extreme cases.

## Dynamic Cournot Model
- Parameters: Standard dynamic Cournot model.
- Analysis: Show no profitable deviation from standard grim trigger strategy given $\delta>\bar{\delta}$.
- Result: Ambiguous whether collusion is more sustainable under dynamic Cournot competition than under dynamic Bertrand competition.
	- Analytically, deviation-period deviation profit is lower but punishment-phase profit is higher in Cournot.

## Dynamic Bertrand Model
- Parameters: Standard dynamic Bertrand model.
- Analysis: Show no profitable deviation from standard grim trigger strategy given $\delta>\bar{\delta}$.
- Result: Collusion is easier to sustain in concentrated markets.
	- Analytically, by inspection, $\uparrow n\Rightarrow\uparrow\bar{\delta}$.
	- Intuitively, concentration increases each firm's share of collusive profits, hence decreases incentive to deviate.
- Result: Collusion is easier to sustain among similar firms.
	- Analytically, collusion is sustainable only if it is rational for all firms, and efficient firms have greater incentive to deviate.
	- Additionally, asymmetrical firms find it difficult to agree on profit distribution.
- Result: Collusion can be unilaterally undermined by impatient firms.
- Evaluation: Model over-predicts occurrence of collusion.
- Evaluation: Unrealistic assumption that firms can credibly commit to not renegotiating.

## Rotemberg-Saloner Model
- Parameters: Standard dynamic Bertrand model except $Q=D_t(p)=\theta_tD(p)$ where $\theta_t$ fluctuates observably.
- Analysis: Argue that $p^M\perp\!\!\!\perp\theta_t$. Show no profitable deviation from standard grim trigger strategy in periods where $\theta_t=\theta_H$ if $\delta>\hat{\delta}$, show no profitable deviation from standard grim trigger strategy in periods where $\theta_t=\theta_L$ if $\delta>\bar{\delta}$. Show that $\hat{\delta}>\bar{\delta}$. Argue that for $\bar{\delta}<\delta<\hat{\delta}$ partial collusion is sustainable in periods where $\theta_t=\theta_H$.
- Result: Price wars are observed in high demand periods.
	- Intuitively, deviation-period deviation profit is greater under high demand.
- Case Study (Armed Services Medical Procurement Agency):
	- In 1956, collusion in the market for the antibiotic tetracycline broke down when the Armed Services Medical Procurement Agency placed a large order.

## Green-Porter Model
- Parameters: Standard dynamic Bertrand model except $Q=D_t(p)=\theta_tD(p)$ where $\theta_t\sim B(1,1-\alpha)$ unobservably.
- Analysis: Argue that each firm plays a trigger strategy in the subgame-perfect equilibrium for sufficiently large $\delta,T$.
- Result: Price wars are observed following low demand periods.
	- Intuitively, if firms do not cut prices after observing low demand, each firm has incentive to deviate.
- Case Study (Joint Executive Committee):
	- Between 1880 and 1886, the Joint Executive Committee, a cartel controlling eastbound freight shipments from Chicago to the Atlantic seaboard, adopted a variant of the above trigger strategy, resulting in occasional price wars following unobservable demand slumps.

## Facilitating Practices
- Discussion: Facilitating practices either restructure firms' incentives or facilitate information exchange. Such practices are enforceable if embedded in contracts.

## Retrospective Most-Favoured Nation Clause
- Discussion:
	- Retroactive most-favoured-nation clauses penalise sellers for reducing price. When the seller reduces price, the seller is required to retrospectively reimburse recent customers the amount that they would have saved had they been offered the same discount. Deviation-period deviation profit decreases because the firm incurs the additional cost of reimbursement. Profit under collusion is unchanged since colluding firms do not cut prices. Hence firms have less incentive to deviate under a retroactive most-favoured nation clause.
- Case Study (GE):
	- In 1963, GE, a producer of large turbine generators, instituted a most-favoured-customer clause, under which it would be bound, in the event that it reduced prices, to offer all customers in the past six months an identical discount. Rival Westinghouse followed suit within a year. Except for a brief period of price cutting in 1964, prices of the two firms remained stable and identical until regulators intervened in 1975.

## Contemporaneous Most-Favoured Nation Clause
- Discussion: Under a contemporaneous most-favoured-clause, when the seller offers a discounted price to another buyer, the seller must offer the same discount to all buyers. Sellers that universally adopt contemporaneous most-favoured-nation clauses commit to selling at a common price. This prevents price discrimination.
- Parameters: Firms each choose either universal high price, universal low price, or discriminatory pricing whereby only large consumers face a low price.
- Analysis: Argue that full collusion at the high price is more difficult to sustain than under the standard dynamic Bertrand model because of lag in detection of deviation by discriminatory pricing.

## Meeting Competition Clause
- Discussion:
	- Under no-release meeting competition clauses, if a buyer discovers a lower price elsewhere and informs his original supplier of this price, the original supplier must sell to the buyer at this lower price. Then, retaliation is immediate and automatic.
- Discussion:
	- A no-release meeting competition clause also facilitates the achievement of the collusive outcome. For example, a seller who provides a no-release meeting competition clause to current customers can raise price without losing any customers to a lower priced rival. Buyers are automatically given the rival's lower price until all firms raise their prices. This eliminates the transitional losses that might otherwise deter price increases. It also eliminates the rival's transitional gains and with it the incentive to delay a matching price increases.

## Meet-or-Release Clause
- Discussion:
	- Under meet-or-release clauses, if a buyer discovers a lower price elsewhere, he is not released from his obligation to buy from the original supplier unless he informs that supplier of the lower price and that supplier has the opportunity to meet the lower price. The buyer has incentive to inform the original supplier of the lower price since he thereby enjoys a lower price (either by buying from the competitor or by compelling the original supplier to match the lower price). Meet-or-release clauses reduce if not eliminate detection lags.

## Pricing Conventions
- Discussion:
	- Pricing conventions include a relative value scale and product standardisation.  Pricing conventions create price transparency and enable buyers to negotiate for lower prices if and when a selective discount is offered. Buyers who discover that they have paid more than others have a powerful tool for negotiating a matching discount, which can make it costly or difficult for a seller to offer selective discounts. Pricing conventions prevent price-discrimination.

## Symmetric Markets

## Asymmetric Costs

## Asymmetric Market Shares
- Parameters: Standard dynamic Bertrand model except if $p_1=p_2$, $q_1\neq q_2$.
- Case Study (Airlines):
	- Evans and Kessides (1994) studied prices of and routes served by U.S. airlines Delta, American, and Northwest in 1988 and found that an index of "average contact" which measures the number of markets in which competing airlines face each other has a significant positive impact on airfares. This is consistent with the result that multimarket contact facilitates collusion since deviation from a collusive arrangement in one market triggers price wars in all markets.
- Case Study (Dog Food):
	- In 1986, Quaker Oats, a dominant player in the moist dog food segment acquired Anderson Clayton, strengthening Quaker's position in the moist dog food segment and acquiring a foothold for Quaker in the dry dog food segment. Ralston Purina, the dominant player in the dry  segment responded by acquiring Benco Pet Food's Inc., Quaker's primary rival in the moist segment. The behaviour of Quaker and Ralston Purina seem consistent with the intention of putting their respective rivals on notice. Were Quaker to initiate a price war in the dry segment, Ralston Purina would be capable of retaliating in the moist segment, and vice versa.