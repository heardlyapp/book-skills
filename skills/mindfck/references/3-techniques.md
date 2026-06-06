# Techniques: The Cambridge Analytica Playbook

> Source: *Mindf*ck: Cambridge Analytica and the Plot to Break America*, Chapters 3-9

## 1. Facebook Data Harvesting via MTurk + Apps

**The Pipeline:**
1. Post microtasks on Amazon Mechanical Turk (MTurk) offering $1-2 for a personality survey
2. Require users to install a Facebook app to receive payment
3. The app pulls the user's complete Facebook profile AND all friends' data
4. The survey responses train the algorithm, which then predicts personality for all friends

**Scale achieved:** 87 million profiles in 2 months for ~$100,000 in MTurk costs

> **Case: The App Launch** (Chapter 6): In June 2014, Kogan's app went live. For the first 15 minutes, nothing happened. Then a flood: 1 record → 20 → 100 → 1,000 → exponential. Jucikas added a beeping counter. Nix finally understood what they'd built when he could call random Americans and know everything about them.
> **Key takeaway**: Facebook's API made this trivial. No hacking required — just legal access through Facebook's own permission system.

## 2. Cognitive Bias Exploitation

Cambridge Analytica systematically tested and deployed at least 6 cognitive biases:

| Bias | Mechanism | CA Application |
|---|---|---|
| **Availability Heuristic** | Ease of recall = frequency | "People of Walmart" mockery → reinforces victimhood |
| **Affect Heuristic** | Emotion replaces reasoning | Anger-inducing content → reduces rational information-seeking |
| **Identity-Motivated Reasoning** | Information filtered through group identity | Make criticism of racism = attack on identity → boomerang effect |
| **Just-World Hypothesis** | World is fair, victims deserve their fate | "God rewards success; if minorities are poor, there's a reason" |
| **Reactance Effect** | Counter-arguments strengthen original belief | The more Democrats criticized Trump, the stronger his supporters' resolve |
| **Zero-Sum Bias** | One group's gain = another's loss | "The more they take, the less you have" |

> **Case: The Priming Experiment** (Chapter 7): CA showed subjects graphs with uncontroversial labels (phone usage rates). People read them correctly. Then they switched the labels to controversial topics (income inequality, climate change, gun deaths). Angry respondents misread graphs they had previously understood perfectly.
> **Key takeaway**: Anger doesn't just change opinions — it changes the ability to process information. This is why "Project Fear" (Remain's economic warnings) failed: angry voters literally couldn't process risk assessments.

## 3. Fake Groups and Physical Events

**The radicalization funnel:**
1. Create fake Facebook pages: "Smith County Patriots," "I Love My Country"
2. Facebook's algorithm recommends these to users who already liked similar extreme content
3. Members engage in the group, self-identify as part of an extreme community
4. Once group reaches critical mass, convene **physical meetups** at coffee shops or bars
5. Small venue makes 40 people feel like a massive movement
6. In-person fellowship deepens conspiracy beliefs and group identity

> "Lots of reporting on Cambridge Analytica gave the impression that everyone was targeted. In fact, not that many people were targeted at all. CA didn't need to create a big target universe, because most elections are zero-sum games."

## 4. The Nigeria Playbook (Kompromat + Gruesome Propaganda)

**The two-pronged approach:**
1. **Hacking**: CA engaged hackers (some possibly Russian) to steal opposition emails, medical records, and databases. In Nigeria, they discovered Muhammadu Buhari had cancer before it was public.
2. **Propaganda videos**: CA created targeted ads showing beheadings and burnings — actual footage of torture — suggesting these would happen under Buhari's rule. Targeted via Google ad networks to pro-Buhari regions.

> **Case: The Nigeria Videos** (Chapter 9): The ads appeared as clickbait — a gossipy headline or a sexy photo. When clicked, they showed a blank screen with a video: a man having his throat slowly sawed with a blunt machete; a woman drenched in gasoline and set on fire. These were real torture videos, not actors.
> **Key takeaway**: CA treated African elections as unregulated testbeds. The same playbook was later adapted for the US and UK. When Nix was asked about legality, he said: "You can't expect anything legal with these people. It's Africa."

## 5. The Brexit Scheme (AIQ + BeLeave)

**The illegal spending mechanics:**
1. Vote Leave reached its £7 million legal spending limit
2. Cummings created a "separate" campaign called BeLeave, run by interns Darren Grimes and Shahmir Sanni
3. Vote Leave transferred £700,000 to BeLeave on the condition that the interns never touch the money — it goes directly to AIQ (CA's Canadian proxy)
4. AIQ used CA's infrastructure and data to target British voters with 1,433 different ad variations
5. These ads were seen 169 million times but targeted only a narrow segment of a few million voters

> **Case: The Bee in the Bonnet** (Chapter 9): Grimes and Sanni were 22-year-old interns. Vote Leave's lawyers had them sign articles of association making Grimes personally liable. The interns didn't understand they were being set up as fall guys for the largest campaign finance breach in British history. When Parkinson (Sanni's boss and secret lover) found out Sanni was cooperating with investigators, he used the Downing Street press office to out Sanni as gay to the world's media — knowing Sanni hadn't come out to his Pakistani Muslim family.
> **Key takeaway**: The scheme used young, trusting volunteers as personal liability shields. When the cheat was exposed, the powerful walked; the powerless paid.

## 6. Voter Suppression Targeting African Americans

CA internal documents described a "voter disengagement" initiative targeting African Americans:
- Peddle left-wing social justice rhetoric to depict Hillary Clinton as a propagator of white supremacy
- Push minority voters toward third-party candidates (Jill Stein)
- Exploit cognitive biases to demotivate turnout in key demographics

> **Case: The Disingenuous Persuasion** (Chapter 7): CA tested whether showing photos of white men's daughters paired with black men would trigger racial bias responses. The research was designed to identify which messages would suppress minority turnout.
> **Key takeaway**: The same data that could power persuasion was used for suppression. This was flagged internally as potentially illegal but never stopped.
