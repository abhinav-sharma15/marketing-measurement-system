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

  ## 10. Designing a Good Experiment

A good experiment is not just statistically correct.

It must also be:

* operationally feasible
* interpretable by stakeholders
* robust to real-world noise and bias

Most failed experiments are not caused by bad analysis.
They fail because the design was flawed from the beginning.

---

## 11. Step 1 — Define the Business Question

The experiment should start with a clear decision problem.

Bad question:

* “Is this campaign performing well?”

Better question:

* “Does this campaign generate incremental conversions compared to no exposure?”

Best question:

* “Is this the best use of marginal marketing budget?”

A strong experiment is tied directly to a business decision.

---

## 12. Step 2 — Define the Hypothesis

The hypothesis should clearly specify:

* treatment
* expected impact
* metric

Example:

> Retargeting increases conversion rate by at least 5% compared to no retargeting exposure.

Weak hypotheses create ambiguous interpretation.

---

## 13. Step 3 — Choose the Primary Metric

The primary metric should reflect actual business value.

Examples:

* conversion rate
* revenue per user
* pipeline generation
* opportunity creation
* closed-won revenue

A common mistake:

> optimizing for easy-to-measure metrics instead of meaningful outcomes.

For example:

* clicks are easier to measure than revenue
* but may not reflect business impact

---

## 14. Step 4 — Define Treatment Precisely

The treatment must be clearly specified.

Questions to define:

* What exactly changes?
* What is turned on or off?
* Who is eligible?
* How long is exposure?

Example:

* treatment = users exposed to retargeting ads at frequency cap = 3/day

Ambiguous treatment definitions create unreliable experiments.

---

## 15. Step 5 — Choose the Right Duration

Experiments must run long enough to:

* reduce noise
* capture delayed effects
* account for seasonality

Short experiments can:

* overreact to random fluctuations
* miss long conversion cycles

This is especially important in:

* B2B funnels
* high-consideration purchases

---

## 16. Step 6 — Sample Size and Statistical Power

A test needs enough observations to detect meaningful effects.

Low-volume tests create:

* unstable estimates
* false negatives
* overinterpretation of noise

Practical insight:

> many marketing experiments fail because teams try to measure small effects with insufficient scale.

---

## 17. Step 7 — Define Success Before Launch

Before starting the experiment, define:

* success threshold
* decision criteria
* escalation plan

Example:

* if incremental lift < 2%, reduce spend
* if lift > 8%, scale campaign

Changing definitions after results appear introduces bias.

---

## 18. Real-World Constraints

Perfect experiments rarely exist in production environments.

Examples:

* leadership may resist turning off spend
* legal/privacy constraints may limit targeting
* sales teams may interfere with account assignment
* ad platforms may optimize delivery unevenly

As a result:

> experiment design is often a tradeoff between rigor and practicality.

---

## 19. Strong Opinion

Many marketing teams focus heavily on statistical significance while ignoring experimental validity.

A statistically significant result from a poorly designed experiment is still unreliable.

Design quality matters more than model complexity.

---

## 20. Practical Example

### Scenario

A company wants to evaluate whether YouTube advertising drives incremental pipeline.

### Poor Design

* compare exposed vs non-exposed users directly
* no randomization
* no holdout

Result:

* heavily biased toward users already interested in the product

### Better Design

* geo-level holdout experiment
* matched regions
* pre/post analysis
* pipeline value as primary KPI

This creates a more credible estimate of incremental impact.

---

## 21. Key Takeaway

A good experiment is not defined by sophistication.

It is defined by:

* credibility
* clarity
* alignment with decision-making

The best experiments:

* reduce bias
* answer a real business question
* lead to actionable decisions

## 22. Common Failure Modes in Marketing Experiments

Most failed marketing experiments do not fail because of statistics.

They fail because:

* treatment and control are not truly isolated
* exposure is inconsistent
* platform behavior introduces hidden bias
* the experiment does not reflect real-world behavior

