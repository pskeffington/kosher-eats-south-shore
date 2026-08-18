# Kosher Eats South Shore

Public community-data and machine-learning research scaffold for mapping kosher food access on the South Shore of Massachusetts using source-linked establishment, menu, and certification information.

**Maintainer:** Paul Skeffington, MS, MPH  
**Repository status:** early community-data and classification scaffold; active establishment and certification status must be source-verified before public use.  
**Last documentation refresh:** 2026-08-17

## Purpose

The project has two linked goals:

1. Organize reliable local information about kosher food access for families, visitors, community institutions, and small businesses.
2. Develop a small, transparent machine-learning workflow for menu classification, dietary and kashrut tagging, source-quality review, and future community-facing recommendation features.

The current geographic focus is the South Shore Jewish corridor centered on Canton, Sharon, and Stoughton, with broader Plymouth-to-Cape communities treated as an expansion area only when establishments can be verified through authoritative sources.

## Public-interest and community boundary

This repository is maintained for community data organization, food-access research, transparent machine-learning experimentation, and reproducible local information work.

It does not certify establishments, replace a kosher certifying authority, provide religious rulings, guarantee current business status, or infer kosher status from branding, reviews, or geographic proximity. Public claims about certification should remain tied to dated source evidence and preserve scope-specific caveats.

## Current research status

- Stage: early structured-data and prototype scaffold
- Evidence status: initial source-linked establishment research exists; continuing verification is required
- Data status: public establishment, menu, certification, and source metadata only
- Primary limitation: local food and certification information can change quickly and must be re-verified before current-use claims

## Source hierarchy

When sources conflict, prefer:

1. certifier records and certificates;
2. official establishment pages;
3. official ordering pages;
4. community institution pages;
5. reputable local directories;
6. general review sites and scraped snippets.

Lower-tier sources should not silently overwrite higher-tier evidence. Historical and uncertain records should remain distinguishable from currently verified records.

## Planned data products

```text
data/processed/establishments.csv
data/processed/menu_items.csv
data/processed/certifications.csv
data/processed/sources.csv
docs/data_dictionary.md
docs/source_registry.md
```

## Machine-learning scope

Candidate tasks include:

- menu-category classification;
- kashrut and dietary multilabel tagging;
- price normalization and price-band prediction;
- establishment-type classification;
- source-quality scoring;
- content-based recommendation experiments for common community use cases.

The dataset is intentionally small. The priority is clean provenance, correct labels, transparent uncertainty, and useful community documentation rather than model scale or performance claims.

## Documentation and data guardrails

- Do not represent an establishment as kosher without source evidence.
- Do not infer certification scope from general store or restaurant branding.
- Preserve certification qualifiers and product-specific limitations.
- Keep raw source text separate from normalized fields.
- Record source URLs, dates, verification status, and conflict notes.
- Treat stale or closed establishments as historical records rather than silently deleting evidence.
- Do not publish private credentials, API keys, or restricted source material.

## Repository guide

See [`PROJECT_SCOPE.md`](PROJECT_SCOPE.md) for the detailed geographic scope, current source hierarchy, candidate data products, machine-learning tasks, community presentation goals, and project guardrails.

## Supported contribution

A transparent local-data scaffold for studying and documenting kosher food access while exploring small-scale, source-linked machine-learning methods.

## Unsupported contribution

No certification authority, religious ruling, guarantee of current establishment status, or unsupported recommendation claim is made.
