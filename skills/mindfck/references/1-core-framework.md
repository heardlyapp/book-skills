# Core Framework: The Cambridge Analytica Engine

> Source: *Mindf*ck: Cambridge Analytica and the Plot to Break America*, Chapters 1, 5, 6, 7, 10

## Overview

The Cambridge Analytica engine operated on three integrated layers: **data harvesting**, **psychometric profiling**, and **microtargeted message delivery**. Together they formed a weaponized information system that treated the American electorate as a target population for psychological operations.

---

## Layer 1: Facebook Data Harvesting

**The Mechanism:**
- Aleksandr Kogan created a Facebook app that users paid $1-2 (via Amazon MTurk) to complete a personality survey
- When a user installed the app, Facebook's API granted access to not only that user's data but **all of their friends' data** — because Facebook's permissions treated "being a friend" as sufficient consent
- Average user had 150-300 friends → each app install yielded ~200 additional profiles
- At its peak, CA harvested **87 million Facebook profiles**

| App Install Cost | Profiles per Install | Total Profiles |
|---|---|---|
| $1-2 per user | ~200 friends' profiles | ~87 million |

**The Data Collected:**
- Name, gender, age, location
- Status updates, likes, friends list, private messages
- Combined with commercial data (Experian, Acxiom) — airline miles, magazine subscriptions, car model, mortgage data, gun licenses
- Combined with census imputations — inferred diabetes risk, income, education, health status
- Combined with clickstream data from ISP logs

> **Case: The $20 Million Launch** (Chapter 6): After Robert Mercer invested $15-20 million, Cambridge Analytica launched the Facebook data harvesting app in June 2014. The data came in so fast that CTO Tadas Jucikas sabered a bottle of Perrier-Jouët Belle Epoque with a Napoleonic saber. Within two months they had 87 million complete Facebook profiles.
> **Key takeaway**: Facebook's loose API permissions made industrial-scale data theft trivial — $1 per target to access 200 friends' data cost-effectively.

> **Case: Calling Jenny Smith** (Chapter 6): After the data was loaded, Alexander Nix called a random American woman from the London office. He knew her Game of Thrones preferences, who she voted for, her kids' school, her car, her mortgage. She confirmed everything, never knowing she was talking to a psychological warfare firm.
> **Key takeaway**: The combination of Facebook data, commercial data, and satellite imagery created total informational asymmetry — CA knew everything; the target knew nothing.

---

## Layer 2: Psychometric Profiling

**The Five-Factor Model (Big Five):**

| Trait | High Scorers | Political Signal |
|---|---|---|
| Openness | Curious, creative, open to new ideas | More liberal, voted for Obama's "hope and change" |
| Conscientiousness | Organized, structured, orderly | More conservative, values tradition |
| Extraversion | Outgoing, energetic, sociable | Cross-cutting |
| Agreeableness | Cooperative, compassionate | Correlated with social welfare support |
| Neuroticism | Anxious, impulsive, prone to stress | Susceptible to conspiratorial thinking |

**The "Ten Likes" Rule** (from Youyou, Kosinski & Stillwell, 2015):
- 10 likes → predicts behavior better than a co-worker
- 150 likes → better than a family member
- 300 likes → better than your spouse

**The Dark Triad** (targeted for radicalization):
- **Narcissism** — self-centeredness, entitlement, envy → susceptible to victimhood narratives
- **Machiavellianism** — ruthless self-interest, manipulation → susceptible to cynicism about institutions
- **Psychopathy** — emotional detachment, impulsivity → susceptible to anti-social behavior

> **Case: Kombucha Lady** (Chapter 5): In Virginia focus groups, CA found a woman who shopped at Whole Foods, did yoga, burned incense, had Buddhist statues — and belonged to an anti-gay evangelical church. Personality profiling showed the data was right: she was not a contradiction; she was a specific personality type.
> **Key takeaway**: Traditional demographic polling (women voters, Latino voters) misses individual nuance; personality profiling captures who people actually are.

> **Case: The Closeted Voter** (Chapter 7): Focus groups revealed that straight white men felt "closeted" — they had to moderate racist/misogynist speech to pass in society. CA realized the Tea Party and incel communities shared the same psychological structure as LGBTQ "coming out" — a group feeling oppressed and emerging from hiding.
> **Key takeaway**: Personality traits that make people susceptible to radicalization (neuroticism, dark triad) can be identified at scale and targeted with tailored narratives.

---

## Layer 3: Microtargeting + Information Warfare

**The Weapon System (adapted from military PSYOPS):**
- **Payload** = narrative (a rumor, a cultural message, a political identity)
- **Delivery system** = Facebook ads, fake local groups, algorithmically boosted content
- **Targeting system** = psychometric profiles, Facebook lookalike audiences, IP-to-address matching

**The Gerasimov Doctrine** (from Russian General Valery Gerasimov, 2013):
- "The role of nonmilitary means of achieving political and strategic goals has grown"
- "The information space opens wide asymmetrical possibilities for reducing the fighting potential of the enemy"
- Cambridge Analytica implemented this doctrine using commercial tools (Facebook ads, consumer data) rather than military ones

**The Targeting Pipeline (as designed by Tadas Jucikas):**
```
Data Sources → 
- Facebook profiles (87M)
- Commercial data (Experian/Acxiom)
- Census imputations
- ISP clickstreams
→ Identity Resolution →
- Merge into single unified profile per person
→ Deep Learning Models →
- Big Five scores
- Dark Triad scores
- Issue positions
- Turnout likelihood
→ Message Customization →
- Tailored ads targeting specific cognitive biases
→ Ripon Platform →
- Deploy at scale via Facebook/Google ad networks
```

> **Case: Cuccinelli's Blow Jobs** (Chapter 4): In Virginia, CA identified that Republican voters were put off by candidate Ken Cuccinelli's obsession with criminalizing oral sex — but they appreciated predictability. CA tested the message "You might not agree, but at least you know where I stand" — it outperformed all alternatives. Republicans can accept a batshit candidate if the batshittery is consistent.
> **Key takeaway**: Psychometric insight → tailored message → measurable behavior change. This was the model that later informed Trump's "I could stand in the middle of Fifth Avenue and shoot somebody" strategy.
