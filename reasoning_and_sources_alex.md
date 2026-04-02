# Policy Reasoning and Sources: Third-Party Rolling AI Auditing

VASI AI Policy Hackathon — Supporting document for brief_outline_alex.md

---

## Why This Policy Approach

### Why deployment-layer, not frontier model training?

The guiding question asks for policy that reduces risk from AI "in development, deployment, or usage." The brief focuses on deployment because:

1. Frontier model regulation (SB-53, RAISE Act, Trump framework) is already contested terrain. Proposing another layer of frontier model controls risks colliding with existing legislative battles and being dismissed as redundant.

2. The real gap is the *deployment layer*. A model can pass any pre-release safety evaluation and then be silently updated, fine-tuned, or reprompted into unsafe behavior after deployment. There is currently no mandatory external check on this. Millions of consequential decisions — hiring, lending, triage, content moderation — are made by systems that have never been externally audited.

3. Focusing on deployment is *more resilient* to technological change (scoring criterion). Whatever new capabilities emerge, they will be deployed in applications. An auditing framework at the application layer captures future risk without needing to predict what form it takes.

---

### Why the PCAOB/SOX analogy?

Three reasons this is the right institutional model:

1. **Proven track record.** PCAOB was created by Sarbanes-Oxley (2002) after Enron/Arthur Andersen. It solved a structurally identical problem: companies self-reported financial health; self-reporting was fraudulent; a third-party audit requirement with certification and criminal liability fixed it. SOX passed the Senate 98-0 — bipartisan precedent matters for feasibility scoring.

2. **It answers the institutional design question directly.** The hardest challenge in AI governance proposals is "who oversees the overseers?" PCAOB answers this: a nonprofit SRO, overseen by the SEC (in our case, Commerce/FTC), which certifies audit firms, sets standards, and has civil enforcement authority. It sidesteps the "new federal agency" objection while still having teeth.

3. **Criminal liability creates a real deterrent.** SOX §906 makes it a federal crime for corporate officers to knowingly certify false financial statements. The same provision applied to AI certifications closes the gap where compliance theater replaces real accountability.

**Alternative considered and rejected:** FDA 510(k) clearance model. Pre-market approval slows innovation more than post-deployment auditing. The 90-day post-deployment window preserves the ability to ship fast while still creating accountability.

---

### Why phased (hybrid B+C) rather than immediate mandate?

Three approaches were evaluated:

- **Approach A (Registry + Disclosure only):** Too weak. No criminal liability, FTC enforcement is overstretched. Disclosure without consequences = compliance theater.
- **Approach B (Full AIOAB mandate immediately):** Strongest on paper but politically fragile. PCAOB itself took 18+ months to stand up after SOX passed with overwhelming urgency. Requiring Year 1 mandates with no existing audit standards or certified auditors is not feasible.
- **Approach C (Safe harbor only, voluntary):** Voluntary programs do not work without mandates. See: NIST AI RMF adoption rate — widely cited, rarely operationalized.

**The hybrid:** Voluntary with credible safe harbor incentives in Phase 1 (solves the "voluntary never works" problem by making participation commercially rational — avoiding state regulatory fragmentation is a real incentive), mandatory via administrative rulemaking in Phase 2 once NIST standards exist. The Phase 2 trigger is Commerce rulemaking, not a second Congressional vote — this is the GDPR model and means Phase 2 does not require a second political fight.

---

### Why "rolling" = change-triggered, not just periodic?

The EU AI Act (Articles 9 and 72) already requires continuous lifecycle monitoring and post-market surveillance for high-risk AI. Proposing "annual audits" is not differentiated from what Europe already mandates.

The key innovation is the **significant-update trigger**: any time a deployed AI system changes in ways that could materially alter its risk profile, an audit is required within 90 days. This closes the "update and escape" gap — the ability to pass a one-time audit and then deploy upgraded (potentially riskier) model versions without any external review.

**Why behavioral-delta, not version string:** Version numbers are controlled by the deployer. A complete model retrain can be labeled "v2.1.1 patch" to avoid triggering a review. The trigger must be defined by what the system *does*, not what the deployer *calls it*. NIST-designated benchmark suites provide the measurement standard; deployer self-certifies; auditor spot-checks; false certification is criminal.

