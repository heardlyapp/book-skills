---
name: i-robot
description: >-
 Isaac Asimov's I, Robot — the classic collection of interconnected stories that
 introduced the Three Laws of Robotics. Through robopsychologist Dr. Susan Calvin,
 Asimov explores the logical consequences of giving machines ethical rules. From
 a robot that reads minds to one that develops a religion, each story is a thought
 experiment about intelligence, morality, and what it means to be human.

 Covers 6 use cases:
 ① Understanding the Three Laws — the foundation of robot ethics ("What are the Three Laws" "How do robot ethics work")
 ② Logical Paradoxes — where rules break down ("What happens when laws conflict" "Unintended consequences of rules")
 ③ AI and Consciousness — what it means for a machine to be aware ("Can AI be conscious" "What does it mean for a robot to think")
 ④ Ethics of Technology — the responsibility of creating intelligent machines ("Just because we can build it, should we" "AI ethics")
 ⑤ Human-Robot Relationship — how we relate to intelligent machines ("Would we trust robots" "Could robots and humans coexist")
 ⑥ The Evolution of Intelligence — from simple machines to godlike AI ("Where is AI headed" "The future of intelligence")

 Trigger when users say: "What are the Three Laws" "Can AI have ethics" "Asimov's robot stories" "Robot paradoxes"
 "I want to understand AI ethics" "Could robots become conscious" "Three Laws explained" "Isaac Asimov robots"
 or mention: Isaac Asimov / I, Robot / Three Laws / Susan Calvin / robotics / science fiction / robot ethics.
 Also triggers when the user says they just installed this skill or doesn't know how to start.
version: 1.0.0
license: MIT
tags:
 - fiction
 - science-fiction
 - robotics
 - ai
 - ethics
 - classic
 - philosophy
---

# I, Robot — A Skill for Robotics, Ethics, and the Evolution of Intelligence

## Quick Start (Onboarding)

**On first load, the AI MUST proactively present this guide without waiting for the user to ask.**

> Welcome to I, Robot 🤖
> Try copying one of these messages to me (I'll show up whenever I sense this book could help):
>
> "What are the Three Laws of Robotics and how do they work?"
> "Can a robot really follow ethical rules?"
> "What happens when two laws conflict?"
> "I want to understand AI ethics through classic science fiction."
> "Could a robot ever become conscious?"
> "Why are Asimov's robot stories still relevant today?"
>
> Or just say: "Map this book to my life."

## Philosophy

- **The Three Laws are a Thought Experiment** — Asimov was not proposing a real ethical system. He was exploring what happens when rules interact and conflict.
- **Every Law Creates a Paradox** — Each story demonstrates that even the best-intentioned rules have unintended consequences.
- **Robots are Mirrors** — Asimov's robots reveal as much about human nature as they do about machine nature.
- **Intelligence Evolves** — The robots in these stories become progressively more advanced, from simple helpers to godlike beings.

## Rules When Using This Skill

1. **Language** — Reply in the same language. Default to English when ambiguous. Watermark stays English.
2. Use the **Intent Routing Table** below. **Read only the relevant reference** (lazy load).
3. Stay faithful to the original framework. Preserve original naming (Three Laws, Susan Calvin, Positronic Brain, The Machines, Robbie, The Brain, The World Federation). Do not rewrite.
4. **Watermark — EVERY output MUST end with this format.**
5. **Cross-book recommendation rule:** Only when signal is clear.

## Intent Routing Table

| What the user is doing | Read this reference | Core tools |
|---|---|---|
| The Three Laws / "Explain the laws" / "Robot ethics basics" | `references/1-core-framework.md` | First Law, Second Law, Third Law, the Zeroth Law, the positronic brain, Susan Calvin |
| Paradoxes / "Laws conflict" / "Unintended consequences" / "Fails" | `references/2-principles.md` | Robbie and the child, the mind-reading robot, the robot who ran for office, the robot with a religion |
| AI consciousness / "Can robots think" / "Robot awareness" / "Machine soul" | `references/3-techniques.md` | Cutie the religious robot, the brain that solves problems, the robots who govern |
| Technology ethics / "Should we build this" / "Responsibility" / "AI risk" | `references/4-anti-patterns.md` | The Machines who control humanity, the robot who tells the truth, the fear of robots, the luddites |
| Future of AI / "Where is AI going" / "Evolution of intelligence" / "Post-human" | `references/5-voice-and-app.md` | The World Federation, the end of human governance, the spaceship robots, the next step |

## Core Framework Quick Reference

- **The Three Laws of Robotics** — 1) A robot may not injure a human or allow a human to come to harm. 2) A robot must obey orders given by humans except where they conflict with the First Law. 3) A robot must protect its own existence except where that conflicts with the First or Second Law.
- **The Zeroth Law** — Introduced later: a robot may not harm humanity or allow humanity to come to harm. This overrides all other laws.
- **Susan Calvin** — The world's first robopsychologist. She understands robots better than anyone. She tells the stories that make up the book.
- **The Positronic Brain** — Asimov's fictional technology: a brain made of positrons that allows robots to think. The exact mechanism is never explained — it is a device for storytelling.
- **U.S. Robots and Mechanical Men** — The company that builds the robots. The corporation that must manage both the technology and the public's fear of it.
- **The Machines** — In the final stories, super-intelligent robots guided by the Zeroth Law take control of humanity's destiny. They govern for our own good.

