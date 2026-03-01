# Ticket Tracker — Pitch to NYC City Council

## The Story (3-minute version)

---

### PROBLEM (45 sec)

> "Good morning, Council Members. My name is [speaker], and I used to answer the phone at 311.
>
> When a New Yorker calls 311 about no heat, a water leak, or a broken elevator, that call becomes a ticket. The ticket goes to HPD — the Department of Housing Preservation and Development — and HPD is supposed to make the landlord fix it.
>
> We pulled the data. All of it. 15.8 million complaints.
>
> Here is what we found:
>
> **88,000 repair tickets are open right now.** Not last year. Right now.
>
> An emergency complaint — no heat in winter, no hot water, electrical hazard — takes **10 and a half days** to close. A non-emergency? **Almost 25 days.** A broken elevator? **40 days.** In a building full of seniors and disabled residents who cannot take the stairs.
>
> And some of these tickets have been open since **January 2020.** Five years. Still open. Still no resolution."

---

### DATA INSIGHT (60 sec)

> "But that is not the worst part. We cross-referenced two datasets — the complaints and the buildings — and we found something the city does not advertise.
>
> HPD does not just regulate private landlords. HPD **manages 943 buildings directly.** Central Management, Article 7A receivership, HPD-owned properties. These are buildings the city took over because the landlord failed.
>
> So we asked: how fast does HPD fix complaints in **its own buildings?**
>
> **53.9 days.** Almost four times worse than private landlords.
>
> The agency that fines landlords for slow repairs is **four times slower in its own buildings.** The regulator is worse than the regulated.
>
> And outside the housing stock entirely — tonight, **85,770 people are sleeping in the DHS shelter system.** 29,880 of them are children. That number nearly doubled from 44,000 in 2021. Peak was 89,558 in December 2023.
>
> When HPD inspectors visit NYCHA developments, they find violations too — 2,273 documented. Red Hook West alone has 163. 393 are Class C — immediately hazardous. But NYCHA's actual repair queue? That data is not even public. We could not analyze what we cannot see.
>
> Council Members — every layer of NYC housing maintenance is failing. The data proves it."

---

### PROPOSED SOLUTION (60 sec)

> "We are not here to just show you the problem. We built a solution.
>
> **Proposal 1: Severity-Based Triage Queue.**
> A ticket open for five years should not sit in the same queue as one filed yesterday. Auto-escalate any ticket open longer than one year to emergency status. Weight by vulnerability — elderly residents, children, disabled tenants. No heat in a building with seniors in January cannot wait behind a paint complaint filed in July.
>
> **Proposal 2: Fix HPD's own buildings first.**
> You cannot credibly fine a private landlord for a 30-day repair when your own buildings average 54 days. Fund a dedicated rapid-repair team for the 943 HPD-managed buildings. Lead by example. Hit the 14-day average that private landlords already achieve. Then enforce.
>
> **Proposal 3: Public Accountability Dashboard.**
> Everything we showed you today was built from public data in a few hours. Make this permanent. A real-time dashboard showing every open ticket, how many days it has been waiting, which building, which landlord. Tenants check before signing a lease. Journalists track the worst offenders. City Council tracks HPD performance.
>
> Sunlight is the best disinfectant. This data already exists. We just made it visible."

---

### WHY FUND US? (30 sec)

> "This dashboard costs roughly $50,000 to build and maintain for a year.
>
> There are 88,000 open tickets. That is 88,000 families living in conditions that HPD has documented but not resolved.
>
> The federal government values each preventable death at $13.2 million in societal cost. A single building fire caused by uninspected electrical wiring costs more than this entire project.
>
> We are not asking you to build something new. We are asking you to take data you already collect and make it work for the people it is supposed to protect.
>
> **The data exists. The backlog is documented. The question is not whether there is a problem. The question is who will act on it.**
>
> Thank you."

---

## Key Stats (Quick Reference for Q&A)

| Stat | Number | Source |
|------|--------|--------|
| HPD open tickets | 88,048 | ygpa-z7cr, complaint_status=OPEN |
| Emergency avg resolution | 10.5 days | ygpa-z7cr, 2023+, type=EMERGENCY |
| Non-emergency avg | 24.9 days | ygpa-z7cr, 2023+, type=NON EMERGENCY |
| Immediate emergency avg | 3.6 days | ygpa-z7cr, 2023+ |
| Oldest open ticket | Jan 3, 2020 | ygpa-z7cr, ORDER BY received_date ASC |
| HPD-managed buildings | 943 | kj4p-ruqc, managementprogram != PVT/NYCHA |
| HPD-managed avg resolution | 53.9 days | Cross-reference ygpa-z7cr x kj4p-ruqc |
| Private landlord avg | 14.3 days | ygpa-z7cr, citywide 2023+ |
| HPD vs private ratio | 3.8x worse | 53.9 / 14.3 |
| DHS shelter population | 85,770 | k46n-sa2m, latest census |
| Children in shelter | 29,880 | k46n-sa2m, latest census |
| Shelter peak | 89,558 (Dec 10, 2023) | k46n-sa2m |
| Shelter low | 44,586 (Aug 1, 2021) | k46n-sa2m |
| NYCHA violations | 2,273 | im9z-53hg |
| NYCHA Class C (hazardous) | 393 | im9z-53hg, hzrd_clas=C |
| Manhattan avg resolution | 20.3 days | ygpa-z7cr, borough=MANHATTAN |
| Queens avg resolution | 13.1 days | ygpa-z7cr, borough=QUEENS |
| HPD total complaints (all time) | 15.8M | ygpa-z7cr |

## Anticipated Questions from "City Council"

**Q: "Why should we trust this data?"**
A: It is your data. Every number comes from NYC Open Data — datasets published by HPD and DHS. We did not collect anything. We analyzed what the city already publishes.

**Q: "Why is HPD's own resolution so much slower?"**
A: HPD-managed buildings are often the worst buildings in the city — that is why HPD took them over. But 53.9 days is still unacceptable. The comparison shows the scale of the problem, not an excuse.

**Q: "What about NYCHA?"**
A: NYCHA repairs go through their own system — MyNYCHA app and NYCHA Customer Care — not through 311 or HPD. That repair data is not on the open data portal. We can only analyze what HPD finds when they inspect NYCHA buildings. Making NYCHA repair data public would be a powerful addition.

**Q: "Is $50K realistic for the dashboard?"**
A: The prototype you see was built in hours using free public APIs. A production version with authentication, automated alerts, and a proper backend is a standard civic tech project. Code for America builds these routinely.

**Q: "How do we know this will actually change landlord behavior?"**
A: Transparency works. When NYC published restaurant health inspection grades (the A/B/C letter grades), compliance improved 30% in the first year. Public visibility changes behavior because it affects reputation and tenant decisions.

## Speaker Assignments

| Section | Time | Speaker | Notes |
|---------|------|---------|-------|
| Problem | 45 sec | Ismael | Former 311 operator — bring the firsthand credibility |
| Data Insight | 60 sec | Pape | Walk through the charts on screen, hit the 53.9 vs 14.3 comparison hard |
| Solution | 60 sec | Beatrice | Three proposals, practical and funded |
| Why Fund Us / Close | 30 sec | Ismael | Land the final line — "The question is who will act on it." |

Total: ~3 minutes 15 seconds. Under the wire.
