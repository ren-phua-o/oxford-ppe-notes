# Entry and Predation Outline

## Entry and Predation
- Free Entry
	- Bertrand Free Entry
	- Bertrand Hit-and-Run Entry
	- Cournot Free Entry
- Entry Deterrence
	- Dixit-Spence Model
	- Fudenberg-Tirole Taxonomy
- Predatory Pricing
	- Selten Chain Store Paradox
	- Milgrom-Roberts Signalling Model
	- Kreps-Wilson Reputation Model
	- Fudenberg-Tirole Long Purse Model

## Bertrand Free Entry
- Parameters: Potential entrants choose whether to enter at cost $F$, then firms compete in Bertrand. Suppose $Q=SD(p)$.
- Analysis: Analyse second stage Nash equilibrium, then first stage Nash equilibrium.
- Result: Monopoly.
	- Analytically, this is because $\pi=0$ under Bertrand competition.
- Result: $\uparrow S\Rightarrow\uparrow q$.
	- Analytically, this is because the industry is a monopoly in equilibrium.
- Result: $n^a,p\perp\!\!\!\perp S$.
	- Analytically, this is because the industry is a monopoly in equilibrium.

## Bertrand Hit-and-Run Entry
- Parameters: $I$ has $C(q)=f+cq$. Suppose entry and exit are instantaneous and prices are rigid.
- Analysis: Show no profitable deviation from $p=\min\frac{C(q)}{q}$.
- Result: Potential competition sufficient for constrained optimal outcome.
	- Intuitively, positive profit invites entry since entry is costless.
- Evaluation: Unrealistic assumption that entry and exit occur more quickly than price adjustment.
- Evaluation: Unrealistic assumption that entry cost is not sunk.

## Cournot Free Entry
- Parameters: Potential entrants choose whether to enter at cost $F$, then firms compete in Cournot. Suppose $Q=SD(p)$ hence $p=P(\frac{Q}{S})$.
- Analysis: Analyse second stage Nash equilibrium, then first stage Nash equilibrium.
- Result: $\uparrow S\Rightarrow\downarrow p,<\propto\uparrow n^a,<\propto\uparrow q$.
	- Analytically, $p^C\perp\!\!\!\perp S$ given $n^a$, then $\uparrow S$ first order $\Rightarrow\propto\uparrow q\Rightarrow\propto\uparrow\pi^C\Rightarrow\uparrow$ entry incentive second order $\Rightarrow\uparrow n^a\Rightarrow\downarrow p^C,\downarrow q$.
	- Intuitively, $\uparrow S\Rightarrow<\propto\uparrow n^a$ because $\geq\propto\uparrow n^a\Rightarrow\downarrow p,\downarrow q\Rightarrow\pi<F$.
	- Intuitively, $\uparrow S\Rightarrow<\propto\uparrow q$ because $\uparrow S$ first order $\Rightarrow\propto\uparrow q$ but $\uparrow S$ second order $\Rightarrow\uparrow n^a\Rightarrow\downarrow s\Rightarrow\downarrow q$.
- Result: Excessive entry because of the business-stealing effect.
	- Analytically, at equilibrium, marginal entrant enjoys zero profit, marginal consumer has $v=p$ hence marginal entry has no effect on $CS$, and marginal entry $\downarrow\pi$ of other firms, so marginal entry $\downarrow W$.
	- Intuitively, this is because entry imposes a negative externality on other firms.
- Empirical Data (Bresnahan and Reiss, 1991):
	- Bresnahan and Reiss (1991) study the relationship between market size and the number of local providers of (relatively) homogenous services (e.g. doctors, dentsits, and druggists) in 202 geographically isolated markets in the U.S. Bresnahan and Reiss find that the town population required to support two firms is significantly more than double the population required to support one firm, and that in general, the number of firms increases less than proportionately with the size of the market, up to $4$ firms. This observation is mostly consistent with the Cournot free entry model. That the market size per firm does not increase beyond $4$ firms suggests that firms' margins are not eroded by entry of subsequent firms. Bresnahan and Reiss also studied the prices of tire dealers in the U.S., and find that the prices of tires falls as entry occurs and the number of tire dealers in the market increases. This observation is consistent with the Cournot free entry model, under which entry erodes margins.
- Empirical Data (Campbell and Hopenhayn, 2005):
	- Campbell and Hopenhayn (2005) study the size of producers in 13 retail trade industries in 225 markets of different sizes in the U.S. in 1992. Campbell and Hopenhayn find that in most industries, market size has a significant positive effect on firms' average sales and employment. A doubling of market size corresponds to an increase in average sales of $3\%$ to $19\%$. This observation is consistent with the Cournot free entry model. Under this model, firm size increases less than proportionately with market size.

