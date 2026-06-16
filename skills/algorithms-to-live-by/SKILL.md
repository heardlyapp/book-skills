---
name: algorithms-to-live-by
title: "Algorithms to Live By: The Computer Science of Human Decisions"
description: >-
  A skill based on Brian Christian and Tom Griffiths' book that applies computer science algorithms
  to everyday human decisions—from optimal stopping in dating to caching in memory management,
  from explore/exploit tradeoffs in life choices to scheduling theory in time management.
author: heardlyapp
version: 1.0.0
tags:
  - decision-making
  - computer-science
  - cognitive-science
  - optimal-stopping
  - explore-exploit
  - sorting
  - scheduling
  - game-theory
  - probability
language: "Default to English when ambiguous"
---

# Algorithms to Live By

## Overview

This skill distills the core algorithms from Brian Christian and Tom Griffiths' book into actionable decision-making frameworks. The book's central thesis: human life is full of computationally hard problems—finite space, finite time, limited attention, incomplete information, and an unforeseeable future—and computer science has already solved many of their equivalents. By borrowing algorithms designed for machines, we can make better decisions in love, work, money, and everyday life.

**What this skill is good for:**
- Deciding when to stop searching (relationships, apartments, parking)
- Balancing novelty vs. familiarity (restaurants, music, career moves)
- Organizing physical and digital space efficiently
- Managing time and attention under constraints
- Handling uncertainty with Bayesian reasoning
- Avoiding overthinking and overcomplication
- Understanding when randomness helps
- Navigating social and competitive situations

---

## Key Principles

1. **Optimal Stopping — The 37% Rule**: When facing a sequential search with no recall (dating, hiring, apartment hunting), spend the first 37% of your time exploring options without committing, then leap at the first option that beats everything you've seen. This maximizes your chance of picking the best.

2. **Explore/Exploit — The Gittins Index**: The value of trying something unknown is systematically higher than its expected value would suggest, because exploration has future payoffs. The Gittins Index mathematically quantifies when to explore vs. exploit based on track record and remaining time horizon.

3. **Sorting — Scale Hurts, Buckets Help**: The time required to sort grows faster-than-linearly with size. For physical sorting, use Bucket Sort (group items by rough category) first, then sort within small groups. For digital information, sorting is often overrated—search is usually faster.

4. **Caching — Forget Proactively**: Memory (computer or human) is a limited resource best managed by the Least Recently Used (LRU) principle: the items you'll need next are the ones you've used most recently. Prioritize what to keep by recency of use, not by sentiment or potential future need.

5. **Scheduling — Relay, Don't Multitask**: Task switching has overhead. Process batches in a fixed order (like a CPU: shortest processing time first for responsiveness, then round-robin for fairness). Never multitask cognitively demanding work; do one thing to completion before switching.

6. **Overfitting — Think Less When Data is Scarce**: The more complex a model, the more data it needs to be accurate. When information is sparse, simpler rules (heuristics) outperform complex analysis. This is why experts with limited data should trust their gut and why overthinking leads to worse decisions.

7. **Relaxation & Randomness — Let Constraints Go, Toss a Coin**: When a problem is computationally intractable, relax some constraints to find a good-enough solution. When indecisive between equally good options, randomization breaks symmetry and avoids regret. As the book says: "Forgive, but don't forget. To thine own self be true."

---

## Core Algorithms & Applications

### 1. Optimal Stopping (The Secretary Problem)

**The Algorithm**: Look at the first 37% of applicants, choosing none. Then hire the next applicant who beats the best you've seen so far.

**Key Variants:**
- **Full Information (Threshold Rule)**: When you know the score distribution, use a dynamic threshold based on how many options remain. Last option: take anyone above 50%. Second-to-last: above 69%. Third-to-last: above 78%. Etc.
- **With Rejection**: If rejection is possible, start proposing after just 25% of your search.
- **With Recall**: Spend 61% looking noncommittally, then leap during the remaining 39%. If still single, go back to the best you passed up.
- **Burglar Problem**: Number of risks to take ≈ success probability / failure probability. If 90% success rate, retire after 9 jobs.
- **House Selling**: Set a threshold before listing based on the cost of waiting. Never lower it unless the deadline forces you.

**Real Cases:**
- Michael Trick (CMU) applied the 37% Rule to dating at age 26, proposed to his girlfriend at the time—she turned him down. But the variant allowing rejection gave him a strategy, and he found love later.
- Johannes Kepler courted 11 women after his first wife died. He kept returning in his mind to candidate #5, eventually marrying her—a real-world example of optimal stopping with recall (61% rule).
- Russian oligarch Boris Berezovsky literally wrote the book on optimal stopping (the only full-length book on the secretary problem), but failed to apply it to his own life—he didn't stop while ahead and died in exile.

### 2. Explore/Exploit (Multi-Armed Bandit)

**The Algorithm**: Assign a Gittins Index to each option based on its track record and remaining lifespan. Always pick the option with the highest index.