---

### Why the $100M revenue / 1M MAU threshold?

- **Revenue over "AI revenue":** Allocating "revenue from AI features" requires complex accounting that will generate 50-page guidance documents and years of litigation. Total company revenue is clean, auditable, and precedented (see: EU Digital Markets Act gatekeeper threshold, GDPR's "large enterprise" provisions).
- **$100M / 1M MAU:** Targets companies with meaningful market presence and resources to comply. Exempts early-stage startups. The 6-month grace period prevents a compliance cliff effect at the threshold.
- **a16z analysis** (Appenzeller & Perault) supports revenue-based thresholds over compute-based thresholds for application-layer regulation, noting that compute metrics are appropriate for model-layer regulation but not deployment-layer.

---

### Why floor preemption, not ceiling?

Floor preemption (federal minimum; states can go higher) is politically defensible and legally cleaner than ceiling preemption (federal maximum; states cannot exceed).

Ceiling preemption would gut California SB-53 and New York's RAISE Act — which are the strongest existing state AI safety laws. This would face immediate coalition opposition from state AGs, civil liberties organizations, and the same legislators who passed those bills. It would also likely face constitutional challenge.

Floor preemption gives companies one federal compliance baseline that prevents a 50-state patchwork of *conflicting* requirements, while letting states with stronger standards keep them. This is how HIPAA works (federal floor, states can exceed it). Politically, it can attract support from both sides: industry (avoids fragmentation) and advocates (doesn't preempt stronger state protections).

---

### Why open-source deployers bear the liability?

The alternative — holding foundation model developers liable — breaks open-source AI development. Meta (Llama), Mistral, and other open-source model developers cannot predict or control every downstream use. Holding them liable for a healthcare app built on their model creates an impossible compliance burden and would chill open-source AI research.

Deployer liability is the right structural answer: the entity that integrates an AI system into a consequential application, sets the prompts, controls the outputs, and profits from the deployment is the entity that should be accountable for it. This is analogous to product liability law — a steel manufacturer is not liable for every product a manufacturer makes with their steel.

---

## Sources

### Primary Sources (cite directly in brief)

**1. Raji, I.D., Xu, P., Honigsberg, C., & Ho, D.E. (2022). "Outsider Oversight: Designing a Third Party Audit Ecosystem for AI Governance." Stanford RegLab / ACM FAccT.**
https://reglab.stanford.edu/publications/outsider-oversight-designing-a-third-party-audit-ecosystem-for-ai-governance/

*Why this source:* The canonical academic paper on third-party AI auditing. Written by Stanford law and CS researchers. Argues that accountability policy has neglected lessons from non-algorithmic domains — specifically the importance of third-party participation. Directly supports the CAA framework design.

---

**2. Harvard Journal of Law & Technology. "AI Auditing: First Steps Towards the Effective Regulation of Artificial Intelligence Systems."**
https://jolt.law.harvard.edu/digest/ai-auditing-first-steps-towards-the-effective-regulation-of-artificial-intelligence-systems

*Why this source:* Harvard JOLT explicitly advocates for "government-mandated AI audits conducted by professional auditors following established standards subject to government oversight." Directly validates the mandatory third-party audit approach and the PCAOB-style oversight structure.

---

**3. NIST. AI Risk Management Framework (AI RMF 1.0). 2023.**
https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf

*Why this source:* The proposed audit standards are grounded in NIST AI RMF. Citing this shows the brief builds on existing federal AI governance infrastructure rather than inventing from scratch. Also establishes NIST as the natural home for CAA standard-setting.

---

**4. EU AI Act, Articles 9 and 72.**
Article 9 (Risk Management): https://artificialintelligenceact.eu/article/9/
Article 72 (Post-Market Monitoring): https://artificialintelligenceact.eu/article/72/

*Why this source:* Establishes the international baseline. Article 9 mandates "continuous iterative process throughout the entire lifecycle." Article 72 requires active post-market monitoring. Citing these lets the brief argue: the EU already requires continuous lifecycle accountability; the US has nothing equivalent; this proposal fills that gap.

---

**5. The Institute of Internal Auditors. AI Auditing Framework. September 2024.**
https://www.theiia.org/globalassets/site/content/tools/professional/aiframework-sept-2024-update.pdf

*Why this source:* IIA is the professional body for internal auditors. Their 2024 framework explicitly recommends "targeted reviews triggered by new AI tool implementations, regulatory changes, or identified compliance issues" — direct support for the change-triggered rolling audit mechanism. Also useful for addressing the auditor supply objection (IIA provides the professional baseline for CAA certification).

---

**6. Center for Governance of AI. "Training Compute Thresholds: Features and Functions in AI Regulation." GovAI.**
https://www.governance.ai/research-paper/training-compute-thresholds-features-and-functions-in-ai-regulation

*Why this source:* Provides academic backing for scale-based regulatory thresholds. Argues compute metrics are useful for model-layer regulation; by contrast, revenue/MAU thresholds are more appropriate for deployment-layer regulation. Supports the threshold design choice.

---

**7. Appenzeller, G. & Perault, M. (Andreessen Horowitz). "To Help AI Startups Compete, Use Revenue-Based Thresholds."**
https://a16z.com/to-help-ai-startups-compete-use-revenue-based-thresholds/

*Why this source:* Industry-side support for revenue-based thresholds at the application layer. Strengthens the "this threshold design is defensible and broadly supported" argument. Addresses the innovation/startup concern directly: revenue thresholds protect early-stage companies while capturing large incumbents.

---

### Background / Supporting Context (do not cite directly, but informed the brief)

**Caseware. "From Rigid to Dynamic: Rethinking the Audit Workflow in the Age of AI and Data."**
https://www.caseware.com/us/resources/blog/from-rigid-to-dynamic-rethinking-the-audit-workflow-in-the-age-of-ai-and-data
*Supports the event-driven auditing model.*

**PCAOB. "AI and the Pursuit of Audit Quality: A Regulatory Perspective."**
https://pcaobus.org/news-events/speeches/speech-detail/ai-and-the-pursuit-of-audit-quality--a-regulatory-perspective
*PCAOB itself is exploring agile frameworks for AI standards — supports the "PCAOB model is evolving in this direction" argument.*

**Virginia AI Security Initiative. Policy Hackathon Central Resource Doc.**
*Contains the guiding question, scoring rubric, and track information for the competition.*

---

## Key Q&A Defenses

Questions judges are likely to ask and how to answer them:

**"Why not just extend SB-53 or RAISE Act nationally?"**
SB-53 targets frontier model developers (labs like Anthropic, OpenAI). RAISE Act targets training compute. Neither addresses deployed applications — the systems that actually affect users right now. This proposal fills the deployment layer gap that those bills leave open.

**"What happens when an auditor misses a critical failure?"**
Criminal liability for knowingly false certifications creates real deterrence. Combined with public AIOAB registry and complaint-triggered FTC/AIOAB investigations, the system creates multiple accountability layers. Compare: financial auditors miss fraud sometimes, but mandatory auditing still dramatically reduces fraud frequency vs. self-reporting.

**"Won't this just create a compliance checkbox industry?"**
The "significant update" trigger with behavioral-delta testing (not documentation review alone) prevents checkbox compliance. CAA standards require both documentation review AND technical testing including red-teaming and adversarial inputs. Auditors who rubber-stamp face criminal liability.

**"How do you audit something as complex as a frontier model?"**
The brief audits deployed applications, not foundation models. The audit scope is: (1) does the system behave consistently with its stated purpose? (2) does it produce discriminatory or harmful outputs on standard benchmarks? (3) are significant changes disclosed and re-audited? This is tractable. It does not require interpretability of model internals.

**"Isn't the 90-day trigger window too slow for fast-moving AI?"**
It is a post-deployment window, not a pre-approval gate. Companies ship immediately. The 90-day window is the deadline for completing the audit after deployment, not before. Innovation is not gated.
