# Providers I Do Not Recommend (And Why)

I explicitly omit these popular providers from my main recommendations. While they advertise free tiers, live testing shows they fail in real-world agent workflows.

---

### 1. NVIDIA NIM
* **Why I Exclude It**:
  * It is simply slow. A lot of YouTubers recommend it, but members keep reaching out saying it hangs. You cannot use it on a day-to-day basis inside an agent loop without hitting timeouts.

---

### 2. Cerebras
* **Why I Exclude It**:
  * Daily limits exhaust fast. That is just it. The context window is too small for reading whole codebases, and the daily cap burns out after a few turns.

---

### 3. OpenRouter Free (`:free` models)
* **Why I Exclude It**:
  * You need to deposit $10 USD to unlock 1,000 requests per day. The completely free tier is heavily over-subscribed, drops context, and triggers 429 rate limit errors constantly during agent runs.
