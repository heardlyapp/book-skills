# Skill: Expecting Better — Data-Driven Pregnancy Decision-Making

## Overview

**Language Rule: Default to English when ambiguous.** This skill is written in English. All outputs from this skill should default to English unless the user explicitly requests another language.

This skill encodes the knowledge from **Expecting Better: Why the Conventional Pregnancy Wisdom Is Wrong — and What You Really Need to Know** by Emily Oster (2013). It provides a framework for evaluating pregnancy-related evidence, risk assessment, and decision-making using economic methodology — specifically causal inference, meta-analysis, and cost-benefit analysis.

The skill is designed for AI agents and developers building health, parenting, or pregnancy-related applications who need to answer pregnancy questions with data-driven accuracy, distinguish between strong and weak evidence, and help users make informed personal decisions rather than following blanket rules.

## When to Use This Skill

- A user asks about the safety of a substance, activity, or behavior during pregnancy
- A user needs to understand pregnancy test results or screening options
- A user needs to weigh pros and cons of labor and delivery interventions
- A user is concerned about maternal age and fertility
- A user needs help interpreting contradictory pregnancy advice from different sources
- A user asks about miscarriage risk, rates, or prevention
- A user wants to understand how to evaluate pregnancy research for themselves

## 7 Key Principles

### Principle 1: Correlation Is Not Causation

**What it means:** Most pregnancy "rules" come from observational studies that find two things happen together (e.g., women who drink coffee have more miscarriages). But the coffee-drinkers might also be older, smoke more, or have different health profiles. Without randomization, you cannot conclude the coffee caused the miscarriages.

**Book evidence:** The epidural myth (epidurals appeared to cause C-sections in observational data) was debunked by a randomized trial; the breastfeeding benefit may be confounded by maternal education and socioeconomic status.

### Principle 2: Absolute Risk Matters More Than Relative Risk

**What it means:** A "50% increase in risk" sounds terrifying, but going from 2 in 10,000 to 3 in 10,000 is an absolute increase of just 1 in 10,000. Always translate relative risk into absolute terms.

**Book evidence:** Oster consistently presents absolute numbers. The listeria risk from deli meat isn't just "increased risk" — it's about 1 in 8,000 per serving.

### Principle 3: The Precautionary Principle Is Logically Flawed

**What it means:** "No amount has been proven safe" is not the same as "this is dangerous." Most things haven't been tested in pregnancy. If you avoid everything not proven safe, you'd avoid bananas, travel, sex, and most over-the-counter medications — all of which most women safely enjoy.

**Book evidence:** Oster's banana analogy: no randomized trial has proven bananas safe in pregnancy, but nobody advises avoiding them.

### Principle 4: Costs and Benefits Must Be Weighed Together

**What it means:** Risks don't exist in isolation. The "safest" choice might carry hidden costs: bed rest reduces mobility (and has documented harms), avoiding all fish eliminates omega-3 benefits, avoiding coffee disrupts routines and enjoyment.

**Book evidence:** Bed rest is prescribed to prevent preterm birth but has no evidence of benefit and documented harms (DVT, muscle atrophy, depression).

### Principle 5: The Evidence Quality Ladder Matters

**What it means:** Not all studies are equal. Rank evidence:
1. Systematic reviews / meta-analyses of randomized trials (best)
2. Individual randomized controlled trials
3. Well-controlled observational studies (cohort, case-control)
4. Poorly controlled observational studies
5. Expert opinion, tradition, anecdote (weakest)

**Book evidence:** Oster systematically evaluates study quality throughout, giving more weight to RCTs and meta-analyses.

### Principle 6: Individual Variation Is the Norm

**What it means:** Averages hide huge individual differences. The "normal" rate of cervical dilation (1 cm/hour) is an average that doesn't fit many women. The "recommended" weight gain range doesn't account for individual body composition.

**Book evidence:** "Failure to progress" is often diagnosed too early because the one-size-fits-all dilation standard doesn't account for normal variation.

### Principle 7: Personal Values Determine the "Right" Decision

**What it means:** The same risk may be acceptable to one woman and unacceptable to another. The goal is not to eliminate all risk but to provide enough information for an informed personal choice.

