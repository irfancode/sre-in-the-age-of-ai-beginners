---
title: "The Playground — a fake service that can't break anything"
description: "Rehearse your whole 5-step loop on a pretend service. Zero risk, real habits. The 20-minute sandbox."
layout: default
---

<div class="chapter-meta"><b>Part of:</b> Step 3's playground shortcut. <b>Time:</b> 20 minutes. <b>Promise:</b> it runs on your laptop, nothing to prod, nothing to apologize for later.</div>

<h1>The Playground — a fake service that can't break anything</h1>

<p>Real SREs rehearse on fake systems before touching real ones — the classic book was unapologetic about rehearsal [full book Ch 12](appendix of the full book). The playground is that idea in its friendliest form: <b>a tiny pretend service whose "users" you watch, so you can practice Step 1–5 without anyone (or anything) you love depending on you.</b></p>

## What you're building in 20 minutes (a pretend order-taker)

A fake "Order Service." It has three rules, and those rules are your sensors:

1. An order succeeds if a pretend customer gets a "thanks" within **2 seconds**.
2. Every ~3rd pretend customer is a little unlucky and the system is slow — so your "% good" number wobbles realistically.
3. The simulation prints one line per minute of pretend traffic to a folder you own: `global`,`slow`,`crashed`, and a running `%good`.

That's it. There is no real database, no pager, and no boss watching — because the point is to build the *habit*, not the stakes.

### Quick start (copy into a `playground.sh` or paste into your AI teammate as "make me traffic")

```bash
#!/bin/bash
# playground.sh — watch %good wobble, like real life but safe
for t in {1..60}; do
  r=$((RANDOM % 100))
  if   [ $r -lt 90 ]; then echo "global  ... tomar seconds ok  "        # the good 90%
  elif [ $r -lt 97 ]; then echo "slow    ... 2.8s => 1 request slow "     # the wobble
  else                     echo "crashed ... timeout, 1 request lost  "   # the rare sad case
  fi
  sleep 1
done
```

Run it. Watch. Now you have the exact behavior Step 3's sensor was built to catch: a service that is *usually* fine, occasionally slow, rarely broken — exactly what an SLO measures, only safer.

## The honest bit (this is the point)

When the uncomfortable moment comes (a 3 a.m. page on your real service, years from now), your muscle memory isn't "I knew the theory" — it's "I've *rehearsed this* in the playground, and I know the two lines to run." That rehearsal is the entire distance between a beginner and someone engineers trust.

<div class="callout good">
  <span class="faint"><i class="fa-solid fa-flask"></i> Upgrade when ready</span>
  <p><b>Point the SAME habit at your real service</b> (Step 3's "one honest sensor"): measure real user "good ÷ all," check it weekly, and let your AI teammate draft the dashboard while you keep the judgment. The playground showed you the pattern; production is just the pattern with the handrails on. [glossary-lite](glossary-lite/) has the words; the full book has the deep dive — but nothing replaces having rehearsed it yourself.</p>
</div>

<p><a href="step5/"><b>← Back to Step 5 (you've earned it)</b></a> · <a href="glossary-lite/">No-jargon word box →</a></p>