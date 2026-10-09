# Project Summary

## Business problem
A telecom company is losing customers and needs to know who is leaving, how early, and where retention effort is most likely to pay off.

## Analytical questions
- What proportion of customers churned?
- Which contract types and payment methods have higher churn?
- How does churn vary by internet service, tech support and online security?
- How do tenure and monthly charges relate to churn and retention?
- Where should retention efforts be focused?

## Data and method
- **Data:** IBM Telco Customer Churn sample dataset; 7,032 customers after removing 11 rows with a blank `TotalCharges` (zero-tenure customers).
- **Power Query:** typed the columns and removed the blank-`TotalCharges` rows.
- **Data model:** one table, plus calculated columns for tenure groups and monthly-charge groups (each with a hidden sort column so the groups appear in natural order).
- **DAX measures:** Total, Churned and Retained Customers, Churn Rate, Retention Rate, Average Tenure, and segment-specific churn rates.
- **Report:** a landing page plus three analysis pages with page-to-page navigation.

## What the data shows
- Overall churn is **26.6%** (1,869 of 7,032 customers).
- Churn falls sharply with commitment and time: month-to-month customers churn at 42.7% versus 2.8% on two-year contracts, and customers in their first six months churn at 53.3% versus 9.5% after four years.
- Electronic check payers (45.3%), fiber optic customers (41.9%) and customers without tech support or online security (about 42%) churn at roughly twice the overall rate.

## Suggested focus areas
These follow from the patterns above and would need testing before acting:
- Early-tenure customers (first 6-12 months) are the highest-risk group, so onboarding and early follow-up are a natural focus.
- Moving month-to-month customers onto longer contracts, for example with an incentive, targets the largest churn gap.
- Tech support and online security add-ons are worth testing as retention offers.
- Fiber optic customers churn far more than DSL customers. Pricing or service quality deserve investigation.

## Limitations
- This is a single snapshot of observational data. The findings show associations, not causes.
- Many factors overlap, such as fiber optic service, no tech support and month-to-month contracts. A model that controls for them together is a natural next step.
- The data has no cost or revenue-at-risk figures, so the business value of each segment is not quantified.
