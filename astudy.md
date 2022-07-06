---
pagetitle: "BBR Answers"
title: "Some Answers to BBR Study Questions"
author: "Frank Harrell"
date: "2020-06-10"
output:
  rmdformats::readthedown:
    usebookdown: false
    hightlight: true
    mathjax: null
---

# Biostatistics in Biomedical Research

## Chapter 10: Ordinary Linear Models

### Section 10.1
1. Matching discards data, doesn't work well with continuous baseline
   variables or when there are many baseline variables, and we don't
   really have a best way to analyze matched data.
   
### Section 10.2
1. No; the t-test is a special case of the linear regression model
   (OLS), the Wilcoxon and Kruskal-Wallis tests are special cases of a
   certain ordinal regression model, and the log-rank test is a
   special case of the Cox proportional hazards model.
1. One cannot estimate the right quantity by subsetting the data, and
   there will usually be too few subjects if we subset of blood
   pressures that are very close to 120 and 140.
   
### Section 10.5
1. The expected value may be the best _single_ guess for a subject,
   and we are usually interested in _tendencies_, i.e., what is the
   average drug effect over all patients.
1. A strong predictive model is one that yields a great variety of
   predicted values.
1. Unless SSE=0 ($R^{2}=1$), the subject-to-subject variability, i.e.,
   unexplained variation in Y, cannot be accounted for by the model.
1. Sample subjects so that half are at the lowest x-value and half are
   at the highest.
1. Sample subjects so that the distribution is almost uniform across
   all somewhat commonly occurring x-values.
   
### Section 10.6
1. Percentiles are functions of how individuals were sampled, not of
   biology, physiology, anatomy, etc.  Analysis of percentiles or of
   quantile groups is in effect taking a very strange transformation
   of the variable.  And adjusting for a variable by only adjusting
   for a few quantile groups results in residual confounding.
   
### Section 10.7
1. The intercept is the mean of Y when all the x's are zero; the
   residual variance means the same thing in both types of models.
   Same with residuals.
1. Numerator d.f.
1. No
1. Compute the harm done by dropping the variables being tested in
   terms of a global model summary such as SSE or $R^2$; test
   coefficients using the regression coefficient estimates, standard
   errors, and correlations.
   
### Section 10.8
1. Two-sample (unpaired) t-test
1. Adjusting for baseline variables will explain more variation in Y,
   reducing standard errors and increasing power.

### Section 10.10
1. 3 for race, 1 for sex, 3 for race x sex interaction = 7
1. The power of treatment interaction tests is limited.
1. The ratio of hazard ratios (HRs) of 0.96 is the relative effect of clopidogrel compared to control for carriers divided by the relative treatment effect for non-carriers.  Our single best guess is that the treatment effects are the same but the confidence interval for 0.96 is very wide.
   
## Chapter 9 Sections 9.4-9.9

### Section 9.6
1. Outcome variation by ld72 is much less impressive than by ld73, so we expect the explained variation in Y to be greater for ld73.

### Section 9.8
1. The IQR effect for ld73 of -3.1 is the estimated effect of varying ld73 from its first quartile (24) to its third quartile (37) holding the exposure level in 1972 constant (were that possible).

### Section 9.9
1. ld72 and ld73 are correlated, so their partial effects compete with each other.  They combine forces when doing the 2 d.f. chunk test.  9/747 and 295/747, i.e. 0.01 and 0.4.

## Chapter 13: Analysis of Covariance in Randomized Studies

## Section 13.1
1. The error term (residuals) absorb the unexplained variability in Y.  If we can move the portion of this variability in Y that is due to covariates to the actual covariates, by including them in the model, we reduce the residual variance $\sigm^2$.  This shortens confidence intervals and increases power of all model-based tests.

## Sections 13.2-13.3
1. By getting the model "right".  Failure to adjust for important covariates assumes in effect that every patient in a treatment group has the same outcome distribution, and when outcomes are truly heterogeneous the unadjusted odds- and hazard-ratios are tilted towards the null value of 1.0.

## Section 13.6
1. If the treatment has a nonzero average effect for a binary outcome, it is mathematically necessary for the absolute risk reduction to vary as a function of baseline risk, no matter what the treatment mechanism.
