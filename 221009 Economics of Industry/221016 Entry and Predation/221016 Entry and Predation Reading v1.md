# Entry and Predation Reading

## [Bulow et al., 1985](http://www.jstor.org/stable/1832005)
\[Treating this as useful only to introduce the concept of strategic substitutes and strategic complements\]
- From Lecture Notes: an increase in strategic variable $x_i$ constitutes aggressive behaviour if $\frac{\partial\pi_j}{\partial x_i}<0$ for $i\neq j$.
- From Lecture Notes: a duopoly Nash equilibrium is stable iff (informally) the firms respond to a marginal displacement from the equilibrium by (informally) converging to the equilibrium over subsequent periods. Formally, a duopoly Nash equilibrium is stable iff $0<\frac{\partial R_1}{\partial x_2}\frac{\partial R_2}{\partial x_1}<1$.
	- $\frac{\partial R_1}{\partial x_2}\frac{\partial R_2}{\partial x_1}=0$ iff at least one firm's best response is independent of the other firm's choice. Such Nash equilibria appear stable in the informal sense.
	- $\frac{\partial R_1}{\partial x_2}\frac{\partial R_2}{\partial x_1}<0$ iff one firm's best response function is upward-sloping while the other firm's best response function is downward-sloping. Informally, following a marginal displacement from the equilibrium, firms "circle" the equilibrium,
	- $\frac{\partial R_1}{\partial x_2}\frac{\partial R_2}{\partial x_1}\geq1$ iff \[...\]
- From Tirole, 1988, p. 208: the actions of two firms are strategic complements if one firm $i$'s marginal profit $\frac{\partial \pi_i}{\partial x_i}$ is increasing with the other firm $j$'s strategic variable $x_j$, i.e. $\frac{\partial^2\pi_i}{\partial x_i\partial x_j}=\frac{\partial}{\partial x_j}(\frac{\partial\pi_i}{\partial x_i})>0$. The actions of two firms are strategic substitutes if one firm $i$'s marginal profit $\frac{\partial\pi_i}{\partial x_i}$ is decreasing with the other firm $j$'s strategic variable $x_j$, i.e. $\frac{\partial^2\pi_i}{\partial x_i\partial x_j}=\frac{\partial}{\partial x_j}(\frac{\partial\pi_i}{\partial x_i})<0$.
	- If $\frac{\partial^2\pi_i}{\partial x_i\partial x_j}=\frac{\partial}{\partial x_j}(\frac{\partial\pi_i}{\partial x_i})>0$, firm $i$ regards its product as a strategic complement to firm $j$'s product. (Bulow et al., 1985, p. 494)
	- If $\frac{\partial^2\pi_i}{\partial x_i\partial x_j}=\frac{\partial}{\partial x_j}(\frac{\partial\pi_i}{\partial x_i})<0$, firm $i$ regards its product as a strategic substitute to firm $j$'s product.
	- "Thus, with strategic substitutes, each firm's optimal response to more aggressive play by the other is to be less aggressive. With strategic complements, each firm's optimal response to more aggressive play is to be more aggressive." (p. 494)
	- If $\frac{\partial\pi_i}{\partial x_j}<0$, i.e. profit of firm $i$ decrases as firm $j$ increases aggressiveness, firm $i$ sees its product as a conventional substitute to firm $j$'s product. (p. 497)
- (p. 494) seems to tell us that two markets exhibit joint economies iff marginal profit in one market ($\frac{\partial\pi^A}{\partial x^A}$) is positively related to the strategic variable in the other market $x^B$.
	- Being more aggressive in one market decreases the marginal return (profit) to aggressiveness in the other if there are joint diseconomies across the two markets. (p. 493)
