# Garge — Compliance & governance docs

Controller/org-level data-protection documents for the Garge platform. They describe processing that spans **all** services (`garge-api`, `garge-app`, `garge-operator`, the MQTT broker), so they live here in the umbrella repo rather than in any single service repo.

| Document | Purpose |
|---|---|
| [`article30.md`](article30.md) | Records of Processing Activities (GDPR Art. 30 / ROPA) — the inventory of every processing activity, lawful basis, retention, recipients. |
| [`dpia-sensor-data.md`](dpia-sensor-data.md) | Data Protection Impact Assessment (Art. 35) for continuous sensor-data processing. |
| [`legitimate-interest-assessment.md`](legitimate-interest-assessment.md) | Legitimate Interest Assessment (Art. 6(1)(f)) + re-identification assessment for suspended-sensor retention and the anonymized ML store. |

**Controller:** Sjølyst Innovations (trading as Garge), org. 934 531 035. No DPO designated (not required). Supervisory authority: Datatilsynet (Norway).

## What lives where
- **These governance docs** → here (`garge/docs/compliance/`). Single source of truth.
- **User-facing legal pages** (privacy policy, terms, cookie policy) → `garge-app` (`src/app/privacy`, `/terms`, `/cookies`) — they are rendered pages, not documents.
- **Implementation** referenced by these docs → the service repos (`garge-api` backend, `garge-app` frontend, `garge-operator`).

## Keeping these in sync with code (PR checklist)
Because the docs no longer sit next to the code, when a change in **any** service repo alters data processing, update the relevant doc here in the same change-set:

- [ ] New/changed **collected field**, **data category**, or **recipient/sub-processor** → update `article30.md`.
- [ ] New **lawful basis**, **retention rule**, or **purpose** → update `article30.md` + `dpia-sensor-data.md` (+ `legitimate-interest-assessment.md` if it touches legitimate interest or anonymisation).
- [ ] New **sensor type**, third-party sharing, or safety-critical automation → re-open the DPIA (see its §7 triggers).
- [ ] Bump the document version + `Last updated` + sign-off date on any substantive change.
