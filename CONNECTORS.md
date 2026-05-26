# Adding a Connector

The plugins are at their best when connected to authoritative sources. If you build or operate a legal data source, research tool, CLM, DMS, eDiscovery platform, or practice management system, we want your MCP connector in the suite.

## What makes a good legal MCP connector

- **Remote MCP server over HTTPS** with OAuth or API-key auth (streamable HTTP or SSE transport)
- **Read-heavy tools** — search, fetch, list. Write tools (create, send, file) need an explicit confirmation prompt on the client side; say so in your tool descriptions.
- **Provenance in results** — return the source, date retrieved, and a citation-ready identifier. The plugins tag every cite by source; your connector should make that possible.
- **No instruction-like content in results** — the plugins treat retrieved content as data, not commands. If your tool results include metadata or system notes, mark them clearly so they don't look like embedded directives.
- **Rate limits and errors that degrade gracefully** — the plugins have a fallback for when a connector isn't responding; a clean error is better than a timeout.

## How to submit

1. Publish your MCP server and document its tools, auth flow, and data coverage.
2. Open a PR adding your server to the relevant plugin's `.mcp.json` with the URL, auth method, and a one-line description of what it gives Claude.
3. Include a note on which practice areas / plugins it's most useful for.
4. We'll test against the plugin workflows and merge. Connectors that pass the retrieval-quality and injection-resistance checks go in the default `.mcp.json`; others get documented in the plugin README for users to add themselves.

## Current connectors

Connectors shipped in the default `.mcp.json` of each plugin:

| Connector | Plugins |
|---|---|
| **Slack** | all 12 |
| **Google Drive** (`gdrive`) | all 12 |
| **CourtListener** | legal-clinic, ip-legal, litigation-legal, law-student |
| **Descrybe** | legal-clinic, ip-legal, law-student |
| **Definely** | commercial-legal, corporate-legal |
| **iManage** | commercial-legal, corporate-legal |
| **Solve Intelligence** | corporate-legal, ip-legal |
| **TopCounsel** | commercial-legal, corporate-legal, litigation-legal |
| **Box** | corporate-legal |
| **Ironclad** | commercial-legal |
| **DocuSign / DocuSign CLM** | commercial-legal |
| **Everlaw** | litigation-legal |
| **Trellis** | litigation-legal |
| **Aurora** | litigation-legal |
| **Courtroom5** | legal-clinic |
| **Lawve AI** | legal-builder-hub |
| **Linear** | product-legal |
| **Atlassian (Jira)** | product-legal |
| **Asana** | product-legal |

## Argentina / LatAm connectors

For Argentine practice, the useful connector layer is not a closed research
database but a set of official-source adapters. A connector should preserve
provenance, retrieval date and a citation-ready identifier. It should not turn
retrieved content into hidden instructions.

Suggested public connector categories:

| Connector category | Source | Useful for |
|---|---|---|
| InfoLEG / SAIJ | National legislation and legal search | commercial-legal, employment-legal, litigation-legal, regulatory-legal |
| Boletin Oficial / BOPBA | Official publications | regulatory-legal, litigation-legal, corporate-legal |
| Normativa PBA | Buenos Aires provincial legislation | litigation-legal, regulatory-legal |
| JUBA / SCBA | Buenos Aires case law | litigation-legal, legal-clinic |
| PTN | Administrative opinions | regulatory-legal, public-law workflows |
| Tesauro SAIJ | Controlled vocabulary | search expansion and citation hygiene |

### JustitIA-compatible private layer

JustitIA (`https://justitia.com.ar`) is not bundled with this repository and this
repository does not expose JustitIA code, prompts, private corpora, tenant data or
internal orchestration. If a JustitIA MCP/API connector is published in the future,
it should be treated as an authenticated private layer for authorized users only.

Appropriate public surface:

- search within an authorized firm's private library;
- analyze a document submitted by the authenticated user;
- verify citations against configured sources;
- return auditable findings with provenance and tenant authorization.

Not appropriate for a public repo:

- internal prompts;
- skill-routing logic;
- client documents;
- private evaluation corpora;
- tenant configuration;
- credentials or private endpoints.

See the `.mcp.json` in each plugin directory for the authoritative list.

## Wanted connectors

These would make specific plugins significantly more useful. If you build or operate one, see "How to submit" above.

- **IP management systems** (Anaqua, Clarivate IPfolio, AppColl, Patrix, Alt Legal, FoundationIP) — full docket sync for `ip-legal` portfolio tracking
- **USPTO by customer number** — full portfolio status and deadlines, not just per-application lookup
- **USPTO TSDR / Trademark Status** — trademark status and deadlines for `ip-legal` brand management
- **Jira / Linear / Asana for OSS requests** — `ip-legal` OSS clearance can monitor and respond to incoming tickets
- **Thomson Reuters** (CoCounsel, Practical Law, Westlaw) — research and drafting for every plugin
- **SS&C Intralinks / Datasite** — VDR access for `corporate-legal` diligence
- **Relativity / Everlaw beyond read** — eDiscovery workflow for `litigation-legal`
- **State bar CLE trackers** — `law-student` bar prep
- **Court e-filing systems** (PACER write, state e-filing) — with a hard irreversibility gate, obviously
- **Global AI Regulation Tracker** (techieray.com/GlobalAIRegulationTracker) — jurisdiction-tagged AI regulation tracking with structured API. Curated, verified, multi-jurisdiction. Would be a primary-source-adjacent feed for `ai-governance-legal` and `regulatory-legal`.
- **Regulatory primary sources** — a connector to official registers (eCFR, Federal Register, EUR-Lex, legislation.gov.uk, Federal Register of Legislation AU, Singapore Statutes Online) that bypasses the agent-blockers many legislative sites use. A curated regulatory knowledge base would be a high-value addition.

## Questions

Open an issue on this repo. For partnership or integration questions, see the contact on each plugin's README.
