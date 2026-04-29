# Week 1: Potential Outcomes & Counterfactuals

## 1. The Core Idea

At the heart of causal inference is a simple but powerful concept:

For any unit (user, region, or account), there are two possible realities:

* **Y(1):** outcome if exposed to a treatment (e.g., saw an ad)
* **Y(0):** outcome if not exposed

The causal effect is the difference:

Effect = Y(1) - Y(0)

This defines what we actually care about:

> not whether something happened, but whether the treatment *changed* the outcome.

---

## 2. The Fundamental Problem

We can never observe both outcomes for the same unit.

For example:

* A user sees a paid ad and converts → we observe **Y(1)**
* But we cannot observe what would have happened if they had NOT seen the ad → **Y(0)**

This is known as:

> **The Fundamental Problem of Causal Inference**

Because of this, **causality cannot be directly observed—it must be estimated.**

---

## 3. Why This Matters in Marketing

Most marketing reporting focuses on observed outcomes:

* clicks
* conversions
* attributed revenue

However, these only reflect **Y(1)** (what happened after exposure).

They do not answer:

> Would the user have converted anyway?

This leads to a systematic problem:

* demand capture is mistaken for demand creation
* lower-funnel channels appear more effective than they actually are

---

## 4. Concrete Example (Retargeting)

A user:

* visits a website
* is later shown a retargeting ad
* returns and converts

Observed:

* Y(1) = 1 (conversion after ad exposure)

Unknown:

* Y(0) = ?

If the user was already planning to return:

* Y(0) ≈ 1 → causal effect ≈ 0

If the ad changed behavior:

* Y(0) = 0 → causal effect = 1

At the individual level, we cannot distinguish between these cases.

This is why retargeting often looks highly effective in attribution, but has low incrementality in practice.

---

## 5. From Individuals to Averages

Since individual causal effects are unobservable, we estimate them at the group level.

This is called the **Average Treatment Effect (ATE):**

ATE = average(Y(1) - Y(0))

In practice:

* experiments approximate this by comparing treatment vs control groups
* observational methods try to simulate this comparison

---

## 6. Business Confusion: Conversions ≠ Incrementality

A common misunderstanding:

> “This campaign drove 500 conversions”

This assumes:

* all 500 conversions were caused by the campaign

In reality:

* some users would have converted anyway (Y(0) = 1)
* only a subset are truly incremental

So:

Incremental conversions = Y(1) - Y(0), aggregated across users

This distinction is critical for:

* budget allocation
* channel evaluation
* ROI measurement

---

## 7. Why Attribution Breaks Here

Attribution models assign credit to observed touchpoints.

However:

* they do not estimate Y(0), the counterfactual
* they cannot distinguish between causation and correlation

As a result:

* they measure **sequence**, not **impact**
* they systematically over-credit lower-funnel interactions

This is why attribution alone is insufficient for decision-making.

---

## 8. Practical Implication

Instead of asking:

* “Did users convert after seeing an ad?”

We should ask:

* “On average, how much did the ad increase conversions compared to no exposure?”

This shifts measurement from:

* tracking behavior
  to:
* estimating causal impact

---

## 9. Key Takeaway

Causal inference is fundamentally about estimating missing counterfactuals.

Because we cannot observe both realities for the same unit, we rely on:

* experiments (A/B tests, geo lift)
* quasi-experimental methods

to approximate what would have happened otherwise.

In marketing, this is the difference between:

* measuring activity
  and
* measuring true impact.
