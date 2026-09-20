---
title: "Step 4 — Write One Runbook"
description: "The 6-line document that turns 'I panic' into 'I follow the card.' Your first grown-up reliability artifact."
layout: default
---

<div class="chapter-meta"><b>Time:</b> 15 minutes. <b>You need:</b> the service from [Step 1](step1.html).</div>

<h1>Step 4 — Write One Runbook</h1>

<p>A <b>runbook</b> is the 6-line note you write <i>now</i> so future-you (at 3 a.m., tired) doesn't have to think. Professional speak: "the documented, rehearsed response to a known failure." Honest speak: <b>"when THIS goes wrong, do THESE three things, in THIS order."</b> It is the ancestor of every AI agent's safety plan, and the original [Part VII](https://irfancode.github.io/sre-in-the-age-of-ai/book/part6/) of the full book builds from exactly this choreography.</p>

## The 6-line template (print-friendlier than you'd guess)

```markdown
# Runbook: {Service name} — {one known failure}

TRIAGE  (2 min): 
  Is it REALLY down, or just slow?  [the sensor from Step 3]

DO (in order): 
  1. {first action — e.g. "restart the queue worker"}
  2. {second — e.g. "toggle the canary flag off"}
  3. {third — e.g. "roll back the last deploy"}

IF STILL BROKEN after the 3 steps:
  page the human; say the words from Step 3's dashboard. 
  (Nobody guesses at 3 a.m. — we follow the card.)

AFTER: 
  paste the timeline into [your blameless review](step5.html). Done.
```

## The 2026 rule that makes it shine

The modern version of a good runbook is the one your **AI teammate can also read**: each action is one searchable step ("restart", "toggle flag"), each links to where the receipt lives, and there's a clear "who approves the irreversible bit" line. The machines will draft 90% of this for you and rehearse it; the *human decision inside it* ("is this worth rolling back, or do we ride through?") remains yours [full book: Ch 31–34](https://irfancode.github.io/sre-in-the-age-of-ai/book/part5/).

<div class="callout good">
  <span class="faint"><i class="fa-solid fa-lightbulb"></i> Key insight</span>
  <p><b>The runbook is the shortest distance between "I don't know" and "I'm following the plan."</b> You don't need one for everything — one good card for your one named service is a month ahead of "we'll figure it out live." Future-you silently loves you for writing this today.</p>
</div>

<p><a href="step5/"><b>Next: Step 5 — do your first blameless review</b></a> →</p>