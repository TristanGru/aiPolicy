# Policy Brief Outline: Third-Party Rolling AI Auditing

VASI AI Policy Hackathon — Due Friday, April 3, midnight
Track: Propose one national policy to reduce risk from AI systems in development, deployment, or usage.

---

## Opening Recommendation

**The United States should establish a phased Certified AI Auditor (CAA) program:
(1) a voluntary certification framework with federal safe harbor incentives in Years 1-2
while NIST develops mandatory audit standards, followed by (2) mandatory rolling
third-party audits for AI applications above scale thresholds, overseen by an AI
Oversight and Auditing Board (AIOAB) — a nonprofit SRO modeled on PCAOB — with
criminal liability for knowingly false certifications.**

---

## Section 1: Strategic Context (~1/3 page)

- **Why existing approaches fail:**
  - NIST AI RMF is voluntary — adoption is uneven and unenforceable
  - State patchwork (CA SB-53, NY RAISE Act) is fragmented and legally contested
  - Trump administration's National AI Legislative Framework is silent on deployment-layer accountability
  - Federal preemption pressure makes sensible national policy more urgent, not less

- **The core gap — "update and escape":**
  - AI systems are audited once (if at all), then updated silently with no external check
  - The EU AI Act requires continuous lifecycle monitoring (Articles 9 and 72) but the US has no equivalent
  - Millions of consequential decisions — hiring, lending, medical triage, content moderation — are made by opaque systems with no mandatory external review

- **SOX precedent:**
  - Before Sarbanes-Oxley (2002), companies self-reported financial health
  - After Enron, SOX passed 98-0 in the Senate — mandatory third-party audits by CPA firms overseen by PCAOB
  - The same accountability vacuum exists in AI deployment today

---

## Section 2: Implementation Mechanics (~1/2 page)

**Phase 1 (Years 1-2): Voluntary with Teeth**

1. NIST develops CAA audit standards grounded in AI RMF 1.0, including both documentation review and technical testing (red-teaming, bias evaluation, adversarial inputs)
2. Commerce Dept launches Certified AI Auditor (CAA) program — certifies third-party audit firms; accepts combined CS + audit credentials
3. Voluntary participation incentives: companies that complete CAA audits receive (a) federal safe harbor from conflicting state AI mandates (floor preemption — states may impose stricter standards) and (b) FTC enforcement presumption of compliance
4. NIST publishes benchmark suite for detecting significant model updates (Year 2)

**Scale threshold:** AI applications with >1M monthly active users OR >$100M total annual company revenue. Graduated entry: 6-month grace period after first crossing threshold. Carve-outs for nonprofits and research institutions.

**Phase 2 (Year 3+): Mandatory**

5. AIOAB established as a nonprofit Self-Regulatory Organization (SRO) overseen by Commerce/FTC — identical to PCAOB's actual structure; not a new standalone federal agency
6. Mandatory rolling audits for all in-scope applications: annual baseline PLUS change-triggered review within 90 days of a significant update
7. Civil penalties up to $10M per violation; criminal liability (SOX §906 model) for knowingly false certifications — applies to both the CAA auditor firm and the deployer's certifying officer (CEO/CTO)
8. AIOAB reports to Senate Commerce and House Energy & Commerce committees

**Phase 2 transition:** Triggered by Commerce administrative rulemaking (not a second Congressional vote) within 24 months of NIST standards publication. Phase 1 legislation grants this rulemaking authority upfront.

**Key institutional design:**
- Who certifies auditors? Commerce Dept (Phase 1) → AIOAB (Phase 2)
- Audit standards: NIST AI RMF + sector-specific addenda (healthcare via HHS, finance via FDIC)
- Enforcement: FTC (Phase 1) → AIOAB + DOJ (Phase 2)

**Defining "significant update" (critical — behavioral delta, not version string):**
A triggering update is one that produces measurable distributional shift in model outputs across a NIST-designated evaluation benchmark suite, OR expands deployment to a new regulated sector (healthcare, finance, criminal justice), OR doubles the in-scope user population. Deployer self-certifies; CAA auditor spot-checks; false certification triggers criminal liability.

**Open-source models:**
Audit obligation follows the deployer, not the model origin. Building a healthcare app on Llama makes the deployer — not Meta — responsible for CAA compliance. Open-source foundation model developers under $100M revenue are exempt.

**Agentic AI systems:**
CAA standards for agentic systems (autonomous task execution, multi-agent pipelines) must include: (1) scope-of-action logging — every real-world action is logged and auditable; (2) human-in-the-loop breakpoints for consequential decisions (financial transactions, medical referrals, legal filings).

**Audit result disclosure:**
Aggregate findings published to a public AIOAB registry. Detailed technical reports go to regulators only. Affected individuals may request disclosure of decisions made about them by audited systems (modeled on FCRA adverse action notices).

**Foundation model coordination:**
Foundation model oversight is addressed separately under the AI Safety Institute (Commerce). This proposal targets deployment-layer accountability — the gap that model-layer oversight cannot address.

---

## Section 3: Trade-offs and Projected Impacts (~1/3 page)

| Concern | Response |
|---|---|
| Compliance cost for SMEs | Scale threshold exempts small players; 6-month grace period after crossing; IIA estimates $50K-$500K per audit |
| Innovation slowdown | 90-day post-deployment window, not pre-approval; no AI is blocked from shipping |
| Auditor supply shortage | Phase 1 voluntary program builds the profession before mandates kick in; IIA AI Auditing Framework (2024) provides professional baseline |
| Political feasibility | AIOAB is a nonprofit SRO, not a new federal agency; SOX passed 98-0; Phase 2 via rulemaking, not second legislation |
| State preemption concerns | Floor preemption only; states (CA, NY) may impose stricter standards than federal floor |

---

## Resilient Benefits

Auditing adapts to whatever AI capabilities emerge — the policy does not require predicting future risks, only that assessments track current NIST standards, which update via formal public comment cycles (see: 2024 NIST generative AI supplement). As agentic systems grow, CAA standards extend to cover them through NIST addenda. The institutional model (SRO with rulemaking authority) is designed to evolve faster than notice-and-comment federal rulemaking would allow.
