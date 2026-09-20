---
title: "Step 1 — Name Your One Service"
description: "The 'which door do I guard' question. Pick the single service whose uptime matters most, in 10 minutes."
layout: default
---

<div class="meta"><span><i class="fa-solid fa-clock"></i> 10 minutes</span><span><i class="fa-solid fa-tag"></i> Gives you: ONE service name, written down</span></div>

<h1>Step 1 — Name Your One Service</h1>

<p>Ask your human (or a friend) the embarrassing question every beginner wants answered but is afraid to ask: <b>"If the building catches fire, which one door do I guard?"</b> In SRE terms, that's <b>"what one service, if it went down, would users actually notice?"</b></p>

<p>The SLO discipline works best when you start tiny. You are not measuring a whole platform; you are measuring <b>one service</b> — one URL, one function, one queue of work that a real user touches. If you can't name it in a sentence, you're not ready for a number yet.</p>

## Pick it with this filter

| The question | A good answer feels like | A bad answer feels like |
|---|---|---|
| Who touches it? | "Our customers open it to log in" | "It's part of our micro-architecture" |
| What breaks first? | "A user can't get in" | "Technically there's a latency bloom" |
| Is it yours to guard? | "I/we own it" | "Someone else runs it and I'm just watching" |

<div class="callout good">
<span class="faint"><i class="fa-solid fa-lightbulb"></i> The under-10-line version</span>
<p><b>Name it, own it, sentence it.</b> Write one sentence like: <i>"The login service is the door; if a customer can't log in, they can't use us at all."</i> That one sentence IS your mission statement for the whole exercise. If the sentence requires three clauses, shrink the service.</p>
</div>

<p>When you have it, you're ready for <a href="step2/">Step 2 — write the SLO (the one honest number)</a> →</p>