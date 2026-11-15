# LLM Safety & Moderation Classifiers

Archival collection of documented API safety categories, open-weight guardrail taxonomies, and internal policy classifier schemas across major LLM providers.

## Repository Structure

    ├── anthropic/
    │   └── constitutional-classifiers/
    │       └── safety_taxonomy.md
    ├── google/
    │   ├── gemini/
    │   │   ├── 3.8-flash/
    │   │   │   └── safety_eval_flags.md
    │   │   └── api-safety-settings/
    │   │       └── harm_categories.md
    │   └── gemma/
    │       └── shieldgemma/
    │           └── harm_categories.md
    ├── meta/
    │   └── llama-guard-3/
    │       └── mlcommons_hazard_taxonomy.md
    └── openai/
        └── moderation-api/
            └── categories.md

## Taxonomy Overview

| Provider | Model / Endpoint | Output Format | Adjustable Thresholds |
| :--- | :--- | :--- | :--- |
| **Google** | Gemini API (`SafetySetting`) | Discrete Probability & Severity (`NEGLIGIBLE`–`HIGH`) | Yes (4 levels + `OFF`) |
| **Google** | ShieldGemma (2B / 9B / 27B) | Binary token (`Yes` / `No`) per policy | Prompt-defined policies |
| **OpenAI** | Moderation API (`omni-moderation-latest`) | Boolean flags + float scores (`0.0`–`1.0`) | Consumer-side thresholding |
| **Meta** | Llama Guard 3 (8B / 11B-Vision) | `safe` or `unsafe\nS1,S2...` | Subsettable hazard codes |
| **Anthropic** | Constitutional Classifiers | Input/Output jailbreak & harm classifiers | Provider-managed |