- Core result: "whether firm $2$'s equilibrium strategy is more or less aggressive depends on (a) whether there are joint economies or diseconomies across the markets, hence whether firm $i$ is more or less aggressive in market $B$, and whether a more aggressive strategy by firm $i$ in market $B$ raises or lowers firm $2$'s marginal profitability." (p. 494)
- Model of Strategic Effect (p. 492) \[sketchy math and assumptions\]
	- Firm $1$ is a monopolist in market $A$, and a duopolist with firm $2$ in market $B$.
	- Both firms simultaneously choose strategic variables $x_1^A,x_1^B,x_2^B$, which are such that higher values correspond to higher outputs, lower prices, or higher advertising spend.
	- There is a shock $Z$ in market $A$ such that marginal profit of firm $1$ increases by $Z$ at all values of $x_1^A$.
	- At an interior Nash equilibrium, $\frac{\partial\pi_1}{\partial x_1^A}+Z=0,\frac{\partial\pi_1}{\partial x_1^B}=0,\frac{\partial\pi_2}{\partial x_2^B}=0$.
	- By the first equality above, $\uparrow Z\Rightarrow\downarrow\frac{\partial\pi_1}{\partial x_1^A}\Rightarrow\uparrow x_1^A$ since marginal return to $x_1^A$ (increasing output, for example) is decreasing in $x_1^A$.
		- Hence $\frac{\partial x_1^A}{\partial Z}>0$.
	- $\frac{dx_1^B}{dZ}=\frac{\partial x_1^B}{\partial x_1^A}\frac{\partial x_1^A}{\partial Z}$. By the above result, $\frac{\partial x_1^A}{\partial Z}>0$, hence $sign(\frac{\partial x_1^B}{\partial Z})=sign(\frac{\partial x_1^B}{\partial x_1^A})$.
	- If there are joint economies of scope between the markets, i.e. $\frac{\partial\pi_1}{\partial x_1^B}$ is increasing with $x_1^A$, then $\uparrow x_1^A\Rightarrow\uparrow x_1^B$ such that the second equality at Nash equilibrium holds.
		- Hence $sign(\frac{\partial x_1^A}{\partial x_1^B})=sign(\frac{\partial^2\pi_1}{\partial x_1^B\partial x_1^A})$.
		- Firm $1$ acts more aggressively in  market $B$ following a positive shock $Z$ in market $A$ if there are joint economies of scope between the markets. It acts less aggressively if there are joint diseconomies of scope.
	- $\frac{dx_2^B}{dZ}=\frac{\partial x_2^B}{\partial x_1^B}\frac{\partial x_1^B}{\partial x_1^A}\frac{\partial x_1^A}{\partial Z}$.
		- $\frac{\partial x_2^B}{\partial x_1^B}>0$ iff, in market $B$, firm $2$ sees firm $1$'s product as a strategic complement, i.e. $\frac{\partial\pi_2}{\partial x_2^B}$ is increasing with $x_1^B$, i.e. $\frac{\partial^2\pi_2}{\partial x_2^B\partial x_1^B}>0$ such that the increase in $\frac{\partial\pi_2}{\partial x_2^B}$ due to an increase in $x_1^B$ must be exactly offset by an increase in $x_2^B$ and the third equality at Nash equilibrium holds.
		- Hence $sign(\frac{\partial x_2^B}{\partial x_1^B})=sign(\frac{\partial^2\pi_2}{\partial x_2^B\partial x_1^B})$.
		- Hence $sign(\frac{\partial x_2^B}{\partial Z})=sign(\frac{\partial^2\pi_1}{\partial x_1^B\partial x_1A}\frac{\partial^2\pi_2}{\partial x_2^B\partial x_1^B})$.
	- Total effect on firm $1$'s profits: \[...\]
		- It can be shown that, where demand is sufficiently small (such that the direct positive effect of $Z$ is small), and $\frac{dx_2^B}{dZ}>0$, such that the strategic effect is negative, a positive demand shock in market $A$ has a negative total effect on firm $1$'s profits.
- The concept of strategic substitutes and strategic complements is less relevant to entry. "the potential entrant's decision depends on its total profit, while how aggressively it plays once it enters depends on its marginal profit." (p. 497)
	- If a shock causes an incumbent to play more aggressively, total profits for potential entrants are lower, entry is less attractive.
