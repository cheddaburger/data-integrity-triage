# Site Data Integrity Triage & Remediation

A company-agnostic notebook for **data integrity** work: find missing or inconsistent site records, reconcile what can be safely filled from authoritative sources, and generate a **field/ops work queue** for the items that require human verification.

## Why this exists

In large organizations, the data you need often **exists somewhere**—just not in the right spot. This notebook helps you:
- Detect gaps (missing required fields, invalid combinations, duplicates)
- Pull candidate values from other sources (when appropriate)
- Route unresolved items (e.g., equipment configuration) to technicians with clear instructions

## Workflow

1. Load site inventory (assumes GPS LAT/LON already present, if expected)
2. Run integrity audit (missing/duplicates)
3. Reconcile from supporting datasets (optional)
4. Generate prioritized work queue
5. Export reconciled dataset + audit artifacts

## Getting started

- Place your files in `./data/`
- Update `COLUMN_MAP` to match your column names
- Run the notebook top-to-bottom

## Outputs

- `output/site_inventory_reconciled.xlsx`
- `output/work_queue.xlsx`
- `output/audit_summary.xlsx`

## Notes

This repo contains **no proprietary data**. It is designed to be adapted to your organization’s systems and sources.