**Table Interpretation (90% discount)**:
- A 0-0 unknown: index = 0.7029 (worth a guaranteed 70% success rate!)
- A 9-6 machine: index = 0.6300
- A 1-1 machine: index = 0.6346 → explore this over 9-6
- A 9-1 machine (10 trials): index = 0.8695

**Key Insights:**
- The unknown has inherent value: a brand-new option (0-0) is worth more than a machine you know pays out 70%.
- Your time horizon changes everything: explore when you have time to use what you learn; exploit when the end is near.
- "Carpe diem" and "life is long" require opposite strategies.

**Real Cases:**
- Scott Plagenhoef (Pitchfork editor) had to force himself to only listen to new music by putting only new albums on his iPod—pure exploration mode.
- Hollywood's sequel obsession signals a short time horizon: studios think the movie industry is in decline, so they exploit known brands instead of exploring new IP.
- The Unilever drug trial problem directly led to Gittins' discovery of the index.

### 3. Sorting

**Key Insight**: Scale hurts—sorting 100 items takes more than 2x the time of sorting 50 items.

**Algorithm Hierarchy**:
| Method | Big-O | Best Use |
|--------|-------|----------|
| Bubble Sort | O(n²) | Never use intentionally |
| Insertion Sort | O(n²) | Small piles (≤ 25 items) |
| Mergesort | O(n log n) | Large datasets, parallel workers |
| Bucket Sort | O(n) | When you know the distribution |
| Comparison Counting | O(n²) | Most robust against noise |

**Real Cases:**
- Danny Hillis (supercomputer pioneer) was horrified by his roommate who matched socks by random pull—taking 110 pulls for 20 socks. A better approach: do laundry more often to reduce batch size.
- The King County Library System's Preston Sort Center sorts 85,000 books/day in linear time using Bucket Sort (destination branch bins).
- UC Berkeley student Jordan Ho sorts 150 library books in <40 minutes using Bucket Sort: first rough-sort by call number range based on experience, then Insertion Sort within each bucket.
- March Madness is a Single Elimination Mergesort: it finds the champion in linear time but gives no information about second place (which Dodgson/Lewis Carroll mathematically proved is "entirely unmeaning").
- Dean Oliver, pioneer of basketball analytics, showed that using big-O thinking reveals how basketball has "noise" issues similar to sorting with a faulty comparator.

### 4. Caching & Memory

**Key Insight**: Forgetting is as important as remembering. The optimal memory strategy is LRU (Least Recently Used).

**Applications:**
- **Closets**: Store frequently-used items at eye level. Store rarely-used items in hard-to-reach places. Get rid of items you haven't used in the last year.
- **Email**: Don't file emails into folders. Search instead. Studies by Steve Whittaker show that email organizing is a waste of time—the search cost is lower than the sorting cost.
- **Human Memory**: The "recency effect" in psychology (remembering the last item best) exactly mirrors LRU cache eviction. Forgetting old memories is a feature, not a bug.

### 5. Scheduling

**Key Insight**: Throughput vs. responsiveness is the fundamental tradeoff.

**Rules:**
- **Shortest Processing Time (SPT)**: Do quick tasks first to minimize average wait time.
- **Earliest Due Date (EDD)**: Meet deadlines by prioritizing time-sensitive work.
- **Round-Robin**: Give each task a fixed time slice—ensures fairness but adds switching overhead.
- **Never multitask**: Context switching cost is real and measurable. Batch similar cognitive tasks.

**Real Cases:**
- Intel's Andy Grove used "SLAC" (Specific, Limited, Action-oriented, Continuous) time management—essentially scheduling theory applied to executive life.
- The airplane cockpit "sterile cockpit" rule (no non-essential conversation below 10,000 feet) is a scheduling protocol: eliminate interruptions during critical phases.

### 6. Bayes's Rule

**Key Insight**: Update beliefs proportionally to the likelihood of new evidence.

**Heuristic**: Start with a prior belief. When you see new data, adjust your belief. The amount of adjustment depends on how surprising the data is.

**Real Cases:**
- Bayesian search for the missing Flight MH370 used prior probabilities from ocean currents and satellite data, updated with each failed search.
- The "base rate fallacy" (ignoring how rare something is) is Bayes's Rule violated—e.g., thinking you have a rare disease because a test came back positive, ignoring that the false positive rate is higher than the disease prevalence.

### 7. Overfitting

**Key Insight**: Complex models require exponentially more data. When data is limited, simplicity wins.

**Applications:**
- **Investing**: Stock-picking overfits to recent history. Index funds (simple model) outperform most active managers over 10+ years.
- **Wine tasting**: Expert ratings are inconsistent. Simple rules (expensive = good) often beat expert analysis.
- **Self-help**: The best advice is simple ("sleep more, exercise, eat well") not complex 12-step programs.
- **Machine Learning**: "Regularization" penalizes complexity—a direct lesson for human decision-making.

