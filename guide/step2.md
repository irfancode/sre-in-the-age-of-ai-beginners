---
title: "Step 2 — Write Your First SLO"
description: "One number you can defend: '99.9% of the time, X happens in Y seconds.' The collar around your worry."
layout: default
---

<div class="chapter-meta"><b>Time:</b> 15 minutes. <b>You need:</b> the service name from [Step 1](step1/).</div>

<h1>Step 2 — Write Your First SLO</h1>

<p>An <b>SLO</b> (service level objective) is just this:<br><br>
<b>"In a month, this should work X% of the time, and when it works it should do it in Y seconds."</b><br><br>
You set it. You measure it. That's the whole contract with yourself — nothing you can get in trouble for, no vendor menu to memorize. It is the collar your worry wears [full book: Chapter 4–5](https://irfancode.github.io/sre-in-the-age-of-ai/book/part2/ch04/).</p>

## Why "one number" is the point

An SLO where someone can compute "were we good this month? yes/no" is a **concrete SLO**. A sentence like "we should really stay available" is a **vibe**, and vibes can't be paged at 3 a.m. with any authority. One number turns a feeling into a ledger:

```
Good in a month  =  the count of good requests ÷ all requests
Targets         =  99.9% good, 95% of the time it answers within 2000 ms
```

## The 2026 upgrade (why your AI teammate loves this)

This number is now also the **trust budget** your agents spend (full book [Part V](https://irfancode.github.io/sre-in-the-age-of-ai/book/part5/)). When you write a precise SLO, you've handed the machines a *legible promise* — they can draft dashboards, de-dup alerts, and rehearse responses *against a number*, instead of against a guess. You are not making their life harder; you are making your judgment legible to them, which is the entire modern trick.

## Write yours (the template)

> "Between Jun 1 and Jun 30, **{the service}** will be healthy **{99.9%}** of the time, and **{95%}** of those moments it will finish as fast as **{2 seconds}**."

Fill the three `{braces}`. If a brace makes you stall, use the default already written — you can always tighten later. Done is better than perfect [full book: Ch 6](https://irfancode.github.io/sre-in-the-age-of-ai/book/part2/ch06/).

<div class="callout good">
<span class="faint"><i class="fa-solid fa-lightbulb"></i> Key insight</span>
<p><b>The SLO is the number you choose to be honest about — not a score you're graded on.</b> If you're never hitting it, the answer is never "lie better"; it's "this service deserves a lower target (and a plan)." The number keeps you honest, and the honesty is what your sensors and your agents get to trust.</p>
</div>

<p><a href="step3/"><b>Next: Step 3 — Measure the real thing</b></a> →</p>