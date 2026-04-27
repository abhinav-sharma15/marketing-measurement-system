# Week 1: Causal Reasoning Primer

## 1. What Last-Click Attribution Shows

Last-click attribution assigns 100% credit for a conversion to the final touchpoint before the conversion event.

In many cases, this is:

* branded search
* direct traffic
* retargeting ads

This creates a simple view of performance but does not reflect true causality.

---

## 2. Why Branded Search Gets Over-Credited

Branded search is primarily a **demand capture channel**, not a demand creation channel.

Most users searching for the brand already have high purchase intent. As a result, branded search often appears highly effective in attribution models because it sits close to the conversion event.

This creates a structural bias:
- high-intent users are more likely to convert regardless of ads
- attribution assigns credit to the last touchpoint, not the source of demand

However, the decision to invest in branded search is not trivial.

Even if a portion of conversions would happen organically, paid ads may:
- defend against competitors bidding on brand terms
- improve visibility and click-through rates
- control messaging at a critical decision moment

This makes branded search a **strategic channel**, but not necessarily a highly incremental one.

---

## 3. The Missing Counterfactual

The key causal question is:

> What would have happened if the user had NOT seen or clicked the ad?

This is the central limitation of attribution systems.

We observe:
- users who converted after interacting with ads

But we do not observe:
- whether those same users would have converted without the ad

Without this counterfactual, we cannot distinguish between:
- demand creation
- demand capture

---

## 4. How to Test Incrementality

To measure true impact, we need an experiment:

* Treatment group: users exposed to ads
* Control group: users not exposed

Compare:

* conversion rate (treatment)
* conversion rate (control)

Incremental impact = difference between the two

This isolates **causal effect**, not just correlation.

---

## 5. Business Implication

If branded search is not incremental:

* reducing spend may not reduce revenue significantly
* budget may be better allocated to channels that generate new demand

This changes decision-making from:

* “which channel gets credit?”
  to:
* “which channel actually drives incremental growth?”

## 6. Example

A user:
- sees a YouTube ad earlier in the week
- later searches for the brand on Google
- clicks a paid search ad
- converts

In last-click attribution:
- paid search gets 100% of the credit

However:
- the YouTube ad likely created initial awareness
- paid search simply captured existing intent

If paid search ads were removed:
- many of these users may still convert via organic search

This means the incremental value of paid search is likely lower than reported.

## 7. Key Takeaway

Attribution tells us where conversions happen.

Causal measurement tells us what actually caused them.

In practice, channels that look strongest in attribution are often the weakest in incrementality.

Effective marketing decisions require understanding this difference.
