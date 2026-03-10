# Statistics and Probability

<aside> 🎯

**Goal:** Build intuition, learn core formulas, and practice solving problems.

</aside>

## 1) Big picture

- **Statistics**: describing data and making conclusions from samples.
- **Probability**: modeling uncertainty and predicting outcomes.

## 2) Quick cheat sheet

- **Mean**: $\bar{x} = \frac{1}{n}\sum_{i=1}^n x_i$
- **Variance (sample)**: $s^2 = \frac{1}{n-1}\sum_{i=1}^n (x_i-\bar{x})^2$
- **Probability rules**:
    - $P(A^c)=1-P(A)$
    - $P(A\cup B)=P(A)+P(B)-P(A\cap B)$
    - $P(A\mid B)=\frac{P(A\cap B)}{P(B)}$
- **Bayes' theorem**: $P(A\mid B)=\frac{P(B\mid A)P(A)}{P(B)}$

## 3) Distributions to know

- **Bernoulli($p$)**: $P(X=1)=p$
- **Binomial($n,p$)**: number of successes in $n$ trials
- **Normal($mu,sigma^2$)**: bell curve, many real-world sums
- **Poisson($lambda$)**: counts per interval

## 4) Core topics checklist

- [ ] [[Chapter 1_ The Roles of Statistics in Engineering]]
- [ ] [[Chapter 2_Probability]]
- [ ] [[Chapter 3_ Discrete Random Variables and Probability Distributions]]
- [ ] [[Chapter 4_ Continuous Random Variables and Probability Distribution]]
- [ ] [[Chapter 5_Joint Probability Distributions]]
- [ ] [[Chapter 6_ Descriptive Statistics (thống kê mô tả)]]
- [ ] [[Chapter 7_ Sampling Distributions and Point Estimation of Parameters]]
- [ ] [[Chapter 8_ Statistical Intervals for a Single Sample]]
- [ ] [[Chapter 9_ Test of Hypotheses for a Single Sample]]
- [ ] [[Chapter 10_ Statistical Inference for Two Samples (Suy luận thống kê cho samples)]]
- [ ] [[Chapter 11_ Simple Linear Regression and Correlation (Hồi quy tuyến tính)]]
- [ ] [[Chapter 12_Multiple Linear Regression]]
- [ ] [[Chapter 13_ Design and Analysis of Single-Factor Experiments The Analysis of Variance]]
- [ ] [[Chapter 14_ Design of Experiments with Several Factors]]
- [ ] [[Chapter 15_ Statistical Quality Control]]


## 5) Practice prompts

1. If a test has 95% specificity and 90% sensitivity, what is $P(\text{disease}\mid\text{positive})$ given prevalence 1%?
2. Compute $E[X]$ and $\mathrm{Var}(X)$ for $Xsimtext{Binomial}(n,p)$.
3. Use the CLT to approximate $P(S_n \le a)$ for a sum of i.i.d. variables.

## 6) What to study next

- Choose your level:
    - **High school**: counting, basic probability, mean/variance
    - **University intro**: random variables, distributions, inference
    - **Data science**: estimation, testing, regression, simulation

**Tell me your level and goal (exam, data science, or just learning), and I’ll make a 2-week study plan with exercises.**