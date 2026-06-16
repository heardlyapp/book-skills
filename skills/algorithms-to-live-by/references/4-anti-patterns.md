# 4. Anti-Patterns — When Algorithms Fail

> Source: "Algorithms to Live By" by Brian Christian and Tom Griffiths (2016), Chapters 6 (Bayes's Rule), 7 (Overfitting), and 8 (Relaxation).

## Mistake 1: Overthinking When Data Is Scarce

**What it looks like**: Spending hours analyzing a decision with very little information. Comparing 10 restaurants on Yelp when you've only been to 2 of them.

**Why it fails**: Complex models require exponentially more data to be accurate. When data is scarce, simple heuristics outperform complex analysis. The more elaborate your decision framework, the more information you need to fill it — and you don't have that information.

> **Case: Stock-Picking vs. Index Funds** (Chapter 7): The vast majority of actively managed mutual funds underperform the market over 10+ years. Stock-picking is a classic overfitting problem: analysts build complex models to explain past performance, but these models don't generalize to the future. The simple heuristic (buy an index fund) consistently outperforms complex analysis. As the book puts it: "The best advice is simple ('sleep more, exercise, eat well') not complex 12-step programs."
> **Key takeaway**: When you have limited data, don't build a cathedral. Build a hut. Simple rules that ignore nuance often outperform models that try to capture everything.

> **Case: Wine Tasting and Expert Ratings** (Chapter 7): Expert wine ratings are notoriously inconsistent — the same wine scored differently by the same expert on different days. The simplest heuristic — "expensive wine is better" — roughly predicts enjoyment as well as expert analysis. Overfitting in wine: trying to detect notes of "elderberry with a hint of saddle leather" from a $12 bottle is using a complex model where a simple one (enjoyable or not) suffices.
> **Key takeaway**: The complexity of your decision framework should match the richness of your data. Thin data + thick model = bad decisions.

## Mistake 2: Ignoring Base Rates

**What it looks like**: Concluding you have a rare disease because a test came back positive, ignoring that the false positive rate exceeds the disease prevalence.

**Why it fails**: Bayes's Rule says your posterior belief depends on both the evidence AND your prior. People systematically ignore priors and over-weight new evidence.

> **Case: Bayesian Search for Flight MH370** (Chapter 6): When Malaysia Airlines Flight 370 disappeared in 2014, the search used Bayesian methods. They started with prior probabilities (ocean currents, satellite data, flight trajectory), then updated with each failed search. When a search area turned up nothing, that area's probability was lowered and others increased. This systematic approach eventually found wreckage.
> **Key takeaway**: Your starting assumptions (priors) matter enormously. If you start with bad priors, even good evidence won't save you. Update systematically, not emotionally.

## Mistake 3: Trying to Solve Intractable Problems Exactly

**What it looks like**: Spending weeks trying to plan the "perfect" vacation itinerary, career path, or business strategy.

**Why it fails**: Many problems are computationally intractable (NP-hard). The Traveling Salesman Problem — finding the shortest route visiting n cities — gets exponentially harder with each additional city. The optimal solution requires checking n! possibilities.

> **Case: The Traveling Salesman Problem** (Chapter 8): TSP is the canonical example of a problem that can't be solved optimally at scale. But "relaxation" — removing a constraint — transforms it. By allowing routes that revisit cities, you get a minimum spanning tree: a provably good approximation that's computable in linear time. In life: when you can't find the perfect plan, relax one assumption. Can't plan the perfect career? Relax the assumption that you know your final destination.
> **Key takeaway**: Perfection is the enemy of good-enough. If a problem resists solution, remove a constraint. The relaxed version might not be perfect, but it's solvable — and often good enough to act on.

## Mistake 4: Playing Deterministically When Randomness is Optimal

**What it looks like**: Always choosing the same option, always using the same strategy, always being predictable.

**Why it fails**: Predictability is exploitable. In any competitive situation, a deterministic pattern can be studied and countered.

> **Case: Penalty Kicks in Soccer** (Chapter 9): Statistical analysis shows 94% of penalty kick goals go in the top corners. Yet 90% of kicks go to the goalkeeper's natural side. Players avoid randomizing because it feels "out of control." But game theory proves that randomizing (even occasionally kicking center, which has lower success rate) improves overall conversion because it makes you unpredictable.
> **Key takeaway**: Randomness is a strategic tool, not a surrender of control. When your opponent can study your patterns, determinism is a liability.
