# 9Router Gateway

> Lightweight self-hosted AI gateway that aggregates free provider keys, local models, and search lanes into a single endpoint.

---

### Quick Specs
* **Repository**: https://github.com/decolua/9router
* **Base URL**: `http://localhost:20128/v1` (or local IP behind Tailscale)
* **Auth Requirement**: Local API key (configured in your 9Router dashboard)
* **Tested In**: Hermes Agent, OpenCode, n8n
* **Tool Calling Support**: Fully supported
* **Last Verified**: 2026-09-13

---

### Why It Works Well for Agents
9Router is not an API provider, it is a self-hosted orchestrator. Instead of configuring separate API keys across 5 different agents, all your agents point to your local 9Router address:
* **Fallback routing**: Automatically switches to an alternative free model when one provider hits rate limits or throws errors.
* **Integrated search**: Exposes `/v1/search` so agents can search the web without needing paid search APIs.
* **Lightweight**: Consistently lighter on memory and faster to start than older proxy stacks.

---

### Real Experience & Honest Comment
"9Router is the most practical self-hosted gateway I have used. It keeps all provider keys in one place so you can swap models on the fly without touching your agent configs. Setup takes about 30 minutes if you know basic terminal commands."

---

### How to Configure in Hermes Agent (`config.yaml`)
```yaml
providers:
  9router:
    base_url: "http://127.0.0.1:20128/v1"
    api_key: "YOUR_LOCAL_9ROUTER_KEY"
    models:
      - "cmc/deepseek/deepseek-v4-flash"
      - "mimo/mimo-v2.5"
```

---

### Notes & Honest Gotchas
* **Not an API host**: You must plug your own free provider keys (Kilo, OpenCode Zen, etc.) into its dashboard.
* **Initial setup**: Requires running Node.js locally.
