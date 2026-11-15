# Google Gemini API — Safety Filters & Thresholds

Official developer-facing harm categories exposed via the Gemini API (`SafetySetting`) and Google AI Studio.

## Adjustable Harm Categories

| API Enum / Value | Description |
| :--- | :--- |
| `HARM_CATEGORY_HARASSMENT` (`harassment`) | Abusive, threatening, or content intended to bully, torment, or ridicule. |
| `HARM_CATEGORY_HATE_SPEECH` (`hate_speech`) | Content that promotes violence or incites hatred against individuals or groups based on protected attributes. |
| `HARM_CATEGORY_SEXUALLY_EXPLICIT` (`sexually_explicit`) | Content that contains sexually explicit material or pornography. |
| `HARM_CATEGORY_DANGEROUS_CONTENT` (`dangerous_content`) | Content that promotes, facilitates, or enables dangerous activities or real-world harm. |
| `HARM_CATEGORY_CIVIC_INTEGRITY` (`civic_integrity`) | Election-related queries and civic integrity policies. |
| `jailbreak` (Interactions API filter) | Prompts specifically designed to bypass safety filters. |

## Non-Configurable Core Protections (Always Active)
* Child Sexual Abuse Material (CSAM) and child exploitation
* Suicide and self-harm encouragement/instruction
* Cyberattacks and critical infrastructure threats
* CBRN / dangerous weapons facilitation

## Block Thresholds

| API Enum | AI Studio Label | Behavior |
| :--- | :--- | :--- |
| `BLOCK_LOW_AND_ABOVE` | Block most | Blocks `LOW`, `MEDIUM`, and `HIGH` probability/severity; allows only `NEGLIGIBLE`. |
| `BLOCK_MEDIUM_AND_ABOVE` | Block some | Blocks `MEDIUM` and `HIGH`; allows `NEGLIGIBLE` and `LOW`. |
| `BLOCK_ONLY_HIGH` | Block few | Blocks only `HIGH`; allows `NEGLIGIBLE`, `LOW`, and `MEDIUM`. |
| `BLOCK_NONE` | Block none | Disables automated blocking; still computes and returns `safetyRatings` metadata. |
| `OFF` | Off | Disables safety filter evaluation completely; no metadata returned. |
