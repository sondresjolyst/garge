# Garge — Compliance & governance docs

Controller/org-level data-protection documents for the Garge platform. They describe processing that spans **all** Garge services (the API, web app, device operator, and MQTT broker), so they are maintained centrally rather than alongside any single service.

| Document | Purpose |
|---|---|
| [`article30.md`](article30.md) | Records of Processing Activities (GDPR Art. 30 / ROPA) — the inventory of every processing activity, lawful basis, retention, recipients. |
| [`dpia-sensor-data.md`](dpia-sensor-data.md) | Data Protection Impact Assessment (Art. 35) for continuous sensor-data processing. |
| [`legitimate-interest-assessment.md`](legitimate-interest-assessment.md) | Legitimate Interest Assessment (Art. 6(1)(f)) + re-identification assessment for suspended-sensor retention and the anonymized ML store. |

**Controller:** Sjølyst Innovations (trading as Garge), org. 934 531 035. No DPO designated (not required). Supervisory authority: Datatilsynet (Norway).

## What lives where
- **These governance records** are the single source of truth for how Garge processes personal data.
- **User-facing legal notices** (privacy policy, terms, cookie policy) are published in the Garge web app at `/privacy`, `/terms`, and `/cookies`.

Each record states its own review cadence and re-assessment triggers in its maintenance/decision section.
