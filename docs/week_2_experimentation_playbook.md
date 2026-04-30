# Week 2: Experimentation Playbook

## 1. Why Experiments Matter

Experiments are the most reliable way to measure causal impact because they explicitly construct a counterfactual.

By randomly assigning units into treatment and control groups, experiments ensure that:

* both groups are statistically comparable
* differences in outcomes can be attributed to the treatment

Without experiments:

* we rely on observational data
* estimates are vulnerable to bias (selection, confounding)

In marketing, this distinction is critical:

> high-performing channels in attribution are not necessarily high-impact channels in reality.

---

## 2. Core Components of an Experiment

### Treatment Group

Units exposed to the intervention (e.g., users shown ads)

### Control Group

Units not exposed, representing the baseline

### Randomization

Assignment mechanism that ensures:

* no systematic differences between groups
* unbiased estimation of treatment effect

---

## 3. Unit of Randomization (Critical Design Choice)

The unit of randomization defines *what gets assigned* to treatment or control.

### Common Options

#### User-Level

* each user is independently assigned
* high statistical power
* best for: email, product features, lifecycle marketing

#### Geo-Level

* entire regions assigned to treatment/control
* reduces contamination
* best for: paid media, brand campaigns

#### Account-Level (B2B)

* entire accounts assigned together
* avoids cross-user contamination within the same company
* critical for: sales-assisted funnels

---

## 4. Tradeoffs in Choosing the Unit

Choosing the wrong unit can invalidate the experiment.

### Smaller Units (e.g., user-level)

Pros:

* higher sample size
* more precise estimates

Cons:

* higher risk of contamination
* harder to isolate exposure

---

### Larger Units (e.g., geo-level)

Pros:

* cleaner separation between treatment and control
* better for channels with shared exposure

Cons:

* lower sample size
* higher variance

---

## 5. Practical Insight

The unit of randomization should match how the treatment is delivered.

Examples:

* Ads targeted by region → use geo-level randomization
* Emails sent to individuals → use user-level randomization
* Sales outreach to accounts → use account-level randomization

Misalignment leads to biased results.

---

## 6. Key Takeaway

Experiment design is not just about running tests.

It is about designing a setup where:

* the counterfactual is credible
* bias is minimized
* results can be trusted for decision-making

Choosing the correct unit of randomization is one of the most important decisions in this process.

