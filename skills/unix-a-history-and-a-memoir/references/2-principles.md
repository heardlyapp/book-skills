# 2 — Key Principles

> Source: *UNIX: A History and a Memoir* by Brian Kernighan — synthesized from the entire book.

## The 8 Principles

### 1. Write Clearly — Don't Be Too Clever

The first rule from *The Elements of Programming Style*: "Write clearly — don't be too clever." The identity matrix example (DO 14 I=1,N / DO 14 J=1,N / 14 V(I,J)=(I/J)*(J/I)) is clever. The simpler version (set row to 0, set diagonal to 1) is better. This applies to code, documentation, and design.

> **Case: The Identity Matrix** (Chapter 1): The clever one-liner relied on integer division truncation — a technique that would confuse any reader. The simple version was 4 lines and obvious. Hamming's reaction to the original — "all up in arms" — set the standard.

### 2. Invest in Tools That Compound

Yacc, Lex, Make, pipes — each tool multiplied the productivity of everyone who followed. The at command was hacked together in an evening and is still used 40 years later. The question isn't "should I build a tool instead of shipping?" It's "will this tool be used more than once?"

### 3. Remove Code, Don't Add It

"Productivity was often measured by the number of special cases or lines of code that were removed." Dennis's C reference manual is admired for its spine-tingling precision — every word carries weight.

### 4. Physical Proximity Is Strategy

Kernighan spent 30 years in the same office. His neighbors included Ken Thompson, Dennis Ritchie, Bob Morris, and Joe Ossanna. "It's easier to collaborate with people who are physically close." The Unix room was the serendipity engine.

### 5. Read Everything. Criticize Generously.

Doug McIlroy read drafts of every paper, manual, and book from 1127. He "deftly punctured rhetorical balloons, cut flabby prose, weeded out unnecessary adverbs." This wasn't a role; it was a culture. "Doug was the first person to try out some new program or idea."

### 6. Good Management Gets Out of the Way

"Researchers had the freedom to explore areas that might not have a near-term payoff and perhaps never would." Ken was never told what to work on. Bill Baker defended Belle (the chess computer) to a visitor who questioned its relevance to telephones. The manager's job is to protect the team's focus.

### 7. Badges and Bureaucracy: Resist Thoughtfully

When Bell Labs required badges, colleagues protested creatively: super-gluing badges to foreheads, wearing them on chest hair. They created a fake person (Grace R. Emlin) who had her own login, badge, and official appearances. Pushback against pointless rules is a sign of organizational health.

### 8. Write Books, Not Just Code

1127 published an extraordinary number of influential books: the Dragon book, K&R C, Programming Pearls, C++ books, Unix manuals. Writing was supported (6 months full-time), valued (kept royalties), and reviewed (Doug's critique). Books recruited talent and built reputation.

> **Case: The Dragon Book** (Chapter 5): Al Aho and Jeff Ullman's *Principles of Compiler Design* became a standard text for a generation. The bell Labs connection — researchers writing textbooks — was unusual for an industrial lab but it made the Labs visible to students who became the next generation of hires.