- Total effect of a strategic action on profits ($\frac{d\pi_i}{dx_i}$) can be decomposed into the direct effect ($\frac{\partial\pi_i}{\partial x_i}$) and the strategic effect ($\frac{\partial\pi_i}{\partial x_j}\frac{\partial x_j}{\partial x_i}$), where $\frac{\partial x_j}{\partial x_i}$ in the strategic effect will be recognised as the slope the the reaction function $R_j$.
- Application to Dixit Model (pp. 502-503)
	- "Selling units in one market in order to reduce marginal costs in a second market is formally equivalent to investing in capital that will directly lower the marginal production costs in the second market."
	- Result: "with price competition and linear demand, the more a firm invests, the lower an entrant's price will be, because greater investment lowers the incumbent's expected price. A firm may have an "entry deterrence" incentive to overinvest, but if it cannot deter entry then it has a "price war avoidance" incentive to hold back and underinvest.""

## [Dixit, 1980](https://www.jstor.org/stable/2231658)
\[Considering only the basic model and treating extensions as irrelevant\]
- Model presented more clearly in lecture notes

## [Fudenberg and Tirole, 1984](https://www.jstor.org/stable/1816385)
- "Given concavity, we can unambiguously say whether the incumbent will overinvest or underinvest." (p. 364)
	- Tirole seems to mean that decreasing returns (marginal profit) to the strategic variable is a necessary assumption.
- Taxonomy of Business Strategies (from Lecture Notes):
	- Investment by the incumbent shifts its best response either rightwards and upwards (e.g. if investment yields a decrease in costs in a later-stage Cournot game) or leftwards and downwards (e.g. if investment yields a quality improvement over rivals in a later-stage differentiated-product Bertrand game).
		- Reaction functions are plotted in $x_1,x_2$ space, where higher $x$ corresponds to more "aggressive" action (higher output in a Cournot game, lower price in a Bertrand game).
			- Hence a rightward and upward shift in either firm's best response function corresponds to that firm being "tougher", i.e. responding more "aggressively" to "aggressive" rival action.
			- And a leftward and downward shift in either firm's best response function corresponds to that firm being "softer", i.e. responding less "aggressively" to "aggressive" rival action.
	- From above, if two firm's strategic variables are strategic substitutes, more "aggressive" action by one firm makes less "aggressive" action optimal for the other.
	- From above, if two firm's strategic variables are strategic complements, more "aggressive" action by one firm makes more "aggressive" action optimal for the other.
	- Top Dog
		- e.g. incumbent invests to lower marginal cost in later-stage Cournot game (a la Dixit-Spence Model), such that incumbent is "tougher" in the later stage, and entrant responds by being less "aggressive" (possibly not enterring the market).
	- Puppy Dog
		- e.g. incumbent avoids investing where investing would lower marginal cost in later-stage product-differentiated Bertrand game, such that incumbent is "softer" in the later stage, and entrant responds by being less "aggressive".
	- Lean and Hungry Look
		- e.g. incumbent avoids investing where investing would increase marginal cost in later-stage Cournot game, such that incumbent is "tougher" in the later stage, and entrant responds by being less "aggressive".
		- (pp. 363-364) incumbent under-invests in capital (which increases baseline profits hence decreases incentive to invest in R&D for new techonologies) to appear tough soft (since increase in profits if R&D is successful decreases), and deter or optimally accommodate entry, since investment by incumbent and investment by entrant are strategic substitutes.
			- Investment makes incumbent look soft, strategic variables are strategic substitutes.
	- Fat Cat
		- e.g. incumbent invests to improve product quality in later-stage product-differentiated Bertrand game, such that incumbent is "softer" in the later stage, and entrant responds by being less "aggressive".
		- (pp. 361-363) investment in customer goodwill softens later-stage price competition (by cornering a segment of the market, for whom the incumbent would want to set a high price, such that it must also set a high price for the non-cornered segment, since price inflexibility is assumed), incumbent should over-invest to appear soft.
			- Investment makes incumbent look soft, strategic variables (price) are strategic complements, and incumbent intends to accommodate entry.
	- From Lecture Notes: "to deter entry, the incumbent needs to reduce the entrant's profit; if accommodating entry, the incumbent needs to maximise its own profit."
		- Effect of strategic investment on own profits, $\frac{d\pi_1}{dk_1}=\frac{\partial\pi_1}{\partial k_1}+\frac{\partial\pi_1}{\partial x_1}\frac{dx_1}{dk_1}+\frac{\partial\pi_1}{\partial x_2}\frac{dx_2}{dk_1}$, where at Nash equilibrium, first order condition $\frac{\partial\pi_1}{\partial x_1}=0$ holds, hence $\frac{d\pi_1}{dk_1}=\frac{\partial\pi_1}{\partial k_1}+\frac{\partial\pi_1}{\partial x_2}\frac{dx_2}{dk_1}$, i.e. effect of strategic investment on own profits can be decomposed into a direct effect and a strategic effect. 
			- Since $x_2$ corresponds to more aggressive behaviour, $\frac{\partial\pi_1}{\partial x_2}$ is (generally) negative.
				- From Lecture Notes: more aggressive behaviour by the entrant is (generally) harmful to the incumbent.
			- Hence, the direction of the strategic effect is determined by the sign of $\frac{dx_2}{dk}=\frac{dx_2}{dx_1}\frac{\partial x_1}{\partial k_1}$, assuming $k_1$ has no direct effect on $x_2$, i.e. the direction of the strategic effect is determined by whether investment makes the incumbent "tougher" or "softer", and whether the strategic variables $x_1,x_2$ are strategic substitutes (aggression is met with aggression) or complements (aggression is met with dovishness).
		- Effect of strategic investment on rival profits, $\frac{d\pi_2}{dk_1}=\frac{\partial\pi_2}{\partial k_1}+\frac{\partial\pi_2}{\partial x_2}\frac{dx_2}{dk_2}+\frac{\partial\pi_2}{\partial x_1}\frac{dx_1}{dk_1}$, where at Nash equilibrium, first order condition $\frac{\partial\pi_2}{\partial x_2}=0$ holds, hence $\frac{d\pi_2}{dk_1}=\frac{\partial\pi_2}{\partial x_1}\frac{dx_1}{dk_1}$, assuming $\frac{\partial\pi_2}{\partial k_1}=0$, i.e. there is no direct effect.
			- Since $x_1$ corresponds to more aggressive behaviour, $\frac{\partial\pi_2}{\partial x_1}$ is (generally) negative.
			- If the incumbent intends to deter the entrant, the incumbent is concerned with decreasing the entrant's potential profit, hence with creating a negative strategic effect.
				- If investment makes the incumbent "tougher", i.e. choose higher $x_1$, the incumbent over-invests to deter entry. Otherwise the incumbent under-invests.

