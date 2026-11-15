# LLM Safety & Moderation Classifiers

Archival collection of API safety categories, open-weight guardrail taxonomies, and community-captured policy classifier artifacts across major LLM providers.

## Naming Convention
* `official_*.md` — Verbatim schemas, enums, and taxonomies published in official provider documentation or technical papers.
* `<artifact_name>.md` (no prefix) — Unofficial, leaked, or network-inspected safety/moderation artifacts captured from client telemetry or model disclosures.

## Repository Structure

    ├── anthropic/
    │   └── constitutional-classifiers/
    │       └── official_safety_taxonomy.md
    ├── google/
    │   ├── gemini/
    │   │   ├── api-safety-settings/
    │   │   │   ├── official_harm_categories.md
    │   │   │   └── internal_block_reasons.md
    │   │   └── gemini-pro/
    │   │       └── reddit_leak_eval_flags.md
    │   └── gemma/
    │       └── shieldgemma/
    │           └── official_harm_categories.md
    ├── meta/
    │   └── llama-guard-3/
    │       └── official_mlcommons_hazard_taxonomy.md
    ├── openai/
    │   └── moderation-api/
    │       ├── official_categories.md
    │       └── chatgpt_web_moderations.md
    └── xai/
        └── grok/
            └── system_guardrails.md