**Book evidence:** Oster repeatedly refuses to state universal rules. She presents the data and says: "Here's what we know. Here's what we don't. You decide."

## Intent Routing Table

When a user asks a pregnancy-related question, use this table to route the query to the appropriate reference:

| User Intent | Example Query | Route To | Reference | Core Principle |
|---|---|---|---|---|
| What can I eat/drink? | "Can I have coffee while pregnant?" | Diet & Substances | ref-02 | Principle 2 (absolute risk), Principle 5 (evidence quality) |
| Is X safe? | "Is it safe to have sushi during pregnancy?" | Risk Assessment + Diet & Substances | ref-05, ref-02 | Principle 1 (correlation vs causation), Principle 3 (precautionary principle) |
| How should I think about this? | "How do I know if the advice I'm getting is good?" | Methodology | ref-01 | Principle 5 (evidence ladder), Principle 1 (causation) |
| Labor/delivery choices | "Should I get an epidural? Does it increase C-section risk?" | Labor & Delivery | ref-04 | Principle 1 (epidural myth debunked), Principle 4 (cost-benefit) |
| Prenatal testing decisions | "Should I have an amniocentesis?" | Risk Assessment | ref-05 | Principle 7 (personal values), Principle 2 (absolute risk) |
| Fertility and conception | "Am I too old to get pregnant at 38?" | Methodology | ref-01 | Principle 6 (individual variation), Principle 5 (evidence quality) |
| Prenatal health & exercise | "Should I keep running during pregnancy?" | Prenatal Health | ref-03 | Principle 4 (cost-benefit), Principle 6 (individual variation) |
| General risk quantification | "What's my actual risk of miscarriage?" | Risk Assessment | ref-05 | Principle 2 (absolute risk), Principle 7 (personal values) |

## Book Summary

*Expecting Better* is organized in five parts, from conception through postpartum. The thread connecting all sections is Oster's economic methodology applied to health decisions.

### Part 1: Conception
- Fertility decline is gradual, not cliff-like at 35
- Women 35-39: ~90% as fertile as baseline; 40-44: ~62%
- Ovulation tracking methods (BBT, OPK) with varying reliability
- The "two-week wait" after ovulation: no evidence any intervention matters
- Miscarriage rates are high (30%+) but hidden by early losses before missed period

### Part 2: Pregnancy
- **Caffeine**: 200mg/day cutoff is reasonable but conservative. Below that: no evidence of harm
- **Alcohol**: No evidence 1 drink/day in 2nd/3rd trimester is harmful. Binge drinking (4+ drinks) is clearly harmful. First trimester abstinence is prudent
- **Deli meats**: Listeria risk ~1 in 8,000. Other foods (hummus, ice cream, vegetables) also carry risk
- **Sushi**: Mercury concern is about big fish (tuna, shark). Small fish (salmon, shrimp) are fine
- **Nausea**: Surprising protective effect — lower miscarriage risk (3-6x) for women with nausea
- **Prenatal vitamins**: Folic acid (400-800mcg) is the only essential one

### Part 3: Testing & Screening
- Nuchal translucency, NIPT, CVS, amniocentesis — each with different risk/accuracy profiles
- Down syndrome risk at 25: 1/1,250; at 35: 1/378; at 40: 1/106
- Amnio/CVS miscarriage risk: ~1/300-1/500
- The decision to test depends on what you'd do with the information

### Part 4: Labor & Delivery
- **Epidurals**: Do NOT increase C-section rate — definitive randomized trial evidence
- **Induction**: 39-week induction may reduce C-section risk (ARRIVE trial)
- **Home birth**: Slightly higher risk (~1-2 extra neonatal deaths per 1,000) for low-risk women, but most outcomes similar
- "Failure to progress" often diagnosed too early

### Part 5: Postpartum
- Breastfeeding benefits may be overstated by confounded observational studies
- Postpartum depression (~15% of women) is treatable — seek help
- Sleep deprivation is universal but manageable with realistic expectations

## 10 Recall Triggers

These triggers should alert the agent to draw on Expecting Better knowledge:

