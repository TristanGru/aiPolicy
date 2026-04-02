# Combined Policy Brief: AI Accountability Oversight Board (AIAOB)

VASI AI Policy Hackathon
Track: Reducing AI Risk
Format: 2 pages, 12 pt Times New Roman, 1.15 spacing, 1-inch margins
Status: Combined draft synthesized from `Brief Outline.md`, `brief_outline_alex.md`, and `reasoning_and_sources_alex.md`

## Opening Recommendation

The United States should establish the AI Accountability Oversight Board (AIAOB), a nonprofit self-regulatory organization overseen by the Commerce Department and FTC, to certify third-party AI auditors and implement a phased national auditing regime for deployed AI systems. In Years 1 and 2, the federal government should launch voluntary certified audits tied to safe-harbor incentives and floor preemption from conflicting state requirements while NIST develops common standards. Beginning in Year 3, the AIAOB should require rolling third-party audits, meaning annual and change-triggered review rather than one-time compliance snapshots, for AI systems deployed in high-risk domains such as healthcare, criminal justice, hiring, lending, housing, and critical infrastructure, with scale-based backstops for very large systems outside those domains. This closes the deployment gap that current AI policy misses: systems change after launch, drift in performance, and make consequential decisions without any mandatory external check.

## Strategic Context

Current AI governance is failing in three ways at once. First, the United States has a fragmented state patchwork, including California SB-53, New York's RAISE Act, New York City's Local Law 144, and Colorado's AI law, all with different scopes and targets. Federal preemption pressure is already rising, which means the real choice is not between state experimentation and no national policy. It is between a credible federal standard and deregulation by default.

Second, the best existing real-world audit example already shows why audits without institutional design fail. New York City's Local Law 144 required bias audits for hiring AI, yet only 18 of 391 covered employers posted compliant audit reports, and the New York State Comptroller later described enforcement as ineffective. The lesson is not that audits are useless. It is that weak audits, chosen by the companies being audited and performed by underqualified reviewers, create false reassurance.

Third, most current AI proposals focus on frontier model development before deployment, while the real governance gap is what happens after deployment. A system can pass a pre-release test, then be updated, fine-tuned, or redeployed in a riskier context with no external review. That is the AI equivalent of the pre-Sarbanes-Oxley world, where companies chose their own auditors and the conflict of interest was structural. Congress solved that problem after Enron by creating the PCAOB. AI deployment now needs the same accountability logic.

## Implementation Mechanics

### 1. Institutional Design

- The AIAOB is a nonprofit self-regulatory organization, not a new standalone federal agency, overseen by Commerce and the FTC.
- In Phase 1, Commerce launches the certification program and NIST develops audit standards grounded in the AI Risk Management Framework, with sector-specific addenda where needed.
- In Phase 2, the AIAOB assumes certification, registry, standard-setting, and enforcement coordination responsibilities, reporting to Senate Commerce and House Energy and Commerce.

### 2. Phase 1, Voluntary With Teeth

- For the first two years, deployers may obtain certified third-party audits under a federal framework.
- In exchange, audited firms receive safe-harbor incentives, including a presumption of compliance for certain federal enforcement purposes and protection from conflicting state AI requirements, creating a single national compliance pathway for firms that opt in.
- This phase builds the auditor pipeline, normalizes standards, and prevents the policy from promising mandatory audits before the profession exists.

### 3. Certified Auditor Requirements

- Certified AI auditors must demonstrate both technical competence, including model evaluation, data science, and adversarial testing, and legal compliance knowledge relevant to the sectors they audit.
- Audit firms must employ domain experts for regulated sectors such as healthcare, finance, and criminal justice.
- Certifications renew annually, include continuing education, and are subject to conflict-of-interest restrictions.
- To avoid the Local Law 144 problem, the oversight structure should prevent direct auditor dependence on the company being reviewed.

### 4. Phase 2, Mandatory Rolling Audits

