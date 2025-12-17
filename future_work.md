# Future Work & Recommendations

## Current Focus

- Actively working on National Grid tariff documents and bill validation.
- Pipeline in place: Extract (PDF) → Group (SC tariffs) → LLM logic → Validate (calculation engine).

## Near‑Term Additions

1. Add More Utilities and Tariff Types
   - Extend beyond National Grid: start with Virginia (Dominion), then add Con Edison (NY), NYSEG, PSEG, RG&E.
   - Create per‑utility profiles (file naming, SC codes, special riders/surcharges).
   - Build import templates for each utility’s tariff format.

2. Improve Anomaly Rules
   - Tighten discrepancy thresholds per SC and season.
   - Add rule sets for riders, demand charges, taxes/fees.
   - Use historical baselines to flag outliers (month‑over‑month, year‑over‑year).

3. Human‑in‑the‑Loop QA
   - Reviewer workflow: auto‑flag → human review → approve/reject.
   - UI actions: “Mark correct”, “Escalate”, “Add note”, “Request re‑run”.
   - Track reviewer decisions to continuously improve rules.

4. Orchestration & Scheduling
   - Expand Airflow usage (or evaluate Prefect) for multi‑utility pipelines.
   - Add scheduled runs, retry policies, and SLA alerts.
   - Queue uploads; process at controlled concurrency.

5. Environment Upscaling
   - Separate dev/stage/prod with isolated S3 buckets and databases.
   - CI/CD for Streamlit + Airflow images; parameterize via environment variables.
   - Secrets management (Streamlit Secrets / AWS Parameter Store / Vault).

## Medium‑Term Improvements

- OCR fallback for scanned PDFs; auto‑detect scans and re‑run with OCR.
- Table extraction robustness (merged/multi‑page tables).
- Model fallback: OpenAI primary with Claude/Gemini backup for resilience.
- Cost and latency tracking per bill; optimize hot paths in calculation engine.

## Monitoring & Ops

- Dashboard metrics: processed bills, success rate, anomaly rate, avg runtime.
- Alerts: pipeline failures, missing outputs in S3, cost spikes.
- Audit trail: inputs/outputs, rule versions, reviewer actions.

## Handoff Checklist

- [ ] Document per‑utility onboarding steps (data paths, SC mapping, riders).
- [ ] Define anomaly rules by utility/SC and publish in repository.
- [ ] Set up staging environment credentials and test runs.
- [ ] Populate sample datasets (tariffs + bills) for each new utility.
- [ ] Write runbooks for operators and reviewers.

## Notes

- Start with Virginia state tariffs to validate multi‑utility support.
- Keep pipelines simple; prefer explicit rule configuration over opaque prompts.

