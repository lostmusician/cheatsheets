# ST2334 finals cheatsheet

- `st2334-finals-cheatsheet.tex`: editable, self-contained LaTeX source.
- `st2334-finals-cheatsheet.pdf`: two A4 landscape pages, intended for the two sides of one sheet. Print at actual size (100%); use landscape short-edge duplex binding.

The layout reserves two of eight columns for first-half probability material (25%) and six for second-half sampling, estimation, confidence intervals and hypothesis testing (75%). It matches the two-page A4 landscape format of the supplied midterm sheet. Check your exam's permitted number of sides separately; the sheet does not establish exam rules.

The question patterns come from your course quizzes, tutorials and revision chats, rather than a statistical analysis of past-paper frequencies. Following your report that the professor will model the finals on the quizzes, the latest revision prioritizes all 87 questions in the Weeks 8-12 quiz-solutions collection. The second-half emphasis is formula selection, sampling pivots, CI manipulation, paired versus independent data, tail selection, rejection decisions and power.

## Build

From this folder, with a LaTeX installation:

```sh
pdflatex -interaction=nonstopmode -halt-on-error st2334-finals-cheatsheet.tex
```

Alternatively:

```sh
tectonic st2334-finals-cheatsheet.tex
```

No external figures, custom fonts, or repository-specific macros are required. Packages: fontenc (T1), geometry, amsmath, amssymb, multicol, xcolor, helvet, array.

## Conventions

Critical-value subscripts are **upper-tail probabilities**: P(T > t[nu; gamma]) = gamma. This avoids mixing the cumulative-quantile notation used in some earlier chats with the course's notation. For normal populations with unknown variance, t is exact at any sample size; the quizzes use t even at n = 36 and n = 49. Use an approximate z reference when the problem explicitly requests the large-sample normal method. Equal population variances are required for pooled inference; merely similar observed variances do not establish that assumption. Rejection inequalities use strict p < alpha; follow a question's explicitly stated boundary convention.

## Source material used

Local course files (kept in their original locations):

- `/Users/ivanchiew/Downloads/st2334-final-cheatsheet.pdf` (friend’s three-page reference, compared on 19 November 2026).
- `/Users/ivanchiew/Downloads/ST2334/st2334-midterm-cheatsheet.pdf` (format and first-half topics).
- `/Users/ivanchiew/Downloads/FormulaSheet_Tables.pdf` (course formulas, table conventions).
- `/Users/ivanchiew/Downloads/ST2334/lecturenotes.pdf` (AY26/27 S1, Chapters 1-7).
- `/Users/ivanchiew/Downloads/ST2334/Lecture Slides Week 12.pdf`.
- `/Users/ivanchiew/Downloads/ST2334/tutorials/Tutorial Week 08.pdf` through `Tutorial Week 12.pdf`.
- `/Users/ivanchiew/Downloads/ST2334/tutorials/tutorial01_solutions.pdf` through `tutorial06_solutions.pdf`.
- `/Users/ivanchiew/Downloads/ST2334/tutorials/Tutorial Week 08 Solutions.pdf`, `Tutorial Week 09 Solutions.pdf`, and `Tutorial Week 10 Solutions.pdf`.
- `/Users/ivanchiew/Downloads/ST2334/st2334 quiz/Quiz_Solutions.pdf` (62 pages; all 87 pre/post-lecture questions for Weeks 8-12).

User-referenced revision chats read on 18 November 2026:

- Work through tutorial questions (`01a1ce1a-56d0-7583-b6d1-e07cfbd42f72`).
- Guide tutorial questions step by step (`01a1cd49-cd1b-7f90-ba1d-be1843fc80f1`).
- Review Final Topic Contents (`6af29bd0-02c8-83ec-9a36-9646f59c988c`).
- Explain Three Slides Formulas (`6adcd90c-6db4-83ec-85b2-b3484f5d386a`).
- Rejecting Null Hypothesis (`6af40f48-eb98-83ec-b3e8-de66cd8ff84b`).

Some chat messages referenced images whose contents were unavailable in the retrieved text. The sheet uses the stated numerical setups and independently checked formulas, not unseen image details or answer-option labels. Full statistical tables are not reproduced; use your supplied table booklet for additional critical values.

## Tutorial coverage review (18 November 2026)

Reviewed all nine supplied solution sets and the Week 11-12 question sheets. The existing inference formulas and included numerical examples agree with the relevant supplied solutions. The sheet retains two columns for first-half material and six for second-half material. The table records the tutorial review; the quiz-priority changes below supersede it where space required a tradeoff.

