# 4 — Anti-Patterns

> Source: *UNIX: A History and a Memoir* by Brian Kernighan — failures and traps from the Unix story.

## Common Mistakes Exposed

### Anti-Pattern 1: The Second System Effect

**The trap:** After a success, you try to build the "perfect" version that fixes everything and includes everyone's favorite features.

**Why it fails:** You "climb too many trees at once." The result is over-engineered, late, and disappointing. Multics was the textbook case — took on too much, failed on cost, never achieved its goal.

> **Case: Multics** (Chapter 2): "Multics was intrinsically a challenging prospect, and it soon ran into problems." The "second system effect": after CTSS (a success), Multics tried to add everything. "The phrase 'over-engineered' appears in several descriptions." Bell Labs dropped out in April 1969. The lesson: after success, resist the urge to fix everything. Pick one thing.

### Anti-Pattern 2: The "It Must Be Important" Trap

**The trap:** Only work on things that management explicitly asks for. Assume that if no one tells you to do it, it's not valued.

**Why it fails:** The most important work at Bell Labs was never assigned. None of the Unix-related breakthroughs were management directives. "Projects were not assigned by management, but grew from the bottom up."

> **Case: Belle Chess Computer** (Chapter 2): A visitor asked Bill Baker (president of Bell Labs) why they supported computer chess. Baker defended it on the spot — special-purpose computers, new design tools, visibility. But Ken Thompson never asked permission. He just built it. The lesson: if you need permission, you'll never build anything that changes the world.

### Anti-Pattern 3: The Feature Creep Spiral

**The trap:** Each release adds more options, more toggles, more configuration. Users ask for it. Competitors have it.

**Why it fails:** The GNU version of `cat` now has 12 options for tasks that existing tools handle. "All of those are easily handled with existing programs; none has anything to do with the core task of copying bytes." The tool has become a kitchen sink.

> **Case: Cat vs the 12 Options** (Chapter 9): "The cat command hasn't changed in 50 years, aside from acquiring a few optional and probably unnecessary arguments." This is the constant pressure: every feature addition seems harmless in isolation. It kills simplicity by a thousand cuts.

### Anti-Pattern 4: The Closed Innovation Model

**The trap:** Keep your technology proprietary. Control all access. Extract maximum value through licensing.

**Why it fails:** AT&T's restrictive licensing of Unix (after giving it away to universities) created a market vacuum that Linux filled. By trying to commercialize and control, AT&T lost the ecosystem — and ultimately the market.

> **Case: AT&T vs BSD** (Chapter 8): After divestiture, AT&T tried to monetize Unix aggressively. The lawsuit against Berkeley over intellectual property backfired. Berkeley rewrote the AT&T code, released it freely, and the community radicalized toward open source. "AT&T was trying to lock the barn door after the crown jewels had flown the coop."

### Anti-Pattern 5: Quarterly Thinking vs Long-Term Building

**The trap:** Plan in 3-month cycles. Focus on quarterly results. Shift priorities frequently.

**Why it fails:** Bell Labs' most productive era was built on 30-year horizons. The transistor, Unix, C — none of these would have been created under quarterly planning. "Stable funding was a crucial factor."

> **Case: The Decline of Bell Labs** (Chapter 7-8): After divestiture, AT&T's focus shifted to short-term commercial results. The company split, split again, was bought, merged. By 2005, 1127's number was retired. The research model that produced Unix was dismantled not by failure, but by the corporate pressure for shorter-term returns.
