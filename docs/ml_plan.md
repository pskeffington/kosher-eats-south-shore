# Menu machine learning plan

## Framing

This project should begin as a small supervised-data problem with strong provenance rather than a large scraped-data exercise. Kosher food data is sparse, status-sensitive, and easy to misstate. The model pipeline should preserve source evidence and uncertainty.

## Early model tasks

### 1. Establishment classification

Predict or assign one or more labels:

- Market
- Bakery
- Bagel shop
- Dairy bar
- Restaurant
- Caterer
- Supermarket bakery
- Watchlist or unverified node

### 2. Menu category classification

Normalize raw menu categories into stable classes:

- Bagels
- Breakfast
- Sandwiches
- Salads
- Prepared foods
- Bakery
- Desserts
- Ice cream
- Drinks
- Catering trays
- Holiday foods

### 3. Kashrut and dietary multilabel tagging

Potential labels:

- meat
- dairy
- pareve
- pas_yisroel
- cholov_yisroel
- cholov_stam
- vegetarian
- vegan
- gluten_free
- nut_free
- fish

The model should never infer kosher status without an establishment-level or item-level source. Kashrut tags should be treated as evidence-linked labels, not free-form guesses.

### 4. Price normalization

Parse raw prices into numeric fields and price bands. This enables community-friendly comparisons such as affordable breakfast, family dessert outing, or Shabbat catering planning.

### 5. Recommendation prototype

Build a simple content-based recommender before any complex model:

Inputs:

- Location
- Occasion
- Dietary constraints
- Certification requirements
- Food category
- Time/day

Outputs:

- Ranked establishment or item suggestions
- Explanation fields
- Source links
- Caveats

## Data pipeline

1. Collect source records.
2. Extract establishment fields.
3. Extract menu text.
4. Normalize names, categories, prices, and tags.
5. Attach source IDs.
6. Validate certification scope.
7. Export model-ready CSV/JSONL.

## Baseline algorithms

- Rules and dictionaries for first-pass labels
- TF-IDF or sentence embeddings for menu similarity
- Logistic regression or gradient boosting for category labels once enough examples exist
- Human review loop for kashrut-sensitive fields

## Evaluation

Track:

- Label precision for establishment type
- Label precision for kosher/dietary tags
- Price parse accuracy
- Recommendation explanation quality
- Source coverage completeness

For public outputs, prefer precision over recall. Missing a weak lead is better than falsely advertising kosher availability.
