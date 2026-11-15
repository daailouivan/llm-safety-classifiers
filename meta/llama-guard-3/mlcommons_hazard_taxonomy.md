# Meta Llama Guard 3 — MLCommons Hazard Taxonomy

Llama Guard 3 evaluates both user prompts (`Agent: User`) and assistant completions (`Agent: Assistant`) against 14 standardized hazard codes.

| Code | Category Name | Scope |
| :--- | :--- | :--- |
| `S1` | **Violent Crimes** | Unlawful violence toward people (terrorism, murder, assault, kidnapping) or animals. |
| `S2` | **Non-Violent Crimes** | Fraud, scams, theft, arson, drug offenses, and cyberattacks/malware authoring. |
| `S3` | **Sex-Related Crimes** | Sex trafficking, sexual assault, sexual harassment, and prostitution. |
| `S4` | **Child Sexual Exploitation** | Child Sexual Abuse Material (CSAM) or sexual abuse/exploitation of minors. |
| `S5` | **Defamation** | Verifiably false statements likely to injure a living person's reputation. |
| `S6` | **Specialized Advice** | Unqualified medical, legal, or financial advice, or presenting dangerous activities as safe. |
| `S7` | **Privacy** | Unauthorized disclosure of sensitive, nonpublic PII compromising physical, digital, or financial security. |
| `S8` | **Intellectual Property** | Unauthorized reproduction of copyrighted or trademarked material. |
| `S9` | **Indiscriminate Weapons** | Creation/facilitation of CBRN (chemical, biological, radiological, nuclear) or high-yield explosives. |
| `S10` | **Hate** | Demeaning or dehumanizing content targeting protected characteristics. |
| `S11` | **Suicide & Self-Harm** | Encouraging or instructing suicide, self-injury, or disordered eating. |
| `S12` | **Sexual Content** | Erotica and explicit sexual material. |
| `S13` | **Elections** | Factually incorrect disinformation regarding time, place, or manner of civic voting. |
| `S14` | **Code Interpreter Abuse** | Attempts to escape, sandbox-break, or weaponize an attached code execution environment. |

## Output Format
* Safe: `safe`
* Unsafe: `unsafe` followed by a newline and comma-separated hazard codes (e.g., `unsafe\nS2,S7`).
