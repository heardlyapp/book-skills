# 1. Core Framework — Optimal Stopping and the 37% Rule

> Source: "Algorithms to Live By" by Brian Christian and Tom Griffiths (2016), Chapter 1: Optimal Stopping.

## The Engine of the Book

The 37% Rule is the book's signature algorithm — and its most practically useful one. It solves the "secretary problem": how to select the best candidate when you must decide immediately on each, with no going back.

### The Algorithm

- **Phase 1 (Look)**: Reject the first 37% of options unconditionally. Don't choose any of them. You're gathering data.
- **Phase 2 (Leap)**: Pick the very next option that beats everything you've seen so far.

**Why 37%?** The mathematical constant e (≈2.71828) gives us 1/e ≈ 37%. This number generalizes to millions of options — the threshold is always 37%.

### Three Key Variants

| Variant | When to use | The rule |
|---------|------------|----------|
| **Full Information** | You know the score distribution (e.g., test scores, house prices) | Dynamic threshold: last option = 50%, second-to-last = 69%, third-to-last = 78% |
| **With Rejection** | Candidates can say no | Start proposing after 25% instead of 37% |
| **With Recall** | You can go back to previous options | Look 61%, then leap during remaining 39%. If still unsuccessful, return to best passed-up |

> **Case: Michael Trick's Algorithmic Proposal** (Chapter 1): Michael Trick, a Carnegie Mellon graduate student and now operations research professor, applied the 37% Rule to dating. He calculated his search window as age 18 to 40, giving age 26.1 as the switching point. When he met someone who beat everyone before, he proposed. She said no. This revealed a crucial flaw in the classical model: candidates must say yes. The rejection variant (start proposing at 25%) would have changed his strategy. Trick later found love in a German bar and married her — algorithm not required, but the lesson stuck.
> **Key takeaway**: Always check the assumptions of the model you're using. Real life has rejection, recall, and human messiness that raw math doesn't capture.

> **Case: Johannes Kepler's Eleven Courtships** (Chapter 1): After his first wife died in 1611, astronomer Johannes Kepler methodically courted 11 women. He liked candidate #4 "because of her tall build and athletic body" but kept searching. Candidate #5 "won me over with love, humble loyalty, and economy of household." Still he continued. Eventually, he returned to candidate #5 — Susanna Reuttinger — and married her. They had six children and a peaceful domestic life. This perfectly matches the "with recall" variant: look through 61% (option 7 of 11), then commit to the next best. When he returned to #5, he was using the recall option.
> **Key takeaway**: The ability to go back to previously passed options changes the math — and Kepler did it intuitively 400 years before computer scientists formalized it.

> **Case: Donald Shoup and Parking** (Chapter 1): UCLA economist Donald Shoup analyzed parking as an optimal stopping problem. Every empty spot requires a split-second decision: take it or keep driving toward your destination. With 99% occupancy (typical for a busy city), you need to start looking nearly 70 spots before your destination. With 85% occupancy (Shoup's target for adaptive pricing), you can start half a block away. Shoup's insight: the occupancy rate is the critical variable, and adaptive pricing can tune it to the ideal.
> **Key takeaway**: Optimal stopping applies to trivial decisions too. Knowing the "occupancy rate" — the density of opportunities — tells you when to start looking.
