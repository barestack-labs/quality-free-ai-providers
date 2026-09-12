# Contributing to Quality Free AI Providers

We only accept providers that **actually work inside AI agents** like Hermes Agent and OpenCode. Marketing promos, dead 24-hour trials, and unstable endpoints will be closed immediately.

---

### The Human Touch Rule
You can ask an AI agent to help write your Pull Request, but do not just dump unedited text. 
* Check whatever the AI writes before submitting.
* Add your own real 2-3 sentence personal experience comment in the markdown file.
* Tell us how the provider actually performed in your daily agent work, what broke, and what worked. Keep it honest.

---

### The Submission Guidelines

1. **Must Be an API Endpoint**: No web chat UIs. It must provide an OpenAI-compatible `/v1/chat/completions` endpoint.
2. **Quality & Stability**: Must be stable for at least 1 week, unless it is a genuinely exceptional and reliable model that the community should know about.
3. **Usable for Hermes or Subagents**: The model should be capable enough to run tasks in Hermes Agent, or at least serve as a reliable subagent worker (where a smarter model plans and the free model executes the smaller files).
4. **Reliable Latency**: Should respond in a reasonable time. Occasional hiccups are expected on free tiers, but it should not constantly hang or time out.
5. **Use the Template**: Copy [providers/template.md](providers/template.md) and place your file in `providers/<provider-name>.md`. Include the exact Base URL and Model ID.

---

### Verification (Honesty-Based for Now)
We do not have an automated CI testing bot yet, so submissions currently rely on honesty and manual testing.

In your PR description:
* Paste a sample curl response or test output if you have one.
* Note the general speed and whether you tested it on Hermes Agent, OpenCode, or another harness.
* State your honest thoughts on stability.

---

### Review Process
All submissions are reviewed in the Bare Stack Discord (`#github-prs`).
