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

## 4. Types of Marketing Experiments

Different marketing channels require different experiment designs. The choice depends on:

* how the channel operates
* what level you can realistically randomize at
* business constraints (risk, scale, feasibility)

In practice, experiment design is often constrained less by theory and more by **what the business is willing to change**.

---

### 4.1 A/B Tests (User-Level Experiments)

#### Description

Users are randomly assigned to treatment or control groups.

#### Best For

* Email campaigns
* Product features
* Lifecycle marketing

#### Example

* Send promotional email to 50% of users
* Hold out 50% as control

#### Strengths

* High statistical power
* Cleanest form of randomization
* Easy to interpret

#### Limitations

* Not feasible for most paid media channels
* Cross-device behavior and identity gaps can introduce contamination

---

### 4.2 Geo Experiments

#### Description

Geographic regions (cities, states, countries) are assigned to treatment or control.

#### Best For

* Paid media (YouTube, TV, Paid Social)
* Brand campaigns
* Channels where user-level control is not possible

#### Example

* Ads ON in London, Manchester
* Ads OFF in Birmingham, Leeds

#### Strengths

* Does not rely on user-level tracking
* Reduces contamination from shared exposure

#### Limitations

* Requires a sufficient number of comparable regions
* Sensitive to regional differences (confounding)
* Lower statistical power than user-level experiments

---

### 4.3 Holdout Tests

#### Description

A subset of users (or geos) is intentionally excluded from marketing exposure.

#### Best For

* Incrementality testing
* Retargeting evaluation
* Always-on performance channels

#### Example

* 10% of eligible users are withheld from retargeting ads

#### Strengths

* Direct measurement of incremental impact
* Simple and intuitive interpretation

#### Limitations

* Can reduce short-term revenue
* Often faces internal resistance from marketing teams

---

### 4.4 Platform Experiments (e.g., Meta Conversion Lift)

#### Description

Experiments run within advertising platforms using their internal randomization.

#### Best For

* Large-scale paid campaigns
* Situations where internal experimentation is difficult

#### Example

* Meta splits audience into exposed vs non-exposed groups

#### Strengths

* Easy to deploy
* Scales quickly
* No need for internal infrastructure

#### Limitations

* Limited transparency (black-box methodology)
* Dependent on platform assumptions
* Results are not always comparable across channels

---

## 5. Choosing the Right Experiment

There is no universally “best” method.

The right choice depends on:

* **Channel mechanics**
  Can you control exposure at the user level?

* **Data availability**
  Do you have reliable geo or user-level data?

* **Business constraints**
  Can you afford to reduce or stop spend?

---

## 6. Real-World Constraints

In practice, ideal experiments are often not feasible.

Examples:

* Paid search cannot be fully turned off due to revenue risk
* Cross-device behavior makes user-level randomization imperfect
* Marketing teams resist holdouts due to short-term performance impact

As a result:

> experiment design is often a compromise between rigor and feasibility

---

## 7. Practical Comparison

* **Geo vs Platform Experiments**

Geo experiments:

* more transparent
* fully controlled internally
* require more setup and data

Platform experiments:

* faster and easier
* rely on platform logic
* should not be treated as ground truth without validation

---

## 8. Strong Opinion

Most teams over-rely on platform experiments because they are easy to run.

However:

> convenience should not be confused with accuracy.

Without independent validation, platform-reported lift can create a false sense of confidence.

---

## 9. Key Takeaway

Experiment design is context-dependent.

The goal is not to use the most sophisticated method, but to use:

> the most credible method given real-world constraints.

The best marketing measurement systems combine:

* experiments (for ground truth)
* models (for scalability)
* judgment (for decision-making)


