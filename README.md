# WISK.ai (wisk)

WISK.ai is an inventory management and hospitality intelligence platform for bars, restaurants, and hotels, covering inventory counts, invoicing, purchasing, recipe costing, and cost-of-goods tracking. It syncs with 60+ POS systems to align sales with inventory. WISK's integration surface is built for POS and data partners rather than a broad public developer program: partners can let WISK pull from their sales and product/menu APIs, or push daily sales data into WISK using its public sales-upload API, which is documented in a public Notion guide. New integrations begin by contacting the WISK integrations team, and email-based CSV/XLS feeds are supported as a fallback.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/wisk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/wisk/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- Restaurant
- Bar
- Inventory
- Hospitality
- Sales
- POS Integration

## Timestamps

- **Created:** 2026-06-02
- **Modified:** 2026-06-03

## APIs

### WISK Public Sales Upload API

WISK's public sales-upload API lets POS providers and partners push sales data into customer WISK accounts. The documented operation is a POST to /public/sales/upload that accepts a JSON array of sales line items, each with id, date, plu_number, title, quantity, and total. The destination venue is identified by a WISK-provisioned venue unique identifier supplied in the request header. It is documented in a public Notion guide, and integrations are initiated by contacting the WISK integrations team. WISK can alternatively pull from a partner's own sales and product/menu APIs.

- **Human URL:** [https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers](https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers)
- **Base URL:** `https://api.wisk.ai`

#### Tags

- Sales
- POS Integration
- Upload

#### Properties

- [OpenAPI](openapi/wisk-sales-upload-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/wisk-sales-upload.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/wisk-sales-upload.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://wiskai.notion.site/Public-Sales-upload-9d06c365cdea42069598a526dd657086)
- [Getting Started](https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers)
- [JSON Schema](json-schema/sales-upload-sales-line-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/sales-upload-sales-line-structure.json)
- [JSON-LD](json-ld/wisk-sales-upload-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/sales-upload-sales-line-example.json)

## Common Properties

- [Website](https://www.wisk.ai/)
- [Documentation](https://help.wisk.ai/en/articles/5071983-integrating-with-wisk-for-pos-providers)
- [Sign Up](https://www.wisk.ai/demo)
- [Login](https://web.wisk.ai/signin)
- [Pricing](https://www.wisk.ai/price)
- [Support](https://help.wisk.ai/en/)
- [Blog](https://www.wisk.ai/blog)
- [LinkedIn](https://www.linkedin.com/company/wisk)
- [X (Twitter)](https://twitter.com/WISK_ai)
- [Plans](plans/wisk-plans-pricing.yml)
- [Rate Limits](rate-limits/wisk-rate-limits.yml)
- [Fin Ops](finops/wisk-finops.yml)
- [Spectral Rules](rules/wisk-spectral-rules.yml)
- [Vocabulary](vocabulary/wisk-vocabulary.yaml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
