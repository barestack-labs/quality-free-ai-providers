# Provider Name

> A quick 1-sentence summary of what this provider offers and why it works for agents.

---

### Quick Specs
* **Website / Signup**: https://example.com
* **Base URL**: `https://api.example.com/v1` *(Include the full path ending in /v1)*
* **Auth Requirement**: Free account / No card required (or $0 Card Verification)
* **Tested In**: Hermes Agent, OpenCode, Cursor, etc.
* **Tool Calling Support**: Supported / Flaky / Not Supported
* **Last Verified**: YYYY-MM-DD

---

### Tested Models & Real Limits

| Model Name | Exact Model ID (API String) | Real Limits (RPM / RPD) | Best Used For |
| :--- | :--- | :--- | :--- |
| Model 1 | `provider/model-1` | 20 RPM / 200 RPD | Coding and edits |
| Model 2 | `provider/model-2` | 30 RPM / 1,000 RPD | Fast chat and planning |

---

### Real Experience & Honest Comment
> *Required: Write 2-3 sentences of your actual experience using this provider. Do not just let an AI generate generic praise. Tell us what tasks it handled well, where it failed, and how stable it felt in daily use.*

Example:
"I used this for 5 days inside Hermes Agent to write small Python scripts. It never hit rate limits during normal turns, but it struggled when I asked it to edit multiple files in one turn. Good for simple tasks, bad for large refactors."

---

### How to Configure in Your Agent

#### 1. Hermes Agent (`config.yaml`)
```yaml
providers:
  custom_provider:
    base_url: "https://api.example.com/v1"
    api_key: "YOUR_API_KEY"
    models:
      - "provider/model-1"
```

#### 2. OpenCode / Terminal Agents
```bash
export OPENAI_BASE_URL="https://api.example.com/v1"
export OPENAI_API_KEY="YOUR_API_KEY"
export OPENAI_MODEL="provider/model-1"
```

---

### Standard Verification Test (Proof)
```bash
curl -X POST https://api.example.com/v1/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{
    "model": "provider/model-1",
    "messages": [{"role": "user", "content": "Return the word OK."}],
    "max_tokens": 10
  }'
```
* **Test Result**: Returned `OK` with HTTP 200 in `< 3s`.

---

### Notes & Honest Gotchas
* Mention any real quirks (rate limits, prompt logging, or token caps).
