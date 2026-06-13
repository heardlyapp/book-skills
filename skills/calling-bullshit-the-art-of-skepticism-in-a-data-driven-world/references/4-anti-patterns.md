# Anti-Patterns: The Limits of Data and Science

> Source: Calling Bullshit, Chapters 8-9

## Big Data Hype

Big data is not automatically better. Larger datasets amplify biases and generate spurious correlations. Size alone doesn't fix biased sampling or bad methodology.

> **Case: Google Flu Trends Failure** (Chapter 8): Google claimed to predict flu from search queries. It failed badly — overestimating flu prevalence for years. Correlations in training data didn't hold in real time. Big data without causal models is unreliable.

> **Case: The Drug Trial Reporting** (Chapter 8): Pharmaceutical companies test many endpoints but only report significant ones. The published result looks strong. The full picture reveals selective reporting — a systematic problem in medical research.

> **Key takeaway**: More data doesn't mean better insights. Ask: is the data representative? Were the analyses pre-registered? Were null results reported?

## P-Hacking and Publication Bias

Test many hypotheses, report only significant results. This is classic p-hacking.

> **Case: The Nutrition Study** (Chapter 9): Test 20 foods against 20 diseases, one combination will be "significant" at p<0.05 by chance. That's what gets published. The other 399 tests vanish from the record.

## Failing to Distinguish Signal from Noise

With massive datasets, random patterns are inevitable and often mistaken for real discoveries.

> **Key takeaway**: Science produces bullshit when incentives reward novelty over accuracy. Always ask: can this finding be independently replicated?
