# WISK.ai (wisk)

WISK.ai is an inventory management and hospitality intelligence platform for bars, restaurants, and hotels, covering inventory counts, invoicing, purchasing, recipe costing, and cost-of-goods tracking. It syncs with 60+ POS systems to align sales with inventory. WISK's integration surface is built for POS and data partners rather than a broad public developer program: partners can let WISK pull from their sales and product/menu APIs, or push daily sales data into WISK using its public sales-upload API, which is documented in a public Notion guide. New integrations begin by contacting the WISK integrations team, and email-based CSV/XLS feeds are supported as a fallback.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/wisk/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Restaurant, Bar, Inventory, Hospitality, Sales, POS Integration

## Timestamps

- **Created:** 2026-06-02
- **Modified:** 2026-06-03

## APIs

### WISK Public Sales Upload API

WISK's public sales-upload API lets POS providers and partners push sales data into customer WISK accounts. The documented operation is a POST to /public/sales/upload that accepts a JSON array of sales line items, each with id, date, plu_number, title, quantity, and total. The destination venue is identified by a WISK-provisioned venue unique identifier supplied in the request header. It is documented in a public Notion guide, and integrations are initiated by contacting the WISK integrations team. WISK can alternatively pull from a partner's own sales and product/menu APIs.

**Human URL:** [https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers](https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers)

**Base URL:** https://api.wisk.ai

#### Tags:

 - Sales, POS Integration, Upload

#### Properties

- [OpenAPI](openapi/wisk-sales-upload-openapi.yml)
- [Documentation](https://wiskai.notion.site/Public-Sales-upload-9d06c365cdea42069598a526dd657086)
- [GettingStarted](https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers)
- [JSONSchema](json-schema/sales-upload-sales-line-schema.json)
- [JSONStructure](json-structure/sales-upload-sales-line-structure.json)
- [JSONLD](json-ld/wisk-sales-upload-context.jsonld)
- [Example](examples/sales-upload-sales-line-example.json)
- [NaftikoCapability](capabilities/sales-upload-sales.yaml)

## Common Properties

- [Website](https://www.wisk.ai/)
- [Documentation](https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers)
- [SignUp](https://www.wisk.ai/demo)
- [Login](https://web.wisk.ai/signin)
- [Pricing](https://www.wisk.ai/price)
- [Support](https://help.wisk.ai/en/)
- [Blog](https://www.wisk.ai/blog)
- [LinkedIn](https://www.linkedin.com/company/wisk)
- [X](https://twitter.com/WISK_ai)
- [Plans](plans/wisk-plans-pricing.yml)
- [RateLimits](rate-limits/wisk-rate-limits.yml)
- [FinOps](finops/wisk-finops.yml)
- [SpectralRules](rules/wisk-spectral-rules.yml)
- [Vocabulary](vocabulary/wisk-vocabulary.yaml)

## Features

| Name | Description |
|------|-------------|
| Sales Upload API | Push point-of-sale sales lines into a WISK venue account via a single POST to /public/sales/upload accepting a JSON array of line items. |
| POS Pull Integrations | WISK can pull from a partner's own Sales API and Product/Menu API to ingest sales and item data into customer accounts. |
| CSV/XLS Email Fallback | For POS systems without an API, automated daily sales or product-mix reports can be emailed to WISK in XLS or CSV format. |
| Inventory and Cost Tracking | Inventory counts, invoicing, purchasing, recipe costing, and cost-of-goods tracking across bars, restaurants, and hotels. |

## Use Cases

| Name | Description |
|------|-------------|
| POS Provider Integration | A POS platform integrates with WISK so its venues' sales data flows into WISK for inventory reconciliation. |
| Daily Sales Reconciliation | Push daily sales lines so WISK can deplete inventory against actual POS sales and surface variance. |
| Multi-Location Inventory | Operators manage inventory, invoices, and cost of goods across multiple venues from one platform. |

## Integrations

| Name | Description |
|------|-------------|
| Direct POS Integrations | 60+ POS systems including Toast, Square, Clover, Lightspeed, Revel, TouchBistro, Heartland, Aldelo, Arryved, and many more. |
| Omnivore Universal API | Several POS systems integrate through Omnivore's Universal API, including Aloha, Brink, Oracle Hospitality (Micros/Simphony), POSitouch, and Doshii-connected systems. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [WISK Public Sales Upload API](openapi/wisk-sales-upload-openapi.yml)

### JSON Schema

- [Sales Line](json-schema/sales-upload-sales-line-schema.json)

### JSON Structure

- [Sales Line](json-structure/sales-upload-sales-line-structure.json)

### JSON-LD

- [WISK Sales Upload Context](json-ld/wisk-sales-upload-context.jsonld)

### Examples

- [Sales Line Example](examples/sales-upload-sales-line-example.json)

## Capabilities

Naftiko capabilities organized as self-contained per-surface definitions exposing both REST and MCP adapters.

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Sales Upload — Sales](capabilities/sales-upload-sales.yaml) | WISK Public Sales Upload API | 1 | POS Provider / Integration Partner |

## Commercial

- [Plans & Pricing](plans/wisk-plans-pricing.yml) — Tiered per-location subscription (Essentials / Professional / Premium) plus food add-on and human-review packs
- [Rate Limits](rate-limits/wisk-rate-limits.yml) — No numeric limits published; daily per-venue push cadence arranged via integrations onboarding
- [FinOps](finops/wisk-finops.yml) — FOCUS-aligned tiered-subscription billing model

## Vocabulary

- [WISK.ai Vocabulary](vocabulary/wisk-vocabulary.yaml) — Unified taxonomy mapping 1 resource, 1 action, 1 workflow, and 2 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [WISK Spectral Rules](rules/wisk-spectral-rules.yml) — 26 rules across info, servers, paths, operations, tags, request bodies, responses, schemas, and security categories enforcing WISK API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
