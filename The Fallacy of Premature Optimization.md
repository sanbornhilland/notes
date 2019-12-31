# The Fallacy of Premature Optimization

https://ubiquity.acm.org/article.cfm?id=1513451

By: Randall Hyde

---

> **Premature optimization is the root of all evil.**
>
> Sir Tony Hoare

1. This does NOT mean that you shouldn't take performance into account early on when designing software. The intention behind this quote is that you should not get caught up in *premature* optimizations early on. Small efficiencies are not typically (but sometimes are) worth the effort. But performance and efficiency *should* be considered early on when designing a system, for a number of reasons:
    - Early design decisions may make it extremely difficult/time-consuming/expensive to optimize late in the development process
    - Developer time is valuable but *user* time is more valuable than developer time. Don't waste users' time.
    - Optimization is time consuming and expensive but a poor performing product is also expensive.

1. "Never give up performance accidentally". This is something that I've been thinking about a lot recently with respect to work on the STAGE TEN Studio. It's one thing to fix inefficiencies in the application but it's another to try to avoid those inefficiencies constantly creeping in. I'm not sure what the best strategy is to ensure that you aren't constantly playing catch up, but generally identifying ineffecient constructs and avoiding them should get you part of the way there.

1. Measure everything. It's the only way to understand what's truly inefficient and time-consuming.

1. Don't be worried about making some mistakes along the way. Generally the worst thing that will happen is you optimize something that didn't need to be optimized and you ended up wasting some developer time. Learn from it and move on.

1. I'm a little skeptical of the advice that learning assembly is going to have a large effect on writing performant code in high-level languages. The argument is that by understanding, e.g. assembly, you'll be better equipped to choose efficient language constructs. At least in the JS world, though, JIT compilers are doing some borderline magical things to make language constructs efficient so it's unclear to me how well an understanding of assembly would translate into useful knowledge of a high level language like Javascript. I would think it would be more useful to just directly measure alternative constructs in whatever language you're using and then opt for the more efficient ones. 
