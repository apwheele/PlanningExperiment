I am going to have you make a WASM web-app, using R, to help individuals input data and plan how long they should use to conduct an experiment.

One part of the app is going to be about my WDD statistic, and planning for reducing crime counts. For WDD materials, review:

 - https://crimede-coder.com/graphs/WDD (original test)
 - https://crimede-coder.com/blogposts/2025/WDDExtensions (extensions for different metrics)
 - https://github.com/apwheele/ptools/blob/main/R/wdd.R (R code showing how to do the weighting, rate per unit time, per area, etc.)
 - https://github.com/apwheele/ptools/blob/main/R/wdd_harm.R (R code for combining tests with harm weights)
 - https://andrewpwheeler.com/2021/03/18/comparing-the-wdd-vs-the-wilson-log-irr-estimator/ (the IRR estimator, so estimate incident rates)

The other part is going to be planning for an experiment in rates per event, like arrest rates. Review:

 - https://crimede-coder.com/blogposts/2026/PlanningExperiment (blog post on how to plan to increase proportions)

I want the application to have two tabs. Tab 1 is for planning for counts. Tab 2 is planning for proportion events. I want the app to be able to input events per unit time in treated and control, an estimate of the increase/decrease in the event of interest, and then a graph to show the standard error over time with tool tips

I want the application to be a client side application. I want to use R wasm, as the planning experiment part uses logistic regression. 

 - understanding R WASM, https://docs.r-wasm.org/webr/latest/