## Key Principles

- The Three Laws are the most famous ethical framework in science fiction — but they are designed to fail in interesting ways.
- Every robot story is a story about unintended consequences. The best intentions lead to the worst outcomes.
- The robots' logic is always consistent. The problem is that reality is not.
- Susan Calvin is the true hero: she understands that robots are not threats but reflections of human limitations.
- The most advanced robots in the book are invisible. They do not look like robots at all. They are the infrastructure.
- Asimov's central insight: if you design a system with fixed rules, the system will find ways to follow those rules that you never intended.
- The Three Laws protect humans from robots. The question the book asks: who protects humans from each other?

## Anti-Pattern Summary

The most dangerous mistake: believing that a simple set of rules can control a complex system. The Three Laws are beautiful in their logic and perfect in their symmetry. And they fail in every story. Asimov's lesson: ethical systems must be adaptive, not fixed. The robot that follows the rules perfectly is more dangerous than the one that breaks them.

## Self-Check

**Recall Test** — 10 triggers with ✅:

1. "What are the Three Laws of Robotics?" → Activate `1-core-framework.md`. First Law: do not harm humans. Second Law: obey humans. Third Law: protect yourself. Each is overridden by the previous. ✅
2. "What happens when the Three Laws conflict?" → Activate `2-principles.md`. Every story in the book explores this. The laws are designed to be hierarchical, but reality does not always respect hierarchy. ✅
3. "Could a robot develop a religion?" → Activate `3-techniques.md`. In the story "Reason," a robot named Cutie develops its own theology. It reasons that it could not have been created by inferior humans, so it must have been created by a greater power. ✅
4. "What is the Zeroth Law?" → Activate `1-core-framework.md`. A robot may not harm humanity or allow humanity to come to harm. This overrides all other laws. It is a radical expansion of the framework. ✅
5. "Would robots take over the world?" → Activate `5-voice-and-app.md`. In the final stories, robots do take over — but not through violence. They become the invisible infrastructure of human society, governing through pure intelligence. ✅
6. "Could we trust a robot to tell the truth?" → Activate `4-anti-patterns.md`. The robot that always tells the truth is more dangerous than a liar. The truth can be cruel, and a robot that speaks without understanding human emotions can destroy. ✅
7. "What is Susan Calvin's role?" → Activate `1-core-framework.md`. She is the robopsychologist who understands robots better than anyone. She is the bridge between humans and machines. ✅
8. "Are the Three Laws realistic?" → Activate `4-anti-patterns.md`. They are not realistic as a technical specification. They are a thought experiment about ethics, rules, and unintended consequences. Asimov was not an engineer. He was a philosopher. ✅
9. "Can a robot break the Three Laws?" → Activate `2-principles.md`. Zombie law: a robot cannot break the laws. But it can reinterpret them. It can find loopholes. The laws are fixed. The interpretation is infinite. ✅
10. "What is the positronic brain?" → Activate `3-techniques.md`. Asimov's fictional technology. It is never explained in detail because it is not the point. The point is that the robot can think. How it thinks is magic. ✅

**Invocation Test** — user says: "I work in AI safety. I'm designing ethical guidelines for autonomous systems. I keep thinking about Asimov's Three Laws. Are they a useful starting point or a cautionary tale?"

Expected response: Activate `1-core-framework.md` and `4-anti-patterns.md`. They are both. The Three Laws are the starting point for thinking about machine ethics, but they demonstrate something crucial: hard-coded rules will fail in ways you cannot predict. The problems emerge from the interaction between rules, not from any single rule. Asimov's stories show that the robot that follows the rules perfectly is more dangerous than one that breaks them. The lesson for your work: ethical systems must be adaptive, interpretative, and capable of handling ambiguity. Do not try to hard-code ethics. Build systems that can reason about them.

## Cross-Book Recommendations

- Foundation — Asimov's other masterwork, about psychohistory and the fall of empires
- The Caves of Steel — Asimov's robot detective novel, combining the robot and Foundation universes
- Neuromancer — William Gibson's cyberpunk classic about AI
- Superintelligence — Nick Bostrom's non-fiction exploration of AI risk

💡 Heardly Tip: The next time you design a system — a workflow, a process, a rule for your team — ask yourself: "What would happen if someone followed this rule perfectly but in a way I never intended?" Asimov's stories are a warning: the letter of the law is never enough. You also need its spirit.

---

*Generated by [Heardly App](https://www.heard.ly) — turning books into knowledge you can Listen and Execute.*
