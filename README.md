# A/B Test Simulation: Optimizing Email Signup Flow

## Introduction

This project simulates and analyzes an A/B test designed to evaluate the effectiveness of a new, potentially more efficient email signup flow on a website. The core objective is to determine if the new design (treatment group) leads to a statistically significant improvement in signup rates compared to the existing design (control group). This type of analysis is crucial for data-driven decision-making in product development and marketing.

## Methodology

The project followed a structured approach, from data simulation through to statistical evaluation:

1.  **Data Simulation:**
    * **User Assignment:** 100,000 simulated users were randomly assigned to either a control group (existing signup flow) or a treatment group (new signup flow), with a 50/50 split.
    * **Probability Setup:** A baseline email signup probability of 30% was established for the control group. For the treatment group, a 10% relative increase in this baseline probability was introduced to model the anticipated improvement from the new design.
    * **Outcome Generation:** Binary signup outcomes (1 for signed up, 0 for not signed up) were generated for each simulated user based on their assigned group and the corresponding signup probability.

2.  **Experiment Evaluation:**
    The simulated data was then analyzed to quantify the impact of the new signup flow using two statistical methods:
    * **Linear Regression (OLS):** An Ordinary Least Squares regression model was employed. The model included a variable indicating whether a user was in the treatment group. The coefficient for this 'treated' variable directly estimates the absolute difference in signup rates attributable to the new flow. Statistical significance was assessed using the t-statistic and p-value.
    * **Two-Sample T-test:** This test was used to directly compare the mean signup rates between the control and treatment groups, providing an additional measure of the observed difference and its statistical significance (via t-statistic and p-value).

## Visualizing the Impact

The bar plot below visually compares the mean email signup rates for the control and treatment groups, along with their 95% confidence intervals. This provides a clear visual summary of the new signup flow's performance.

<p align="center">
   <img width="862" alt="Screenshot 2025-05-27 at 12 39 28 PM" src="https://github.com/user-attachments/assets/5e68b50c-1479-4b69-9282-e0fa1f98bf95" />
</p>

This chart helps to quickly grasp the magnitude of the difference in signup rates and the precision of these estimates.

## Key Insights from the Analysis

The analysis of the simulated A/B test data yielded clear and statistically significant results:

* **Improved Signup Rate:** The new signup flow (treatment group) demonstrated a clear improvement in email signup rates compared to the existing design (control group).
* **Quantifiable Impact:**
    * The analysis estimated an **absolute increase in the signup rate of approximately 3.4 percentage points** for users exposed to the new flow.
    * This translates to an estimated **relative increase of about 11.3%** over the control group's baseline signup rate.
* **Statistical Significance:** Both the linear regression model and the two-sample t-test confirmed that these observed differences are **highly statistically significant**. The p-values were very close to zero, indicating that the improvement seen in the treatment group is highly unlikely to be a result of random chance.

These findings strongly suggest that implementing the new signup flow would likely lead to a meaningful increase in overall email signups.

## Conclusion & Key Learnings

This project successfully demonstrated an end-to-end A/B testing process, from initial data simulation to statistical analysis and interpretation of results. It showcased how simulated experiments can be used to estimate the potential impact of website changes.

The key takeaway is the clear, statistically significant improvement in signup rates attributed to the new flow design. This provides a solid, data-backed rationale for making a business decision to roll out the new design. This exercise highlights the power of A/B testing in providing actionable insights and de-risking changes before full-scale implementation.