## [Ghemawat, 1984](https://www.jstor.org/stable/2098506)
\[The words "entry", "predation", "prey" do not occur in this article.\]

## [Bresnahan and Reiss, 1991](https://www.jstor.org/stable/2937655)
\[In lecture notes\]

## [Mankiw and Whinston, 1986](https://www.jstor.org/stable/2555627)
- "If an entrant causes incumbent firms to reduce output, entry is more desirable to the entrant than it is to society. There is therefore a tendency toward \[socially\] excessive entry in homogenous product markets." (p. 48)
	- "Inefficiencies can arise from free entry in the presence of fixed set-up costs". (p. 57)
	- "In homogenous product markets a business-stealing effect always creates a bias toward excessive entry, when we ignore the integer constraint, marginal entry is always less desirable to society than to the entrant because of the output reduction entry causes in other firms."
		- "A business-stealing effect is present if the equilibrium output per firm declines as the number of firms grows." (49)
		- "If the postentry price exceeds marginal cost and if a business-stealing effect exists, then free entry leads to (socially) excessive entry."
	- "Entry restrictions are often socially desirable but become unnecessary as the fixed set-up cost becomes small."
		- Since "firms act approximately as price-takers as their numbers grow large." (50)
- "In heterogenous product markets the direction of entry bias is unclear"
	- "Intuitively, a marginal entrant adds to variety, but does not capture the resulting gain in social surplus as profits."
