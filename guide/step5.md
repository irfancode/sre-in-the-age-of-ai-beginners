---
title: "Step 5 — Do Your First Blameless Review"
description: "Look back on the week without blaming anyone (including yourself), and write one next-action. 15 minutes."
layout: default
---

<div class="chapter-meta"><b>Time:</b> 15 minutes. <b>You need:</b> the sensor's numbers from [Step 3](step3/), and honest curiosity.</div>

<h1>Step 5 — Do Your First Blameless Review</h1>

<p>You've done the hard, operacy work: you named the service, wrote the number, measured it, and wrote the card. Step 5 is where most people quit — and it's the step that actually turns SRE from a chore into a craft. It is also the step the classic's famous chapter was about, so we steal its one sentence in plain clothes: <br><br>
<b>"A blameless postmortem is a means to actually improve the system, not just to say you did."</b> [full source: the classic SRE postmortem culture, Chapter 12]</p>

## How to look back without hurting anyone

Teach yourself (or your team) the **blameless habit**: when a thing went wrong, don't ask *"who did what?"* Ask *"what in the system made this possible, and what changes so it can't happen again?"*

The template (the whole thing):

```markdown
## The blameless review — {date}
This week my service was {good%} good against {target%}.
What in the SYSTEM led to the dip (no people):   {line}
What I/we changed so it can't repeat:            {line}
One thing to try next week:                       {line}
```

## The 2026 kindness upgrade

Your first reviews will be a little raw, and that's correct and brave. The modern edition's addition: let the **AI scribe draft the finding** ("here's what the numbers say happened this week") — then *you* decide what to believe and what to do. Drafting is a machine skill; judgment is a human one, and it stays yours [full book: Ch 31–34, 36](https://irfancode.github.io/sre-in-the-age-of-ai/book/part5/). You've just done your first loop: choose → measure → rehearse → review. That loop *is* SRE, and now you can do it alone or with a full crew.

<div class="callout">
  <span class="faint"><i class="fa-solid fa-trophy"></i> You did it</span>
  <p><b>You've now run the entire SRE feedback loop once — the same loop the classic describes and the AI edition automates.</b> Next step, whenever you're ready — not homework, an invitation: the <a href="playground/"><b>Playground</b></a> to practice without fear, the <a href="glossary-lite/">no-jargon word box</a>, and the <a href="https://irfancode.github.io/sre-in-the-age-of-ai/">full 36-chapter book</a> with its AI frontier. Congratulations — you are officially someone who <i>engineers for reliability</i>.</p>
</div>

<p><a href="playground/"><b>Try the Playground</b></a> →</p>