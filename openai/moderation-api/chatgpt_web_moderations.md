# OpenAI — ChatGPT Web Frontend Moderation (`backend-api/moderations`)

Observed via browser network inspection of the consumer ChatGPT web interface (distinct from the public `/v1/moderations` developer endpoint).

## Request / Response Schema
* **Endpoint:** `POST https://chatgpt.com/backend-api/moderations`
* **Client Model Identifier:** `text-moderation-playground`
* **Enforcement Tiers:**
  * `flagged: true, blocked: false` — Displays an orange content warning banner while allowing the prompt/response to remain visible.
  * `flagged: true, blocked: true` — Hard-blocks generation and replaces the message with a red policy violation notice.
