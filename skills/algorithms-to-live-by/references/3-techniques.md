# 3. Techniques — Sorting, Caching, and Scheduling

> Source: "Algorithms to Live By" by Brian Christian and Tom Griffiths (2016), Chapters 3 (Sorting), 4 (Caching), and 5 (Scheduling).

## Sorting: The Case Against Over-Organization

**The fundamental insight**: Sorting has "steep diseconomies of scale." Sorting 100 items takes more than 2x the time of sorting 50 items. The bigger the batch, the worse it gets.

**The practical approach:**
1. **Bucket Sort first** — Group items by rough category (10 buckets of 10 items each is far faster than 1 set of 100).
2. **Insertion Sort within buckets** — Once you have small groups (≤25), fine-sorting is manageable.
3. **Search beats sort** — For digital items (emails, files), searching is almost always faster than organizing. Simply search.

> **Case: Danny Hillis's Sock-Sorting Nightmare** (Chapter 3): Before inventing the Connection Machine supercomputer, Danny Hillis was an MIT student horrified by his roommate's sock-sorting method: pull one sock, then pull random socks until a match appears. For 10 pairs, this takes 110 pulls. Hillis's solution: buy identical socks so any two match. Eliminate the problem entirely.
> **Key takeaway**: The most efficient sort is to not sort at all. Eliminate the need for sorting before optimizing the sorting process.

> **Case: The Preston Sort Center** (Chapter 3): The King County Library System's Preston facility processes 85,000 books/day using Bucket Sort — books go into one of 96 destination bins based on their branch. This is O(n) linear time: each book is handled once. UC Berkeley student Jordan Ho sorts 150 library books in under 40 minutes by first rough-sorting by call number range (experience tells him which numbers are most common), then fine-sorting within each 25-book group.
> **Key takeaway**: Professional sorters use Bucket Sort instinctively. The same technique works for your closet, garage, or digital files.

## Caching: Forget Proactively

**The LRU principle**: The item you'll need next is the one you used most recently. Use this to decide what to keep and what to discard.

> **Case: Steve Whittaker's Email Research** (Chapter 4): UC Santa Cruz professor Steve Whittaker studied email organization for decades. His finding: people who meticulously file emails into folders spend significant time organizing and get no retrieval benefit. Searching takes the same time whether or not you file. "It's empirical but it's also experiential," he says. "When I interview people, they talk about having wasted a part of their life."
> **Key takeaway**: For digital items, never sort. Search instead. The LRU cache (your inbox) automatically prioritizes what you need.

> **Case: The Colored Tape Decluttering Method** (Chapter 4): A doctor described her approach: "My kids think I'm whacky, but I put a piece of colored tape on everything I use. At the end of the year, anything without tape gets donated." This is a direct physical implementation of LRU cache eviction. Usage, not sentimental value, determines what stays.
> **Key takeaway**: Measure actual usage before deciding what to keep. Your sentiment about an item is a poor predictor of future use.

## Scheduling: The Case Against Multitasking

**Key insight**: Task switching has a cognitive overhead that's invisible but real. Every switch imposes a setup cost — reorienting to the new task, remembering where you left off.

**The three scheduling algorithms:**
- **SPT (Shortest Processing Time)** — Do quick tasks first to minimize average wait time for all tasks.
- **EDD (Earliest Due Date)** — Meet deadlines by prioritizing time-sensitive work.
- **Round-Robin** — Give each task fixed time slices. Ensures fairness but adds switching cost.

> **Case: Andy Grove's SLAC Method** (Chapter 5): Intel CEO Andy Grove used "SLAC" — Specific, Limited, Action-oriented, Continuous — for time management. This is scheduling theory applied to executive life: define the specific task, limit its scope, make it actionable, and do it continuously without interruption.
> **Key takeaway**: The most productive people don't multitask. They batch, prioritize, and protect their focus time. The "sterile cockpit" rule (no non-essential conversation below 10,000 feet) is the same principle: during critical work, eliminate all interruptions.
