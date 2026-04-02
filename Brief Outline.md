# Policy Brief Outline: AI Accountability Oversight Board (AIAOB)

**Track:** Reducing AI Risk
**Format:** 2 pages, 12pt Times New Roman, 1.15 line spacing, 1-inch margins
**Due:** Friday, April 3, 2026 by midnight

---

## POLICY RECOMMENDATION (opening paragraph, ~0.2 pages)

The United States should establish the **AI Accountability Oversight Board (AIAOB)**, an independent federal body modeled on the Public Company Accounting Oversight Board (PCAOB), to certify third-party AI auditors and mandate **rolling audits** — continuous, change-triggered oversight with persistent access rather than one-time compliance snapshots — of high-risk AI applications deployed in healthcare, criminal justice, financial services, hiring, and critical infrastructure.

---

## STRATEGIC CONTEXT (~0.5 pages)

### 1. The State Patchwork Is Failing
- CA's SB-53 (Sep 2025), NY's RAISE Act (Dec 2025), NYC's Local Law 144, CO's SB 21-169 — incompatible, fragmented frameworks
- Federal preemption is already happening (Dec 2025 EO) — better to preempt with a real standard than with deregulation

### 2. The Proof That Audits Without Certified Auditors Fail
- NYC LL144 mandated bias audits for hiring AI — only 18 of 391 employers (4.6%) posted audit reports
- NY State Comptroller (Dec 2025): enforcement is "ineffective" — companies picked their own auditors, auditors lacked technical expertise
- **This is your Exhibit A:** not that audits are bad, but that badly designed audits are worse than none

### 3. The Deployment Gap Nobody Is Closing
- SB-53 and RAISE Act regulate frontier model *developers* pre-deployment
- Nobody is watching what happens *after* deployment — model drift, performance degradation, and real-world data shifts make pre-deployment testing insufficient
- [Source: model drift is "the most common and least visible risk" of deployed AI systems]

### 4. The Enron Parallel
- Before Sarbanes-Oxley (2002), companies chose their own financial auditors — Arthur Andersen audited Enron
- Congress created PCAOB: independent oversight board, certified auditors, no direct company-to-auditor payment
- The same structural failure (self-selected, unqualified auditors) exists in AI today

---

## IMPLEMENTATION MECHANICS (~0.75 pages)

**[TARGET: 375 words max in this section. One tight sentence per point. Cut Enforcement (4) first if over page budget.]**

### 1. The AIAOB
- Independent, non-partisan board under Commerce Department oversight
- Self-funding via registration fees from audited companies (modeled on PCAOB — no Congressional appropriations required)
- Sets national auditing standards; certifies AI auditing firms
- Congressional reporting through Senate Commerce and House Energy & Commerce committees

### 2. Certified AI Auditor Requirements
- Core certification: technical competence (ML/data science) + legal/compliance knowledge (anti-discrimination law, HIPAA, FCRA, etc.)
- Auditing firms must employ domain experts on staff for each sector they audit (healthcare, criminal justice, financial services)
- Annual certification renewal with continuing education requirements
- Conflict-of-interest rules: no direct company-to-auditor payment relationship; AIAOB assigns firms from certified pool
- Creates a new professional market — pro-innovation, not purely restrictive

### 3. What Triggers a Mandatory Audit (Bright-Line Rule)
Audit is mandatory if a deployed AI system meets **any** of:
- Makes binding decisions about individuals (denied loan, rejected job application, criminal risk score)
- Operates in a named high-risk sector (healthcare, criminal justice, hiring, credit, housing, critical infrastructure)
- Exceeds scale thresholds (>10,000 consequential decisions/year OR >50,000 users in a regulated domain)

**Open source:** Deployers always audited in high-risk contexts; model creators (e.g., Meta releasing Llama) audited only if they specifically develop or market models for high-risk domains.

### 4. Rolling Audit Framework (Dual Trigger)
- **Change-triggered:** Any model update, retraining, or new deployment context automatically requires a new audit
- **Time-tiered by risk:**
  - Tier 1 (Critical: healthcare diagnosis, criminal sentencing, autonomous systems) — quarterly + continuous monitoring access
  - Tier 2 (High: hiring, lending, insurance underwriting) — semi-annual
  - Tier 3 (Elevated: content recommendation, educational assessment) — annual
