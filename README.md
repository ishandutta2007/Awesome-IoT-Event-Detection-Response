# Awesome-IoT-Event-Detection-Response

# Top IoT Event Detection & Response Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Complex Event Processing, Automated Response & Self-Hosted IoT Analytics*  
**Last updated: October 2026**

This repository tracks notable **commercial IoT event detection platforms** and **open-source projects** that monitor device telemetry, detect meaningful events (failures, anomalies, threshold breaches), and trigger automated responses — from fully managed cloud services to self-hosted complex event processing engines.

**Examples** include AWS IoT Events, Losant Enterprise IoT, PTC ThingWorx, Software AG Cumulocity, ThingsBoard, Waylay, Datadog IoT, Azure Stream Analytics, ClearBlade, and Falco (the category leaders).

**Open-source emphasis**: IoT event detection is anchored by **ThingsBoard** as the most popular open-source IoT platform with a comprehensive rule engine, **Magistrala** for cloud-native IoT messaging with fine-grained access control and a rules engine, **Rule Engine Core** for declarative complex event processing with deterministic replay, and **StreamSQL** for SQL-based event processing on edge gateways. **Falco** provides runtime security event detection for IoT and edge computing environments. **Node-RED** and **Apache Flink** handle event-driven automation and stream processing. This section is heavily expanded.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[AWS IoT Events](https://aws.amazon.com/iot-events/)**  
  **AWS's fully managed complex event detection service** — easily detect and respond to events from IoT sensors and applications . **Uses simple "if-then-else" statements to define event logic** across multiple telemetry sources . **Triggers alerts and actions** such as notifying support teams or shutting down faulty equipment . **Pricing**: pay per message evaluation (1KB increments) with 2 triggered actions included per evaluation; additional actions count as extra evaluations . **Free tier**: 2,500 message evaluations/month for 12 months (China regions only) . **Alarm pricing**: ¥0.653 per active alarm per month (China regions) . **Best for AWS-native IoT event detection** .

- **[Software AG Cumulocity Streaming Analytics](https://cumulocity.com/docs/2026/streaming-analytics/introduction-analytics/)**  
  **Enterprise IoT platform with built-in Apama complex event processing engine** — immediate processing of incoming data from devices or data sources . **Typical use cases**: remote control (turn off device if temperature exceeds 40°C), validation (discard invalid readings), derived data (calculate sales volume), aggregation, notifications, and compression . **Analytics Builder** for drag-and-drop model creation and **EPL Apps** for custom Event Processing Language code . **Runs automatically within the platform** with no manual setup required . **Available in Core (cloud) and Edge (local installation)** modes . **Best for enterprise IoT with real-time analytics** .

- **[Waylay](https://www.waylay.io/platform)**  
  **Low-code hyper-automation platform for IoT event detection and response** — unifies process automation, decision management, and API orchestration . **Integrates time series data, event streams, and AI models** in a low-code environment . **Enables accelerated service roll-out up to 20x faster** — subject matter experts translate domain knowledge into automation flows without bespoke software development . **AI models wired into automated flows** for intelligent, near real-time insights and closed-loop automation . **Scales to millions of workflow executions per day** . **Deployment**: SaaS (AWS region of choice) or on-premises (Kubernetes) . **Best for workflow-based IoT automation** .

- **[Losant Enterprise IoT](https://www.losant.com/)**  
  **Enterprise IoT application platform** — visual workflow builder, edge compute, and device management . **Best for enterprise IoT event-driven workflows** .

- **[PTC ThingWorx](https://www.ptc.com/)**  
  **Industrial IoT platform** — IoT solutions, AR, and data analytics with event-driven processing . **Enterprise licensing varies**  . **Best for industrial IoT applications** .

- **[Datadog IoT](https://www.datadoghq.com/)**  
  **Observability platform with IoT monitoring** — infrastructure metrics, logs, and alerts for device fleets . **Best for unified observability across IoT and cloud** .

- **[Azure Stream Analytics](https://azure.microsoft.com/en-us/products/stream-analytics/)**  
  **Microsoft's real-time analytics service** — SQL-like queries on streaming data with event detection . **Best for Azure-native event processing** .

- **[ClearBlade](https://clearblade.com/)**  
  **Enterprise IoT platform with event types and rules** — define event types with severity, priority, and lifecycle states; create rules that trigger actions (email, SMS) when conditions are satisfied . **Device event logs capture MQTT/HTTP lifecycle events** including connects, publishes, subscribes, and disconnects . **Best for enterprise IoT event management** .

## Open-Source GitHub Projects

### IoT Platforms with Rule Engines

- **[ThingsBoard](https://github.com/thingsboard/thingsboard)**  
  **The most popular open-source IoT platform with 17,000+ GitHub stars**, Apache-2.0 licensed . **Rule Engine for event-based workflows** — trigger actions on device data, alarms, and schedules . **Device management, data collection, processing, and visualization** . **Multi-tenancy with RBAC** — manage multiple organizations from one instance . **Supports MQTT, CoAP, HTTP, LwM2M, SNMP** with dashboards and device management . **Security**: Two-Factor Authentication, OAuth 2.0, Access Tokens, X.509 Certificates, SSL, DTLS . **Trade-offs**: Can be resource-heavy; Community edition lacks many Professional features . **Best for comprehensive IoT platform with rule engine** .

- **[Magistrala](https://github.com/absmach/magistrala)**  
  **Modern, Go-based, cloud-native IoT platform framework** (formerly Mainflux), Apache-2.0 licensed . **Includes a dedicated Rule Engine service** for event-driven processing . **Small number of main concepts**: users, devices, channels, messages, policies — familiar to most engineers . **Atom integration model** provides identity, authorization, and catalog with workspaces (tenants), entities, resources, and groups . **Fine-grained access control** — define object-scoped roles like "reader on channel1" . **Scales from simple prototypes to complex deployments** without rigid patterns . **Trade-offs**: No built-in dashboard (available via plugins); community support still catching up to Java-based platforms . **Best for high-performance, cloud-native IoT event processing** .

### Complex Event Processing (CEP) Engines

- **[Rule Engine Core](https://zenodo.org/records/22015264)**  
  **Compact, embeddable complex event processing (CEP) runtime written in Python**, open-source . **Detection logic expressed declaratively in YAML**, validated against formal schema, compiled into executable runtime objects . **Five trigger families**: event (matching event satisfies condition), window (aggregate over time window), absence (no matching event before timeout), composite (per-source absence timers), and scheduled (cron expression) . **Window rules support count, sum, mean, minimum, maximum, standard deviation, delta, rate, and percentile aggregations** . **Deterministic replay** — timer-driven rules advance on explicit watermark rather than wall-clock, enabling reproducible and testable behavior . **At-least-once delivery** with idempotency keys, bounded retries, and dead-letter recording . **Five sink adapters**: stdout, file, webhook (with HMAC signing), queue, and object storage . **Event-time order enforced** with configurable allowed lateness tolerance . **Engine state capture and restore** — versioned JSON snapshots for resumed runs . **Alert lifecycle** with cooldown, reminder intervals, and resolution emission . **Pattern matching** for ordered temporal sequences with negating event cancellation . **Explain facility** reports what each rule would do without altering engine state . **Simulation facility** backtests streams against rule sets . **Best for deterministic, embeddable CEP** .

- **[StreamSQL](https://github.com/rulego/streamsql)**  
  **SQL-based stream processing engine for IoT edge gateways**, open-source . **Sliding, counting, session, and global windows** with built-in aggregates (MAX, MIN, AVG, SUM, COUNT, STDDEV, MEDIAN, PERCENTILE) . **Event-time and processing-time semantics** with watermarks for out-of-order and late data . **Configurable tolerance**: MAXOUTOFORDERNESS, ALLOWEDLATENESS, IDLETIMEOUT . **Custom functions registrable at runtime** — eight function types (math, string, conversion, datetime, aggregate, analytic, window, custom) . **Performance**: ~1.92M msg/s for filter, ~740K msg/s for transform, ~480K msg/s for analytic with partition on x86 single-core . **128MB holds 100k+ devices of partition state** — memory is not the bottleneck, CPU throughput is . **Runs as RuleGo rule-chain nodes** . **Best for edge gateway event processing with SQL** .

### Runtime Security Event Detection

- **[Falco](https://github.com/falcosecurity/falco)**  
  **Runtime security event detection for Linux, Kubernetes, and IoT & Edge computing**, Apache-2.0 licensed . **Detects any behavior including Linux system calls and triggers alerts** based on specific system calls, arguments, and process properties . **Operates in both user space and kernel space** — system calls interpreted by Falco kernel module, parsed using user-space libraries . **Events filtered using rule engine configured with Falco rules** . **Suspicious events alerted to configured outputs** (Syslog, file, stdout) . **Deployable on Linux hosts, containers, managed Kubernetes clusters, or K3s clusters on IoT & Edge** . **Best for IoT security event detection** .

### Event-Driven Automation

- **[Node-RED](https://github.com/node-red/node-red)**  
  **Flow-based programming for event-driven IoT applications**, Apache-2.0 licensed with **20,000+ GitHub stars** . **Visual wiring of devices, APIs, and services** . **The standard for IoT automation and triggering** . **Best for visual IoT event-driven automation** .

- **[Apache Flink](https://github.com/apache/flink)**  
  **Stateful stream processing engine**, Apache-2.0 licensed with **24,000+ GitHub stars** . **Exactly-once semantics, event-time processing, and savepoints** . **Best for mission-critical stream processing** .

- **[Apache Kafka](https://github.com/apache/kafka)**  
  **Event streaming platform**, Apache-2.0 licensed with **28,000+ GitHub stars** . **Distributed pub/sub with persistence** . **Best for high-throughput event streaming** .

- **[NATS](https://github.com/nats-io/nats-server)**  
  **Cloud-native messaging system**, Apache-2.0 licensed . **Lightweight, high-performance pub/sub** with JetStream for persistence . **Best for lightweight IoT messaging** .

### Additional Strong Open-Source Options

- **Eclipse Mosquitto** — MQTT broker for IoT messaging .
- **EMQX** — Scalable MQTT broker with rule engine .
- **Telegraf** — Metrics collection agent with processing plugins .
- **Apache NiFi** — Data flow automation with event processing .
- **Benthos (Redpanda Connect)** — Stream processing without code .
- **Vector** — Observability data pipeline .
- **Huginn** — Agent-based automation for event monitoring .
- **Pipedream** — Event-driven workflow automation .

**Frameworks for building custom IoT event detection and response solutions**: Combine **ThingsBoard** for comprehensive IoT platform with rule engine and visualization . Use **Magistrala** for cloud-native IoT messaging with fine-grained access control and rules engine . Deploy **Rule Engine Core** for deterministic, embeddable complex event processing with YAML-declared rules . Choose **StreamSQL** for SQL-based event processing on edge gateways . Integrate **Falco** for runtime security event detection on IoT and edge devices . Use **Node-RED** for visual event-driven automation . Note that true managed IoT event detection with global infrastructure, automatic scaling, and vendor-supported SLAs (AWS IoT Events, Cumulocity, Waylay) remains primarily commercial territory; open-source stacks provide strong rule engines, complex event processing, and event-driven automation foundations that require integration for complete IoT event detection and response.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- IoT event detection platforms handle device telemetry and may trigger physical actions. Self-hosted solutions require proper security hardening, access controls, and compliance with data privacy regulations.
- **Event detection logic must be carefully designed** — false positives can trigger unnecessary actions; false negatives can miss critical failures . Test rules thoroughly before production deployment.
- **License considerations**: ThingsBoard uses Apache-2.0, Magistrala uses Apache-2.0, Rule Engine Core is open-source, StreamSQL is open-source, and Falco uses Apache-2.0 . Verify licensing against your use case before committing.
- The open-source ecosystem provides strong rule engines, complex event processing, and event-driven automation foundations, but **managed infrastructure, global scale, and vendor-supported SLAs** remain primarily commercial offerings.

---

**Made for IoT engineers, embedded developers, and organizations seeking IoT event detection sovereignty.**  
Let's make IoT event detection and response more open, transparent, and automated.
