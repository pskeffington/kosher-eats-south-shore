# Project scope

## Mission

`kosher-eats-south-shore` is a source-linked research and machine learning scaffold for mapping kosher food access on the South Shore of Massachusetts and turning sparse community food information into structured, useful data.

The project has two parallel purposes:

1. Help local families and visitors understand where kosher options actually exist.
2. Build a small, transparent menu intelligence pipeline that can classify establishments, normalize menus, identify dietary and kashrut tags, and support future recommendation features.

## Geographic scope

The initial verified scope is the South Shore Jewish corridor centered on Canton, Sharon, and Stoughton. Current evidence supports this cluster more strongly than a broad coastal Plymouth-to-Cape kosher restaurant footprint.

Primary towns in scope:

- Canton
- Sharon
- Stoughton
- Adjacent South Shore communities when an establishment has reliable kosher certification or clear community relevance

Extension watchlist:

- Plymouth
- Bourne
- Sandwich
- Barnstable
- Falmouth
- Hyannis
- Other Cape Cod communities

The Plymouth-to-Cape area should be handled as a monitored expansion zone until active, supervised kosher establishments are verified through certifier pages, establishment pages, or direct confirmation.

## Current verified active nodes

The first research pass identified these active nodes:

- Zayde's Market, Canton
- Life's A Bagel, Canton
- Crescent Ridge Dairy Bar, Sharon
- Shaw's bakery department, Canton, for marked KVH-certified items
- Shaw's bakery department, Sharon, for marked KVH-certified items
- Stop & Shop bakery department, Stoughton, for marked KVH-certified items

Historical or excluded records should remain in the dataset with status fields when useful for preventing stale information from re-entering active training data.

## Source hierarchy

Use this trust order when conflicts appear:

1. Certifier records and certificates
2. Official establishment pages
3. Official ordering pages
4. Community institution pages
5. Reputable local directories
6. General review sites and scraped snippets

Lower-tier sources must not silently overwrite higher-tier sources. Conflicts should be preserved in structured fields.

## Data products

Initial data products:

- `data/processed/establishments.csv`
- `data/processed/menu_items.csv`
- `data/processed/certifications.csv`
- `data/processed/sources.csv`
- `docs/data_dictionary.md`
- `docs/source_registry.md`

## Machine learning scope

Initial ML tasks:

- Menu category classification
- Kashrut and dietary multilabel tagging
- Price normalization and price-band prediction
- Establishment type classification
- Source-quality scoring
- Content-based recommendation for occasions such as weekday breakfast, Shabbat catering, dessert, holiday shopping, and family outings

The early dataset is intentionally small. The first goal is not model scale; it is clean data lineage, correct labels, and a useful community-facing prototype.

## Social and community presentation

This project should be presented as a constructive community data story rather than a generic food app:

> A small machine learning project mapping kosher food access across the South Shore, showing how structured local data can help families, visitors, synagogues, students, and small businesses find each other.

LinkedIn and social posts should emphasize:

- Community connection
- Food access
- Small business visibility
- Transparent data practices
- Practical machine learning for real local needs

## Guardrails

- Do not represent an establishment as kosher without source evidence.
- Do not infer certification scope from general store branding.
- Preserve certification caveats, such as dairy, pareve, meat, Cholov Stam, Cholov Yisroel, Pas Yisroel, and label-dependent supermarket bakery certification.
- Keep raw source text and normalized fields separate.
- Treat scraping and API keys as private operational concerns.