- Audits check: performance drift, bias emergence, data integrity, alignment with stated purpose, incident response

### 5. Enforcement
- Graduated: warning → mandatory remediation plan → fines scaled to company revenue → deployment suspension
- Whistleblower protections for auditors and employees
- Public disclosure of audit summaries (transparency without revealing trade secrets)

---

## IMPACTS AND TRADE-OFFS (~0.5 pages)

### Projected Benefits
- Solves the state patchwork: one federal standard replaces 50 competing, incompatible frameworks
- Closes the deployment gap: catches failures that pre-deployment testing (SB-53/RAISE Act) can't detect
- Creates accountability without blocking innovation — audit and fix, don't ban
- Market-creating: certified AI auditor becomes a new professional class (like CPAs after SOX)

### Trade-offs
- **Compliance costs:** Offset by reduced litigation exposure; companies with clean audits have a defensible record
- **Institutional ramp-up:** 12–18 months to stand up AIAOB and initial certified auditor pool — Tier 1 (Critical) domains first, expand to Tiers 2 and 3 as capacity grows
- **Regulatory capture risk:** Mitigated by independence requirements, fee-based funding (not appropriations), and mandatory Congressional reporting
- **Does NOT address frontier model development** directly — complementary to SB-53/RAISE Act, not a replacement

### Political Survival (Resilient Benefits)
Three reasons this works even in a deregulatory environment:
1. **Market-creating:** Creates a new professional industry (AI auditing firms), not just costs. SOX created a multi-billion-dollar auditing industry.
2. **Fixes market failure:** Companies cannot credibly self-audit; investors and customers cannot verify AI safety claims. This information asymmetry cannot be resolved without an independent standard.
3. **Reduces litigation risk:** Without a clear audit standard, every AI failure invites open-ended lawsuits. Compliant companies have a defined safe harbor. Industry should want this.

**Resilience to tech change:** Risk tiers and audit standards are set by the AIAOB board via rulemaking (not locked in statute), so they update as technology evolves. Change-triggered audits catch model updates automatically, without waiting for a legislative cycle.

---

## CITATIONS (do not count toward 2-page limit)

| Claim | Source |
|-------|--------|
| NYC LL144: 18 of 391 employers compliant (4.6%) | "Null Compliance," FAccT 2024 (ACM) |
| NYC enforcement "ineffective" | NY State Comptroller Audit, Dec 2025 |
| SB-53 signed, frontier model regulation | Governor Newsom signing, Sep 29, 2025 |
| NY RAISE Act signed | Governor Hochul signing, Dec 2025 |
| Dec 2025 federal preemption EO | White House EO on AI framework, Dec 11, 2025 |
| Model drift: "most common and least visible risk" | EC-Council / Royal Society Open Science, 2024 |
| PCAOB creation post-Enron | Sarbanes-Oxley Act, 2002; PCAOB.org |
| State AI patchwork landscape | Drata / King & Spalding AI law tracker, 2026 |

---

## Q&A PREP (for judges, not in the brief)

**Q: Isn't this too burdensome for small AI startups?**
A: The trigger thresholds (>10K decisions/year, named sectors) exempt small-scale or low-risk deployments. A startup building a recipe recommender isn't audited. A startup selling a loan underwriting tool to banks is.

**Q: Why not just use FTC or NIST?**
A: FTC is already overloaded with existing consumer protection enforcement. NIST has no enforcement authority — its frameworks are voluntary. The PCAOB model works precisely because it's independent, self-funding, and has real teeth.

**Q: Republicans want to abolish PCAOB — why model on something that might disappear?**
A: The PCAOB abolition debate is about accounting industry consolidation and SEC authority, not the oversight model itself. The AIAOB is market-creating (new industry, new jobs) — a framing that has bipartisan appeal independent of the PCAOB's fate.

**Q: What about AI systems that cross multiple tiers?**
A: Apply the highest applicable tier. A healthcare hiring tool (hiring = Tier 2, healthcare = Tier 1) gets Tier 1 treatment.

**Q: How do you certify auditors fast enough to meet demand?**
A: Phase in by risk tier. Tier 1 domains first (smallest set, highest stakes). AIAOB sets provisional certification standards in year 1, full standards by year 2. Existing cybersecurity and financial compliance auditors are a natural pipeline.
