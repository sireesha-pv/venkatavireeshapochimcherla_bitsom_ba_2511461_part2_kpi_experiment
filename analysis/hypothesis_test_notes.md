# Hypothesis test notes

This file contains brief notes about hypothesis tests performed for the experiment.

- Purpose: Compare treatment vs control on primary KPI.
- Tests: t-test for means, bootstrap for confidence intervals.
- Data source: data/campaign_experiment_data.xlsx
- Next steps: run final analysis and record results in outputs/experiment_summary.xlsx


# Hypothesis Test Notes

## Business Decision
Determine whether the new onboarding (Treatment) should be rolled out to all users based on its impact on paid conversion.

## Metric Being Tested
**Paid Conversion Rate** (converted to paid / total users)

### Reason for Choosing This Metric
Paid conversion rate directly measures the campaign's success in turning new users into paying subscribers, making it the primary business outcome.

## Null Hypothesis (H0)
There is **no statistically significant difference** in the paid conversion rate between the Control and Treatment groups.

## Alternative Hypothesis (H1)
The **Treatment group has a higher paid conversion rate** than the Control group.

## Test Type
**One-tailed test**, because the business objective is specifically to determine whether the new onboarding improves conversion rather than simply being different.

## Significance Level
**α = 0.05 (5%)**

## Interpretation Logic
- If **p-value < 0.05**, reject the null hypothesis and conclude that the Treatment significantly improves paid conversion. Recommend rollout if guardrail metrics remain acceptable.
- If **p-value ≥ 0.05**, fail to reject the null hypothesis. There is insufficient evidence to recommend a full rollout; continue testing or iterate on the onboarding experience.

## Connection to Business Decision
The hypothesis test provides statistical evidence for whether the new onboarding experience delivers a meaningful improvement in paid conversion while supporting an informed rollout decision.
