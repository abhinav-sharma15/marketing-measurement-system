# Week 1: Bias in Marketing Measurement

## 1. Why Bias Matters

In marketing measurement, most errors do not come from bad models.

They come from **biased data**.

If bias is not addressed:

* models will be directionally wrong
* attribution will over-credit certain channels
* decisions will reinforce incorrect strategies

Understanding bias is more important than choosing the right algorithm.

---

## 2. Selection Bias

### Definition

Selection bias occurs when the group exposed to marketing is not randomly chosen.

### Marketing Example

Users who see or click ads are often:

* more engaged
* further down the funnel
* already interested in the product

### Impact

* conversion rates for exposed users are inflated
* marketing appears more effective than it actually is

### Real-World Case

Retargeting campaigns:

* target users who already visited the site
* these users are more likely to convert anyway

### Fix

* randomized experiments (A/B tests)
* holdout groups

---

## 3. Confounding

### Definition

A confounder is a variable that influences both:

* treatment (ad exposure)
* outcome (conversion)

### Marketing Example

High-income regions:

* receive more ad spend
* have higher purchasing power

### Impact

* increased conversions may be incorrectly attributed to ads
* actual driver (income) is ignored

### Fix

* control variables (regression)
* matching methods
* geo experiments

---

## 4. Reverse Causality

### Definition

When the outcome influences the treatment, not the other way around.

### Marketing Example

* increased demand → more branded search queries
* platforms allocate more spend to high-performing segments

### Impact

* it appears that ads drive demand
* in reality, demand drives ad exposure

### Fix

* time-based analysis
* experiments
* careful interpretation of trends

---

## 5. Survivorship Bias

### Definition

Focusing only on users who completed the funnel.

### Marketing Example

Analyzing only converted users:

* ignoring users who dropped off
* ignoring those never reached

### Impact

* distorted view of performance
* overestimation of effectiveness

### Fix

* include full funnel data
* analyze non-converters

---

## 6. Measurement Bias (Tracking Limitations)

### Definition

When data collection is incomplete or inaccurate.

### Marketing Example

* cookie loss
* cross-device tracking gaps
* ad blockers
* platform reporting inconsistencies

### Impact

* undercounting or misattribution of conversions
* inconsistent reporting across tools

### Fix

* aggregated measurement (geo tests, MMM)
* triangulation across methods

---

## 7. Key Insight

Different channels are affected by different biases:

* Lower-funnel channels (search, retargeting):
  → heavily impacted by selection bias

* Upper-funnel channels (video, brand):
  → often undervalued due to attribution limitations

This creates a systematic distortion:

> channels that capture demand look strongest, while channels that create demand look weakest.

---

## 8. Practical Implication

If bias is not addressed:

* budget shifts toward demand capture
* investment in demand creation declines
* long-term growth suffers

Correcting for bias is not just a technical issue:

> it directly impacts business strategy.

---

## 9. Key Takeaway

Most marketing measurement problems are not modeling problems.

They are bias problems.

The goal of causal inference is to:

* identify these biases
* design methods to reduce them
* estimate true incremental impact