- Beginning in Year 3, mandatory rolling audits apply to deployed AI systems in named high-risk domains, especially where systems make binding or highly consequential decisions about individuals.
- Rolling audits mean both a baseline recurring review and a change-triggered review when a system is materially updated, retrained, or deployed in a new high-risk context.
- The point is simple: a company should not pass one audit and then silently ship a meaningfully different system.

### 5. Trigger Rule

Primary trigger:
- Any AI system used in a named high-risk domain such as healthcare, criminal justice, hiring, lending, housing, or critical infrastructure is presumptively in scope, especially when it makes binding or highly consequential decisions about individuals.

Secondary scale backstops:
- Lower thresholds inside regulated domains: more than 10,000 consequential decisions per year or more than 50,000 users in a regulated domain.
- Higher thresholds outside regulated domains: more than 1 million monthly active users or more than 100 million dollars in annual revenue.

### 6. Significant Update Rule

- A new audit is required after any material model retraining, major system update, or expansion into a new regulated use case.
- The trigger should be defined by behavioral change and deployment context, not by whatever version label the company assigns to the system.

### 7. Open-Source Liability

- The audit obligation falls on the deployer, not the original open-source model creator.
- If a company uses an open model in a high-risk application, the company deploying that system is responsible because it controls the prompts, data, workflow, and real-world decision context.

### 8. Enforcement

- Enforcement should be graduated: warning, remediation plan, civil fines scaled to company size, and deployment suspension for repeated or severe violations.
- Public audit summaries should be disclosed without revealing trade secrets.
- Whistleblower protections should apply to auditors and employees.
- Knowingly false certifications should trigger criminal liability for both the certifying officer and the auditor, modeled on Sarbanes-Oxley logic, to prevent the system from becoming compliance theater.

## Impacts and Trade-Offs

This approach closes the deployment gap without requiring pre-approval of every AI product. It creates a national standard where the current patchwork is collapsing into conflict. It is also pro-market in an important sense: it creates a new professional class of certified AI auditors rather than only imposing restrictions.

The trade-offs are real. Building a credible auditor pipeline takes time. Compliance costs will fall unevenly across sectors. Regulatory capture is a live risk if auditor independence is weak. The policy also does not directly solve frontier model training risk. That is intentional. This brief is aimed at deployment-layer accountability, which is where current governance is weakest and where technological change is easiest to absorb through updated standards.

The phased structure is what makes the proposal durable. Phase 1 gives firms a reason to participate early through safe harbor and floor preemption. Phase 2 turns that temporary incentive structure into a mandatory regime once standards and certified auditors exist. The result is stronger than a purely voluntary code and more realistic than pretending the federal government can impose immediate mandatory audits without the infrastructure to back them up.

## Best Combined Positioning

This combined version keeps the strongest parts of both drafts:

- From `Brief Outline.md`: the deployment-gap framing, the Local Law 144 failure example, the Enron/PCAOB analogy, the sharper AIAOB naming, and the emphasis on rolling audits in high-risk sectors.
- From `brief_outline_alex.md` and `reasoning_and_sources_alex.md`: the phased rollout, NIST-based standards, safe harbor plus floor preemption, deployer-only open-source liability, criminal liability for false certification, and stronger political-feasibility framing.

## Sources To Carry Forward

- Raji et al., "Outsider Oversight: Designing a Third Party Audit Ecosystem for AI Governance"
- Harvard JOLT, "AI Auditing: First Steps Towards the Effective Regulation of Artificial Intelligence Systems"
- NIST AI Risk Management Framework 1.0
- EU AI Act Articles 9 and 72
- Institute of Internal Auditors, AI Auditing Framework
- FAccT 2024, "Null Compliance" on NYC Local Law 144
- New York State Comptroller audit on Local Law 144 enforcement
- Sarbanes-Oxley / PCAOB source material

## Remaining Decisions To Polish In A Final Submission Draft

- Whether to explicitly name a 90-day deadline for completing a post-update audit in Phase 2
- Whether to describe the AIAOB's funding as registration fees, an audit fund, or both
- Whether to keep the word "critical infrastructure" in the opening sentence or move it to the implementation section to save space