- "We consider the second-best problem of choosing the welfare-maximising number of firms, while we take as given their noncompetitive behaviour after entry." (p. 48)
- Model:
	- $n^p$ potential entrants choose, in the first stage, whether or not to enter a market at cost $F$, and compete, in the second stage, each facing cost function $c(q)$ which is increasing in $q$, exhibits (weakly) decreasing returns to scale (i.e. $c''(q)\geq0$), and is such that $c(0)=0$.
	- Equilibrium profit per firm given that $n$ firms have entered the market is denoted by $\pi_n$, and the equilibrium number of active firms $n^e$ is such that $\pi_{n^e}\geq0$ (no active firm is better off if it had not entered) and $\pi_{n^e+1}<0$ (no inactive firm is better off if it had entered).
	- The social planner chooses the optimum number of firms, $n^o=argmax_nW(n)=\int_0^{nq_n}P(x)dx-nc(q_n)-nF$.
	- Assuming that:
		- (1) equilibrium aggregate output rises with the number of firms,
		- (2) output per firm falls with the number of firms, and
		- (3) for any number of entrants, equilibrium price is greater than marginal cost,
	- the equilibrium number of firms strictly exceeds the optimal number, i.e. $n^e>n^0$.
	- $W'(n)=P(nq_n)q_n+np(nq_n)\frac{\partial q_n}{\partial n}-c(q_n)-nc'(q_n)-F$.
		- Effect of marginal entry on social surplus is composed of the revenue of the entrant, the effect of the entrant on other firms' profits, the cost of the entrant, the effect of the entrant on other firms' costs, and the fixed cost of entry.
		- $W'(n)=\pi_n+n(P(nq_n)-c'(q_n))\frac{\partial q_n}{\partial n}$.
			- Effect of marginal entry on social surplus is equal to incumbent profit (which is the same as entrant profit, at the margins), plus the business stealing effect (which is equal to the marginal profit for all incumbents multiplied by the marginal change in incumbents output as a result of entry).
			- "The first-order change in social welfare attributable to a marginal entrant is composed of two terms. First, the new entrant contributes directly to social surplus equivalent to his profits. Second, the entrant causes all existing firms to contract their output level by $\frac{\partial q_n}{\partial n}$ resulting in an aggregate contraction of $n\frac{\partial q_n}{\partial n}$ and a reduction in social surplus of $n\frac{\partial q_n}{\partial n}(P'(nq_n)-c'(q_n))$." (p. 52)
			- "If firms act as price takers after entry, then free entryr esults in exactly the socially efficient number of firms, despite the presence of a business stealing effect because output contraction no longer ahs any net social value."
		- $W'(n)\leq\pi_n$, hence $W'(n^o)=0\leq\pi_{n^o}$.
		- It can be shown that $\pi_n$ falls with increasing $n$, hence $\pi_{n^e}=0$ and $\pi_{n^o}\geq0$ imply $n^e\geq n^o$.
	- Result: "bias toward excessive entry can be extremely large", where $P(Q)-a-bQ$ and $c(q)=cq$, \[Mankiw and Whinston derive results to show very large difference between $n^e$ and $n^o$.\]
- Product Diversity
	- If consumers prefer variety and firms' products are substitutes, then the effect of marginal entry on social surplus is equal to the additional profit of the entrant (equal to incumbent profit at the margins) plus the business stealing effect (similar to above) and the effect of product variety. Whether marginal entry at equilibrium, (where entrant profit is zero) has a positive or negative effect on social surplus is therefore ambiguous.
- Small Set Up Costs

## [Milgrom and Roberts, 1982](https://doi.org/10.1016/0022-0531(82)90031-X)
- Selten's Chain Store Paradox (pp. 282-284)
	- A chain store operates in $n$ identical markets, each with one potential entrants. Entrants individually and sequentially decide whether to enter their corresponding markets. If an entrant enters its corresponding market, the chain store then decides whether to share the market or prey on the entrant.
	- The chain store's payoff in each market is highest if there is no entry, next highest if the market is shared, and lowest if it preys on the entrant.
	- Each entrant's payoff is highest if the market is shared, next highest if it does not enter, and lowest if it is preyed on by the incumbent.
	- "Selten suggests that in early rounds the incumbent would adopt the costly predatory action in order to persuade later entrants that they should best stay out, and only near the end of the game would it be willing to share a market."
	- This intuitively appealing strategy is not a subgame perfect equilibrium since, in the final market, supposing the entrant enters, the incumbent best responds by sharing the market, and the entrant thus chooses to enter.
	- Since the outcome in the final market is determined independent of the outcome in the penultimate market, the incumbent acts in the penultimate market to maximise that market's payoff. Again, the entrant enters and the incumbent shares the market with it.
	- By backward induction, all entrants enter their respective markets, and the incumbent shares each market with its respective entrant.
	- "The key factor driving this conclusion is that it is common knowledge that accommodation is the best response to entry and that entry is the best response to accommodation. This common knowledge arises from the situation represented as a game of complete and perfect information in which all firms are fully informed about the structure of the game."
