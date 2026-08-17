# A/B Experiment Brief, RouteLogic (B2B)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | One-Click Compliance Checklist — a smart pre-filled workflow that lets coordinators review, correct, validate, and submit compliance information in one flow. |
| Persona | Frontline Logistics Coordinators responsible for planning, tracking, and updating daily shipments across multiple customers and carriers. |
| Expected outcome | More coordinators complete the end-to-end daily dispatch workflow by reducing compliance friction and manual effort. |
| Primary success metric | End-to-end Coordinator Daily Dispatch Workflow completion rate. |
| Baseline rate | 18% |
| Guardrail metric | Live Dispatch Board coordinator adoption remains ≥90% |
| Guardrail boundary | Must remain at or above 90%. |
| Second guardrail | Compliance submission accuracy must not decrease versus control |
| Minimum Detectable Effect | +10 percentage points |
| Sample size per arm | 277 |
| Traffic split | 50 / 50 |
| Test duration | 4 weeks |
| Significance threshold | p < 0.05 (95%) |

## Control vs. Variant
- **Control (A):** Coordinators complete the existing RouteLogic compliance workflow using the current multi-step experience, including manual data entry, validation, and navigation across existing workflow screens.
- **Variant (B):** Replace only the existing compliance step with the One-Click Compliance Checklist: available shipment data is pre-filled, coordinators review and correct fields, required fields are validated, and the checklist is submitted in one action.
- **Held constant (isolation check):** Same coordinators, shipment mix, RouteLogic version, dispatch workflow, Route Optimizer, Live Dispatch Board, scheduling, notifications, reporting, training, and carrier processes. Only the compliance checklist experience changes.

## Hypothesis
> I believe that One-Click Compliance Checklist — a smart pre-filled workflow that lets coordinators review, correct, validate, and submit compliance information in one flow. for Frontline Logistics Coordinators responsible for planning, tracking, and updating daily shipments across multiple customers and carriers. will result in More coordinators complete the end-to-end daily dispatch workflow by reducing compliance friction and manual effort., as measured by a +10 percentage points change in End-to-end Coordinator Daily Dispatch Workflow completion rate. within 4 weeks. We will protect Live Dispatch Board coordinator adoption remains ≥90% throughout the test.

## Shipping criteria
> We will **ship** if End-to-end Coordinator Daily Dispatch Workflow completion rate. improves by ≥ +10 percentage points at p < 0.05 (95%) and Live Dispatch Board coordinator adoption remains ≥90% does not reach Must remain at or above 90%. after 4 weeks.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 4 weeks, no results reviewed before this date.
