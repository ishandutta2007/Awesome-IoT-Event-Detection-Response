# Awesome-IoT-Event-Detection-Response

## Top IoT Event Detection & Response Ecosystem



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

| Platform | Company Size / Valuation | Starting Price | Free Tier / Free Trial Limits | Key Features & Best For |
| :--- | :--- | :--- | :--- | :--- |
| **[Azure Stream Analytics](https://azure.microsoft.com/en-us/products/stream-analytics/)** | **$3.92 Trillion** Market Cap<br>*(Microsoft, $331.8B Annual Rev)* | **$0.11 / SU-hour**<br>*(Streaming Unit V2 model)* | **$200 free credit for 30 days**<br>*(Azure Free Account)* | Real-time SQL queries on telemetry stream with automated event triggers. **Best for Azure-native event processing**. |
| **[AWS IoT Events](https://aws.amazon.com/iot-events/)** | **$2.18 Trillion** Market Cap<br>*(Amazon, $128.7B AWS Annual Rev)* | **$0.15 / 1,000 message evaluations**<br>*(+ $0.10 / 100k state changes)* | **2,500 message evaluations / month for 12 months**<br>*(China regions / $300 AWS trial credit)* | Managed complex event processing using conditional "if-then-else" rules across telemetry sources. **Best for AWS-native IoT event detection**. |
| **[Datadog IoT](https://www.datadoghq.com/)** | **$97.2 Billion** Market Cap<br>*($3.43B Annual Rev)* | **$15 / host / month**<br>*(Pro plan, annual billing)* | **14-day free trial**<br>*(Unlimited metrics & platform features)* | Unified infrastructure metrics, log monitoring, and telemetry anomaly alerts for device fleets. **Best for unified IoT & cloud observability**. |
| **[PTC ThingWorx](https://www.ptc.com/)** | **$22.6 Billion** Valuation<br>*(Acquired by Schneider Electric, $2.2B Rev)* | **~$2,000 / month**<br>*($24,000/yr starting enterprise base)* | **30-day developer sandbox trial**<br>*(PTC Developer Portal access)* | Industrial IoT platform with drag-and-drop event processing, AR integration, and asset tracking. **Best for industrial IoT applications**. |
| **[Losant Enterprise IoT](https://www.losant.com/)** | **$2.5 Billion** Parent Valuation<br>*(Acquired by SUSE, $25.2M total funding)* | **$150 / month**<br>*(Starter plan for 500k payload evaluations)* | **Free Developer Sandbox**<br>*(Up to 10 devices & 30-day data retention, no expiration)* | Visual workflow builder, edge compute engine, and device state monitoring. **Best for enterprise IoT event workflows**. |
| **[Cumulocity Streaming Analytics](https://cumulocity.com/docs/2026/streaming-analytics/introduction-analytics/)** | **~$500M - $1 Billion** Valuation<br>*(Backed by Avedon/Schroders; Software AG €2.6B buyout)* | **€299 / month**<br>*(Cloud Tenant starter tier up to 100 devices)* | **30-day free trial**<br>*(Full Analytics Builder CEP & EPL app access)* | Enterprise IoT platform powered by Apama complex event processing engine for drag-and-drop analytics. **Best for enterprise IoT with real-time analytics**. |
| **[Waylay](https://www.waylay.io/platform)** | **$17.9 Million** Valuation<br>*(Acquired by Vertiv, ~$9M Annual Rev)* | **€5 / month**<br>*(Waylay IO Developer Plan)* | **14-day free trial**<br>*(1,000 rule executions & visual flow builder access)* | Low-code hyper-automation unifying time-series telemetry, event streams, and AI automation flows. **Best for workflow-based IoT automation**. |
| **[ClearBlade](https://clearblade.com/)** | **~$15M - $25 Million** Est. Valuation<br>*($6.8M Annual Recurring Rev)* | **$0.0005 / MB**<br>*(Or $50/mo starter cloud package)* | **Free Developer Account**<br>*(5 edge nodes, 100 devices & 10,000 msg/mo)* | Event types with severity/priority levels; triggers actions on MQTT/HTTP lifecycle events. **Best for enterprise IoT event management**. |





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
