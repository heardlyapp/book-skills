# Optimal Stopping: The 37% Rule in Love, Life, and Business

This reference covers the most famous algorithm from *Algorithms to Live By*: optimal stopping, also known as the secretary problem. It's the mathematical framework for deciding when to stop searching and commit—whether you're looking for a partner, an apartment, or a parking spot.

## The 37% Rule: Mathematics of "When to Leap"

The 37% Rule emerges from the "secretary problem," first popularized by Martin Gardner's *Scientific American* column in 1960. The setup is deceptively simple: you interview n applicants in random order, one at a time. After each interview, you must immediately decide to hire or move on. Rejected applicants are gone forever. Your goal: maximize the chance of hiring the single best applicant.

The optimal strategy: reject the first 37% of applicants unconditionally (the "look" phase), then hire the very next applicant who beats everyone you've seen so far (the "leap" phase). This yields a 37% chance of getting the best applicant—and crucially, that 37% holds regardless of whether you're interviewing 10 applicants or 10 million.

The number 37% comes from 1/e, where e is Euler's number (≈2.71828). The math is symmetrical: both the look/leap threshold and the success probability converge on 37%.

### Case 1: Michael Trick's Algorithmic Proposal

Michael Trick, then a graduate student at Carnegie Mellon and now a professor of operations research, applied the 37% Rule to his love life. He calculated that searching from age 18 to 40 gave age 26.1 as the switching point. When he met a woman who beat everyone he'd dated before, he followed the algorithm and proposed. She turned him down. This real-world failure exposed a critical assumption of the classical secretary problem: applicants always accept. Trick's story illustrates the "rejection variant," where the math says to start proposing after just 25% of the search rather than 37%. Happily, Trick later found love in a German bar—no algorithm required—and they married six years later.

### Case 2: Johannes Kepler's Eleven Courtships

The 17th-century astronomer Johannes Kepler, after his first wife died in 1611, embarked on a methodical quest to remarry, ultimately courting 11 women. He liked candidate #4 best ("because of her tall build and athletic body") but kept searching. Candidate #5 "won me over with love, humble loyalty, economy of household, diligence." Yet he continued. Eventually, after 11 courtships, he returned to candidate #5—Susanna Reuttinger—and married her. They had six children and biographies describe his domestic life as "particularly peaceful." Kepler's story illustrates the "recall" variant of optimal stopping: when you can go back to previous candidates, the optimal strategy is to look noncommittally through 61% of options, then leap for anyone better during the remaining 39%. If still single after exhausting all possibilities, return to the best one that got away.

### Case 3: Donald Shoup and Parking

UCLA professor Donald Shoup (the "parking rock star") analyzed parking as an optimal stopping problem. When you drive along a street, every empty spot requires a decision: take it or keep going closer to your destination. With 99% occupancy (typical big city), you should start looking nearly 70 spots from your destination. With 85% occupancy (Shoup's target for adaptive pricing), you only need to start half a block away. Shoup's insight: empty spots on desirable blocks indicate a well-functioning system, not a failure. He personally avoids the problem entirely: "I ride my bike."

### Case 4: Boris Berezovsky and the Burglar Problem

Boris Berezovsky, who authored the only full-length book on the secretary problem, became Russia's richest man (≈$3B) by applying optimal stopping to business—but failed to apply it to politics. The "burglar problem" provides the algorithm: the number of risks you should take = success probability / failure probability. A skilled burglar with 90% success rate should retire after 9 jobs. Berezovsky, by getting into politics after amassing his fortune, violated this principle. He died by suicide in exile in 2013, having lost most of his wealth.

### Practical Takeaways

- **For hiring**: Look at 37% of applicants, then hire the first who beats the best you've seen.
- **For dating (with possible rejection)**: Start proposing after 25%.
- **For selling a house**: Set a threshold price upfront based on the cost of waiting. Never lower it arbitrarily.
- **For risky ventures**: Retire when you've succeeded success% / failure% times.
- **For parking**: The occupancy rate is the key variable. Lower occupancy = start looking closer to your destination.

---

*Source: "Algorithms to Live By" (2016), Chapter 1: Optimal Stopping, and author interviews with Michael Trick, Donald Shoup, and others.*
