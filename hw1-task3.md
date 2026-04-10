# Homework 1 Task 3

---

Answer the following questions based on exercises from *An Introduction to Statistical Learning with Applications in Python*.

## Chapter 2.4 Exercises

---

### Exercise 1 (ISLP exercise 2)

Explain whether each scenario is a **classification or regression** problem, and indicate whether we are most interested in **inference or prediction**. Finally, provide **n** (size of observation dataset) and **p** (number of predictors).

**(a)**  We collect data on 200 protected marine reserves worldwide. For each reserve we record species richness, reserve size, years since establishment, enforcement budget, and proximity to human settlements. We are interested in understanding which factors affect species richness.

> **Your Answer:**

Our output is a numeric value so this scenario is describing a regression problem. Understanding which factors affect a response is a classic inference problem, its a matter of understanding the association between X and Y rather than predicting Y with X. In this example we have n = 200, and p = 4 (reserve size, years since establishment, enforcement budget, and proximity to human settlements).

---

**(b)** A conservation agency wants to know whether a proposed habitat corridor will successfully support wildlife movement or fail to do so. They collect data on 30 previously established corridors. For each corridor they have recorded whether wildlife movement was successful or unsuccessful, corridor width, length, surrounding land use type, and eight other variables.

> **Your Answer:**

This one is a classification problem since the outcome is categorical (successful or unsuccessful). The agency is interested only in what the outcome will be, a corridor is successful or not, so this is a prediction problem. In this case, n = 30 and p = 11 (corridor width, corridor length, surrounding land use type, +8 others).

---

**(c)** We are interested in predicting weekly average ground-level ozone concentration in a coastal city. We collect weekly data for all of 2019. For each week we record average ozone concentration, sea surface temperature, wind speed, solar radiation, and atmospheric

> **Your Answer:**
Once again we have a numeric response (weekly ozone concentration) so we are looking at a regression problem. As it states in the scenario description, we are interested in prediction here, specifically ozone levels from weekly environmental conditions. We have an n of 52 (weeks in a year) and p = 4 (sea surface temp, wind speed, solar radiation, and atmospheric __?).
---

### Exercise 2 (ISLP exercise 5)

What are the advantages and disadvantages of a very flexible (versus a a less flexible) approach for regression? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?

> **Your Answer:**
A more flexible model can capture more complicated patterns by being able to take on many different forms, so its better when the true relationship is complicated. The risk is that fitting a flexible model to something less complicated leads to overfitting, which is when the model is doing too much work and is picking up a bunch of noise from the data. A less flexible model is often better in this case, in particular it can be better when the sample size is small, the data is noisy, or we are interested in fully understanding the relationships in the data (such as is the case with inference). On the other hand, if the data is more complex than we are giving it credit for, a more restrictive model may miss important patterns in the data and end up being inherently wrong.

---

### Exercise 3 (ISLP exercise 6)

Describe the differences between a **parametric** and a **non-parametric** statistical learning approach. What are the **advantages** of a parametric approach to regression or classification (as opposed to a non-parametric approach)? What are its **disadvantages**?

> **Your Answer:**
A parametric approach assumes a specific form for the relationship (e.g. a linear model) and then estimates a fixed number of parameters. The main advantages of this is that it simplifies the job of estimating some unknown f into estimating a set number of betas. This can often make it simpler, faster, effective with less data, and easier to interpret than other methods. On the down side, if the assumed form is wrong, then our estimates will also be wrong. A non-parametric approach addresses this by making fewer assumptions about the shape of f. Instead it is attempting to produce an f that gets as close as possible to the observed data which can make it far more accurate. But it can also make it far more sensitive to noise and sparse data leading to overfitting and unnecessary complexity.