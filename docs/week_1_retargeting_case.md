# Week 1: Case Study — Retargeting Incrementality

## 1. Problem Statement

Retargeting campaigns show strong performance in attribution reports:

* high conversion rates
* strong ROI
* consistent volume

However, there is concern that:

* retargeting primarily targets users who already intend to convert
* reported performance may overstate true impact

The key question is:

> How much of retargeting performance is truly incremental?

---

## 2. Why This Is a Hard Problem

Retargeting inherently targets:

* users who have already visited the site
* users further down the funnel

This introduces strong **selection bias**:

* these users are more likely to convert regardless of ads

As a result:

* observed performance ≠ causal impact

---

## 3. Naïve Interpretation (What Goes Wrong)

Typical reporting shows:

* Retargeting conversion rate: 8%
* Other channels: 2–3%

Conclusion:

> Retargeting is the most effective channel

This is misleading because:

* retargeted users are not comparable to cold audiences
* conversion rates are inflated due to pre-existing intent

---

## 4. Causal Approach (Experiment Design)

To measure incrementality, we need a controlled experiment.

### Design

* **Treatment group:** users eligible for retargeting ads
* **Control group:** similar users excluded from retargeting

### Key Metric

* conversion rate (treatment vs control)

### Incrementality Calculation

Incremental lift = Conversion(Treatment) - Conversion(Control)

---

## 5. Example Outcome

* Treatment conversion rate: 8%
* Control conversion rate: 6%

Incremental lift = 2%

Interpretation:

* Only 25% of observed conversions are incremental
* 75% would have happened without retargeting

---

## 6. Business Implications

If retargeting is mostly non-incremental:

* reported ROI is overstated
* budget may be inefficiently allocated
* opportunity cost exists (other channels may drive true growth)

However, retargeting may still:

* accelerate conversions (shorten time to purchase)
* improve user experience (reminders, nudges)

---

## 7. Decision Framework

Instead of asking:

* “Is retargeting profitable?”

We should ask:

* “Is retargeting the best use of marginal budget?”

Actions:

* reduce spend if incremental lift is low
* cap frequency
* reallocate budget to higher-incrementality channels

---

## 8. Limitations & Considerations

* holdout design must avoid contamination
* platform constraints (e.g., audience exclusions)
* delayed effects may not be fully captured
* results may vary by segment

---

## 9. Key Takeaway

Retargeting often appears highly effective due to selection bias.

Only a small portion of its performance may be truly incremental.

Effective measurement requires:

* controlled experiments
* careful interpretation of results
* focus on incremental impact, not attributed conversions

