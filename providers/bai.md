# b.ai

> Direct API access offering free models for agent experiments. Gained recent traction on X.com.

---

### Quick Specs
* **Website**: https://b.ai
* **Base URL**: OpenAI and Anthropic compatible endpoints
* **Auth Requirement**: No credit card / No account needed
* **Tested In**: Hermes Agent, 9Router
* **Tool Calling Support**: Supported
* **Last Verified**: 2026-09-13

---

### Tested Models & Real Limits

| Model Name | Exact Model ID | Rate Limits | Best Used For |
| :--- | :--- | :--- | :--- |
| **Tencent HY3** | `tencent/hy3` | Not really sure, but generous | General agent tasks and tool calling |
| **Qwen 3.8 Flash** | `qwen-3.8-flash` | Not really sure, but generous | Fast coding and instruction following |
| **MiMo 2.5** | `mimo-v2.5` | Not really sure, but generous | General text generation |
| **GLM 5.3 Flash** | `glm-5.3-flash` | Not really sure, but generous | Fast review and evaluation |

---

### Real Experience & Honest Comment
"b.ai gained quick traction on X.com because you can get an API key with no credit card and no complex setup. The daily quota is generous. In testing, GLM 5.3 Flash and MiMo 2.5 can be slow, but Tencent HY3 is the standout here and works well. DeepSeek V4 Flash was available earlier, but expired in early September. Always check their website for active models."

---

### Notes & Honest Gotchas
* **Context Window**: Unspecified on their public documentation. Avoid feeding massive multi-file repos in a single prompt.
* **Privacy Warning**: Free public endpoints log data. Never pass confidential files, client code, or private keys through this endpoint.
