# Demo Instructions: Commodity Operations Disruption Briefing with Microsoft 365 Copilot

Classification: Public

**Fictional Microsoft Fake Company:** Northstar Grain Exchange

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## 1. Demo title

Commodity Operations Disruption Briefing with Microsoft 365 Copilot

## 2. Scenario

Northstar Grain Exchange is managing several grain and oilseed shipments affected by port congestion, inland freight delays, inventory buffers, and sustainability-traceability exceptions. The Operations Manager needs to brief leadership, protect customer trust, and decide which shipments need intervention in the next 72 hours. Microsoft 365 Copilot helps reason across a business brief, a structured shipment workbook, exception data, and communication templates.

## 3. Demo Tool

- **App:** Microsoft 365 Copilot Chat
- **Experience:** File-grounded chat with attached Word, Excel, CSV, JSON, and Markdown files
- **Scope:** Use an existing Copilot experience; no agent build is required
- **Duration:** 25 minutes

## 4. Files to Attach

1. `demo/sample-data/northstar-grain-operations-brief.docx`
2. `demo/sample-data/shipment-risk-register.xlsx`
3. `demo/sample-data/supplier-sustainability-exceptions.csv`
4. `demo/sample-data/customer-update-template.docx`
5. `demo/sample-data/executive-brief-template.docx`
6. `demo/sample-data/expected-output-executive-brief.md`

Supporting prompt reference: `demo/sample-data/copilot-prompt-pack.json`.

## 5. Prompts

### Prompt 1: Create the disruption picture

```text
Using the attached operations brief, shipment risk register, and supplier sustainability exceptions, summarize the current disruption picture for Northstar Grain Exchange. Group the findings by commodity, corridor, customer impact, and compliance or traceability concern. Return a table with issue, evidence, likely business impact, and recommended next action.
```

- **Sources/files used:** northstar-grain-operations-brief.docx, shipment-risk-register.xlsx, supplier-sustainability-exceptions.csv
- **Required result format:** Executive summary plus a four-column issue table.
- **Acceptance criteria:** Mentions at least three corridors, separates logistics risk from sustainability exceptions, and names the highest-risk shipments by invented shipment ID.
- **Next handoff:** Use the prioritized issues for the customer communication draft.
- **Failure behavior:** If the workbook cannot be read, ask Copilot to use the operations brief and CSV first, then reattach the workbook.
- **Expected output:** A presenter-ready response that can be compared with `demo/sample-data/expected-output-executive-brief.md` where applicable.

### Prompt 2: Prioritize shipments for intervention

```text
From the shipment risk register, identify the top 10 shipments requiring intervention in the next 72 hours. Consider risk score, contract value, delivery window, customer tier, inventory buffer, and sustainability exception severity. Return ranked recommendations with owner, reason, and decision needed.
```

- **Sources/files used:** shipment-risk-register.xlsx, supplier-sustainability-exceptions.csv
- **Required result format:** Ranked table with shipment ID, owner, risk drivers, decision needed, and confidence.
- **Acceptance criteria:** Uses risk drivers from both the workbook and CSV; does not invent unavailable facts beyond the provided files.
- **Next handoff:** Select the top three customer-facing issues for Prompt 3.
- **Failure behavior:** If ranking is vague, ask Copilot to show the exact evidence column used for each rank.
- **Expected output:** A presenter-ready response that can be compared with `demo/sample-data/expected-output-executive-brief.md` where applicable.

### Prompt 3: Draft customer update

```text
Draft a concise customer update for the three highest-impact shipments using the customer update template. Keep the tone calm, specific, and commercially aware. Include what changed, what Northstar is doing, expected timing, and what the customer needs to decide. Do not mention internal risk scores.
```

- **Sources/files used:** customer-update-template.docx, shipment-risk-register.xlsx
- **Required result format:** Email-ready draft with subject line and three shipment sections.
- **Acceptance criteria:** Customer-safe language, no internal scoring, clear asks, and credible operations next steps.
- **Next handoff:** Use the same decisions and commitments in the executive brief.
- **Failure behavior:** If the response over-shares internal data, ask Copilot to rewrite for customer-facing language only.
- **Expected output:** A presenter-ready response that can be compared with `demo/sample-data/expected-output-executive-brief.md` where applicable.

### Prompt 4: Prepare executive decision brief

```text
Using the executive brief template, create a one-page decision brief for the COO. Include the situation, financial exposure, operational tradeoffs, customer risk, sustainability or traceability implications, recommended decisions, and open questions for the 4:00 PM operations call.
```

- **Sources/files used:** executive-brief-template.docx, shipment-risk-register.xlsx, supplier-sustainability-exceptions.csv, northstar-grain-operations-brief.docx
- **Required result format:** One-page brief with decision table and meeting agenda.
- **Acceptance criteria:** Includes quantified invented exposure from the workbook, three decisions, and five agenda questions.
- **Next handoff:** Use the agenda to prepare meeting talking points.
- **Failure behavior:** If the output is too long, ask for a version under 500 words with a decision table.
- **Expected output:** A presenter-ready response that can be compared with `demo/sample-data/expected-output-executive-brief.md` where applicable.

### Prompt 5: Create meeting talking points

```text
Turn the executive decision brief into talking points for a 15-minute operations call. Include a 60-second opening, three decision moments, stakeholder-specific objections, and close with assigned owners.
```

- **Sources/files used:** expected-output-executive-brief.md
- **Required result format:** Timed run-of-show with speaker notes.
- **Acceptance criteria:** Fits within 15 minutes and includes operations, commercial, sustainability, and finance perspectives.
- **Next handoff:** Use owner assignments to update the risk register after the call.
- **Failure behavior:** If roles are generic, ask Copilot to map each point to the persona list in the operations brief.
- **Expected output:** A presenter-ready response that can be compared with `demo/sample-data/expected-output-executive-brief.md` where applicable.

### Prompt 6: Update action tracker

```text
Create an action tracker from the decisions and open questions. Include action, owner role, due date, dependency, status, and success measure. Use only information already present in the brief and attached files.
```

- **Sources/files used:** expected-output-executive-brief.md, shipment-risk-register.xlsx
- **Required result format:** Markdown table suitable for pasting into Teams or Loop.
- **Acceptance criteria:** Every action has an owner role, due date, and measurable outcome; no customer confidential information is included.
- **Next handoff:** Presenter can show how Copilot converts decisions into follow-through.
- **Failure behavior:** If due dates are missing, ask Copilot to propose due dates relative to the delivery window shown in the workbook.
- **Expected output:** A presenter-ready response that can be compared with `demo/sample-data/expected-output-executive-brief.md` where applicable.

## 6. Build or Configure

No product build is required. Before delivery, copy or upload the files into the demonstration environment where Microsoft 365 Copilot can access them. Keep all files classified as Public.

## 7. Test and Validate

1. Confirm Copilot can read the Word, Excel, CSV, and Markdown files.
2. Run Prompt 1 and check that it names multiple corridors and differentiates logistics risks from sustainability exceptions.
3. Run Prompt 2 and check that workbook data affects the ranking.
4. Run Prompt 3 and verify the draft excludes internal risk scores.
5. Run Prompt 4 and compare the decision brief to `expected-output-executive-brief.md`.

## 8. Cleanup

Remove uploaded demo files from any temporary chat, meeting, or shared location used during the delivery. Do not retain customer-added notes in this package.
