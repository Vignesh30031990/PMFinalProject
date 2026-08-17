# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on our qualitative and quantitative evidence, I believe simplifying compliance workflow friction for Frontline Logistics Coordinators will increase end-to-end daily dispatch workflow completion while reducing manual effort and protecting adoption of the core dispatch experience.
- **From M3, your primary success metric & guardrail metric:** Primary: End-to-end Coordinator Daily Dispatch Workflow completion rate. Guardrail: Live Dispatch Board coordinator adoption rate.
- **From M4, the feature you scoped in your PRD this is what you're testing:** One-Click Compliance Checklist — a smart pre-filled workflow that lets coordinators review, correct, validate, and submit compliance information in one flow.

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** One-Click Compliance Checklist
- **Persona pull your M2 persona:** Frontline Logistics Coordinators responsible for planning, tracking, and updating daily shipments across multiple customers and carriers.
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** More coordinators complete the end-to-end daily dispatch workflow by reducing compliance friction and manual effort.
- **Primary success metric the one number that defines success, from M3:** End-to-end Coordinator Daily Dispatch Workflow completion rate.
- **Baseline rate today's rate of your primary metric, from your M3 data:** 18%
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Live Dispatch Board coordinator adoption rate must remain at or above 90%.
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** +10 percentage points
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 277 users
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 split for 4 weeks.
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05 (95%); 80% statistical power.

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** Coordinators complete the existing RouteLogic compliance workflow using the current multi-step experience, including manual data entry, validation, and navigation across existing workflow screens.
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** Replace only the existing compliance step with the One-Click Compliance Checklist: available shipment data is pre-filled, coordinators review and correct fields, all required fields are independently validated, and the checklist is submitted in one action.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** Same coordinators, shipment mix, RouteLogic version, dispatch workflow, Route Optimizer, Live Dispatch Board, scheduling, notifications, reporting, training, and carrier processes. Only the compliance checklist experience changes.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that the One-Click Compliance Checklist for Frontline Logistics Coordinators will result in more coordinators completing the end-to-end daily dispatch workflow, as measured by a +10 percentage-point improvement in workflow completion rate within 4 weeks. We will protect Live Dispatch Board coordinator adoption at ≥90% throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if end-to-end Coordinator Daily Dispatch Workflow completion improves by ≥10 percentage points at p < 0.05 and Live Dispatch Board coordinator adoption remains ≥90% after 4 weeks. We will ITERATE if the direction is positive but lift is below the MDE. We will KILL if the primary metric shows no improvement or moves negatively. Results will be read only at the end of the 4-week test.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The MDE was the hardest parameter to define because it required deciding what improvement would be meaningful enough to justify shipping. Setting it at +10 percentage points made the hypothesis more specific and testable, but did not change the underlying belief that simplifying compliance will improve workflow completion.
