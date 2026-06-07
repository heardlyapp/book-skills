# 5 — Voice & App

> Source: *UNIX: A History and a Memoir* by Brian Kernighan — voice and application scenarios.

## Kernighan's Voice

1. **Clear, precise, and warm.** The same voice that made K&R C the gold standard of technical writing. No jargon without explanation. No pomposity. You feel like a smart friend is explaining something fascinating.
2. **Self-deprecating humility.** "I was well below average as an intern." "I spent an entire summer trying to write a giant Cobol program... it never worked." The author of multiple classic books presents himself as someone who bumbled into success through luck.
3. **Tasteful storytelling.** Every technical point is wrapped in a story: the calculator upside-down words (grep), the tuxedo-clad OB-GYN (Fauci's birth — wait, that's a different book), the identity matrix code that outraged Hamming.
4. **Reverence without worship.** He clearly adored his colleagues but captures their flaws: Ken's disdain for comments, Dennis's sparse prose, Gary's surgical psychopathy. The heroes are human.
5. **Optimism about individuals, skepticism about institutions.** "The great ideas come from individuals." But Bell Labs was dismantled by corporate short-termism. The tension runs through the book.

## Signature Passages

> "You ain't never the same when the air hits your brain." — *Gary's first rule*

> "The only minor operation is one that someone else is doing."

> "If the patient isn't dead, you can always make him worse."

> "One look at the patient is better than a thousand phone calls."

### From this book specifically:

> "Write clearly — don't be too clever."

> "We don't hire PhD dropouts." — *Sam Morgan, after Kernighan delayed his thesis*

> "I'd spell creat with an e." — *Ken Thompson, asked what he'd change about Unix*

> "The purpose of computing is insight, not numbers." — *Hamming's motto*

> "Collegiality was the genius of the system. Nobody's advancement depended on the relationship with just one boss." — *Doug McIlroy on Bell Labs evaluation*

## Five Application Scenarios

### Scenario 1: The CTO Fighting Feature Bloat

**The situation:** Your product has 50 features, 5 of which do the core job. Each new release adds more toggles. Engineers are unhappy.

**Kernighan's playbook:**
1. Audit every feature against the Unix philosophy: does it do one thing well?
2. Resist the Second System Effect: you don't need to fix everything at once
3. Create a preprocessor layer: let power users compose features through APIs
4. Study how GNU cat accumulated 12 options — then decide what to kill
5. Invest in tools (Make-like automation) that reduce complexity instead of adding code
→ *Reference: The Second System Effect and the GNU cat anti-pattern.*

### Scenario 2: The Startup Founder with Tiny Resources

**The situation:** You have 2 engineers and a shoestring budget. Investors want a prototype in 6 weeks.

**Kernighan's playbook:**
1. Accept the PDP-7 constraint: limited resources force better design
2. You're not building the final product; you're building an editor, an assembler, and a kernel
3. Set a 3-week deadline. Ship the absolute minimum. Ken did it with 4K words of memory.
4. "The only minor operation is someone else's" — everything you're doing is major right now
5. Don't build for scale you don't have yet

### Scenario 3: The Manager Building an Engineering Team

**The situation:** You're hiring your first 10 engineers. You want a culture of quality.

**Kernighan's playbook:**
1. Hire athletes, not first basemen: look for broad curiosity, not narrow expertise
2. Create the Unix room: a shared space where serendipity happens
3. Institute the one-page "I am great report" — everyone documents their year on one page
4. Make Doug McIlroy your culture: someone who reads everything and gives generous criticism
5. Protect the team from quarterly thinking: stable funding, long view
6. Support book-writing: people who write well think clearly

### Scenario 4: The Product Leader Needing to Simplify

**The situation:** You're in a feature war with a competitor. Your roadmap is 18 months of new features.

**Kernighan's playbook:**
1. Ask: what's our CTSS (our current success that works)?
2. Don't build your Multics (don't try to add everything at once)
3. Build your Unix instead: what's the PDP-7 version of this product?
4. Pipes over monoliths: design for composition, not for doing everything
5. Text as universal interface: design data formats that any tool can process

### Scenario 5: The Young Developer Finding Their Path

**The situation:** You just started in tech. Everyone around you seems smarter. You don't know what to specialize in.

**Kernighan's playbook:**
1. The butterfly effect: Kernighan's entire career was "lucky accidents" — a missed course, a wrong turn, a chance meeting
2. You don't need to know what you want to be. Try things. Summer internships, side projects, visiting different teams.
3. "I gradually drifted into other areas: document preparation software, specialized programming languages, and a bit of writing."
4. The best programmers (Ken, Dennis) didn't plan their careers. They just followed what was interesting.
5. Find your office neighbors — the people whose work excites you.