## Dixit-Spence Model
- Parameters: $I$ chooses $k_I$ at cost $rk_I$, then $E$ chooses whether to enter at cost $F$, then $I$ and $E$ compete in Cournot.
- Analysis: Analyse third stage Nash equilibrium graphically, then discuss subgame-perfect equilibrium for impeded entry, blockaded entry, deterred entry, and accommodated entry.
- Result: Over-investment in capacity to deter or accommodate entry.
	- Analytically, if $I$ deters entry over-investment is relative to monopoly capacity, if $I$ accommodates entry, over-investment is relative to Cournot quantity (optimal given no strategic effect).
	- An intuitive explanation borrows from the Fudenberg-Tirole taxonomy.
- Discussion: Necessary assumption that investment is sunk.
- Empirical Data (Chemical Plants):
	- Lieberman (1987) studied rates of market growth and capacity utilisation in periods just prior to the construction of new plants by entrants and incumbents in a sample of $38$ chemical product industries from 1952 to 1982. Lieberman found that the threshold levels of market growth and capacity utilisation required to induce investment in an additional plant were similar for incumbents and entrants. This observation is not consistent with the hypothesis that incumbent firms over-invest in capacity in order to deter entry. If incumbents over-invest in capacity in order to deter entry, we would expect that incumbents expand capacity pre-emptively at a lower threshold than entrants. This finding is, however, not decisive, since the decision of an incumbent to open an additional plant and the decision of an entrant to open an additional plant are not symmetrical decisions. Incumbents can often expand through incremental additions to existing plants, which plausibly increases the threshold of market growth and capacity utilisation required to induce investment in an additional plant. Incumbents may open an additional plant not in an effort to expand capacity, but to replace existing capacity. This would reduce the sensitivity of incumbent investment to rates of market growth and capacity expansion, hence impose a negative bias on the observed thresholds. If the net effect of these asymmetries increases the threshold at which incumbents invest in an additional plant, the empirical observation could be consistent with an incentive for incumbents to deter entry by maintaining excess capacity.

## Fudenberg-Tirole Taxonomy
- Parameters: $I$ chooses $k_I$, then $E$ chooses whether to enter at cost $F$, then $I,E$ choose $x_I,x_E$.
- Definition (Strategic Complements and Strategic Substitutes): $x_1$ and $x_2$ are strategic complements iff one firm's marginal profit is increasing with the other firm's strategic variable, i.e. iff $\frac{\partial}{\partial x_j}(\frac{\partial\pi_i}{\partial x_i})=\frac{\partial^2\pi_i}{\partial x_i\partial x_j}>0$ for all $i\neq j$. $x_1$ and $x_2$ are strategic substitutes iff $\frac{\partial}{\partial x_j}(\frac{\partial\pi_i}{\partial x_i})=\frac{\partial^2\pi_i}{\partial x_i\partial x_j}<0$ for all $i\neq j$.
- Definition (Toughness and Softness): $\uparrow k_I$ makes $I$ "tough" iff $\uparrow k_I\Rightarrow\uparrow\frac{\partial\pi_I}{\partial x_I}$ for all $x_E$ and makes $I$ "soft" iff $\uparrow k_I\Rightarrow\downarrow\frac{\partial\pi_I}{\partial x_I}$ for all $x_E$.
- Definition (Over-Investment and Under-Investment): $I$ over-invests iff it invests more than would be optimal if $k_I$ had no strategic effect, i.e. $\frac{d\pi_E}{dk_I}=\frac{\partial\pi_E}{\partial k_I}$ and $\frac{d\pi_I}{dk_I}=\frac{\partial\pi_I}{\partial k_I}$.
- Analysis (Deterrence): Suppose for simplicity that $\frac{\partial\pi_E}{\partial k_I}=\frac{\partial\pi_I}{\partial k_I}=0$, $\frac{d\pi_E}{dk_I}=\frac{\partial\pi_E}{\partial k_I}+\frac{\partial\pi_E}{\partial x_I}\frac{dx_I}{dk_I}+\frac{\partial\pi_E}{\partial x_E}\frac{dx_E}{dk_I}=\frac{\partial\pi_E}{\partial k_I}+\frac{\partial\pi_E}{\partial x_I}\frac{dx_I}{dk_I}=\frac{\partial\pi_E}{\partial x_I}\frac{dx_I}{dk_I}$ since first-order condition $\frac{\partial\pi_E}{\partial x_E}=0$ holds and $\frac{\partial\pi_E}{\partial k_I}=0$ by supposition.
- Analysis (Accommodation): $\frac{d\pi_I}{dk_I}=\frac{\partial\pi_I}{\partial k_I}+\frac{\partial\pi_I}{\partial x_I}\frac{dx_I}{dk_I}+\frac{\partial\pi_I}{\partial x_E}\frac{dx_E}{dk_I}=\frac{\partial\pi_I}{\partial k_I}+\frac{\partial\pi_I}{\partial x_E}\frac{dx_E}{dk_I}=\frac{\partial\pi_I}{\partial x_E}\frac{dx_E}{dk_I}=\frac{\partial\pi_I}{\partial x_E}\frac{\partial x_E}{\partial x_I}\frac{dx_I}{dk_I}$ since first-order condition $\frac{\partial\pi_I}{\partial x_I}=0$ holds and $\frac{\partial\pi_I}{\partial k_I}=0$ by supposition.
- Case Study (Southwest Airlines):
	- Goolsbee and Syverson (2008) study the response of incumbent major airlines to the threat of entry by Southwest Airlines in the U.S. from 1993 to 2004. Goolsbee and Syverson find that when Southwest begins operating out of two airports, but has not yet offered direct flights between the two airports, such that incumbents offering flights on this route face a heightened threat of Southwest's entry but do not yet face actual entry, incumbents decrease average fares on this route substantially. The decrease in average fares by incumbents in response to the threatened entry is greater than the decrease in average fares by incumbents following actual entry. The decrease in fares is not explained by shifts in airport-specific operating costs. The response of incumbents to the threat of entry by Southwest observed by Goolsbee and Syverson may be understood as an investment in customer loyalty, which has the direct effect of reducing Southwest's profit were it to enter, thus deterring entry. Alternatively, the investment in customer loyalty could be understood as an effort to accommodate entry, since investment in customer loyalty softens price competition in the event that Southwest enters.
