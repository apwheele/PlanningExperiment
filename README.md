# Crime De-Coder Experiment Planning App

This repository contains a client-side web application designed to help crime analysts and researchers plan the duration and sample size requirements for experimental evaluations.

This is currently deployed on my Crime De-Coder page at <https://crimede-coder.com/graphs/Planning>. (The app has diverged slightly from what is in this repo already, but either should work fine. You can right click and see the source on my PHP website as well, there is no hidden server side logic that prevents you from seeing how the calculations are done.)

## ASEBP Conference Talk
This application was developed as part of a presentation given at the **American Society of Evidence-Based Policing (ASEBP)** Conference.
- **Speaker**: Andrew Wheeler
- **Session Info**: [ASEBP Speaker Profile](https://whova.com/embedded/speaker/GEGQuzvoi@0BMeBBGR4YQoIYQy0--p71zjtQE5-RA-0=/51070681/)

## Features
The app includes four main planning tools:
1. **WDD Counts Planning**: For planning experiments using the Weighted Displacement Difference statistic.
2. **IRR Counts Planning**: Uses the Wilson log IRR estimator for count data (Incident Rate Ratios).
3. **Proportion Events Planning**: Planning for proportions, such as arrest rates or use-of-force incidents.
4. **Simulation Proportion Events**: A power simulation engine using logistic regression to handle complex crime distributions and baseline solve rates.

## Technology Stack
- **WebR (R-WASM)**: Executes R code entirely in the browser.
- **Chart.js**: Dynamic visualization of standard errors and confidence intervals over time.
- **Vanilla JS/CSS/HTML**: Lightweight, serverless implementation.

## Citations
If you use these tools or the WDD statistic in your research, please use the following citations:

- **WDD Statistic**: Wheeler, A. P., & Ratcliffe, J. H. (2018). A simple weighted displacement difference test to evaluate place based crime interventions. *Crime Science*, 7(1), 11. [DOI](https://doi.org/10.1186/s40163-018-0085-5)
- **Wilson IRR Estimator**: Wilson, D. B. (2022). The relative incident rate ratio effect size for count-based impact evaluations: When an odds ratio is not an odds ratio. *Journal of Quantitative Criminology*, 38(2), 323-341. [DOI](https://doi.org/10.1007/s10940-021-09494-w)
- **Planning Application**: Wheeler, A. P. (2026). Experiment Planning for Crime Analysts. *Crime De-Coder*. [Website](https://crimede-coder.com/graphs/Planning)

## Use of AI

I used Google's Antigravity tool to help create the initial app (conversation not saved, but can see the initial prompt in GEMINI.md, and I mostly used the free flash 3 model).

I used Claude to help write the technical document (using Opus 4.6 via Bedrock, see the ClaudeTech.txt for the session information).

I personally reviewed each for accuracy. Any errors are due to my own, not the LLM tools.

## Other resources

 - Excel document on the different WDD metrics, WDD_Spreadsheet_CrimeDeCoder.xlsx (see <https://crimede-coder.com/blogposts/2025/WDDExtensions> for a blog post about this as well with links to many other posts). 
 - My ptools R package, (on [CRAN](https://cran.r-project.org/web/packages/ptools/index.html), [GitHub](https://github.com/apwheele/ptools))
 - python code for the WDD is in my [crimepy library](https://github.com/apwheele/crimepy)

Then I have several posts on my personal blog that are relevant for planning with the counting type designs:

 - [Minimum detectable effect sizes for place based designs](https://andrewpwheeler.com/2021/04/02/minimum-detectable-effect-sizes-for-place-based-designs/)
 - [Comparing the WDD vs the Wilson log IRR estimator](https://andrewpwheeler.com/2021/03/18/comparing-the-wdd-vs-the-wilson-log-irr-estimator/)
 - [Poisson designs and Minimum Detectable Effects](https://andrewpwheeler.com/2024/03/18/poisson-designs-and-minimum-detectable-effects/)

## Running Locally
To run the application locally, you can serve the directory using any static web server. For example:
```bash
python3 -m http.server
```
Then navigate to `http://localhost:8000`.