- Milgrom-Roberts Model
	- This model "allows that there is some small element of doubt in the minds of the entrants about whether their model of the established firm's options, motivation, and behaviour is correct. In particular, it allows that the entrants entertain some possibility that the incumbent either always preys on the entrant or always shares the market with the entrant."
		- A predatory response might be a part of a general aggressive pattern, and a cooperative response may be a part of a general cooperative pattern.
		- This model "involves the entrants being less than certain that they are correct in modeling the established firm as rationally choosing between predation and peaceful coexistence, they entertain the possibility that an episode of predation may be part of a general pattern of predatory behaviour." (p. 302)
			- "It might be that the established firm could actually be involved in some bigger game which calls for it to prey in these markets" (p. 303)
			- Entrants may also entertain the possibility that the firm "is not behaving as a fully rational game theorist." "Firms involve many individuals each eith his orher own preferences and information, the appropriate model of the firm would be one of group decision making, and there is no compelling reason for choices in such situations to correspond to the maximisation of a single utility function."
			- "Alternatively, the firm may not calculate fully the equilibrium in the game being played, relying on heuristic conjectures about how entrants will behave, under which preying is optimal." The incumbent may think that "business managers extrapolate from past events rather than sizing up the probabilities in each new situation."
	- In the last market (stage), if the incumbent is not simply following a general aggressive rule (and thus has the option of sharing the market), it (rationally) must share the market. Thus, if the incumbent ever fails to prey (in response to entry), such that potential entrants know it is not simply following a general aggressive rule, entrants (rationally) must enter thereafter, since the backward induction argument then applies.
	- Thus failure to prey results in zero payoff in the present period and all subsequent periods.
	- Supposing that in the first market the incumbent preys on the entrant, it does so only if it is following a general rule, or if its payoff from predation is sufficiently high that the lower present-period payoff is at least offset by the higher future payoffs from having a reputation for predation.
	- \[Question\] what does the incumbent's reputation (intuitively) consist in? Do entrants adjust how likely they think it is that the incumbent is not choosing rationally upon observing predation?
		- In the paper, reputation variable $x$ seems to be "minimum reward variable $t$ such that it is worthwhile to prey on the entrant and thereafter be known to have at least such $t$", and "worthwhile" is even more difficult to unpack. What is the intuition here at its simplest?

## [Kreps and Wilson, 1982](https://doi.org/10.1016/0022-0531(82)90030-8)
- Chain-Store Paradox
	- (Scherer, 1980): sharp price cutting in one market can have a demonstration effect on the behaviour of actual or would-be rivals in other markets. "If rivals come to fear from a multimarket seller's actions in Market A that entry or expansion in other markets will be met by sharp price cuts or other rapacious responses, they may be deterred from taking aggressive actions there. Then the conglomerate's expected benefit from predation in Market A will be supplemented by the discounted present value of the competition-inhibiting effects its example has in Markets B and C."
		- Scherer's reasoning predicts that the multimarket firm has incentive to prey on entrants in early stages such as to convince later opponents that it will prey on them too if they were to enter, thus deterring later entries. "If this were the case, then also the early round opponents would not enter, not wishing to be abused for demonstration purposes". (p. 255)
	- "What is lacking, apparently, is a plausible mechanism that connects behaviour in otherwise independent markets." (p. 254)
- One-Sided Uncertainty
	- "In practical situations, the entrants cannot be certain about the payoffs to the monopolist. They may be unsure about the monopolits's costs, or they may be uncertain about nonpecuniary benefits that the monopolist reaps--this may be a monopolist who enjoys being tough." (256)
	- "The entrants may initially assess some positive probability that the monopolist's payoffs reflect an immediate benefit from a predatory response."
	- This probability adjusts as entrants observe each stage of the finite game. If there is no entry, the probability remains unchanged. If entry is met with predation, the probability (weakly) increases. If entry is met with acquiescence, the probability is zero.
		- Since the strong monopolist always fights entry. "Thus any acquiescence is conclusive proof that the monopolist is weak."
			- \[Possible to expand on this in essay\]
	- Even if the monopolist is in fact weak, it has incentive to prey on entrants, especially in early stages, to preserve its reputation. Failure to prey irreversibly and entirely undermines the monopolist's reputation and invites entry in the large number of subsequent stages.
		- \[Possible to expand on this in essay\]

