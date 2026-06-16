# Caching and Memory: The Art of Forgetting

This reference covers the computer science of caching—how systems (both machines and minds) manage limited memory by strategically forgetting. The book's central insight: forgetting is not failure; it's optimization.

## How Computer Memory Works (and What It Teaches Us)

Computer memory is organized in a hierarchy. The fastest memory (CPU registers, L1 cache, L2 cache, RAM) is small and expensive. The slowest (hard drives, cloud storage) is large and cheap. When a processor needs a piece of data, it checks the fastest memory first. If the data isn't there (a "cache miss"), it fetches from slower memory and stores a copy in the fast cache for next time.

The key question: when the cache is full and new data needs to come in, which old data gets evicted? The default answer: the Least Recently Used (LRU) item. This is the optimal strategy because of "temporal locality"—if you used a piece of data recently, you're likely to need it again soon.

### Case 1: Steve Whittaker and the Email Organizing Folly

Steve Whittaker, an IBM research scientist and UC Santa Cruz professor, has studied email management for over two decades. His landmark 2011 paper asked a provocative question: "Am I Wasting My Time Organizing Email?" The answer was emphatically yes. People who meticulously file emails into folders spend about the same time filing as sorting physical papers. But emails can be searched in seconds—unlike physical files.

Whittaker's study found that "filers" didn't perform better than "pilers" (people who leave everything in their inbox) in finding old emails. The search cost of email is essentially zero, making the sorting cost a pure waste. His personal approach: "It's empirical, but it's also experiential. When I interview people about these problems, that's something they characteristically talk about—that they sort of wasted a part of their life."

The LRU principle applies directly: your inbox naturally surfaces the most recently used emails (temporal locality). Searching handles everything else. The most efficient strategy: don't touch your email filing system. Just search.

### Case 2: The Closest Cache Study

A study on how people organize their homes reveals the same LRU principle at work. Researchers found that the best predictor of how frequently people used an item was how recently they had last used it—not how much they liked it, not its sentimental value, not how much it cost. Items used in the last month were used again in the next month. Items unused for a year were unlikely to ever be used again.

This suggests a practical rule for decluttering: if you haven't used something in the past year, get rid of it. Your future usage pattern will match your past usage pattern with high probability. The problem is that people keep items based on potential future need rather than actual past use—a violation of the LRU principle. The optimal strategy for closets is the same as for computer caches: evict what you haven't touched recently.

A related insight from the book: a doctor described her approach: "My kids think I'm whacky, but I put a piece of colored tape on everything I use. At the end of the year, anything without tape gets donated." This is a direct implementation of LRU-based cache eviction.

### Human Memory as a Caching System

Psychologists have long observed the "recency effect"—people remember the last item in a list better than items from the middle. This maps perfectly onto LRU cache behavior: the most recently accessed memories are the most readily retrieved.

But there's a deeper point. Our brains have limited storage and retrieval bandwidth. Forgetting isn't a bug; it's a feature that allows us to focus on what's relevant now. The book shows that computer cache design and human memory face the same fundamental tradeoffs: capacity vs. speed, freshness vs. persistence.

The "spacing effect" in psychology (you learn better by spacing out practice sessions) is mirrored in computer science's cache prefetching strategies. Both systems benefit from distributing "refreshes" over time rather than cramming.

### Practical Takeaways

- **Email**: Don't file. Search instead. This alone can save hours per week.
- **Closets**: Keep recently-used items accessible. Donate untouched items after one year. Use visual tracking (colored tape) to measure actual usage.
- **Workspace**: Keep only current projects visible. Archive everything else. Your desk is your L1 cache.
- **To-do lists**: The LRU principle suggests that tasks you haven't thought about for a while are least likely to be done. Periodically review and purge rather than accumulating indefinitely.
- **Learning**: Space out practice. Distributed practice trumps massed practice because it forces your memory cache to be refreshed rather than just kept hot.
- **Relationships**: The LRU principle also applies: the friends you talk to most recently are the ones you're most likely to talk to again. If you want to maintain a relationship, reach out regularly—otherwise LRU eviction is inevitable.

### Connection to Overfitting

Caching decisions are essentially overfitting decisions at the memory level. Keeping too much information (never forgetting) leads to a cluttered mind that overfits to irrelevant details. Forgetting systematically (by recency, not by importance judgment) is a form of regularization that improves decision quality.

---

*Source: "Algorithms to Live By" (2016), Chapter 4: Caching, and interviews with Steve Whittaker and others.*
