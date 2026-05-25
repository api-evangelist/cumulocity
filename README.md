# Cumulocity (cumulocity)
Cumulocity is an enterprise AIoT (Artificial Intelligence of Things) platform that connects, manages, and analyzes industrial assets from cloud to edge. Founded inside Software AG and divested via a 2025 management buyout into an independent company (sale announced alongside the IBM acquisition of Software AG's StreamSets and webMethods), Cumulocity provides a full-stack platform — REST and MQTT APIs, device management, digital twin modeling, streaming analytics powered by Apama, DataHub data-lake offload, Cockpit dashboards, and on-prem Edge deployments — validated at 100 million devices and 1 million messages/second.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/cumulocity/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - IoT, Internet of Things, Industrial IoT, AIoT, Device Management, Digital Twin, MQTT, Edge Computing, Streaming Analytics, Data Lake

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Plans

| Plan | Type | Price | Messages / mo | SLA | Notes |
|---|---|---|---|---|---|
| Free Trial | Free | $0 | trial | — | 30 days, up to 10 devices |
| Starter | Subscription | EUR 215 / mo (billed annually) | 2.5 M | 95% | 1 tenant, 30-day retention |
| Business | Contract | Contact Sales | 250 M | 99.0% | Multi-region, 24/7 crisis support |
| Enterprise | Contract | Contact Sales | Unlimited | 99.9% | Isolated infra, 24/7 all-incident |
| Edge Connected | Contract | Contact Sales | n/a (per-node) | — | Single-node on-prem with cloud sync |
| Edge Air-Gapped | Contract | Contact Sales | n/a (per-node) | — | Fully offline single-node |

## APIs

### Cumulocity Inventory API
Manage managed objects which represent any IoT-relevant asset including devices, groups, assets, and digital twins. Supports hierarchical parent/child relationships, fragment-based extensibility, full-text search, and bulk operations.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-inventory-api-openapi.yml)
- [JSON Schema — Managed Object](json-schema/cumulocity-managed-object-schema.json)
- [JSON-LD](json-ld/cumulocity-context.jsonld)
- [Naftiko Capability — Managed Objects](capabilities/inventory-managed-objects.yaml)
- [Naftiko Capability — Child References](capabilities/inventory-child-references.yaml)

### Cumulocity Identity API
Link external identifiers (IMEI, serial number, MAC, ICCID, c8y_Serial) to Cumulocity managed object IDs. The primary lookup table used by device bootstrap, MQTT auto-registration, and any provider-specific ID translation.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-identity-api-openapi.yml)
- [Naftiko Capability — External IDs](capabilities/identity-external-ids.yaml)

### Cumulocity Measurement API
Ingest, query, and delete device measurements (telemetry) including temperature, voltage, location, and arbitrary custom fragments with units. Supports time-range queries, source/type filters, series aggregations, and bulk creation.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-measurement-api-openapi.yml)
- [JSON Schema — Measurement](json-schema/cumulocity-measurement-schema.json)
- [Naftiko Capability — Measurements](capabilities/measurement-measurements.yaml)
- [Naftiko Capability — Series](capabilities/measurement-series.yaml)

### Cumulocity Event API
Create, query, and delete events emitted by devices and applications. Events carry a type, time, text, source device, and arbitrary custom fragments. Binary attachments are supported via the events/{id}/binaries sub-resource.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-event-api-openapi.yml)
- [JSON Schema — Event](json-schema/cumulocity-event-schema.json)
- [Naftiko Capability — Events](capabilities/event-events.yaml)
- [Naftiko Capability — Event Binaries](capabilities/event-binaries.yaml)

### Cumulocity Alarm API
Raise, query, acknowledge, clear, and bulk-update alarms with four severity levels (CRITICAL/MAJOR/MINOR/WARNING) and four statuses (ACTIVE/ACKNOWLEDGED/CLEARED). Cumulocity auto-deduplicates alarms by source + type.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-alarm-api-openapi.yml)
- [JSON Schema — Alarm](json-schema/cumulocity-alarm-schema.json)
- [JSON Structure — Alarm](json-structure/cumulocity-alarm-structure.json)
- [Naftiko Capability — Alarms](capabilities/alarm-alarms.yaml)

