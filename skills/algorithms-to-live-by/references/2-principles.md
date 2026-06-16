# 2. Principles — Explore/Exploit and the Value of the Unknown

> Source: "Algorithms to Live By" by Brian Christian and Tom Griffiths (2016), Chapter 2: Explore/Exploit. Additional material from Chapter 11: Game Theory.

## The Fundamental Dilemma

Every day we face the same choice: try something new or stick with what we know. Computer science calls this the "explore/exploit tradeoff," formalized as the multi-armed bandit problem.

### The Gittins Index

John Gittins, a statistician at Oxford, solved this problem in the 1970s while working for Unilever. His insight: assign each option a single number (the Gittins Index) that captures both its known performance AND its future potential. Always pick the option with the highest index.

**The surprising result**: A brand-new option (0 successes, 0 failures) has a Gittins Index of 0.7029 — worth a guaranteed 70% success rate. A machine you've played 15 times with a 9-6 record (60% success) has an index of only 0.6300. The unknown option is better, even though its expected value (50%) is lower. The unknown has inherent value because it might be better, and you can use that knowledge in the future.

| Track record | Gittins Index (90% discount) |
|-------------|------------------------------|
| 0-0 (untested) | 0.7029 |
| 1-1 (50%) | 0.6346 |
| 9-6 (60%) | 0.6300 |
| 9-1 (90%, 10 trials) | 0.8695 |
| 99-1 (99%, 100 trials) | 0.9966 |

> **Case: John Gittins and the Unilever Drug Trial** (Chapter 2): Gittins was approached by Unilever to solve a practical problem: how to allocate drug trials when each drug has unknown efficacy, and testing one drug means NOT testing others. The cost of a wrong answer was measured in lives. Gittins realized this was a multi-armed bandit and devised the Gittins Index as the optimal solution. Unilever implemented it and dramatically improved their trial efficiency.
> **Key takeaway**: When the cost of exploration is high (lives, money, time), the Gittins Index provides the mathematically optimal allocation — better than intuition or rules of thumb.

> **Case: Scott Plagenhoef's iPod Strategy** (Chapter 2): As editor-in-chief of Pitchfork, Scott Plagenhoef had to constantly listen to new music for work. He described it as "a particular kind of hell" — forced into pure exploration mode, never able to enjoy favorites. His solution: load only new music onto his iPod, making exploitation physically impossible.
> **Key takeaway**: When you need to explore but your instincts pull you toward exploitation, remove the option to exploit. Physical constraints on behavior are more reliable than willpower.

> **Case: Hollywood's Sequel Strategy** (Chapter 2): In 1981, only 2 of the top 10 films were sequels. By 2011, the number was 8. This is not creative laziness — it's a rational response to a shrinking time horizon. When studios anticipate fewer years of profitability (the film industry declined 40% between 2007 and 2011), they exploit known brands rather than exploring new IP. As data scientist Chris Stucchio put it: "I'm more likely to try a new restaurant when I move to a city than when I'm leaving it."
> **Key takeaway**: Your time horizon drives your strategy. If you think the end is near, exploit. If you think you have time, explore. This principle applies to careers, relationships, and investments.

## The Win-Stay Principle

The simplest effective explore/exploit strategy: keep doing what works, and switch when it stops working. But "Lose-Shift" (switching after every failure) is too aggressive — a 9-1 option shouldn't be abandoned after one loss. The better rule: only shift after enough failures to be confident the option has degraded.
