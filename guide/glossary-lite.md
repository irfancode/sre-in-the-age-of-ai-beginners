---
title: "The No-Jargon Word Box (glossary-lite)"
description: "Every SRE term in this guide, in one plain sentence each. You will never feel dumb reading what these mean."
layout: default
---

<div class="chapter-meta"><b>For:</b> total beginners. <b>Rule:</b> if the full book ever speaks a word you don't know, it lands here in one plain line. Bookmark it.</div>

<h1>The No-Jargon Word Box (glossary-lite)</h1>

| Word | Plain meaning (one sentence, back-of-the-napkin) |
|---|---|
| **SRE** | A way of running systems where "it works today" is *measured* and *rehearsed*, not hoped. |
| **Service** | The one thing users use — the door you decided to guard in Step 1. |
| **SLO** | A **S**ervice **L**evel **O**bjective: the number you pick ("99.9% of the time, works in 2s"). |
| **SLI** | A **S**ervice **L**evel **I**ndicator: how you actually *count* good vs. bad (Step 3's sensor). |
| **Error budget** | Your allowance to be imperfect: 100% − your SLO. You're allowed to spend it, not to hide it. |
| **Toil** | The boring, repetitive work a machine is better at — 2026: the stuff the AI teammate should eat. |
| **Runbook** | The "when X, do Y" card from Step 4 that future-you follows at 3 a.m. |
| **Blameless review** | Looking at what went wrong without pointing at a person (Step 5) — including not at yourself. |
| **Repair / mitigation** | Making it *hurt less now* (mitigation) vs. removing the cause forever (repair). Do mitigation first. |
| **Agent (2026)** | The AI teammate that can draft, watch, and propose actions — but the *you decide*. |
| **Verification** | Checking the machine's work before trusting it — the new-skill of the AI era. |
| **Autonomy ladder** | The rungs of "how much may the machine act on its own," earned by evidence. |

<div class="callout">
  <span class="faint"><i class="fa-solid fa-book"></i> Want the full dictionary?</span>
  <p>The complete 2026 glossary lives in the [full book's appendix](https://irfancode.github.io/sre-in-the-age-of-ai/book/appendix/glossary/). This box is the first-rung version you keep beside the playground.</p>
</div>

<p><a href="step1/"><b>← Restart the steps</b></a> · <a href="../"><b>Home</b></a></p>