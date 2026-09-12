# OmniRoute Gateway

> Self-hosted AI proxy and router fork designed for local agent setups.

---

### Quick Specs
* **Type**: Self-hosted local gateway
* **Base URL**: `http://localhost:20128/v1` (or local network IP)
* **Auth Requirement**: Local API key
* **Tested In**: Hermes Agent
* **Tool Calling Support**: Supported
* **Last Verified**: 2026-09-13

---

### What It Does
OmniRoute is a self-hosted routing proxy that lets you pipe multiple model providers behind a single OpenAI-compatible `/v1` endpoint. It translates requests between different model formats so your local agents only need to connect to one address.

---

### Real Experience & Honest Gotchas
* **Heavier resource usage**: OmniRoute tends to consume more memory and CPU compared to lighter alternatives like 9Router.
* **Build complexity**: Requires Node.js and local dependencies. If you are running on low-resource hardware, watch out for RAM constraints during compilation.
* **Maintenance overhead**: Past updates have occasionally had configuration breaking changes between versions. Test upgrades locally before relying on it for daily work.
