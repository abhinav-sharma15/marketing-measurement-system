# Week 4: Synthetic Control for Geo Lift

## 1. Why Synthetic Control?

In a geo lift test, the core problem is the same as all causal inference:

> What would have happened in the treatment regions if the campaign had not run?

This missing outcome is the counterfactual.

Difference-in-Differences estimates this counterfactual using the average change in control regions.

Synthetic control takes a more tailored approach.

Instead of comparing treatment regions to an average control group, it builds a weighted combination of control regions that closely matches the treatment regions before the campaign.

This creates a more credible counterfactual when some control regions are more comparable than others.

---

## 2. The Core Idea

Synthetic control tries to construct:

> a weighted version of the control group that behaves like the treatment group before treatment.

Example:

Treatment geo: London

Synthetic London:
- 40% Birmingham
- 30% Manchester
- 20% Leeds
- 10% Bristol

If Synthetic London closely tracks London before the campaign, then after the campaign:

> the gap between actual London and Synthetic London can be interpreted as estimated incremental lift.

The logic is simple:

- before campaign: actual treatment and synthetic control should look similar
- after campaign: any clear divergence may indicate treatment impact

---

## 3. Why This Helps Compared to Simple DiD

DiD often compares treatment geos against the average control group.

That can be weak if:
- some control geos are very different from treatment geos
- treatment geos have different baseline demand
- markets vary in maturity
- historical trends differ across regions

Synthetic control improves this by giving more weight to the control geos that best resemble the treatment group before the campaign.

In other words:

> DiD assumes the control group is a reasonable counterfactual.  
> Synthetic control tries to build a better one.

---

## 4. Marketing Example

A company launches YouTube advertising in selected regions.

Treatment geos:
- London
- Manchester
- Bristol

Control geos:
- Birmingham
- Leeds
- Liverpool
- Glasgow
- Cardiff
- Sheffield

A simple DiD might compare treatment geos against the average of all control geos.

Synthetic control instead asks:

> Which weighted combination of control geos best matches the treatment geos before YouTube launched?

For example:
- 35% Birmingham
- 25% Leeds
- 20% Glasgow
- 20% Cardiff

If this synthetic control closely matches treatment performance during the pre-period, it becomes a stronger basis for estimating lift.

---

## 5. Key Difference: DiD vs Synthetic Control

| Method | Counterfactual | Strength | Main Risk |
|---|---|---|---|
| DiD | Average control group trend | Simple and explainable | Weak if controls are poorly matched |
| Synthetic Control | Weighted control group matched to treatment pre-period | Stronger tailored counterfactual | Misleading if pre-period fit is poor |

DiD is often easier to explain.

Synthetic control is often more convincing when the pre-period match is strong.

---

## 6. The Most Important Diagnostic: Pre-Period Fit

Synthetic control is only credible if it closely matches treatment geos before the campaign.

A good pre-period fit means:
- actual treatment and synthetic control move similarly before treatment
- baseline gaps are small or stable
- no obvious divergence exists before the campaign starts

A poor pre-period fit means:
- the synthetic control does not represent a credible counterfactual
- post-period lift estimates should not be trusted

This is the most important rule:

> If the synthetic control cannot explain the past, do not trust it to estimate the counterfactual future.

---

## 7. What Good Looks Like

A good synthetic control analysis should show:

1. Strong pre-period fit  
   Treatment and synthetic control move closely together before the campaign.

2. Clear post-period divergence  
   A gap appears after treatment begins.

3. Reasonable weights  
   The counterfactual is not driven by one strange or irrelevant control geo.

4. Placebo checks  
   Other untreated regions should not show similar “effects” when treated as fake treatment geos.

5. Business plausibility  
   The estimated lift should make sense given spend, market size, and historical performance.

---

## 8. When Synthetic Control Is Useful

Synthetic control is especially useful when:

- there are few treatment geos
- not all control geos are equally comparable
- treatment regions have unique baseline patterns
- pre-period data is rich enough to match trends
- leadership needs a more credible counterfactual than a simple average control group

Common marketing use cases:
- YouTube geo lift
- TV campaigns
- brand campaigns
- market launches
- regional paid media tests
- pricing or promotion changes

---

## 9. When Synthetic Control Is Not Enough

Synthetic control is not always the right answer.

It may fail when:
- no combination of control geos matches the treatment group
- pre-period data is too short
- there are strong spillovers between regions
- treatment affects the entire market
- external shocks hit treatment regions differently

In these cases, synthetic control may look sophisticated but still produce weak evidence.

---

## 10. Cross-Method Insight

Synthetic control should not replace DiD automatically.

A strong measurement workflow often compares both:

- DiD gives a simple benchmark
- synthetic control gives a tailored counterfactual
- placebo tests challenge the credibility of the result
- MMM can later use experimental estimates for calibration

If DiD and synthetic control point in the same direction, confidence increases.

If they disagree, the analyst should investigate:
- pre-period fit
- geo selection
- spillovers
- external shocks
- data quality

---

## 11. Strong Opinion

Synthetic control is not better because it is more advanced.

It is better only when it creates a more credible counterfactual.

A poorly matched synthetic control is worse than a simple, transparent DiD because it can create false confidence.

The method should earn trust through diagnostics, not complexity.

---

## 12. Key Takeaway

Synthetic control is a method for building a stronger counterfactual in geo lift measurement.

Its credibility depends on one central question:

> Did the synthetic control behave like the treatment group before the campaign?

If yes, post-treatment gaps may provide useful evidence of incremental impact.

If no, the result should not drive business decisions.
