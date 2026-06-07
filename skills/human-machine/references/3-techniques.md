> Source: Human + Machine, Chapters 5, 7, 8

# Techniques: Training AI, Building Guardrails, and Running MELDS

## Training AI Systems — The Three Categories

### Category 1: Physical Robot Training
- **Technique:** Deep reinforcement learning — give the robot a picture of success, let it use trial and error
- **Timeline:** Fanuc arms achieve 90% accuracy in 8 hours
- **Scale:** "Distributed learning" — when one robot learns, it shares knowledge across the network
- **Human role:** Prepare gear casing; perform fine adjustments; handle tasks too complex for robots

### Category 2: Empathy Training
- **How Koko works:** Users share anxieties → Koko responds → if inappropriate, human trainer corrects → algorithm improves
- **Example response** (trained Alexa to someone worried about exams): "Exams are really stressful but a little anxiety can help us succeed. It sharpens our minds… I wonder if you could think of your nerves as your secret weapon."
- **Key principle:** Empathy training requires domain experts from unexpected backgrounds — poets, novelists, playwrights are training Cortana's personality at Microsoft

### Category 3: Data Hygiene
- **Problem:** "Biases in, biases out" — training data must be free of slanted perspectives
- **Data hygienist role:** Clean data exhaust (byproducts of other processes like Facebook activity, satellite images)
- **Example:** BlackRock analyzing satellite images of China for industrial activity indicators → led to "quantamental" funds

---

## Building Guardrails for Responsible AI

### Technique 1: Set Behavioral Boundaries
Like Asimov's Three Laws of Robotics, but for business:

1. A robot/AI may not injure a human or allow harm through inaction
2. AI must obey human orders except when conflicting with Rule 1
3. AI must protect its own existence except when conflicting with Rules 1 and 2

**Practical application:**
- Keyword filters (prevent Tay scenario — Microsoft's chatbot that learned racist language in hours)
- Content moderation systems
- Sentiment monitoring

### Technique 2: Create Human Checkpoints
- Visual dashboards showing what AI is "thinking"
- Analytics and metrics on system behavior
- 76% of automation technologists say visual output is the top solution for trust

### Technique 3: Use Explainability Tools
- **LIME (Local Interpretable Model-Agnostic Explanations):** Doesn't need to know the algorithm. Makes slight changes to inputs, observes how decisions change. Highlights variables that led to a conclusion.
- **Falling rule list algorithms:** Ordered if-then rules for maximum explainability (good for regulated industries)
- **Tradeoff:** Deep learning = higher accuracy, lower explainability. Decision tree = lower accuracy, higher explainability. Choose based on context.

---

## The 5-Step Process Reimagination Framework (MELD)

### Step 1: Mindset — Discover & Describe
- **Method:** Design thinking / empathic design
- **Focus:** Customer pain points previously impossible to solve
- **Example:** Agricultural company initially wanted to predict crop yields. Research revealed farmers wanted real-time adaptive recommendations → pivoted to actionable advice (which crops to grow, where, how much nitrogen)
- **AI tool:** Use ML to sift through customer emails, social media, digital exhaust to identify where reimagination is most needed

### Step 2: Mindset — Co-create
- **Method:** Bring stakeholders together to envision missing middle work
- **Example:** Audi's telepresence robots (ART). Expert technicians + dealer mechanics + AI technologists co-created a system where remote experts guide on-site repairs via mobile robots. Standard protocols were modified based on feedback from all sides.

### Step 3: Mindset — Scale & Sustain
- **Internal first:** SEB tested Aida on 15,000 employees before deploying to 1M customers
- **Minimum viable approach:** Pilot → iterate → scale

### Step 4: Experimentation
- **Build-Measure-Learn cycles:** Amazon Go as the prime example
- **Don't bet the company:** "I've made billions of dollars of failures at Amazon.com. Literally. What matters is companies that don't continue to experiment." — Jeff Bezos
- **Walmart's Store No. 8:** Isolated incubator, ring-fenced from bureaucracy, backed by corporate resources

### Step 5: Data Supply Chain
1. **Think dynamically** — Ducati Corse: 100 IoT sensors on bikes, real-time analytics, machine-learning predictions
2. **Widen access** — Beiersdorf: internal data + syndicated Nielsen data for board insights
3. **Increase velocity** — Facebook: 3-tiered storage (hot/cold), 8% of photos account for 82% of traffic
4. **Enable discovery** — Ayasdi + Texas Medical Center: find new subsets of breast cancer survivors in minutes
5. **Fill the missing middle** — Trainers, explainers, sustainers needed to manage the data supply chain

---

## The Trainers' Toolkit

| Role | Tool/Technique | Application |
|------|---------------|-------------|
| Empathy trainer | Koko's cognitive engine | Chatbots respond appropriately to frustration, anxiety |
| Personality trainer | Scriptwriting, character development | Cortana's confident/caring demeanor |
| Worldview trainer | Cultural sensitivity analysis | Bots adapted for Japanese vs American AI norms |
| Interaction modeler | Shadowing + behavioral capture | Julie Shah's robots that learn from watching human workers |
| Data hygienist | Bias detection, feature engineering | Cleaning "data exhaust" for BlackRock |
| Crowdsourced trainer | Mighty AI platform | Init.ai's conversation models via community role-playing |

---

## The Explainers' Toolkit

| Role | Technique | Application |
|------|-----------|-------------|
| Algorithm forensics analyst | LIME, falling rule lists | Investigate why a credit decision was made |
| Transparency analyst | System classification | Catalog which systems are black-box vs accessible |
| Explainability strategist | Accuracy vs explainability tradeoff | Choose deep learning for internal supply chain, decision tree for consumer-facing |
| ZestFinance approach | Veracity/Stability/Prudence scoring | Rank loan applicants across categories, then analyze with 50+ algorithms |

---

## The Sustainers' Toolkit

| Technique | What it prevents | Example |
|-----------|-----------------|---------|
| Safety green paint | Worker anxiety | GM/Fanuc: lime color ("safety green") for cobots vs orange (danger) or yellow (caution) |
| Performance reviews for AI | Degrading/biased systems | Machine relations managers promote/demote/decommission AI systems |
| Ethics compliance | Unethical outcomes | Investigate if credit AI discriminates by geography |
| Automation ethics | Employee fear, uncanny valley | Evaluate noneconomic impact; plan for the emotional response |
| Moral crumple zone analysis | Human liability | Build accountability into algorithms, not just human operators |