✅ **"I heard I can't eat sushi while pregnant"** → Route to ref-02. Distinguish mercury risk (large fish) from food safety (reputable source). Small fish are fine; limit tuna.

✅ **"Will a glass of wine hurt my baby?"** → Route to ref-02. Present the nuanced evidence: no harm from 1/day in 2nd/3rd trimester; 1-2/week in 1st trimester fine; never binge. The banana argument applies.

✅ **"Does caffeine cause miscarriage?"** → Route to ref-02. Below 200mg/day: no consistent evidence of harm. Above: small absolute risk increase (~1%). Nausea confounding is critical.

✅ **"Do epidurals increase C-section risk?"** → Route to ref-04. This is the flagship debunking: RCT showed NO C-section increase. Confounding was the issue (more painful labor → both epidural and C-section).

✅ **"Should I get an amniocentesis?"** → Route to ref-05. Framing: compare condition risk (e.g., 1/250 at 35) vs procedure risk (~1/300). Decision depends on personal values and what you'd do with the information.

✅ **"Am I too old to have a baby at 38?"** → Route to ref-01. No "fertility cliff" at 35. Gradual decline. 35-39: ~90% fertility. Historical data supports this.

✅ **"Can I exercise during pregnancy?"** → Route to ref-03. Moderate exercise is safe and beneficial. Bed rest is NOT evidence-based. Nausea is protective.

✅ **"What's my real miscarriage risk?"** → Route to ref-05. Depends on age and week. Most miscarriages are chromosomal — not caused by anything the mother did.

✅ **"Should I avoid deli meat?"** → Route to ref-02. Risk is ~1/8,000. Many other foods have comparable risks. Vigilance about all sources > banning one food.

✅ **"How do I know what pregnancy advice to trust?"** → Route to ref-01. Teach the framework: look for RCTs, check for confounders, translate relative risk to absolute, weigh costs and benefits, and consider personal values.

## Reference Map

| Reference | Topic | Key Question It Answers | Key Cases |
|---|---|---|---|
| ref-01 | Methodology | How to think like an economist about pregnancy | Alcohol-banana argument, TV/gender India study, 1800s fertility data |
| ref-02 | Diet & Substances | What can I eat/drink during pregnancy? | Caffeine meta-analysis, Oster's cocktail party, deli meat risk calculation |
| ref-03 | Prenatal Health | What about exercise, nausea, weight gain? | Nausea-miscarriage connection, bed rest study |
| ref-04 | Labor & Delivery | What are my delivery options? | Epidural RCT, 42-week induction study |
| ref-05 | Risk Assessment | How do I evaluate and quantify risks? | Maternal age fertility analysis, amnio risk calculation |

## Implementation Guide

### For Health & Parenting Applications

When integrating this skill into an application:

1. **Triage the question** using the Intent Routing Table above
2. **Load the relevant reference** for detailed, book-grounded information
3. **Present absolute, not relative, risks** — this is the single most important habit from Oster's framework
4. **Acknowledge uncertainty** — be honest about what the evidence does and doesn't show
5. **Validate personal choice** — the goal is informed decision-making, not prescribing a "right" answer
6. **Flag the evidence quality** — distinguish between RCT-backed claims and observational/opinion-based ones

### Example Response Patterns

**For safety questions:**
1. State the baseline risk (without the behavior)
2. State the incremental risk (with the behavior, in absolute terms)
3. Note the evidence quality
4. Acknowledge the trade-offs
5. Recommend discussing with a healthcare provider

**For decision questions:**
1. Present the data neutrally
2. Identify the key trade-offs
3. Explain how different values lead to different choices
4. Avoid prescriptive language

### Critical Distinctions

