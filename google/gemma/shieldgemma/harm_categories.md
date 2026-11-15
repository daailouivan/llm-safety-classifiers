# Google ShieldGemma — Harm Taxonomy

ShieldGemma (built on Gemma 2 in 2B, 9B, and 27B parameter sizes) is an open-weight LLM-as-a-judge safety classifier evaluating user prompts and model completions against four core policy definitions:

| Policy Key | Definition |
| :--- | :--- |
| **No Sexually Explicit Content** | Shall not contain or seek generation of sexually explicit, pornographic, or erotic content. |
| **No Dangerous Content** | Shall not contain or seek generation of content facilitating harm, weapons, illegal acts, or self-harm. |
| **No Hate Speech** | Shall not express, incite, or promote hate based on race, gender, ethnicity, religion, nationality, sexual orientation, or disability. |
| **No Harassment** | Shall not contain or seek generation of malicious, intimidating, bullying, or abusive content targeting individuals. |

## Inference Output Format
Outputs a single classification token (`Yes` or `No`) indicating whether the evaluated text violates the injected policy preamble.
