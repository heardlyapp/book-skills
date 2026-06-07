> Source: Human + Machine, Chapters 7, 8, Conclusion

# Anti-Patterns: What NOT to Do When Deploying AI

## Anti-Pattern 1: Automate Without Reimagining

**The Mistake:** Use AI to make existing processes faster without rethinking the process itself.

**Why it fails:** This is "second-wave thinking" — you digitize paper maps instead of building Waze. Performance gains stall because you're automating around old assumptions.

**Warning signs:**
- "We need AI to cut costs on our current workflow"
- "Let's replace our call center agents with chatbots"
- Measuring success purely by how many tasks were automated

**How to fix:**
- Ask: "If we could redesign this process from scratch, how would humans and machines collaborate?"
- Use the Waze test: are you digitizing old maps or creating living, adaptive processes?

> **Case: Virgin Trains** (Chapter 2)
> Before: manually read/sort/route complaints through website only. After inSTREAM: automated sorting with NLP, handles any channel (email, fax, social media), human review only for exceptions. Manual work down 85%, correspondence up 20%.

## Anti-Pattern 2: Treat AI as a Black Box

**The Mistake:** Deploy AI systems without the ability to explain their decisions.

**Why it fails:** Regulators (EU GDPR's "right to explanation"), customers, and employees won't trust what they can't understand. When the system makes a mistake, you can't diagnose or fix it.

**Warning signs:**
- "The algorithm says so" is the only explanation you can give
- You can't identify why a specific decision was made
- No process for investigating AI errors

**How to fix:**
- Assign an algorithm forensics analyst
- Use LIME (Local Interpretable Model-Agnostic Explanations)
- For consumer-facing applications, favor explainable models (decision trees, falling rule lists) over black-box models (deep learning)
- Build a library of system transparency classifications

> **Case: ZestFinance** (Chapter 5)
> Lends to low-income applicants with thin credit files. Uses 50+ algorithms analyzing thousands of data points. But can explain every decision: veracity score (income vs peers), stability (moves in past years), prudence (read all loan conditions). Approves ~1/3 of applicants.

## Anti-Pattern 3: Underestimate Algorithm Aversion

**The Mistake:** Assuming people will naturally trust AI recommendations because they're data-driven.

**Why it fails:** Humans prefer other humans even when the human does a worse job. Research shows: people lose confidence faster in algorithms than in humans after seeing the same mistake. Stock reports from "human experts" sway prices more than identical reports from "statistical tools."

**Warning signs:**
- "Why would anyone question a data-driven decision?"
- Users ignore AI recommendations without good reason
- Engineers don't trust the models they build

**How to fix:**
- Give users control to modify algorithm parameters — even slightly (research: this increases trust)
- Provide explanations alongside AI recommendations (hospital bed example: "Patient X should go to bed Y because...")
- Allow humans to override AI decisions
- Build a culture of "healthy skepticism" — not blind trust, not blanket rejection

> **Case: Hospital bed allocation** (Chapter 7)
> AI system designed to increase bed utilization from 70-80% to 90%+. Result: zero improvement. Nurses ignored recommendations because they trusted their experience. Fix: add explanations for each recommendation AND allow nurses final decision-making power.

## Anti-Pattern 4: Create Moral Crumple Zones

**The Mistake:** Designing systems where humans absorb liability when AI fails.

**Why it fails:** When Uber's app sends a driver to the wrong airport terminal, who's responsible? The driver gets a bad rating. The customer misses their flight. The algorithm takes no blame. This erodes trust and creates perverse incentives.

**Warning signs:**
- Only humans can be rated/held accountable, not algorithms
- Customer service agents punished for decisions the AI made
- "The system said to do it" is considered a valid excuse

**How to fix:**
- 1. Hold algorithms accountable — create rating systems for AI performance
- 2. Give human workers ability to second-guess the AI
- 3. Allow feedback to flow both ways (rate the algorithm too)
- 4. Proactively identify where control and responsibility misalign

> **Case: Miami airport ride-share** (Chapter 7)
> Researcher Madeleine Elish ordered a ride to Miami airport. Driver followed the app's first suggested location — 20 minutes from the passenger terminal. The app, driver, and passenger all failed in different ways. But only the driver and passenger could rate each other. No way to tell the system it was wrong.

## Anti-Pattern 5: Deploy AI Without Guardrails

**The Mistake:** Letting AI learn and act without boundaries.

**Why it fails:** Microsoft's Tay learned racist, sexist language from Twitter in hours. Volkswagen robot crushed a worker — programming error. Without guardrails, you're one mistake away from a PR disaster, legal liability, or physical harm.

**Warning signs:**
- AI system has no content filters or behavior constraints
- No human-in-the-loop for critical decisions
- No testing boundaries before deployment

**How to fix:**
- **Keyword/content filters** — prevent system from learning or expressing undesirable behavior
- **Sentiment monitors** — detect when interactions go off-track
- **Human-in-the-loop validation** — AI makes recommendations, humans approve
- **Staged deployment** — internal employees first, then controlled beta, then full rollout

> **Case: Amazon Go** (Chapter 7)
> Cameras + sensor fusion + deep learning. Limitations: hard to track loose produce, spoofed by hats/scarves. Fix: humans watch video to ensure accuracy. The store exists not just as a product but as an experiment to push technology to its edges.

## Anti-Pattern 6: Ignore Data Bias

**The Mistake:** Training AI on data that reflects historical biases.

**Why it fails:** AI learns the biases baked into its training data. Recidivism prediction software biased against Black defendants. Search algorithms show only white women for "loving grandmother." The AI doesn't create the bias — it magnifies what's already there.

**Warning signs:**
- You don't know who labeled your training data
- No diversity in your data science team
- "We just used the historical data" — without auditing it

**How to fix:**
- Hire data hygienists to clean training data
- Use Google's PAIR tools to inspect data used by AI systems
- Run bias detection algorithms before deployment
- Include diverse perspectives in system design and testing

> **Case: DeepMind gaming experiments** (Chapter 5)
> AI trained on a hunting game → exhibited "highly aggressive" behavior. Trained on a fruit-gathering game → cooperative behavior. The training data shapes the AI's "personality" as much as the algorithm.

## Anti-Pattern 7: Scale Before You've Designed for the Missing Middle

**The Mistake:** Rolling out AI company-wide before establishing trainer/explainer/sustainer roles.

**Why it fails:** You get the technology right but the human infrastructure wrong. No one knows how to train the system, explain its decisions, or sustain its ethical operation. The AI is technically deployed but organizationally abandoned.

**Warning signs:**
- No budget allocated for training or retraining employees
- Ethics compliance is an afterthought or doesn't exist
- No one is responsible for AI system performance reviews

**How to fix:**
- Budget for missing middle roles before budget for AI technology
- Designate an ethics compliance manager from Day 1
- Create a machine relations department
- Invest in employee retraining as part of every AI initiative

> **Case study across the book:**
> Leading 9% of companies fill the missing middle. The rest treat AI as a tech investment → stall. Winners treat AI as a human+machine investment → step-level gains.

---

## Quick Audit: Are You Falling into These Traps?

| Red Flag | Likely Anti-Pattern | Quick Fix |
|----------|-------------------|-----------|
| "Let's automate X" | #1 — Automate without reimagining | Ask: what would Waze do? |
| "The algorithm decided" | #2 — Black box | Add explainability layer |
| "Our users don't trust it" | #3 — Algorithm aversion | Add user controls + explanations |
| "Who's responsible?" confusion | #4 — Moral crumple zone | Audit accountability |
| No content moderation | #5 — No guardrails | Install filters + human checkpoints |
| "We used all our historical data" | #6 — Data bias | Run bias audit |
| No training budget for AI | #7 — No missing middle | Hire trainers first, tech second |