### Cumulocity Device Control API
Send and track operations (commands) to devices including firmware updates, configuration changes, software installation, shell commands, and restart requests. Operations transition PENDING → EXECUTING → SUCCESSFUL or FAILED. Bulk operations target entire device groups.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-device-control-api-openapi.yml)
- [Naftiko Capability — Operations](capabilities/device-control-operations.yaml)
- [Naftiko Capability — Bulk Operations](capabilities/device-control-bulk-operations.yaml)

### Cumulocity Device Bootstrap API
Zero-touch device onboarding flow. Factory-bootstrapped devices authenticate with a shared bootstrap user, poll for credentials, and receive back tenant-scoped credentials once an admin accepts the registration request.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-device-bootstrap-api-openapi.yml)
- [Naftiko Capability — Credentials](capabilities/device-bootstrap-credentials.yaml)

### Cumulocity Tenant API
Manage tenants (sub-tenants in enterprise and management hierarchies), tenant options (key-value config including encrypted secrets), tenant applications, and tenant usage statistics.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-tenant-api-openapi.yml)
- [Naftiko Capability — Tenants](capabilities/tenant-tenants.yaml)
- [Naftiko Capability — Options](capabilities/tenant-options.yaml)
- [Naftiko Capability — Statistics](capabilities/tenant-statistics.yaml)

### Cumulocity User API
Manage users, user groups, global roles, inventory roles, and device permissions. Supports SSO via SAML/OIDC and SCIM provisioning for enterprise tenants.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-user-api-openapi.yml)
- [Naftiko Capability — Users](capabilities/user-users.yaml)
- [Naftiko Capability — Groups](capabilities/user-groups.yaml)
- [Naftiko Capability — Roles](capabilities/user-roles.yaml)

### Cumulocity Application API
Register, subscribe, configure, and upload microservices, hosted web applications, and plugins. Microservices run inside Cumulocity's managed container runtime and authenticate via a bootstrap user issued by this API.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-application-api-openapi.yml)
- [Naftiko Capability — Applications](capabilities/application-applications.yaml)
- [Naftiko Capability — Bootstrap Users](capabilities/application-bootstrap-users.yaml)

### Cumulocity Audit API
Read the immutable audit trail of changes made within a tenant — user management actions, operations triggered, managed-object create/update/delete. Critical for compliance, security review, and incident forensics.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-audit-api-openapi.yml)
- [Naftiko Capability — Records](capabilities/audit-records.yaml)

### Cumulocity Retention Rules API
Define retention rules that automatically delete measurements, events, alarms, audit records, and operations older than a configured age. Rules can be scoped by data type, source, and fragment.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-retention-api-openapi.yml)
- [Naftiko Capability — Rules](capabilities/retention-rules.yaml)

### Cumulocity Real-Time Notifications API
Bayeux/CometD-based long-poll subscription protocol for live updates of measurements, events, alarms, operations, and inventory changes. Default for the Web SDK and legacy integrations.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-real-time-api-openapi.yml)
- [Naftiko Capability — Subscriptions](capabilities/real-time-subscriptions.yaml)

### Cumulocity Notification 2.0 API
High-throughput, persistent, ordered notification streaming for production microservices. Subscribers declare typed subscriptions, exchange them for JWT tokens, and consume via WebSocket. Survives subscriber outages by buffering messages on the server.

**Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)

- [OpenAPI](openapi/cumulocity-notification2-api-openapi.yml)
- [AsyncAPI](asyncapi/cumulocity-notification2-asyncapi.yml)
- [Naftiko Capability — Subscriptions](capabilities/notification2-subscriptions.yaml)
- [Naftiko Capability — Tokens](capabilities/notification2-tokens.yaml)

### Cumulocity MQTT and SmartREST API
Constrained-device MQTT broker fronting the Cumulocity REST API with a CSV-based SmartREST 2.0 payload format saving up to 80% mobile traffic vs JSON. 16 KiB max payload, MQTT 3.1.1 and 5.0, TLS on port 8883.

