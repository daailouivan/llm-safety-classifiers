# Anthropic — Constitutional AI & Classifier Architecture

Anthropic does not expose a static boolean moderation API endpoint like OpenAI or Gemini. Instead, safety enforcement is split across Constitutional AI model alignment, hard red-line constraints, and input/output **Constitutional Classifiers**.

## 1. Hard Red-Line Constraints (Absolute Refusals)
* **CBRN Weapons:** Providing significant uplift for chemical, biological, radiological, or nuclear weapons attacks.
* **Child Safety:** Child Sexual Abuse Material (CSAM) or Child Sexual Exploitation and Abuse (CSAE).
* **Critical Infrastructure & Cyberattacks:** Assisting with severe cyberattacks against critical infrastructure.
* **AI Oversight Subversion:** Undermining human oversight, corrigibility, or safety controls.

## 2. Constitutional Classifiers (Input & Output Guardrails)
Input and output classifiers trained on synthetic constitutional data specifically target universal jailbreaks and domain uplift without over-refusing benign adjacent queries:
* **Input Classifier:** Screens incoming prompts for adversarial obfuscation (ciphers, encodings, roleplay wrappers, keyword substitution, and prompt injections).
* **Output Classifier:** Streams generated tokens and halts generation if output crosses policy thresholds on high-risk domains.