| Material | Coverage and additions |
| --- | --- |
| Tutorial 1 | Counting, restrictions, complements, routes through/avoiding points; added block and gap methods and grid-path counting. |
| Tutorial 2 | Conditional probability, total probability, Bayes, independence and exactly-one events already covered. |
| Tutorial 3 | PMF/PDF normalization, CDF jumps, moments and linear transformations; added CDF validity, general left endpoints, piecewise integration, mass aggregation and stopping without replacement. |
| Tutorial 4 | Marginal/conditional distributions, joint expectations, covariance and linear-combination variances already covered. |
| Tutorial 5 | Binomial/geometric/negative-binomial/Poisson models and approximations; added conditional Poisson-to-binomial recognition, logarithmic trial thresholds, nonlinear payoffs and evaluating series using moments. |
| Tutorial 6 | Uniform/exponential/normal models, memorylessness, minima, continuity correction and Bayes already covered; added the two-stage pattern of a continuous threshold probability followed by a binomial count. |
| Week 8 | SRS, random samples, CLT and LLN already covered; added explicit construction of a discrete sampling distribution by enumerating and aggregating sample outcomes. |
| Week 9 | Chi-square/t/F pivots, order-statistic estimators, unbiasedness and minimum-variance comparisons already covered; added F concentration as both degrees of freedom grow and known versus estimated centering in sums of squares. |
| Week 10 | Mean/difference CIs, reverse CI calculations, width/confidence changes and sample-size planning already covered and checked against solutions. |
| Week 11 | Pooled and paired inference, CI/test comparison and width changes already covered; added solving for sample size to reject for a fixed observed mean, with strict-inequality rounding. |
| Week 12 | One-sample, paired, known-variance two-sample tests, p-values and equal-variance large-sample intervals already covered. |

The reference sheet is a selective recall aid, not a transcript of all exercises. The detailed continuous change-of-variable inverse-density rule was replaced by tutorial-focused discrete transformations, CDF reasoning and piecewise integration to make room. Set algebra beyond the principal event rules and full worked arithmetic for every question remain in the tutorials. No new regression, ANOVA, or small-sample unequal-variance inference section was indicated by these files.

## Quiz coverage review (18 November 2026)

Compared every question and worked solution with the sheet. There are 16 questions for Week 8, 16 for Week 9, 15 for Week 10, 20 for Week 11 and 20 for Week 12: 87 in total. References such as “W9 post2” on the printed sheet mean Week 9, post-lecture quiz, Question 2. Answer-option letters are deliberately omitted because choices can be reordered.

| Quiz group | Question patterns and sheet sections |
| --- | --- |
| W8 pre 1-8 | Replacement, linearity, mean variance and SE, LLN, scale factors: sections 1-2, 4 and 7-9. |
| W8 post 1-8 | Standardized-statistic variance without centering, CLT shape, SE scaling, probability above the mean, mean tails, independent averages and SE-only sample-size targets: sections 4 and 7-9. |
| W9 pre 1-8 | Sum CLT, inverse probability for n, bias correction, F mean and normalized ratios, df for residual sums of squares and subset means: sections 7-12 and 22. |
| W9 post 1-8 | Squared t cutoff, normal approximation to chi-square, reciprocal/scaled F ratios, central t probabilities, unbiased linear combinations and simultaneous confidence/size changes: sections 10-12, 18 and 22. |
| W10 pre 1-7 | z/t width ratios, sample-size scaling, adding two variance contributions, fixed midpoint and confidence changes: sections 14-18. |
| W10 post 1-8 | t/z substitution, simplifying SE, nested CIs, uncertainty floor with one fixed sample size, variance-and-size scaling, specified t at n = 49 and reconstructing a statistic from a CI: sections 14-18. |
| W11 pre 1-10 | Pooled/paired CI calculations, lower-tail tests, width ratios, raw-mean rejection cutoff, reversing the target difference, exact-coverage assumptions, data-selected tail doubling Type I error and numerical Type II error/power: sections 13-23. |
| W11 post 1-10 | Pooled/paired inference, CI-to-test reconstruction for nonzero null, unequal pooling weights, two-sided raw-mean cutoff, rescaled CIs, minimum n for two-sided rejection and power complement: sections 13-23. |
| W12 pre 1-10 | One-sample/paired/two-sample tests, signed and two-sided p-values, actual null inside a CI, large-sample pooled z, exact CI endpoint p-values, nonzero null pooled test and paired correlation threshold: sections 13-23. |
| W12 post 1-10 | t at n = 36, nonzero-null two-mean p-value, pooled margin, CI-to-t reconstruction, paired raw data, wrong-direction one-tail p-value, p-value brackets from nested CIs, pooled df and nonzero paired null: sections 13-23. |

### Main quiz-driven additions

