# Week 3: Geo Lift and Difference-in-Differences (DiD)

## 1. Why Before vs After Comparisons Fail

One of the most common mistakes in marketing measurement is comparing performance before and after a campaign launch.

Example:

* revenue before campaign = £100k
* revenue after campaign = £120k

Naïve conclusion:

* campaign generated +£20k incremental revenue

This conclusion is unreliable because many other factors may have changed simultaneously:

* seasonality
* macroeconomic demand
* competitor activity
* pricing changes
* product launches
* broader market growth

Without a control group:

> growing businesses often end up attributing natural growth to marketing activity.

A simple before/after comparison measures change.
It does not measure causality.

---

## 2. The Core Idea of Difference-in-Differences

Difference-in-Differences (DiD) improves causal estimation by comparing:

* the change over time in the treatment group
  vs
* the change over time in the control group

Instead of asking:

* “Did revenue increase?”

DiD asks:

> “Did the treatment group improve more than it would likely have without the intervention?”

The control group acts as an estimate of the missing counterfactual.

This allows us to separate:

* campaign impact
  from
* broader market movement.

---

## 3. Basic Structure

### Treatment Group

Regions/users/accounts exposed to the intervention.

### Control Group

Comparable units not exposed to the intervention.

### Two Time Periods

* Before treatment
* After treatment

The objective is not simply to compare groups.
It is to compare:

> changes in outcomes across groups over time.

---

## 4. Intuition Example

### Before Campaign

| Group     | Revenue |
| --------- | ------- |
| Treatment | 100     |
| Control   | 100     |

### After Campaign

| Group     | Revenue |
| --------- | ------- |
| Treatment | 130     |
| Control   | 110     |

---

### Naïve Interpretation

Treatment increased:
130 - 100 = +30

Therefore:

> campaign caused +30 lift

This is incorrect because:

* the control group also improved

---

### DiD Interpretation

Control increased:
110 - 100 = +10

Estimated incremental lift:

(130 - 100) - (110 - 100) = +20

The control group estimates:

> what would likely have happened even without treatment.

---

## 5. Why DiD Works

DiD works because it removes effects shared across treatment and control groups.

Examples:

* seasonality
* overall demand growth
* macroeconomic trends

This allows the remaining difference to be interpreted as incremental lift.

However, this only works under an important assumption:

> treatment and control would have followed similar trends without intervention.

This is called:

### The Parallel Trends Assumption

---

## 6. Parallel Trends (Most Important Assumption)

Before treatment:

* treatment and control groups should behave similarly over time

If trends already differ before the experiment:

* causal interpretation becomes unreliable

Example:

* treatment regions already growing faster than control regions before campaign launch

In this case:

* post-treatment lift may simply reflect pre-existing momentum

Good DiD analysis should always:

* visualize pre-treatment trends
* validate comparability before estimating lift

---

## 7. Marketing Example — Geo Lift Test

### Scenario

A company launches YouTube advertising in selected regions.

### Goal

Measure incremental impact on revenue.

### Setup

* Treatment geos → ads ON
* Control geos → ads OFF

### Results

| Group     | Before | After |
| --------- | ------ | ----- |
| Treatment | 100    | 140   |
| Control   | 100    | 115   |

---

### Interpretation

Treatment growth:
140 - 100 = +40

Control growth:
115 - 100 = +15

Estimated incremental lift:
+25

The control group helps isolate:

* true campaign impact
  from
* natural business growth.

---

## 8. Why DiD Is Valuable in Marketing

DiD is especially useful when:

* user-level experimentation is difficult
* campaigns operate regionally
* privacy limits tracking
* platforms restrict visibility into user-level exposure

Common use cases:

* geo lift tests
* retail measurement
* TV campaigns
* YouTube and brand advertising
* B2B regional experiments

---

## 9. Real-World Risks

Even well-designed DiD experiments can fail in practice.

Common risks include:

* treatment and control regions are fundamentally different
* competitor campaigns launch during the experiment
* pricing or promotions change mid-test
* economic shocks affect regions unevenly
* spillovers occur across geographies

This is why:

> experimental design quality matters as much as statistical analysis.

---

## 10. Strategic Insight

DiD is often more useful for:

* directional business decision-making
  than:
* producing perfectly precise causal estimates.

In real-world marketing:

* uncertainty is unavoidable
* the goal is credible decision support, not mathematical perfection.

---

## 11. Strong Opinion

Many teams apply DiD mechanically because the regression output looks scientific.

However:

> a sophisticated model applied to a weak comparison group still produces unreliable conclusions.

Causal credibility depends more on:

* comparison quality
  than:
* model complexity.

---

## 12. Practical Business Tension

Leadership teams often prefer simple before/after reporting because:

* results are easier to communicate
* growth stories look stronger
* attribution dashboards appear more certain

However:

* certainty without a credible counterfactual can lead to systematically poor budget allocation.

---

## 13. Key Takeaway

Difference-in-Differences estimates causal impact by comparing:

* changes over time
  across:
* treatment and control groups.

The goal is not simply to observe performance changes.

It is to estimate:

> how much additional impact was caused by the intervention beyond what would have happened naturally.
