
## EDA Process (ThinkStats Book)

### General Framework for Comparing a Variable to a Distribution

A useful way to think about exploratory data analysis is to treat it as a cycle of question, model, and validation:

1. **Define the question clearly**
   - Identify the variable of interest and the population it comes from.
   - Decide whether you are asking about a single variable, a comparison between groups, or a relationship between variables.

2. **Load and inspect the data**
   - Read the data carefully and understand its units, missing values, and possible coding issues.
   - Check whether the variable is discrete or continuous.
   - Look at the sample size and whether the data are representative of the target population.

3. **Describe the empirical distribution**
   - For discrete data, inspect the PMF or bar plot.
   - For continuous data, inspect the histogram, CDF, and summary statistics.
   - Report key features such as center, spread, skewness, tails, and unusual values.

4. **Choose one or more candidate distributions**
   - Use domain knowledge to suggest plausible models.
   - Examples:
     - **Binomial**: number of successes in repeated trials.
     - **Poisson**: count of events in a fixed interval.
     - **Exponential**: waiting time between events.
     - **Normal**: symmetric, bell-shaped data.
     - **Lognormal**: positive data with right-skew and multiplicative growth.

5. **Estimate model parameters from the data**
   - Fit the model using sample statistics such as mean, proportion, or rate.
   - Example: for a Poisson model, use the sample mean as the parameter $\lambda$.
   - Example: for a normal model, use the sample mean and standard deviation.

6. **Compare the observed distribution with the theoretical model**
   - Plot the empirical distribution and the model side by side.
   - Use PMFs for discrete distributions and CDFs for continuous distributions.
   - Compare shape, center, spread, and tail behavior.

7. **Judge the quality of the fit**
   - A model is not accepted just because it looks similar; it should capture the important structure of the data.
   - Check whether the model explains:
     - the overall shape,
     - the central tendency,
     - the variability,
     - the tails,
     - and any outliers or unusual features.
   - If the fit is poor in the tails or around the center, the model may still be useful for some purposes but not for others.

8. **Test assumptions and look for violations**
   - Ask whether the assumptions behind the model are realistic.
   - Example: a Poisson model assumes events occur independently at a constant rate, which may not be true in practice.
   - If assumptions are clearly violated, the model may still be a rough approximation rather than a true description.

9. **Compare alternative models**
   - Try more than one candidate distribution.
   - Compare their fit visually and, if appropriate, with formal measures such as residual analysis or goodness-of-fit tests.
   - Prefer the simplest model that explains the data well.

10. **Interpret and report the result carefully**
    - Say whether the variable appears to be well modeled by a given distribution.
    - Be explicit about the level of confidence in the conclusion.
    - Note limitations, sample size, and data quality issues.

### Practical Rule of Thumb

A variable can be considered reasonably consistent with a distribution if:

- the overall shape matches the theoretical model,
- key statistics such as mean and variance are compatible,
- the model does not miss obvious patterns in the tails or center,
- and the assumptions behind the model are plausible for the context.

In practice, the goal is not to prove that a variable “belongs” to a distribution in an absolute sense. The goal is to decide whether a distribution is a useful and reasonable model for the data.

### EDA Workflow Summary

- **Ask a question**
- **Collect / load data**
- **Summarize distributions**
- **Compute summary statistics**
- **Visualize patterns**
- **Examine relationships**
- **Stratify by groups**
- **Check for data issues**
- **Compare with candidate distributions**
- **Interpret and report findings**

Follow these steps iteratively: visualization and summary statistics often suggest new questions, and new questions often lead to better models.