- Empirical Data (Ellison and Ellison)
	- Ellison and Ellison (2011) study incumbents' advertising, product proliferation, and pricing decisions as their pharmaceutical patents approached expiry in the U.S. between 1986 and 1992. Ellison and Ellison find that, in some cases, the relationship between strategic investment (in advertising, product proliferation, or customer loyalty or goodwill through lower pricing) has a non-monotonic relationship with market size. Incumbents over-invest in intermediate-sized markets and under-invest in small or large markets. This observation is consistent with the theory of strategic entry deterrence. In small markets, no investment is required to deter entry. In large markets, it is impossible to deter entry. Therefore, the incentive to deter entry through strategic investment is greatest in intermediate-sized markets.

## Selten Chain Store Paradox
- Parameters: $E_1$ chooses whether to enter at cost $F$, $I$ chooses whether to prey or accommodate, $E_2$ chooses whether to enter at cost $F$, and so on.
- Analysis: Analyse by backward induction.
- Result: All $E$ enter and are accommodated.
	- Intuitively, entry occurs and is accommodated in all markets because $I$ cannot credibly threaten predation and predation has no effect on subsequent entrant's assessment.

## Milgrom-Roberts Signalling Model
- Parameters: $I$ operates as a monopolist, $E$ chooses whether to enter at cost $F$, $I$ and $E$ compete. $I$ knows $c_I$, $E$ knows only that $c_I$ is either $c_I^H$ or $c_I^L$.
- Analysis: Argue that low cost $I$ can credibly signal its cost by choosing low price.

## Kreps-Wilson Reputation Model
- Parameters: Selten Chain Store model except each $E$ entertains possibility that $I$ is "strong" and is rewarded for preying.
- Analysis: Argue that accommodation invites subsequent entry hence $I$ has strong incentive to prey in early markets hence early $E$ have no incentive to enter.
- Evaluation: Critical assumption that $I$ is possibly "strong" is plausible since $E$ are uncertain about non-pecuniary benefits and managerial incentives.

## Fudenberg-Tirole Long Purse Model
- Parameters: $I$ and $E$ compete, $E$ chooses whether to exit or finance a fixed investment by debt or equity, $I$ and $E$ compete again.
- Analysis: Predation $\Rightarrow$ $\downarrow$ equity $\Rightarrow$ $\uparrow$ debt $\Rightarrow$ $\uparrow$ risk of bankruptcy $\Rightarrow$ $\uparrow$ expected bankruptcy cost to bank $\Rightarrow$ $\uparrow$ interest rate $\Rightarrow$ $\uparrow$ cost of debt $\Rightarrow$ $\downarrow$ return on equity $\Rightarrow$ $\uparrow$ incentive to exit.