Understanding failure modes is critical for interpreting results correctly.

---

## 23. Contamination

### Definition

Contamination occurs when control units are indirectly exposed to the treatment.

This weakens the difference between treatment and control groups.

---

### Marketing Example

A geo experiment:

* London = treatment
* Birmingham = control

However:

* users travel between regions
* media spillover occurs
* users see ads across devices

As a result:

* control users are partially exposed to treatment

---

### Impact

* measured lift is diluted
* incremental impact is underestimated

---

### Mitigation

* choose well-separated geographies
* reduce audience overlap
* use larger randomization units where appropriate

---

## 24. Spillover Effects

### Definition

The treatment affects users outside the treatment group.

---

### Marketing Example

A YouTube campaign:

* increases brand awareness nationally
* even users in control regions search for the brand later

---

### Impact

* control group behavior changes
* experiment underestimates true impact

---

### Important Insight

Upper-funnel channels often create spillover effects that are difficult to isolate cleanly.

This is one reason:

> brand and video measurement are inherently harder than lower-funnel measurement.

---

## 25. Platform Optimization Bias

### Definition

Ad platforms dynamically optimize delivery toward users most likely to convert.

This means:

* treatment exposure is not always stable or random over time

---

### Marketing Example

A platform algorithm:

* gradually shifts impressions toward higher-intent users
* improves reported performance during the test

---

### Impact

* measured lift may reflect optimization bias
* not true causal impact

---

### Strong Opinion

Platform optimization is one of the most under-discussed sources of bias in digital experimentation.

Many teams assume:

* exposure is fixed
  when in reality:
* delivery systems continuously adapt.

---

## 26. Wrong Unit of Randomization

### Definition

The experiment randomizes at a level that does not match exposure behavior.

---

### Marketing Example

* ads are targeted regionally
* but randomization occurs at user level

Users in treatment and control:

* still experience shared media exposure

---

### Impact

* groups are not truly independent
* causal interpretation becomes unreliable

---

### Key Insight

Choosing the wrong unit of randomization can invalidate an otherwise well-designed experiment.

---

## 27. Short Experiment Duration

### Definition

The test ends before the full impact can be observed.

---

### Marketing Example

B2B campaign measurement:

* experiment runs for 7 days
* pipeline closes 60–90 days later

---

### Impact

* delayed conversions are missed
* upper-funnel impact appears weaker than reality

---

### Practical Insight

Short-term experiments often favor:

* demand capture channels
  while undervaluing:
* long-term demand creation.

---

## 28. Metric Misalignment

### Definition

The experiment optimizes for a metric that does not reflect business value.

---

### Marketing Example

Optimizing:

* click-through rate (CTR)

Instead of:

* revenue
* pipeline quality
* LTV

---

### Impact

* channels that generate cheap engagement are overvalued
* business outcomes are ignored

---

## 29. Stakeholder-Induced Bias

### Definition

Business teams interfere with the experiment due to performance concerns.

---

### Marketing Example

Midway through a holdout:

* marketing teams increase spend
* sales teams prioritize treatment accounts
* campaign settings are changed

---

### Impact

* experiment integrity breaks
* treatment effect becomes uninterpretable

---

### Real-World Insight

Many experiments fail organizationally before they fail statistically.

---

## 30. Survivorship and Reporting Bias

### Definition

Only successful outcomes are analyzed or communicated.

---

### Marketing Example

Teams highlight:

* positive lift tests

But ignore:

* inconclusive or negative experiments

---

### Impact

* distorted learning culture
* false confidence in channels

---

## 31. Key Takeaway

A statistically significant result does not guarantee a trustworthy experiment.

The credibility of an experiment depends on:

* isolation
* stability
* correct randomization
* realistic measurement windows
* organizational discipline

The best marketing scientists are not just good at analysis.

They are good at identifying:

> why an experiment may be wrong.


