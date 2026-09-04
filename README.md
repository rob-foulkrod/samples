# Commodity Operations Disruption Briefing with Microsoft 365 Copilot

Classification: Public

**Fictional Microsoft Fake Company:** Northstar Grain Exchange

This demo uses a fictional Microsoft Fake Company created for demonstration purposes. Any resemblance to real organizations, people, products, services, or data is coincidental. Do not use customer confidential information in this package.

## Scenario overview

This GitHub-ready demo package supports a private delivery for a commodities trading and operations audience. The scenario follows Northstar Grain Exchange, a fictional agricultural commodity merchant, as its operations manager uses Microsoft 365 Copilot to triage shipment disruption risk, sustainability-traceability exceptions, customer communications, and an executive decision brief.

The scenario is inspired only by public industry themes from Louis Dreyfus Company: agricultural goods merchandising and processing, multiple commodity business lines, freight and grains/oilseeds operations, and traceable, agile supply chains. It does not use real LDC data, people, systems, customers, metrics, or internal processes.

## Target audience and persona

- **Industry:** Commodities trading, agricultural merchandising, freight, and operations
- **Primary persona:** Operations Manager / Trade Operations Lead
- **Secondary stakeholders:** Commercial account lead, logistics coordinator, sustainability analyst, finance controller, and COO
- **Delivery ID context:** 108584, private delivery, English, Eastern Time

## Technology focus and prerequisites

- **Demo Tool:** Microsoft 365 Copilot Chat using uploaded files as grounding material
- **Starting experience:** Microsoft 365 Copilot Chat
- **Build/use scope:** Use an existing Copilot experience; no tenant configuration required
- **Recommended demo length:** 25 minutes
- **Prerequisites:** Microsoft 365 Copilot access, ability to upload or reference the sample files, and presenter access to this repository package

## Repository contents

| Path | Purpose |
| --- | --- |
| [demo/DEMO-INSTRUCTIONS.md](demo/DEMO-INSTRUCTIONS.md) | Presenter script and prompt sequence |
| [demo/DEMO-INSTRUCTIONS.docx](demo/DEMO-INSTRUCTIONS.docx) | Word version of the same presenter guide |
| [demo/sample-data/northstar-grain-operations-brief.docx](demo/sample-data/northstar-grain-operations-brief.docx) | Grounding brief with business context, personas, constraints, and priorities |
| [demo/sample-data/shipment-risk-register.xlsx](demo/sample-data/shipment-risk-register.xlsx) | Primary structured dataset with 120 invented shipments, reference tabs, formulas, and chart |
| [demo/sample-data/supplier-sustainability-exceptions.csv](demo/sample-data/supplier-sustainability-exceptions.csv) | Traceability and supplier exception data for cross-file reasoning |
| [demo/sample-data/customer-update-template.docx](demo/sample-data/customer-update-template.docx) | Customer-facing communication template |
| [demo/sample-data/executive-brief-template.docx](demo/sample-data/executive-brief-template.docx) | COO decision brief template |
| [demo/sample-data/copilot-prompt-pack.json](demo/sample-data/copilot-prompt-pack.json) | Machine-readable prompt pack and acceptance criteria |
| [demo/sample-data/expected-output-executive-brief.md](demo/sample-data/expected-output-executive-brief.md) | Example result for presenter validation |
| [manifest.json](manifest.json) | Public package metadata and file inventory |
| [AI-CONTENT-DECLARATION.md](AI-CONTENT-DECLARATION.md) | AI transparency and public safety declaration |
| [LICENSE](LICENSE) | MIT license |

## Demo workflow summary

| Stage | Inputs | Copilot action | Output | Handoff |
| --- | --- | --- | --- | --- |
| Situation scan | Operations brief, risk workbook, exception CSV | Summarize disruptions and classify risk | Issue table | Prioritization |
| Intervention ranking | Workbook and exception CSV | Rank top 10 shipments for action | Ranked intervention list | Customer update |
| Customer communication | Customer template and top issues | Draft customer-safe update | Email-ready text | Executive brief |
| Executive brief | All sources and brief template | Create one-page COO decision brief | Decision brief | Operations call |
| Meeting prep | Decision brief | Convert brief to talking points | 15-minute run-of-show | Action tracking |
| Follow-through | Decisions and shipment data | Create action tracker | Owner-based action table | Post-demo close |

## Public research basis

- [Louis Dreyfus Company - Who We Are](https://www.ldc.com/who-we-are/) - Public description of LDC as a merchant and processor of agricultural goods operating across the value chain.
- [Louis Dreyfus Company - Business Lines](https://www.ldc.com/who-we-are/about-us/our-business-lines/) - Public list of business lines including Coffee, Cotton, Freight, Food & Feed Solutions, Grains & Oilseeds, Juice, Rice, Sugar, and Global Markets.
- [Louis Dreyfus Company - Sustainability](https://www.ldc.com/sustainability/) - Public themes around traceable, agile, efficient supply chains and sustainable practices.

## Setup instructions

1. Open Microsoft 365 Copilot Chat.
2. Attach or reference the files listed in the **Files to Attach** section of `demo/DEMO-INSTRUCTIONS.md`.
3. Run the prompts in order.
4. Compare outputs against the acceptance criteria and `expected-output-executive-brief.md`.
5. Do not add customer confidential information to this package or to Copilot prompts during the delivery.

## License

This package is provided under the MIT License. See [LICENSE](LICENSE).

## AI transparency

This repository contains AI-generated and human-reviewed demo content. All company names, people, shipment records, metrics, and operational details are fictional unless explicitly cited as public source references. See [AI-CONTENT-DECLARATION.md](AI-CONTENT-DECLARATION.md).
