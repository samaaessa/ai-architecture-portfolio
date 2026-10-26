# AI Architecture Portfolio

My work for the **AI Architecture Design** course: one scenario, designed end to end, one session at a time.
## Scenario
The course defines the use case: **Marketing Automation with AI & Agents**. The company, goals and numbers below are my own assumptions, so the decisions have something concrete to trade off against.

**The company:** a fictional e-commerce retailer selling online in **Egypt and Saudi Arabia**, with about **2 million customers**. Marketers run campaigns on **email, SMS, WhatsApp and app push / in-app**.

**The problem:** every campaign needs copy in Arabic and English, adapted for each market and channel. Writing it takes days, and results are reviewed too late to improve the next campaign.

**What the AI does**
- **Content agent:** turns a marketer's brief into on-brand message variants per segment, market, language and channel, using the brand guide, product catalogue and past campaigns.
- **Analysis agent:** reads campaign results and recommends what to test next and where to shift budget.

**What stays with people and existing tools:** marketers choose the audience in the CRM, approve every message, and send it from the current campaign tools. The agents never send anything.

## Business goals
| ID | Goal | Target (12 months) |
|----|------|--------------------|
| G1 | **Grow campaign revenue** (top priority) | +15% campaign-attributed revenue |
| G2 | Launch campaigns faster | Brief-to-send from ~10 days to 2 days or less |
| G3 | Keep customer trust and comply in both countries | Zero privacy incidents; unsubscribe rate no higher than today |
| G4 | Keep AI cost predictable | AI cost at most 2% of campaign-attributed revenue |

## Assumptions
- **Hybrid hosting:** customer data (CRM, orders) stays on-premises, in a data centre in each country: Egyptian customer data in Egypt, Saudi customer data in Saudi Arabia. The new AI platform runs in the cloud.
- **Two privacy laws:** Egypt's Personal Data Protection Law (Law No. 151 of 2020) and Saudi Arabia's PDPL. Both restrict sending personal data abroad.
- **Languages:** Arabic, with tone adapted for Egyptian and Saudi audiences, plus English.
- **Team:** a large platform team that can run its own infrastructure, including self-hosted models.
- All numbers are illustrative course targets, not real company data.

## How to read this repo
| Folder | What's inside |
|--------|---------------|
| [docs/](docs/) | One page per session. Start with [01-framing.md](docs/01-framing.md). |
| [adr/](adr/) | Architecture Decision Records, one decision per file. |
| [diagrams/](diagrams/) | Exported PNG/SVG plus the editable `.drawio` sources. |
| [capstone/](capstone/) | Final architecture (PDF) and slides. |

## Progress
| Session | Topic | Deliverables |
|---------|-------|--------------|
| 1 | Framing & governance | [Governance pack](docs/01-framing.md) (in progress): principles drafted; ADRs, ARB checklist and diagram to do |
