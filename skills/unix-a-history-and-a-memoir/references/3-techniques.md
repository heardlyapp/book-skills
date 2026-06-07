# 3 — Techniques

> Source: *UNIX: A History and a Memoir* by Brian Kernighan — practical methods from how Bell Labs and Unix were built.

## Practical Tools

### Technique 1: The One-Page Merit Review

**The Bell Labs evaluation process:** Each year, every MTS wrote — on one side of one piece of paper — what they'd done. Called the "I am great report." The department head added a second page summarizing and assessing.

**To apply:** When reviewing your own work or your team's, force yourself to one page per person. No more. The constraint clarifies what matters.

### Technique 2: The "One-Week" Prototype

Ken Thompson wrote the first Unix in three weeks: one week for the editor, one for the assembler, one for the kernel. "At some point I realized I was three weeks from an operating system."

**To apply:** Set an impossibly tight deadline. If Ken could write an operating system in three weeks on an outdated machine, your team can ship a prototype in one. The constraint forces prioritization.

### Technique 3: The Overnight Build

**The shell and pipes story:** Ken added the pipe system call in an hour. "He describes it as 'super trivial.'" Then he and Dennis upgraded every command on the system in a single night to read from stdin by default.

**To apply:** When adding a new capability, resist the urge to do a phased rollout. If the change is truly good, do it in one sweep. The pain is compressed and temporary.

### Technique 4: The User-as-Co-Creator

Joe Ossanna invented a form, put copies in the stationery room, listed himself as approver, and submitted them. The forms went through. Bell Labs got home phone lines and Teletypes.

**To apply:** Sometimes the system doesn't know what's possible until you create the mechanism. If you need a process that doesn't exist, invent the paperwork yourself. Make it look official.

### Technique 5: The Demo Engineering Protocol

Kernighan needed to demo spell-checking for the CIA director. The actual script was too slow. He ran it ahead of time, captured the output, and wrote a script that just did `sleep 2; cat previously.computed.output`. The demo worked perfectly.

**To apply:** When demonstrating a system, run heavy computations ahead of time and cache the output. The demo should show the *experience* of the system, not the *mechanics*. But be warned: "be wary of what you're seeing" at any demo.

### Technique 6: The Reverse Engineering Method

When the Linotron 202 typesetter arrived with flaky software, Ken Thompson wrote a disassembler for its binary programs "in a couple of hours one evening." Then he and Joe Condon reverse-engineered the proprietary encoding and wrote their own driver.

**To apply:** When a vendor's system isn't working, don't wait for them to fix it. Understand the interface at the binary level and write your own. This is expensive but sometimes the only way forward.

### Technique 7: The Preprocessor Pattern

When Troff couldn't handle mathematics, Kernighan and Cherry wrote Eqn as a separate preprocessor. When Troff couldn't handle tables, Lesk wrote Tbl separately. When Troff couldn't handle figures, Kernighan wrote Pic. The pattern: **don't modify the existing system. Write a translator.**

**To apply:** When your current system lacks a feature, don't hack it in. Write a preprocessor that translates from a domain-specific language into your system's native format. This keeps the core clean and the extensions flexible.