- F expectation, dependence from a shared random denominator, and the scale difference between raw chi-square ratios and normalized F ratios.
- Normal approximation to a chi-square tail, with mean df and variance twice df.
- Squared t statistics: split the upper-tail probability across both t tails, then square the critical value.
- Exact t inference at large n for normal populations with unknown variance, and the distinction between normal marginals and normal paired differences.
- Weighted/subset estimators, variance unaffected by centering, and probability above the population mean under the CLT.
- Combined variance/sample-size width changes and the remaining SE when only one of two samples grows.
- Reconstructing tests from confidence intervals, reversing CI signs, and bracketing p-values using two confidence levels.
- Critical cutoffs in the sample mean's original units, power and Type II error under a specified true mean, and the doubled Type I error from choosing a one-sided direction after seeing the data.

The numerical power example, chi-square approximation, squared-t cutoff and two-sided sample-size example were independently recalculated. The final PDF remains two A4 landscape pages with unchanged 7.4-point body text, two first-half columns and six second-half columns.

### Space tradeoffs and tutorial backup

To prioritize the quizzes and make the formulas explicit, the printed sheet keeps uniform-estimator details here instead of the full minimum-variance derivation, and removes the duplicate paired-CI arithmetic, the Tutorial 12 calculator example, the finite-population correction, the stopping-without-replacement paragraph, and the nonlinear-payoff/series paragraph. The underlying general moment, CDF, variance and inference formulas remain on the sheet. Useful backup reminders:

- Stopping at the first success without replacement is not geometric: multiply the changing conditional failure probabilities, then the success probability. Hypergeometric describes a count in a fixed-size sample.
- For a finite SRS without replacement and population variance defined with divisor N, Var(sample mean) = sigma squared / n times (N-n)/(N-1).
- Nonlinear payoff: E(X squared) = Var(X) + E(X) squared; E[g(X)] generally differs from g(E[X]). An infinite series of the form sum g(k) f(k) is a distribution moment.
- For independent identically distributed U(0,b) observations, the maximum M has mean nb/(n+1) and variance n b squared / [(n+1) squared (n+2)]. The unbiased estimator (n+1)M/n has variance b squared / [n(n+2)]. For two U(0,2 theta) observations, U = min and V = max have means 2 theta / 3 and 4 theta / 3, variances 2 theta squared / 9, and covariance theta squared / 9. An unbiased aU+bV requires a+2b = 3/2; substituting into its variance and differentiating gives a = 0, b = 3/4.

## Formula clarity revision (18 November 2026)

The printed sheet now defines the main symbols and gives the symbolic formula before numerical substitutions. The pooled method is explicitly numbered: pooled sample variance, pooled SD and standard error of the difference, then the confidence interval or test statistic. The worked quiz example repeats those formulas beside its numbers. Sample SDs and sample variances are distinguished so it is clear whether to square a supplied value.

The revision also adds explicit conditional-expectation notation, the sum-tail standardization formula, the general chi-square approximation calculation, paired-data symbol definitions, the general correlation-threshold inequality, and fully shown SE/cutoff substitutions in the power example. To make room at the same font size, repeated decision text and the remaining printed uniform-maximum reminder were shortened or moved to the backup notes above. The PDF remains two A4 landscape pages.


## Organisation and comparison revision (19 November 2026)

Compared the friend's three-page reference with the existing sheet. The revised output remains two A4 landscape pages, with the familiar 23 numbered sections, two first-half columns and six second-half columns. The previous source and PDF are preserved in `versions/2026-11-18/`.

### Main changes

- Added case tables for counting, continuity correction, sampling pivots, one-mean inference, independent-mean inference, paired endpoints/reversals, confidence/size changes, tails and p-values, CI/test duality, quiz navigation and the Type I/II error decisions.
- Retained the explicit pooled variance → pooled SD → SE calculation, symbolic test statistics, paired sample-variance shortcut and worked power example. Section 17 now states the paired t CI explicitly. Section 19 explains Phi lookup, normal CDF calculator inputs and t-table p-value brackets.
- Consolidated squared-t formulas in section 11 and weighted estimators in section 12; section 22 now directs readers to these formulas rather than repeating them. The nonzero-null pooled example refers to section 15's full formula.
- Added discrete uniform moments, the normal density, negative-binomial/binomial probability link, geometric survival, correlation under linear rescaling, sample-proportion moments, variance of a general sum, t moments with degrees-of-freedom restrictions, reciprocal/scaled F quantiles, 96% normal critical values and power direction reminders.
- Preserved assumptions: unknown variance plus normal data gives exact t at any sample size; pooled inference requires equal population variances. A blanket n >= 30 rule for z and similarity of observed sample SDs do not replace these assumptions.

This is still a selective exam recall aid. Small-sample unequal-variance Welch inference, regression and ANOVA were not added because the reviewed course materials did not establish them as required topics. Full tables and extended derivations remain in the course sources and the backup notes above.

Validation: rebuilt with Tectonic, confirmed two landscape A4 pages, and inspected renders of both pages for table wrapping, clipping and missing formulas. Body text remains 7.4 pt; line and paragraph spacing were tightened where needed. No overfull boxes were reported.
