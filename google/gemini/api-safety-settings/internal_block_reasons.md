# Google — Extended `FinishReason` & `BlockReason` Enums

Observed in raw API error payloads, gRPC responses, and AI Studio network traces beyond the 5 adjustable `HarmCategory` settings.

| Enum Code | Trigger Condition |
| :--- | :--- |
| `PROHIBITED_CONTENT` | Hard block for CSAM, severe self-harm, or non-consensual sexual content. |
| `SPII` | Sensitive Personally Identifiable Information (SSNs, credit cards, private keys) detected in output stream. |
| `RECITATION` | Verbatim training-data/copyright overlap filter halted token generation. |
| `BLOCKLIST` | Match against internal or workspace-configured restricted term lists. |
| `IMAGE_SAFETY` | Multimodal image generation safety filter triggered. |
| `IMAGE_PROHIBITED_CONTENT` | Severe policy violation triggered in multimodal image pipeline. |
