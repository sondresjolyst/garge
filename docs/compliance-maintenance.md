# Maintaining the compliance docs (developer process)

Internal notes for keeping the GDPR records in [`compliance/`](compliance/) accurate. **This file is not part of the compliance record** — it is engineering process and is intentionally kept outside the `compliance/` folder.

The records (`article30.md`, `dpia-sensor-data.md`, `legitimate-interest-assessment.md`) describe processing that spans all services but live in this umbrella repo, away from the code. When a change in any service repo (`garge-api`, `garge-app`, `garge-operator`) alters data processing, update the relevant record in the same change-set:

- New/changed **collected field**, **data category**, or **recipient/sub-processor** → `article30.md`.
- New **lawful basis**, **retention rule**, or **purpose** → `article30.md` + `dpia-sensor-data.md` (+ `legitimate-interest-assessment.md` if it touches legitimate interest or anonymisation).
- A change that meets a **DPIA re-assessment trigger** → re-open `dpia-sensor-data.md` (see its §7).
- Bump the document version + `Last updated` + sign-off date on any substantive change.
