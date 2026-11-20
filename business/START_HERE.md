# REA Commercial Service Launch Kit

This folder is an operating kit for offering lawful software-analysis and reconstruction services using the upstream REA toolkit. It does not change REA's engine, grant additional capabilities, or make REA itself a paid product.

## 1. What to sell

Sell the professional work and verified deliverables—not access to REA.

### Service A — App feature investigation
For a client who owns an app or has written permission to inspect it.

Deliver:
- A map of the requested user journey and observable states.
- Evidence-backed explanation of the rules, inputs, outputs, and edge cases.
- A list of confirmed facts, assumptions, gaps, and items not tested.
- A clean-room implementation plan for the client's own product.

### Service B — Android application technical assessment
For a client-owned APK or an APK they are authorized to assess.

Deliver:
- Package and manifest overview.
- Permissions, exported components, SDK/build clues, and dependency observations where supported.
- Relevant code-flow findings from static analysis.
- Risk/compatibility observations with evidence and limitations.
- Prioritized remediation or modernization recommendations.

Do not describe a static review as a full penetration test or security certification.

### Service C — Web/Electron application analysis
For an authorized local build, source bundle, or application installation.

Deliver:
- Application/module map.
- Relevant feature flow and state transitions.
- API/request observations only where the client has authorized the environment and capture.
- A clean-room feature specification and implementation estimate.

### Service D — Rebuild or modernization
A separate implementation engagement based on the client's requirements and lawful observations. Quote it separately from investigation.

## 2. Ideal first customers

Start with small software companies, agencies, founders, and businesses that:
- Have an app they own but have lost documentation for.
- Need to migrate an old app or understand a legacy workflow.
- Need an Android APK compatibility assessment.
- Want a feature specification before commissioning a rebuild.
- Need to understand an authorized third-party integration or interoperability issue.

Do not promise that REA can recover original source code. It produces evidence and analysis; the engineer interprets the findings and writes any new implementation.

## 3. Standard delivery workflow

1. **Qualify:** identify the client, asset owner, exact target, requested outcome, and deadline.
2. **Authorize:** obtain written proof of ownership or permission. Define whether static inspection, execution, network capture, device changes, and sharing of findings are allowed.
3. **Scope:** choose one app, one build/version, and a small number of named workflows for the first milestone.
4. **Prepare:** record the target hash/version, host OS, REA version, tools/providers, and test environment.
5. **Inspect:** begin with read-only/static analysis. Escalate to runtime observation only when explicitly authorized.
6. **Verify:** reproduce important findings, preserve evidence, and mark uncertainty. Do not present guesses as facts.
7. **Report:** use the report template in this folder.
8. **Handover:** provide the report, agreed evidence files, recommendations, and a short walkthrough. Delete client data according to the contract.

## 4. Client intake — questions to answer before accepting work

- What is the client's legal/business name and contact?
- Who owns the app, APK, website, device, or binary?
- What document or written authorization permits this analysis?
- What exact app name, version, package ID, URL, or file is in scope?
- Which one to three workflows or technical questions matter most?
- Is the work limited to static analysis, or is runtime/network/device testing also authorized?
- Are test accounts and test data supplied by the client?
- What must not be accessed, changed, copied, or retained?
- What deliverables, deadline, and acceptance criteria are agreed?
- Who can approve additional scope?

Decline work where ownership/authorization is unclear or where the requested outcome involves credential theft, unauthorized access, DRM/license circumvention, anti-cheat bypass, malware deployment, or copying protected code/assets.

## 5. Reusable agent prompts

### Feature investigation
> Analyze only the application and workflow I am authorized to inspect. First identify the target/version and the narrowest relevant feature. Trace the observable behavior and supporting code/evidence. Separate confirmed facts from hypotheses. Record inputs, outputs, state transitions, validation rules, errors, and untested cases. Do not bypass authentication, access controls, DRM, or licensing. Do not copy proprietary code or assets. Finish with an evidence-backed feature specification and a clean-room implementation plan.

### Android APK assessment
> Assess this client-authorized APK using read-only/static methods first. Report package identity, manifest/components, requested permissions, SDK/build clues, and relevant code paths where supported. Cite evidence for every finding. Identify coverage gaps and limitations. Do not install, execute, modify, or contact remote services unless the client has separately authorized those actions. Do not call this a penetration test.

### Web/Electron assessment
> Analyze this client-authorized local application/build. Map its modules and trace only the named workflow. Identify relevant state, validation, request construction, and error handling where evidence supports it. Do not probe production endpoints or capture traffic unless that activity is explicitly in scope. Finish with a clean-room specification and list of unknowns.

## 6. Commercial controls

- Use a written statement of work and a deposit/milestone arrangement.
- Price by scope, complexity, risk, turnaround, and deliverable—not by the number of REA tool calls.
- Keep investigation and implementation as separate line items.
- Agree on change-control before investigating additional workflows.
- Never promise complete source recovery, guaranteed vulnerability discovery, or a security certification from static analysis.
- Use client-approved storage and transfer methods. Keep credentials out of reports and source control.
- Do not upload client code, APKs, logs, secrets, or personal data to public repositories.
- Keep a private job folder per client and follow the agreed retention/deletion period.

## 7. Initial launch offer

A practical first offer is a **Fixed-Scope App Workflow & APK Assessment**:
- One client-authorized APK or local app build.
- One to three named workflows or technical questions.
- Static-first inspection.
- Evidence-backed PDF report and prioritized next-step plan.
- Optional separately quoted clean-room prototype.

Before quoting, inspect a sample asset only if the prospect has authorized it. Offer a short discovery call; do not perform unpaid deep analysis.

## 8. Readiness checklist

- [ ] Install a supported Node.js/npm runtime and the official `rea-agents` package.
- [ ] Register REA with a supported local MCP agent and restart that agent.
- [ ] Run REA's doctor/readiness checks and one harmless sample analysis.
- [ ] Confirm the exact target type is supported before promising a deliverable.
- [ ] Create a clean test workspace and a private client-data handling process.
- [ ] Complete one sample report using software you own or are authorized to inspect.
- [ ] Prepare a one-page service description and statement-of-work template.
- [ ] Do not advertise services as available until the workflow has been tested end-to-end.

## 9. Official project and legal boundaries

- Upstream source: https://github.com/morluto/rea
- Official project site: https://rea.tools/
- Package: https://www.npmjs.com/package/rea-agents
- License: MIT (retain applicable notices and third-party license obligations).

Use REA only for software you own or are authorized to examine. Follow the upstream disclaimer and applicable local law. Commercial analysis tools such as IDA or Hopper require their own valid licenses; REA does not grant those licenses.