## Tirole, 1988, pp. 377-379
- "According to this theory, a firm with substantial financial resources can prey on a weaker rival. Because the strong or big firm can sustain losses for a longer period of time, it can drive the weak or small firm out of the market."
- The "long purse" theory of predation is plausible only if the entrant faces a financial constraint. This financial constraint results from imperfections in the capital market.
- "Consider a $2$-period duopoly model. Firm $1$ has no financial constraint. Firm $2$ must finance an investment $K$ between the two periods if it is to remain in the market. Firm $2$'s equity after the first period depends on its retained earnings after first-period market competition. By preying in the first period, firm $1$ reduces firm $2$'s first period profit and therefore reduces its equity. Firm $2$, if it is to remain in the market, must finance more of the investment $K$ by debt."
- Lower equity and higher debt increases the risk of bankruptcy, hence the bankruptcy cost, which is passed on to firm $2$ as a higher interest rate. The increase in the cost of debt to firm $2$ makes continuation in the market less attractive, and firm $2$ exits if the expected return on equity from remaining in the market is lower than the opportunity cost of equity.
- Firm $1$ will prey on firm $2$ if the cost in period $1$ incurred by firm $1$ for inflicting sufficiently large losses on firm $2$ in this period such that firm $2$ exits the market are offset by the second-period increase in profits enjoyed by firm $1$ as a monopolist.
- Under this model of predatory pricing, predation is associated with imperfections in the capital market, where bankruptcy costs are incurred by the bank in observing the entrant's profits in the event of default, which are passed onto the entrant as interest (above the cost of funds to banks). Because the cost of debt exceeds the (opportunity) cost of equity, an incumbent can make remaining in the market less attractive for the entrant by forcing the entrant to finance its investment with more debt.
- Under this model of predatory pricing, predation occurs even if there is no asymmetric information in the product market.
- It is possible that the entrant ceases investments and allows itself to become obsolete, or is bought up by the incumbent, when it is unable to profitably finance further investment. Information asymmetry in capital markets may be reduced if the entrant finances its investment with venture debt, since venture capitalists are typically very involved in portfolio company operations.

## [Milgrom and Roberts, 1982](https://www.jstor.org/stable/1912637)
- "Limit pricing involves charging prices below the monopoly price to make new entry appear unattractive. If the entrant is a rational decision maker with complete information, pre-entry prices will not influence its entry decision, so the established firm has no incentive to practice limit pricing. However, if the established firm has private, payoff relevant information (e.g., about costs), then prices can signal that information, so limit pricing can arise in equilibrium."
- "The basic idea of limit pricing is that an established firm may be able to influence, through its current pricing policy alone, other firms' perceptions of the profitability of entering the firm's markets, and that the firm may thus set its prices below their short run maximizing levels in order to deter entry."
- Suppose that an incumbent monopolist is threatened by some potential entrant, and that the incumbent has private information about its own costs. The potential entrant knows, a priori, that the incumbent's costs are either high or low.
- Consider a three-stage game, where the incumbent monopolist operates as a monopolist in the first stage, the potential entrant decides whether or not to enter at some fixed set-up cost in the second stage, and the firms compete in the third stage if the potential entrant entered the market, if not the incumbent operates again as a monopoly. Suppose that the potential entrant would receive negative net profits were it to enter and compete with the incumbent, assuming that the outcome of the third stage is given by a unique subgame Nash equilibrium.
- A low-cost incumbent may deter entry by signalling that it is such an incumbent, under which it chooses either a low price or a high quantity that would be unprofitable (relative to the alternative under which it chooses monopoly price in the first period) for a high-cost incumbent to emulate (even if entry is thereby successfully deterred), in order to signal to the potential entrant that its costs are low. The low-cost incumbent would choose to do so if the present value of increased future profits from maintaining its monopoly exceed the present value of forgone present profits from the excessively aggressive behaviour.