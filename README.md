# Quality Free AI Providers

> A tested directory of free AI API endpoints built for anyone running agent harnesses like **Hermes Agent**, **OpenCode**, and local coding agents.

---

### ⚠️ Read First: This is for Agents, Not Chatbots
ChatGPT, Claude, and Gemini have free web chat interfaces, but you cannot plug a browser tab into a terminal coding harness.

Every provider listed here gives you a real, working **API endpoint (`/v1/chat/completions`)** that you can plug directly into:
* **Hermes Agent**
* **OpenCode**
* **Cursor / Cline / Roo Code**
* Any OpenAI-compatible agent harness

We list providers that survive real agent workflows: proper tool calling, reliable instruction adherence, and dependable response times.

*(Note: Free Image APIs are deliberately excluded here, they will live in their own dedicated repository).*

---

### 🏆 Verified Providers & Routers

| Provider | Top Models | Real Limits | Auth Requirement | Setup Guide |
| :--- | :--- | :--- | :--- | :--- |
| **Kilo Gateway** | Step 3.7 Flash, Minimax M3, Ling | 200 req/hour | Free account (No card) | [View Guide](providers/kilo-gateway.md) |
| **OpenCode Zen** | Muse Spark 1.3, MiMo 2.5 Free | Okay free quota | Free account (No card) | [View Guide](providers/opencode-zen.md) |
| **Nous Portal** | Solar Pro, LongCat 2.0, Ling 3.0 Flash | High uptime | Card Verification ($0) | [View Guide](providers/nous-portal.md) |
| **b.ai** | Tencent HY3, Qwen 3.8 Flash, MiMo 2.5 | Not really sure, but generous | No card / No account needed | [View Guide](providers/bai.md) |
| **9Router** | Local multi-provider router | Hardware dependent | Local API key | [View Guide](providers/9router.md) |
| **OmniRoute** | Heavier self-hosted fork | Hardware dependent | Local API key | [View Guide](providers/omniroute.md) |

---

### 🚫 Providers Not Recommended (And Why)
We actively test and exclude providers that look good on paper but fail inside real agent loops.

See [providers/excluded-providers.md](providers/excluded-providers.md) for full notes on why we skip:
* **NVIDIA NIM**: Slow response times, agent timeouts, heavy telemetry.
* **Cerebras**: Context window is too small for codebases, and daily caps burn out quickly.
* **OpenRouter `:free`**: Needs $10 to get reliable limits, while the completely free tier drops context and hits rate limits constantly.

---

### How to Contribute
If you have an API provider that has been working reliably for at least 1 week (or a standout reliable model), please contribute:
1. Copy [providers/template.md](providers/template.md) and create `providers/<provider-name>.md`.
2. Follow the rules in [CONTRIBUTING.md](CONTRIBUTING.md) (include your honest testing notes).
3. Open a Pull Request.

---

### Community & Tutorials
* **Discord Community**: [dsc.gg/barestack](https://dsc.gg/barestack)
* **YouTube Tutorials**: [youtube.com/@paulablaza](https://youtube.com/@paulablaza)