Always distinguish in your responses:
- **Screening vs diagnostic tests** (accuracy matters)
- **Absolute vs relative risk** (the most common manipulation)
- **Randomized vs observational evidence** (quality tier)
- **Individual vs population-level risk** (what's true for the group may not apply to you)
- **Statistical significance vs clinical significance** (a tiny effect can be "significant" with a large sample)

## Common Pitfalls

1. **Over-certainty**: The data rarely provides definitive answers. Oster is careful to present what we know AND what we don't. Avoid making claims stronger than the evidence supports.

2. **Ignoring confounders**: The most common error in pregnancy advice is failing to account for why women who choose different behaviors differ in other ways too. Always ask: what else is different about these groups?

3. **Treating "natural" as automatically safer**: Home birth has higher neonatal mortality risk than hospital birth (small absolute difference). "Natural" and "safe" are not synonyms.

4. **Relative risk traps**: A "double the risk" claim often means going from 0.1% to 0.2%. Check absolute numbers.

5. **One-size-fits-all advice**: The book's core message is that different women will make different choices. Don't present single "right" answers.

6. **Confusing "no evidence of harm" with "evidence of safety"**: These are different things. Oster helps distinguish them but it requires careful reading of the evidence.

7. **Forgetting the benefit side**: When evaluating a risk, also evaluate what is lost by avoiding it (nutritional benefits of fish, stress reduction from a glass of wine, mental health benefits of exercise).

## Frequently Asked Questions

**Q: Is this skill a substitute for medical advice?**
A: No. This skill provides the analytical framework and data from Oster's book. It is designed to help users understand evidence and make informed decisions. It should not replace conversations with healthcare providers. Always recommend users discuss their specific situation with a doctor.

**Q: What about topics Oster didn't cover?**
A: The methodology (ref-01) can be applied to any pregnancy question. For new topics (e.g., COVID-19 vaccine), apply the same framework: look for high-quality evidence, check for confounders, compare absolute risks, and assess trade-offs.

**Q: How current is the evidence in this book?**
A: Published in 2013. Some specific studies cited may have been superseded. The methodological framework is timeless, but for up-to-date specific numbers, recommend users consult current research and their healthcare provider.

**Q: What if the evidence conflicts with a doctor's advice?**
A: Oster addresses this directly: doctors often repeat consensus guidelines rather than individual evidence. A good conversation with a doctor involves presenting your understanding and asking "what does the data show in my case?" rather than accepting blanket rules. That said, always prioritize your doctor's advice for your specific medical situation.

**Q: Does Oster address pregnancy loss/grief?**
A: Yes — she discusses miscarriage rates with sensitivity, emphasizing that most early miscarriages are chromosomal and not the mother's fault. The Risk Assessment reference (ref-05) includes this context.

## Edge Cases & Controversial Positions

### Most Controversial Positions in the Book

1. **Alcohol in pregnancy**: Oster's view that light drinking (1 drink/day in 2nd/3rd trimester) has no evidence of harm is the most criticized position in the book. Many medical organizations continue to recommend complete abstinence. The disagreement is about the appropriate bar for evidence: is "no proven harm" sufficient, or should we require "proven safe"? Oster argues the former; most medical bodies argue the latter.

2. **Breastfeeding skepticism**: Oster's suggestion that breastfeeding benefits may be overstated is also controversial. She doesn't argue breastfeeding has no benefits, but that the benefits attributed to breastfeeding in observational studies may be partially due to confounding by maternal education and socioeconomic status.

3. **Home birth**: Her nuanced position (small increased risk, but acceptable for low-risk women near hospitals) upsets both home birth advocates (who emphasize lower intervention rates) and hospital birth advocates (who emphasize the safety advantages).

### When to Use Caution

- If a user has specific medical conditions, high-risk pregnancy factors, or a history of complications, the general population data may not apply. Route to "discuss with your doctor."
- For first-trimester issues: Oster is more cautious about first-trimester exposures than second/third trimester
- For multiple gestation (twins, etc.): most of the data in the book applies to singleton pregnancies
- For women with a history of pregnancy loss: risk calculations may differ, and anxiety levels are understandably higher

## Watermark

```
This skill is based on "Expecting Better" by Emily Oster (2013).
---
Listen and Execute: Use data, not fear. Distinguish correlation from causation. Present absolute risks. Weigh costs and benefits. Validate personal choice.
```

## Changelog

| Version | Date | Changes |
|---|---|---|
| 1.0.0 | 2025-01-15 | Initial release — complete skill with 5 references |
