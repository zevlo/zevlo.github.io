---
layout: post
title: "Why DevOps: The Phoenix Project"
date: 2025-10-20
image: /assets/images/phoenix-cover.png
---
In my last post, I wrote about the Office of Warfighting Advantage (OWA) and the years I spent helping Navy commands learn faster than their problems could compound. That office anchored the final stretch of a decade supporting the Navy. I closed with a promise: next up, why I chose this path.

The honest answer begins with a novel.

In 2013, Gene Kim, Kevin Behr, and George Spafford published *The Phoenix Project*, a business novel that teaches DevOps by embedding it inside a failing company instead of a textbook. It is modeled on Eliyahu Goldratt's manufacturing classic *The Goal*: a plant-floor turnaround story rewritten for information technology.

I expected a book about servers and release pipelines. What I received was a book that described the same methods the OWA uses to build a culture of continuous learning and solve complex operational problems.

## A Business Novel, Not a Textbook

<div style="display: flex; justify-content: center;">
    <img src="/assets/images/phoenix-cover.png">
</div>

The setup: Parts Unlimited, a mid-market auto-parts manufacturer and retailer, is losing to online competitors. The CEO's bet for survival is **Project Phoenix**, a massive retail and e-commerce overhaul that is late, over budget, and technically unstable. Bill Palmer, a mid-level ops manager, is promoted to VP of IT Operations with a brutal mandate: ship Phoenix in ninety days, or the IT organization gets outsourced.

Bill inherits the wreckage. Development and Operations are at war. Security shows up at the end of every project to block the release. Almost every fire routes through one indispensable engineer named Brent. Work arrives from every direction with no single queue and no shared picture of capacity.

A board member named Erik Reid becomes Bill's mentor, and he refuses to talk about technology. Instead, he treats IT like a factory: there is a value stream, there are bottlenecks, and optimizing one team while starving the whole system is how companies die.

The authors later compressed the entire argument into one sentence: **DevOps is the result of applying Lean principles to the IT value stream.**

## Theory of Constraints: The Hero Is the Problem

Early in the book, Erik asks Bill a question that rewires him: where is your bottleneck?

At Parts Unlimited, the answer is Brent. Brent is the senior engineer who holds the tribal knowledge of decades of systems. When anything breaks, Brent gets pulled in. Every team believes its request is the exception that deserves his time. The result: the throughput of the entire organization is limited by how fast one man can context-switch.

The book borrows this directly from Goldratt's **Theory of Constraints**. Every system has exactly one constraint at a time, and that constraint sets the throughput of everything. The rule is stated plainly:

**Any improvement made anywhere besides the bottleneck is an illusion.**

Making a non-bottleneck faster does not increase throughput. It just piles more work up in front of the bottleneck. Goldratt's **Five Focusing Steps** provide the treatment:

1.  **Identify** the constraint.
2.  **Exploit** it. Only the highest-value work gets through.
3.  **Subordinate** everything else to that decision. Other work waits.
4.  **Elevate** the constraint. Document, automate, pair, get it off the critical path.
5.  **Repeat**. Inertia will quietly create a new bottleneck.

I used this playbook during a Kaizen event with Naval Special Warfare. We spent a week inside their inter-deployment training and maintenance cycle. We mapped where work actually queued, identified the constraint, and restructured the cycle around it. The people, the gear, and the mission stayed the same; the flow of work is what changed.

## WIP: The Silent Killer

Once you can see the constraint, a second villain comes into focus: **work in process** (WIP), all the work that has been started but not yet finished.

WIP is a silent killer because it feels like progress. Every started project feels like momentum. But unfinished work creates queues, handoffs, context-switching, and delay. The question that matters: how quickly can the bottleneck resource consume the work?

This is why Kanban boards carry explicit **WIP limits** to keep unfinished work from silently drowning the system. Reduce the batch size, finish the work in flight, and cycle times collapse without adding a single person.

The book's counterintuitive lesson became one of my favorite rules: **being able to take needless work out of the system is more important than being able to put more work into it.**

## Unplanned Work: The Capacity Thief

Erik forces Bill to catalog everything IT actually does. The list falls into four buckets, the **Four Types of Work**, and most organizations only manage the first:

*   **Business projects**: the funded, visible work meant to create customer value. Phoenix itself.
*   **Internal IT projects**: infrastructure, upgrades, security, technical-debt paydown. Easy to defer until they explode.
*   **Changes**: the daily stream of deployments, patches, and tickets that keep systems alive.
*   **Unplanned work**: incidents, rework, firefighting.

The fourth type is the one that ruins everything. Unplanned work is the most destructive type of work because it doesn't just add to the pile; it steals capacity from the other three. Every outage pays for itself by quietly killing a project milestone nobody will miss until the deadline. Every commitment made while firefighting is a lie the team doesn't know it told.

The book gives the root cause a name I think about constantly: **technical debt**. Every shortcut, every undocumented system, every "we'll fix it later" is a loan. And debt compounds. If an organization stops paying it down, eventually every calorie in the organization is spent just paying the interest. The interest payments arrive as unplanned work.

## Systems Thinking: The Goal Is the Whole

All of these ideas roll up into the philosophy Erik hammers from the beginning: **systems thinking**. Always confirming that the entire organization achieves its goal, not just one part of it.

The opposite of systems thinking is local optimization, and it is seductive because every local metric improves. A development team hits every sprint goal by throwing untested batches over the wall to Operations. A security team blocks risky change and racks up zero findings. Each silo is winning. The system is losing.

The book makes this concrete with a definition of IT Operations that could double as a mission statement:

> Ensure the fast, predictable, and uninterrupted flow of planned work that delivers value to the business, while minimizing the impact and disruption of unplanned work, so you can provide stable, predictable, and secure IT service.

Notice what that definition says the job is. The job is **flow**: the throughput of the entire system.

## Improvement Kata: Getting Better at Getting Better

The last concept closed the loop for me.

Erik's most counterintuitive claim: **improving daily work is more important than doing daily work.** Teams treat improvement as a luxury for when there is spare time. Improving how work flows is what creates capacity in the first place. It is the exit from the unplanned-work death spiral.

The mechanism is Mike Rother's **Improvement Kata**: short, repeating improvement cycles on a fixed cadence (two weeks of plan, do, check, act), run forever. Small, safe experiments. Blameless learning from failure. **Standard work**, documented, so every improvement compounds into collective knowledge instead of evaporating. The Navy's nuclear propulsion program has run on exactly this logic for decades: rigorous standard work, so the knowledge lives in the system even when the expert transfers.

<div style="display: flex; justify-content: center;">
    <img src="/assets/images/kata.png" style="margin-top: 5px;">
</div>

The lineage runs from Taiichi Ohno's Toyota factory floor through Steven Spear and Mike Rother's research to Goldratt's constraint math, and, it turns out, through the Office of Warfighting Advantage.

## Why DevOps

Near the end, the book names its own philosophy, the **Three Ways**: **flow** (optimize the whole system), **feedback** (find problems at the source), and **continual learning and experimentation** (build a culture that can fail small and learn fast). Everything I have described here is one of those three in disguise.

In my last post, I asked two questions: How do you build systems that learn faster than they fail? How do you create environments where people surface problems instead of hiding them?

The Phoenix Project was the first place I found those questions being asked about software, and answered with daily practice. DevOps is the discipline of answering them for technology: making work visible, limiting WIP, protecting the constraint, converting unplanned work into signal, and improving the way work improves.