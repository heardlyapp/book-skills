# Anti-Patterns — AI's Blind Spots and Dangers

> Source: Genius Makers, Chapters 12, 13, 15, 16, Epilogue

## The Five AI Traps

### 1. The AGI Mirage
**Pattern**: Every AI advance is followed by claims that AGI (artificial general intelligence) is just around the corner.
**Reality**: Deep learning is pattern matching at unprecedented scale — not intelligence. GPT models can write poetry but can't understand the poem. AlphaGo can beat any Go player but can't learn checkers. The gap between specialized AI and general intelligence remains vast.

### 2. The Scale Delusion
**Pattern**: "If bigger models produce better results, keep scaling."
**Reality**: Scaling produces diminishing returns and hides fundamental limitations. GPT-3 with 175B parameters is not 100x smarter than GPT-2 with 1.5B parameters. The field needs new ideas, not just more compute.

### 3. Bias Baked In
**Pattern**: AI systems trained on human data learn human biases — then amplify them at scale.
**Case**: Facial recognition systems that misidentify Black people at higher rates. NLP models that associate women with domestic roles. Hiring algorithms that discriminate against minority applicants. These are not bugs — they're features of learning from biased data.
**Key takeaway**: AI doesn't solve bias — it amplifies it. A model trained on historical hiring data will reproduce the hiring biases of the past, at scale and with the appearance of objectivity.

### 4. The Black Box Problem
**Pattern**: Deep neural networks are opaque. We can't fully explain why they make the decisions they do.
**Consequence**: In high-stakes domains (medicine, criminal justice, autonomous vehicles), we're asked to trust systems whose reasoning we can't inspect. The more powerful the AI, the less explainable it tends to be.

### 5. The Concentration of Power
**Pattern**: AI talent, data, and compute are concentrated in a few companies.
**Consequence**: Decisions about AI's future are made by a tiny group of people with aligned interests. There is no democratic oversight of the technology that will reshape society.

> **Case: The GPT Chatbot That Was Too Dangerous to Release** (Chapter 15)
> OpenAI trained GPT-2 in 2019 and initially refused to release the full model publicly, citing "concerns about malicious applications." The decision provoked a fierce debate: was OpenAI genuinely worried about misuse, or was it generating publicity for a model that was less dangerous than claimed? When the full model was finally released months later, no major disasters occurred. But the episode established a pattern: AI companies deciding unilaterally what the public should and should not see.
> **Key takeaway**: The decision to release or restrict AI technology is too important to be left to AI companies alone. When OpenAI decided to censor GPT-2, they were acting as de facto regulators of their own technology. In a democracy, that power should be exercised with public oversight.

> **Case: The Google Ethical AI Revolving Door** (Chapter 13)
> Timnit Gebru was a co-lead of Google's Ethical AI team. In December 2020, she co-authored a paper documenting the risks of large language models — including the same GPT-3 that Google was developing. Google told her to withdraw the paper or remove her co-authors. She refused, and Google fired her. The backlash was enormous. The message to researchers: you can study AI ethics, but don't criticize your employer's products.
> **Key takeaway**: Corporate AI ethics is an oxymoron. No company will fund research that threatens its business model. Independent AI safety research is not a luxury — it's a necessity. When the people who build AI also control the research about its dangers, the system is broken.
