# ur-kid-ding-me

"Cleaned up project.pdf" is the annotated and more organized report, so click that one.

This project is half exploration, half tutorial. The guiding question is, "what's the effect of having 3 or more children (variable "morekids=1" from here on out) on income/the decision for a mother to work?" I walk through every component required to conduct this analysis, including a lot of derivations, proofs, some fun unsolved stats problems, and the boring old R implementations. I recommend you read the below for a brief summary before diving in; the whole thing's a lot! (35 pages). I think the most interesting part is the last half regarding instrument selection, model comparison and CACE; the earlier stuff has some fun proofs, and basic data explorations and "checks" for instrument validity, but is not as exciting. 

The first question any econometrician/statistician must have is, "how do I represent my existing data?" For every variable, there are numerous ways to represent it. For a variable like education; maybe the difference between 1 or 2 years of high school doesn't really matter, but the difference between 3 (incomplete) and 4 (graduating) years of high school. I play around with some simple linear probability models to explore different ways to represent our existing data, and briefly discuss how I might be able to use some variables differently.

The second question is, "what controls do we want to include in our model?" To control for omitted variables bias, some might say, "include every control you can. Duh!" But it is nevertheless important to check for the significance of certain control variables and think about what that might mean. If you have some independent variable (morekids), you don't want it to be highly correlated with a certain variable that you then omit from your analysis. 

Third, we ask, "What variable can we use as a valid instrument for morekids=1?" I provide some derivations, empirical evidence, and logical explanations for the relevance and exogeneity of samesex=1 (the sex of the first two children being same). I then, well, do the actual regressions.

After establishing that samesex is a valid instrument to use in our models, we then ask, "ok, but what do we include in the model? What controls do we include, and how does that relate to the explorations we've done earlier?" In this section, I provide some quick and dirty proofs to justify what inclusions I make to the model, explain the variation I see in results with and without inclusion of certain controls, and talk about some fun stats stuff.

Finally, I get heavy into the Complier Average Causal Effects framework (CACE). This framework helps us look at how instrument relevance might differ across different populations by looking at "compliers", for which the instrument does lead to a certain effect on the instrumented variable. If instrument relevance (aka proportion of "compliers" - we'll explain later) differs among different demographics/subjects, then we have good reason to consider that our estimate effect sizes will be different across different demographics too.


