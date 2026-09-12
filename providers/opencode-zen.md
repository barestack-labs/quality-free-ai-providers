# OpenCode Zen

> Free API inference subsidizing open models for agentic coding and terminal harnesses.

---

### Quick Specs
* **Website / Signup**: https://opencode.ai/auth
* **Base URL**: `https://opencode.ai/zen/v1`
* **Auth Requirement**: Free account via GitHub/Google OAuth (No credit card)
* **Tested In**: Hermes Agent, OpenCode Desktop & CLI, Pi Agent
* **Tool Calling Support**: Supported
* **Last Verified**: 2026-09-13

---

### Tested Models & Real Limits

| Model Name | Exact Model ID | Rate Limits | Best Used For |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.3** | `muse-spark-1.3-contributor-free` | Okay free quota | Vision, simple edits, and general scripting |
| **MiMo 2.5 Free** | `mimo-v2.5-free` | Okay free quota | Fast conversational turns |
| **MiniMax M2.5** | `minimax-m2.5-free` | Okay free quota | Code evaluation and syntax checking |

---

### Real Experience & Honest Comment
"Muse Spark 1.3 is lazy for complex tasks and I do not recommend it for heavy engineering, but it is an okay free option if you just need light edits or vision input. The main gotcha with Zen preview keys is that they expire after roughly 7 days. When your agent throws an unauthorized error, grab a fresh key from your OpenCode dashboard."

---

### How to Configure in Your Agent

#### 1. Hermes Agent (`config.yaml`)
```yaml
providers:
  custom:opencode-zen:
    base_url: "https://opencode.ai/zen/v1"
    api_key: "YOUR_OPENCODE_ZEN_KEY"
    models:
      - "muse-spark-1.3-contributor-free"
      - "mimo-v2.5-free"
```

#### 2. OpenCode CLI
```bash
export OPENAI_BASE_URL="https://opencode.ai/zen/v1"
export OPENAI_API_KEY="YOUR_OPENCODE_ZEN_KEY"
export OPENAI_MODEL="muse-spark-1.3-contributor-free"
```

---

### Notes & Honest Gotchas
* **7-Day Token Expiration**: Free preview keys expire on a rolling 7-day cycle. Refresh your key from `opencode.ai/auth` when requests fail.