### 8. Relaxation

**Key Insight**: When a problem is too hard to solve exactly, remove constraints to find a good enough solution.

**Classic Example**: The Traveling Salesman Problem (TSP) is NP-hard. But by "relaxing" the constraint that you must visit each city exactly once, you get a minimum spanning tree—a good lower bound that helps find near-optimal routes. In life: when a perfect plan is impossible, relax one assumption.

### 9. Randomness

**Key Insight**: Randomness breaks symmetry, forces exploration, and prevents exploitation by adversaries.

**Applications:**
- **Tossing a coin**: When two options seem equally good, randomization prevents regret (you'll never wonder "what if I chose the other one?").
- **Penalty kicks in soccer**: 94% of goals are scored in the top corners, yet 90% of kicks go to the natural side. Goalkeepers should randomize their dive direction.
- **Password security**: Randomness is the key to unbreakable encryption—no pattern for attackers to exploit.

### 10. Networking

**Key Insight**: The structure of connections matters more than their number.

- **Erdős–Rényi random graphs**: Most nodes have average degree, few are very connected.
- **Scale-free networks** (like the web): Some hubs have extraordinarily high connectivity—removing them can fragment the network.
- **Six degrees of separation**: Not about knowing everyone, but about short paths through hubs.

### 11. Game Theory

**Key Insight**: Your payoff depends on others' decisions too. The optimal strategy responds to what others are doing.

**Core Models:**
- **Prisoner's Dilemma**: Cooperation can emerge from repeated interaction (tit-for-tat).
- **Zero-sum games**: When one person's win is another's loss, optimal play mixes strategies randomly (Nash equilibrium, minimax theorem).
- **Auctions**: The winner's curse means the winner of a common-value auction tends to overpay—shading your bid is rational.

**Real Cases:**
- John Nash's equilibrium concept explains why traffic jams happen: individually rational choices (take the faster route) collectively produce gridlock.
- Merrill Flood (co-inventor of the Prisoner's Dilemma) also popularized the traveling salesman problem and may have coined "software."

---

## Recall Triggers

1. **User asks about "should I settle or keep looking" → trigger Optimal Stopping (37% Rule)** ✅
2. **User asks about "try new restaurant or go to favorite" → trigger Explore/Exploit (Gittins Index)** ✅
3. **User asks about "how to organize my closet/files/email" → trigger Sorting vs. Caching** ✅
4. **User asks about "I can't decide between two options" → trigger Toss a Coin (Randomness)** ✅
5. **User asks about "overthinking a decision" → trigger Overfitting (think less)** ✅
6. **User asks about "how long to keep looking for a job/house/partner" → trigger Optimal Stopping with threshold** ✅
7. **User asks about "how to manage my time better" → trigger Scheduling (SPT, EDD, no multitasking)** ✅
8. **User asks about "should I try something new" → trigger Explore/Exploit based on time horizon** ✅
9. **User asks about "my expectations vs reality are mismatched" → trigger Bayes's Rule** ✅
10. **User asks about "I'm stuck on a hard problem" → trigger Relaxation (let constraints go)** ✅

---

## How to Use This Skill

When a user presents a life decision problem, follow this diagnostic flow:

1. **Identify the problem type**: Is it a stopping problem, an exploration problem, an organization problem, a scheduling problem, or a game-theoretic problem?
2. **Identify constraints**: What is the time horizon? Is there recall? Is there cost per search? Is information full or partial?
3. **Apply the relevant algorithm**: Use the specific mathematical result from the book (37% Rule, Gittins Index, etc.).
4. **Adjust for human factors**: Remember that real humans get bored, search has endogenous costs, and the best theoretical algorithm isn't always the best practical one.
5. **Provide the concrete number or rule of thumb**: Monsters of the Midway principle—the core insight should be a specific, actionable number or decision rule.

---

## Important Caveats

- **The 37% Rule only works for ordinal comparisons** (you can tell which is better but not by how much). If you have scores (full information), use the Threshold Rule instead.
- **The Gittins Index assumes geometric discounting** of future rewards. For fixed time horizons, use backward induction (Bellman's method).
- **All sorting algorithms assume perfect comparators**. In real life, comparisons are noisy—this is why Round-Robin (sports season) is more robust than Single Elimination (playoffs).
- **Bayes's Rule requires a prior**. If you truly have no information, use a uniform prior—but be aware this is itself a choice with consequences.
- **Game theory assumes rational actors**. In practice, humans are boundedly rational and emotional. Use game theory as a first approximation, then adjust for known biases.

---

## Related Skills

- <unknown>
- <unknown>

---

## Watermark

This skill was produced from a comprehensive analysis of Brian Christian and Tom Griffiths's "Algorithms to Live By: The Computer Science of Human Decisions" (2016), including all core chapters on optimal stopping, explore/exploit, sorting, caching, scheduling, Bayes's rule, overfitting, relaxation, randomness, networking, and game theory.

---

**Listen and Execute.**
