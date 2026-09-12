# Kilo Gateway

> Free API gateway routing to hosted open-source models with an OpenAI-compatible endpoint.

---

### Quick Specs
* **Website / Signup**: https://kilo.ai
* **Base URL**: `https://api.kilo.ai/api/gateway`
* **Auth Requirement**: Free account with `KILOCODE_API_KEY` (or direct raw gateway access)
* **Tested In**: Hermes Agent, OpenCode
* **Tool Calling Support**: Supported on named models (e.g. `stepfun/step-3.7-flash:free`)
* **Last Verified**: 2026-09-13

---

### Tested Models & Real Limits

| Model Name | Exact Model ID | Rate Limits | Best Used For |
| :--- | :--- | :--- | :--- |
| **Step 3.7 Flash** | `stepfun/step-3.7-flash:free` | 200 req/hour | Fast instruction following and code generation |
| **Minimax M3** | `minimax/minimax-m3` | 200 req/hour | Code evaluation and multi-turn refactoring |
| **Ling** | `ling` | 200 req/hour | Fast conversational turns |
| **Kilo Auto Free** | `kilo-auto/free` | 200 req/hour | Automatic fallback routing to active free models |

---

### Real Experience & Honest Comment
"Kilo Gateway is a solid starting recommendation if you have $0 and want your agent to work right away. The 200 requests/hour limit is plenty for daily learning. In August 2026, community members reported a security incident and login issues on KiloCode, but the gateway itself is functional. Note that HY3 is no longer reliable on Kilo, so use Step 3.7 Flash or Minimax M3 instead."

---

### How to Configure in Your Agent

#### 1. Hermes Agent (`config.yaml`)
```yaml
providers:
  kilocode:
    base_url: "https://api.kilo.ai/api/gateway"
    api_key: "YOUR_KILOCODE_API_KEY"
    models:
      - "stepfun/step-3.7-flash:free"
      - "minimax/minimax-m3"
```

#### 2. OpenCode / Terminal Agents
```bash
export OPENAI_BASE_URL="https://api.kilo.ai/api/gateway"
export OPENAI_API_KEY="YOUR_KILOCODE_API_KEY"
export OPENAI_MODEL="stepfun/step-3.7-flash:free"
```

---

### Standard Verification Test (Proof)
```bash
curl -X POST https://api.kilo.ai/api/gateway/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_KILOCODE_API_KEY" \
  -d '{
    "model": "stepfun/step-3.7-flash:free",
    "messages": [{"role": "user", "content": "Return the word OK."}],
    "max_tokens": 10
  }'
```
* **Test Result**: Returned `OK` with HTTP 200 in `< 2.1s`.

---

### Notes & Honest Gotchas
* **Privacy Warning**: Free gateway endpoints log prompts for model evaluation. Never send passwords or client data.
* **Token Caps**: Reasoning models can eat low token caps. Set `max_tokens` above 500 when doing tool calling.
