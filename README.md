# More, Better, Faster: What Changed?

*A software architect's reflection on Scope, Quality, and Speed*

**Shailendra Negi**  
**Version:** 1.0 | **November 2026**

When I think about software delivery, I keep coming back to three expectations:

**Deliver more. Deliver better. Deliver faster.**

Individually, each expectation makes sense. But what happens when we expect all three to improve at the same time, without changing how the team delivers software?

That question led me to think about delivery through three dimensions: **Scope, Quality, and Speed**.

## The three dimensions

- **Scope: How much we deliver.** The functionality and requirements included in a delivery, together with their complexity. Feature count alone is not a reliable measure of scope: one complex change may require more effort than several small ones.
- **Quality: How well we deliver.** Correctness, reliability, security, maintainability, performance, and the confidence with which software can evolve. Quality is more than the absence of defects.
- **Speed: How quickly we deliver.** The time it takes to turn agreed work into usable software. Speed should not be confused with simply keeping people busy or counting deployments.

![A triangle showing Scope, Quality, and Speed, with delivery capacity and capability at its center](diagrams/scope-quality-speed.svg)

## My initial hypothesis

My first instinct was a simple "pick two" rule: if a team increases two dimensions, the third comes under pressure.

There is some truth in that intuition, but it needs an important qualification.

**When a team is operating near its effective delivery capacity, and its engineering capability and other constraints remain broadly unchanged, pushing harder on two dimensions can limit what is achievable in the third.**

Consider the three combinations:

| If we push for... | The likely pressure is on... |
| --- | --- |
| **More Scope + Greater Speed** | **Quality**, if the additional work outpaces the team's ability to design, test, and validate it. |
| **More Scope + Higher Quality** | **Speed**, if the additional engineering work cannot fit into the same schedule. |
| **Higher Quality + Greater Speed** | **Scope**, if focusing on fewer changes is necessary to deliver safely and sooner. |

These are **trade-off risks, not guaranteed outcomes**. The third dimension does not automatically decline. Nor should essential security, correctness, or reliability standards become negotiable simply because a deadline is ambitious.

## A hypothetical delivery scenario

Imagine a team that typically delivers ten similarly sized features in eight weeks.

For the next release, the expectations change:

- Deliver fifteen features.
- Finish in six weeks.
- Reduce production defects.

The expectations may be reasonable aspirations. But if team capacity, complexity, dependencies, tools, and engineering practices remain broadly the same, there is a gap between the ambition and the current delivery plan.

The question I would ask is not merely, "Can we commit to these targets?"

**It is: "What has changed in our engineering capability to make these expectations achievable?"**

If nothing has changed, we need to revisit the scope, schedule, assumptions, or investments required to deliver.

## The part that changed my thinking

The more I considered the triangle, the less convinced I became that it should be a rigid "pick two" rule.

Engineering capability is not fixed forever. Even with the same team size, we can change the system in which the team works:

- Automated testing can shorten feedback cycles and catch defects earlier.
- Clearer architecture and reusable components can reduce the effort needed for changes.
- Smaller batches and continuous delivery can make releases quicker and safer.
- Better observability can help teams detect and recover from failures faster.
- Simpler requirements and fewer dependencies can remove work that adds little value.

In other words, **all three dimensions can improve when we change the constraints**. Teams may also have unused capacity or inefficiencies that allow improvement before a hard trade-off emerges.

This is consistent with [DORA's research](https://dora.dev/guides/dora-metrics/), which finds that software delivery speed and stability do not have to be opposing goals.

So the triangle is more useful to me as a **planning conversation** than as a law.

## The question behind the triangle

When someone asks for more features, better quality, and faster delivery, I would rather make the assumptions visible than argue that one of the three must fail.

What are we changing? Are we reducing complexity, improving architecture, automating validation, removing dependencies, adding capacity, or adjusting the plan?

If the answer is "nothing," we should be careful about promising a different outcome from the same delivery system.

**Delivery pressure is not delivery capability.**

## A note on related thinking

I arrived at this perspective while reflecting on engineering trade-offs, including the style of reasoning that makes the CAP theorem memorable. But **this is not an extension of CAP or an impossibility theorem**. CAP addresses specific guarantees in distributed systems under network partitions; software delivery trade-offs are contextual rather than absolute.

The underlying ideas also overlap with the established project-management triangle and existing discussions of velocity, scope, and quality. I am not claiming to have invented those concepts. This article is my interpretation of how they apply to engineering delivery under constrained capacity.

For further reading:

- [Project Management Institute: Managing the triple constraints](https://www.pmi.org/learning/library/managing-challenges-triple-constraints-6884)
- [Anthony Fu: Velocity, Scope, and Quality](https://antfu.me/posts/mental-health-oss)
- [DORA: Software delivery performance metrics](https://dora.dev/guides/dora-metrics/)
- [Eric Brewer: Inside Cloud Spanner and the CAP theorem](https://cloud.google.com/blog/products/databases/inside-cloud-spanner-and-the-cap-theorem)

## Closing thought

The challenge is not deciding which dimension to sacrifice.

It is understanding what limits us today, making deliberate trade-offs, and improving the engineering system so that better outcomes become possible tomorrow.

**Raising expectations is easy. Raising capability takes engineering.**

---

## License and attribution

© 2026 Shailendra Negi.

The original article and diagram in this repository are licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are welcome to share, use, adapt, and build upon them, including commercially, under the terms of that license. When redistributing the material or an adaptation, give appropriate credit, link to the license, and indicate if changes were made. Attribution must not suggest endorsement by the original author.

**Suggested attribution:**

> Based on [*More, Better, Faster: What Changed?*](https://github.com/shailendranegi/scope-quality-speed) by Shailendra Negi, licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Changes made: [brief description, if applicable].

The license covers the author's original expression and diagram, not ownership of the underlying software delivery concepts. See the [LICENSE](LICENSE) file for details.
