# 1 — Core Framework

> Source: *UNIX: A History and a Memoir* by Brian Kernighan — distributed across all 9 chapters.

## The Five Frameworks

### Framework A: The Bell Labs Model (Chapter 1)

The organizational conditions that made Unix possible:
- **Stable funding**: AT&T's monopoly and regulatory regime meant ~0.3% of phone call revenue funded basic research. No proposals, no quarterly reporting.
- **Bottom-up innovation**: "Projects in 1127 were not assigned by management, but grew from the bottom up." No one told anyone what to work on.
- **Technical management**: Sam Morgan (director) knew every MTS by name and their work. Doug McIlroy was a world-class programmer who managed by being the first user of everything.
- **Collegial evaluation**: Merit review was non-competitive. "Rather than 'My people are better than your people,' the tone was 'Don't forget this other good work that your person did.'"
- **Private offices + shared space**: Private offices for focus; the Unix room for serendipitous collaboration.

> **Case: The Ken Thompson Hiring** (Chapter 2): Ken explicitly didn't want to work for a company. He ignored 6-8 recruiting attempts. The recruiter showed up at his door. Ken agreed to visit only to see high school friends. But when he saw the names on the doors — he knew every one from literature — he accepted the same day. Great hiring sells itself.

### Framework B: The Unix Philosophy (Chapters 3-9)

Doug McIlroy's four maxims (1978):
1. **"Make each program do one thing well."** To do a new job, build afresh rather than complicate old programs.
2. **"Expect the output of every program to become the input to another."** Don't clutter output. Avoid binary formats.
3. **"Build and try early, ideally within weeks."** Don't hesitate to throw away clumsy parts and rebuild.
4. **"Use tools in preference to unskilled help."** Automate. Even if you have to build the tools first.

> **Case: Grep** (Chapter 4): Ken wrote grep months before telling anyone. Doug asked: "Wouldn't it be great if we could look for things in files?" Ken: "Let me think about it overnight." The next morning he showed Doug the program he'd already written. The hardest part was naming it. Grep has since become a noun, verb, and OED entry.

### Framework C: The Second System Effect (Chapter 2)

After a success (CTSS), the temptation to create a "better" system that fixes everything and adds everyone's favorite features. The result: over-engineered, late, expensive, and disappointing (Multics). The lesson: "Don't try to climb too many trees at once."

Unix was the anti-Multics: stripped down, minimal, built for what was available, not what was imagined.

> **Case: Multics vs UNIX** (Chapter 2): Multics tried to create an "information utility" serving everyone — GE, MIT, Bell Labs, three locations, big budgets, ambitious specs. It failed on cost. Unix was one guy in an attic with a PDP-7. "Ken was three weeks from an operating system" while his wife was on vacation.

### Framework D: Constraints as Creativity (Chapters 2-4)

The PDP-7 had 8K 18-bit words of memory (4K kernel, 4K user). This scarcity forced:
- Short command names (because Model 33 Teletypes required physical force to type)
- Simple programs that composed via pipes (no memory for monolithic programs)
- Minimalist kernel that did only what was essential
- The C language itself — "squeezed into 8K bytes of memory and filtered through Thompson's brain"

> **Case: The C Language** (Chapter 4): "C is quirky, flawed, and an enormous success." It was designed not as an ideal language but as one that fit the PDP-11's byte-oriented architecture, could be compiled with limited resources, and was close enough to the machine to be efficient. The constraint of the hardware shaped the language that now runs the world.

### Framework E: Programs That Write Programs (Chapters 5-6)

The book's most powerful meta-idea: the best way to make software is to create tools that create software.
- **Yacc**: "Yet Another Compiler-Compiler" — given a grammar, it generates a parser. Enabled dozens of languages.
- **Lex**: Given patterns, generates a lexical analyzer.
- **Make**: Given dependency specifications, automates compilation.
- **Shell scripts**: "If you find yourself doing the same sequence of commands over and over again, put them into a shell script."

> **Case: The Cat Command** (Chapter 3): Cat has barely changed in 50 years. But today's GNU version has 12 options for tasks easily handled by other tools. "It seems counter-productive to complicate a fundamental tool." The original Unix instinct — do one thing well — is under constant threat even by its own community.
