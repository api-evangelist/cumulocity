# Cumulocity (cumulocity)

Cumulocity is an enterprise AIoT (Artificial Intelligence of Things) platform that connects, manages, and analyzes industrial assets from cloud to edge. Founded inside Software AG and divested via a 2025 management buyout into an independent company (sale announced alongside the IBM acquisition of Software AG's StreamSets and webMethods), Cumulocity provides a full-stack platform — REST and MQTT APIs, device management, digital twin modeling, streaming analytics powered by Apama, DataHub data-lake offload, Cockpit dashboards, and on-prem Edge deployments — validated at 100 million devices and 1 million messages/second across industrial equipment, medical devices, manufacturing, utilities, energy, transport, retail, and telecommunications.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/cumulocity/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/cumulocity/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- IoT
- Internet of Things
- Industrial IoT
- AIoT
- Device Management
- Digital Twin
- MQTT
- Edge Computing
- Streaming Analytics
- Data Lake

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### Cumulocity Inventory API

Manage Cumulocity managed objects which represent any IoT-relevant asset including devices, groups, assets, and digital twins. Supports hierarchical parent/child relationships, fragment-based extensibility, full-text search, and bulk operations on the /inventory/managedObjects collection.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/inventory`

#### Tags

- IoT
- Inventory
- Managed Objects
- Devices
- Assets

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [Documentation](https://cumulocity.com/docs/concepts/domain-model/)
- [OpenAPI](openapi/cumulocity-inventory-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/cumulocity-managed-object-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/cumulocity-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Cumulocity Identity API

Link external identifiers (IMEI, serial numbers, MAC addresses, ICCID, c8y_Serial, etc.) to Cumulocity managed object IDs. The Identity API is the primary lookup table used by device bootstrap, MQTT auto-registration, and any integration that needs to translate provider-specific IDs to Cumulocity IDs.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/identity`

#### Tags

- IoT
- Identity
- External IDs
- Devices

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-identity-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-identity-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-identity-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Measurement API

Ingest, query, and delete device measurements (telemetry data points) including temperature, voltage, location, and arbitrary custom fragments with units. Supports time-range queries, source filters, type filters, series aggregations (hourly/daily), and bulk creation via the /measurement/measurements collection.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/measurement`

#### Tags

- IoT
- Measurements
- Time Series
- Telemetry

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-measurement-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-measurement-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-measurement-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/cumulocity-measurement-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Cumulocity Event API

Create, query, and delete events emitted by devices and applications. Events capture discrete happenings (door opened, geofence crossed, image captured) with a type, time, text, source device, and arbitrary custom fragments. Binary attachments are supported via the events/{id}/binaries sub-resource.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/event`

#### Tags

- IoT
- Events
- Telemetry

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-event-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-event-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-event-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/cumulocity-event-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Cumulocity Alarm API

Raise, query, acknowledge, clear, and bulk-update alarms with four severity levels (CRITICAL, MAJOR, MINOR, WARNING) and four statuses (ACTIVE, ACKNOWLEDGED, CLEARED). Cumulocity auto-deduplicates alarms by source + type so repeated raises increment the count rather than creating duplicates.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/alarm`

#### Tags

- IoT
- Alarms
- Monitoring

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-alarm-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-alarm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-alarm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/cumulocity-alarm-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Cumulocity Device Control API

Send and track operations (commands) to devices including firmware updates, configuration changes, software installation, shell commands, and restart requests. Operations move through PENDING, EXECUTING, SUCCESSFUL, FAILED status. Bulk operations let you target an entire device group with a single request.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/devicecontrol`

#### Tags

- IoT
- Operations
- Device Control
- Bulk Operations

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-device-control-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-device-control-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-device-control-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Device Bootstrap API

Zero-touch device onboarding flow. A factory-bootstrapped device authenticates with a shared bootstrap user, polls /devicecontrol/deviceCredentials with its external ID, and receives back tenant-scoped credentials once an admin accepts the registration request in the Device Management UI.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/devicecontrol/deviceCredentials`

#### Tags

- IoT
- Device Onboarding
- Bootstrap
- Registration

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [Documentation](https://cumulocity.com/docs/device-integration/device-integration-introduction/)
- [OpenAPI](openapi/cumulocity-device-bootstrap-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-device-bootstrap-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-device-bootstrap-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Tenant API

Manage Cumulocity tenants (sub-tenants in enterprise and management hierarchies), tenant options (key-value config including encrypted secrets), tenant applications, and tenant usage statistics. Enterprise customers use this API to programmatically provision and meter sub-tenants.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/tenant`

#### Tags

- IoT
- Multi-Tenancy
- Administration
- Tenant Options

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-tenant-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-tenant-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-tenant-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity User API

Manage users, user groups, global roles, inventory roles, and device permissions. Cumulocity uses an RBAC model where global roles grant API access and inventory roles grant access to specific managed-object subtrees. Supports SSO via SAML/OIDC and SCIM provisioning for enterprise tenants.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/user`

#### Tags

- IoT
- Users
- Roles
- Permissions
- RBAC

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-user-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-user-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-user-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Application API

Register, subscribe, configure, and upload Cumulocity microservices, hosted web applications, and plugins. Microservices run inside Cumulocity's managed container runtime and authenticate via a bootstrap user issued by this API; web applications are uploaded as ZIPs and served from the tenant subdomain.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/application`

#### Tags

- IoT
- Applications
- Microservices
- Plugins

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [Documentation](https://cumulocity.com/docs/microservice-sdk/)
- [OpenAPI](openapi/cumulocity-application-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-application-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-application-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Audit API

Read the immutable audit trail of changes made within a tenant, including user management actions, operations triggered, and managed-object create/update/delete. Critical for compliance, security review, and incident forensics.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/audit`

#### Tags

- IoT
- Audit
- Compliance
- Governance

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-audit-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-audit-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-audit-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Retention Rules API

Define retention rules that automatically delete measurements, events, alarms, audit records, and operations older than a configured age. Rules can be scoped by data type, source, and fragment. Default policies apply per-plan; Enterprise tenants can override.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/retention`

#### Tags

- IoT
- Retention
- Data Lifecycle
- Compliance

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-retention-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-retention-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-retention-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Real-Time Notifications API

Bayeux/CometD-based long-poll subscription protocol for receiving live updates of measurements, events, alarms, operations, and inventory changes. Predates Notification 2.0 but remains the default for the Web SDK and legacy integrations.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/notification/realtime`

#### Tags

- IoT
- Real-Time
- Bayeux
- CometD
- Streaming

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [OpenAPI](openapi/cumulocity-real-time-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-real-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-real-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Notification 2.0 API

High-throughput, persistent, ordered notification streaming designed for production microservices. Subscribers declare typed subscriptions (mo, measurements, events, alarms, operations), exchange them for short-lived JWT tokens, and consume via WebSocket. Survives subscriber outages by buffering messages on the server.

- **Human URL:** [https://cumulocity.com/api/core/](https://cumulocity.com/api/core/)
- **Base URL:** `https://{tenant}.cumulocity.com/notification2`

#### Tags

- IoT
- Notifications
- Streaming
- Webhooks
- Kafka

#### Properties

- [Documentation](https://cumulocity.com/api/core/)
- [Documentation](https://cumulocity.com/docs/reference/notifications/)
- [OpenAPI](openapi/cumulocity-notification2-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-notification2-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-notification2-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/cumulocity-notification2-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Cumulocity MQTT and SmartREST API

Constrained-device MQTT broker fronting the Cumulocity REST API with a CSV-based SmartREST 2.0 payload format that saves up to 80% of mobile traffic versus JSON. Supports static templates for common operations (s/us topic family) and tenant-defined custom templates. 16 KiB max payload, MQTT 3.1.1 and 5.0 supported, TLS on port 8883.

- **Human URL:** [https://cumulocity.com/docs/device-integration/mqtt/](https://cumulocity.com/docs/device-integration/mqtt/)
- **Base URL:** `mqtt://{tenant}.cumulocity.com:1883`

#### Tags

- IoT
- MQTT
- SmartREST
- Device Integration
- Telemetry

#### Properties

- [Documentation](https://cumulocity.com/docs/device-integration/mqtt/)
- [Documentation](https://cumulocity.com/docs/smartrest/smartrest-two/)
- [Documentation](https://cumulocity.com/docs/smartrest/mqtt-static-templates/)
- [AsyncAPI](asyncapi/cumulocity-mqtt-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/cumulocity-alarm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-alarm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-application-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-application-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-audit-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-audit-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-datahub-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-datahub-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-device-bootstrap-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-device-bootstrap-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-device-control-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-device-control-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-dtm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-dtm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-edge-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-edge-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-event-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-event-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-identity-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-identity-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-measurement-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-measurement-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-notification2-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-notification2-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-real-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-real-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-retention-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-retention-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-tenant-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-tenant-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-user-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-user-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity MQTT Service API

Standards-compliant, multi-tenant MQTT broker for application-level messaging that does not need Cumulocity's domain model. Topics are tenant-scoped, persistent, and bridgeable to the Cumulocity domain model via the Dynamic Mapper. Use it as a general-purpose MQTT broker inside your Cumulocity tenant.

- **Human URL:** [https://cumulocity.com/docs/device-integration/mqtt-service/](https://cumulocity.com/docs/device-integration/mqtt-service/)
- **Base URL:** `mqtts://mqtt.{tenant}.cumulocity.com:8883`

#### Tags

- IoT
- MQTT
- Streaming
- Application Integration

#### Properties

- [Documentation](https://cumulocity.com/docs/device-integration/mqtt-service/)
- [AsyncAPI](asyncapi/cumulocity-mqtt-service-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/cumulocity-alarm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-alarm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-application-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-application-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-audit-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-audit-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-datahub-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-datahub-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-device-bootstrap-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-device-bootstrap-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-device-control-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-device-control-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-dtm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-dtm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-edge-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-edge-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-event-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-event-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-identity-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-identity-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-inventory-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-inventory-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-measurement-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-measurement-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-notification2-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-notification2-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-real-time-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-real-time-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-retention-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-retention-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-tenant-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-tenant-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/cumulocity-user-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-user-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity DataHub API

Offload operational IoT data (measurements, events, alarms, inventory) from the Cumulocity MongoDB operational store into a Parquet-backed data lake queryable with ANSI SQL via Dremio. Configure offload pipelines, run analytics queries, and export results to BI tools (Power BI, Tableau) over JDBC/ODBC/Arrow Flight.

- **Human URL:** [https://cumulocity.com/api/datahub/](https://cumulocity.com/api/datahub/)
- **Base URL:** `https://{tenant}.cumulocity.com/service/datahub`

#### Tags

- IoT
- Data Lake
- Analytics
- SQL
- Apache Arrow
- Dremio

#### Properties

- [Documentation](https://cumulocity.com/api/datahub/)
- [Documentation](https://cumulocity.com/docs/datahub/datahub-overview/)
- [OpenAPI](openapi/cumulocity-datahub-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-datahub-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-datahub-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Digital Twin Manager API

Model real-world assets and their hierarchies with strongly-typed asset models, custom properties, and computed smart-function values. Asset instances reference the underlying Cumulocity managed objects so measurements and alarms automatically roll up. Supports inheritance, asset-property widgets, and bulk import via CSV.

- **Human URL:** [https://cumulocity.com/api/dtm/](https://cumulocity.com/api/dtm/)
- **Base URL:** `https://{tenant}.cumulocity.com/service/dtm`

#### Tags

- IoT
- Digital Twin
- Asset Modeling
- Hierarchies

#### Properties

- [Documentation](https://cumulocity.com/api/dtm/)
- [Documentation](https://cumulocity.com/docs/digital-twin-manager/dtm-overview/)
- [OpenAPI](openapi/cumulocity-dtm-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-dtm-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-dtm-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Cumulocity Edge API

Single-node on-premises deployment of Cumulocity that runs the full platform locally (inventory, events, measurements, alarms, streaming analytics, UI) and optionally syncs selected data to a cloud tenant. Targets factory floors, vessels, and regulated/air-gapped environments. Released on a 10.x version cadence.

- **Human URL:** [https://cumulocity.com/api/edge/](https://cumulocity.com/api/edge/)
- **Base URL:** `https://edge.local`

#### Tags

- IoT
- Edge Computing
- On-Premises
- Air-Gapped

#### Properties

- [Documentation](https://cumulocity.com/api/edge/)
- [Documentation](https://cumulocity.com/docs/edge/edge-overview/)
- [OpenAPI](openapi/cumulocity-edge-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/cumulocity-edge-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/cumulocity-edge-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.cumulocity.com)
- [Documentation](https://www.cumulocity.com/docs/)
- [Documentation](https://cumulocity.com/api/)
- [Documentation](https://cumulocity.com/api/core/)
- [Documentation](https://cumulocity.com/api/datahub/)
- [Documentation](https://cumulocity.com/api/dtm/)
- [Documentation](https://cumulocity.com/api/edge/)
- [Getting Started](https://cumulocity.com/docs/welcome/quickstart/)
- [Documentation](https://cumulocity.com/docs/concepts/introduction/)
- [Documentation](https://cumulocity.com/docs/concepts/domain-model/)
- [Authentication](https://cumulocity.com/docs/authentication/)
- [Documentation](https://cumulocity.com/docs/reference/general-aspects/)
- [Documentation](https://cumulocity.com/docs/reference/rest-conventions/)
- [Documentation](https://cumulocity.com/docs/reference/notifications/)
- [Documentation](https://cumulocity.com/docs/device-integration/mqtt/)
- [Documentation](https://cumulocity.com/docs/smartrest/smartrest-two/)
- [Documentation](https://cumulocity.com/docs/microservice-sdk/)
- [Documentation](https://cumulocity.com/docs/web-sdk/)
- [Documentation](https://cumulocity.com/docs/web-sdk/web-sdk-overview/)
- [Documentation](https://cumulocity.com/docs/streaming-analytics/)
- [Documentation](https://cumulocity.com/docs/datahub/datahub-overview/)
- [Documentation](https://cumulocity.com/docs/digital-twin-manager/dtm-overview/)
- [Documentation](https://cumulocity.com/docs/edge/edge-overview/)
- [Changelog](https://cumulocity.com/docs/release-notes/)
- [Status Page](https://status.cumulocity.com)
- [Forum](https://community.cumulocity.com)
- [Support](https://cumulocity.com/contact-support/)
- [Terms of Service](https://cumulocity.com/legal/terms/)
- [Privacy Policy](https://cumulocity.com/legal/privacy/)
- [Documentation](https://cumulocity.com/legal/dpa/)
- [Trust Center](https://cumulocity.com/trust-center/)
- [Security](https://cumulocity.com/security/)
- [Pricing](https://cumulocity.com/pricing/)
- [Sign Up](https://cumulocity.com/free-trial/)
- [Blog](https://cumulocity.com/blog/)
- [Press](https://cumulocity.com/press-releases/)
- [Case Studies](https://cumulocity.com/case-studies/)
- [Events](https://cumulocity.com/events/)
- [Video](https://www.youtube.com/@CumulocityIoT)
- [LinkedIn](https://www.linkedin.com/company/cumulocity/)
- [GitHub Organization](https://github.com/Cumulocity-IoT)
- [GitHub Organization](https://github.com/SoftwareAG)
- [SDK](https://github.com/Cumulocity-IoT/cumulocity-clients-java)
- [SDK](https://github.com/Cumulocity-IoT/cumulocity-python-api)
- [SDK](https://github.com/Cumulocity-IoT/cumulocity-sdk-dotnet)
- [SDK](https://www.npmjs.com/package/@c8y/client)
- [SDK](https://github.com/Cumulocity-IoT/cumulocity-ui-toolkit)
- [C L I](https://github.com/reubenmiller/go-c8y-cli)
- [SDK](https://github.com/reubenmiller/go-c8y)
- [Tool](https://github.com/Cumulocity-IoT/cumulocity-microservice-archetype)
- [Code Examples](https://github.com/Cumulocity-IoT/cumulocity-examples)
- [Tool](https://github.com/Cumulocity-IoT/cumulocity-dynamic-mapper)
- [Integration](https://github.com/Cumulocity-IoT/cumulocity-lora)
- [Integration](https://github.com/Cumulocity-IoT/cumulocity-node-red)
- [Code Examples](https://github.com/Cumulocity-IoT/cumulocity-devicemanagement-agent)
- [Tool](https://github.com/Cumulocity-IoT/cumulocity-mcp-server)
- [Tool](https://github.com/Cumulocity-IoT/c8y-ai-sandbox)
- [Tool](https://github.com/Cumulocity-IoT/cumulocity-cypress)
- [Tool](https://github.com/Cumulocity-IoT/cumulocity-subtenant-management)
- [SDK](https://github.com/Cumulocity-IoT/apama-analytics-builder-block-sdk)
- [Tool](https://github.com/Cumulocity-IoT/apama-eplapps-tools)
- [Code Examples](https://github.com/Cumulocity-IoT/streaming-analytics-sample-repo-template)
- [Tool](https://github.com/Cumulocity-IoT/cumulocity-remote-access-cloud-http-proxy)
- [Documentation](https://github.com/Cumulocity-IoT/cumulocity-os-repo-overview)
- [Integration](https://thin-edge.io/)
- [Plans](plans/cumulocity-plans-pricing.yml)
- [Rate Limits](rate-limits/cumulocity-rate-limits.yml)
- [Fin Ops](finops/cumulocity-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
