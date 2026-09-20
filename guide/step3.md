---
title: "Step 3 — Measure the Real Thing"
description: "One honest sensor on the system, so you're measuring reality — not your hopes. The 20-minute rule."
layout: default
---

<div class="chapter-meta"><b>Time:</b> 20 minutes (+ a lunch to watch it). <b>You need:</b> the SLO from [Step 2](step2/).</div>

<h1>Step 3 — Measure the Real Thing</h1>

<p>An SLO you never actually measure is a wish with a decimal point. Step 3 is where it stops being a wish. You need <b>one sensor that tells the truth</b>: how many times did the thing actually work, measured from the user's point of view. That last bit is the whole game — measuring from the <i>user's</i> view, not the server's. A server can be humming at 100% CPU and still be serving garbage; the user's view is the only approval that counts [full book: Ch 6–7](https://irfancode.github.io/sre-in-the-age-of-ai/book/part2/ch06/).</p>

## The 20-minute version (start here)

Pick ONE of these three, in this order of preference — they get more precise as you go up:

1. **A tiny synthetic check** — a small script/agent curls your service every minute and logs "200 / not 200 + how slow." (Your cloud's load balancer or an uptime bot does this for free.)
2. **The access log** — your server already logs every request; sum "good" ÷ "all" per hour.
3. **Real user pain** — the hardest and best: an error/experience metric, e.g. "first-request-in-page took >3s."

You want at least *one* of these logging numbers you can point to. Don't build a whole observability palace on day one — that's [Appendix the full book](https://irfancode.github.io/sre-in-the-age-of-ai/book/appendix/) territoryholistic. One honest sensor, now.

## Your first week's habit

- Every **Monday**, glance at last week's "good ÷ all." Write it somewhere permanent (a file, a spreadsheet, a chat thread — any of these the AI scribe can read and graph).
- If it dipped, that's not failure: that's *data*, and Step 5 is exactly for looking at it kindly.

<div class="callout">
  <span class="faint"><i class="fa-solid fa-flask"></i> The playground shortcut</span>
  <p>Don't have a production system to measure yet? The [Playground](playground/) has a fake service whose numbers you can watch move. Learn the habit there, then point it at the real thing.</p>
</div>

<div class="callout good">
  <span class="faint"><i class="fa-solid fa-lightbulb"></i> Key insight</span>
  <p><b>Measured beats hoped, every single week.</b> The AI teammates you'll hire in the full book are only as trustworthy as the sensors behind them — an agent with a real sensor is a helper; an agent with none is a rumor. You just installed your first real sensor. That's a bigger step than it sounds.</p>
</div>

<p><a href="step4/"><b>Next: Step 4 — Write one runbook</b></a> →</p>