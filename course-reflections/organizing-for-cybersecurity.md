# Organizing for Cybersecurity — Course Reflection

**Date:** 2026-07-11  
**Course:** Organizing for Cybersecurity (MSc Cybersecurity, Linköping University)

---

## Core Concept

This course taught that cybersecurity is not only a technical discipline but also an
organizational challenge involving people, governance, decision-making, and
collaboration. Instead of focusing on tools and attacks alone, we explored how
organizations prepare for uncertainty, manage incidents, comply with regulations, and
make collective decisions — through real-world cases, literature seminars, and
role-play simulations.

Two threads from the course have stuck with me the most: how organizations govern
themselves *during* a live incident, and how much judgment should be left to humans
versus automated systems when decisions have to be made fast.

---

## Governance and Incident Response: The Swedbank Case

The Swedbank cybersecurity incident (2022) made the course's Cyber Incident
Management Framework concrete. A sound technical response wasn't enough on its
own — *Responsibility* had to be clearly assigned across teams, and *Communication*
had to satisfy regulators and the public at the same time, under pressure and with
incomplete information.

This is also where the Hard Law vs. Soft Law distinction became practical rather than
theoretical. GDPR and NIS2 create hard, non-negotiable reporting and accountability
obligations once an incident occurs. ISO/IEC 27001-style controls, by contrast, are
soft law — they shape how an organization demonstrates it acted responsibly *before*
anything went wrong, but carry no direct legal penalty on their own. Seeing both
operate on the same case made clear that compliance isn't a static checklist; it's a
live constraint on how fast, and how transparently, an organization can act once a
crisis is already underway.

---

## Human Judgment vs. Automated Decision-Making: The Petrov Case

Stanislav Petrov's 1983 decision to disregard a Soviet early-warning system's false
launch alert — against protocol, on his own judgment — is an extreme case, but a
clarifying one for cybersecurity. Automated systems reduce response time and catch
what humans miss at scale, but they can also generate false positives with severe
consequences if human judgment is removed entirely from the loop.

This connects directly to a live tension in modern SOC design: alert fatigue and
over-reliance on automated triage are well-known failure modes. The lesson isn't
"don't automate" — it's that organizations need to deliberately design decision
points where human judgment can still override the system, rather than treating
automation as a substitute for accountability.

---

## Overall Takeaway

The seminars were the most valuable part of this course because they demanded
applying frameworks to real, messy cases rather than reciting them in the abstract.
Swedbank showed me that incident response and regulatory compliance aren't separate
workstreams that happen to overlap — legal obligations like NIS2 directly shape which
technical and communication decisions are even viable mid-crisis. Petrov showed me
that resilience isn't just about having the right systems in place, but about
designing space for human judgment to catch what those systems get wrong.

As a future cybersecurity professional, I want to think about governance,
compliance, and automation not as separate boxes to check, but as design decisions
that have to be made *before* an incident happens — because during one, there's no
time to figure them out from scratch.
