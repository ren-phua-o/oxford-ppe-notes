# R Commands Notes

## Common (Examinable) R Commands
- 191001 Q3a (Variable Construction)
	- `slid$exp = slid$age - slid$educ - 5`
- 191001 Q3bi (Linear Regression)
	- `lm_robust(log(wages) ~ male + exp, data = slid)`
- Other Linear Regressions
	- `lm_robust(log(wages) ~ I(exp^2), data = slid)`
- 191001 Q3ciii (F Test)
	- `linearHypothesis(regfn, c("male"), test = "F")`
- Filter
	- `slid$exp[slid$male == 1]`
- Multiple Columns
	- `slid[c("age","educ","male")]`
- `mean`, `var`, `sd`, `cor`, `summary` are functions on dataframes.
- `hist` is a function on vectors.
- Instrumental Variable Regression
	- `iv_robust(dep ~ endo + ctrl | ctrl + inst, data = df)`