**Human URL:** [https://cumulocity.com/docs/device-integration/mqtt/](https://cumulocity.com/docs/device-integration/mqtt/)

- [AsyncAPI](asyncapi/cumulocity-mqtt-asyncapi.yml)
- [Naftiko Capability — MQTT / SmartREST](capabilities/mqtt-smartrest.yaml)

### Cumulocity MQTT Service API
Standards-compliant, multi-tenant MQTT 5.0 broker for application-level messaging independent of the Cumulocity domain model. Topics are tenant-scoped, persistent, and bridgeable via the Dynamic Mapper.

**Human URL:** [https://cumulocity.com/docs/device-integration/mqtt-service/](https://cumulocity.com/docs/device-integration/mqtt-service/)

- [AsyncAPI](asyncapi/cumulocity-mqtt-service-asyncapi.yml)
- [Naftiko Capability — Topics](capabilities/mqtt-service-topics.yaml)

### Cumulocity DataHub API
Offload operational IoT data into a Parquet-backed data lake queryable with ANSI SQL via Dremio. Configure offload pipelines, run analytics queries, export to BI tools (Power BI, Tableau) over JDBC/ODBC/Arrow Flight.

**Human URL:** [https://cumulocity.com/api/datahub/](https://cumulocity.com/api/datahub/)

- [OpenAPI](openapi/cumulocity-datahub-api-openapi.yml)
- [Naftiko Capability — Jobs](capabilities/datahub-jobs.yaml)
- [Naftiko Capability — Queries](capabilities/datahub-queries.yaml)

### Cumulocity Digital Twin Manager API
Model real-world assets and their hierarchies with strongly-typed asset models, custom properties, and computed smart-function values. Asset instances reference the underlying managed objects so measurements and alarms automatically roll up.

**Human URL:** [https://cumulocity.com/api/dtm/](https://cumulocity.com/api/dtm/)

- [OpenAPI](openapi/cumulocity-dtm-api-openapi.yml)
- [Naftiko Capability — Asset Models](capabilities/dtm-asset-models.yaml)
- [Naftiko Capability — Asset Instances](capabilities/dtm-asset-instances.yaml)

### Cumulocity Edge API
Single-node on-premises deployment of Cumulocity that runs the full platform locally and optionally syncs selected data to a cloud tenant. Targets factory floors, vessels, and regulated/air-gapped environments.

**Human URL:** [https://cumulocity.com/api/edge/](https://cumulocity.com/api/edge/)

- [OpenAPI](openapi/cumulocity-edge-api-openapi.yml)
- [Naftiko Capability — System](capabilities/edge-system.yaml)

## SDKs and Tools

- [Java Client SDK](https://github.com/Cumulocity-IoT/cumulocity-clients-java)
- [Python SDK](https://github.com/Cumulocity-IoT/cumulocity-python-api)
- [.NET SDK](https://github.com/Cumulocity-IoT/cumulocity-sdk-dotnet)
- [@c8y/client (JavaScript/TypeScript)](https://www.npmjs.com/package/@c8y/client)
- [Cumulocity UI Toolkit](https://github.com/Cumulocity-IoT/cumulocity-ui-toolkit)
- [go-c8y-cli (community CLI)](https://github.com/reubenmiller/go-c8y-cli)
- [go-c8y (Go client library)](https://github.com/reubenmiller/go-c8y)
- [Microservice Maven Archetype](https://github.com/Cumulocity-IoT/cumulocity-microservice-archetype)
- [Dynamic Mapper](https://github.com/Cumulocity-IoT/cumulocity-dynamic-mapper)
- [LoRa Framework](https://github.com/Cumulocity-IoT/cumulocity-lora)
- [Node-RED Microservice](https://github.com/Cumulocity-IoT/cumulocity-node-red)
- [Python Reference Device Management Agent](https://github.com/Cumulocity-IoT/cumulocity-devicemanagement-agent)
- [Cumulocity MCP Server (Python)](https://github.com/Cumulocity-IoT/cumulocity-mcp-server)
- [c8y AI Sandbox (MCP microservice)](https://github.com/Cumulocity-IoT/c8y-ai-sandbox)
- [thin-edge.io](https://thin-edge.io/)

## Artifacts

- [Plans & Pricing](plans/cumulocity-plans-pricing.yml) — API Commons Plans 0.1
- [Rate Limits](rate-limits/cumulocity-rate-limits.yml) — API Commons Rate Limits 0.1
- [FinOps](finops/cumulocity-finops.yml) — FOCUS 1.3 aligned
- [Spectral Ruleset](rules/cumulocity-rules.yml)
- [Vocabulary](vocabulary/cumulocity-vocabulary.yml)
- [JSON-LD Context](json-ld/cumulocity-context.jsonld)
