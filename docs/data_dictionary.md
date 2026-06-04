# Data dictionary

## `establishments.csv`

| Field | Type | Notes |
| --- | --- | --- |
| `establishment_id` | string | Stable lowercase identifier. |
| `name` | string | Public establishment name. |
| `status` | string | `active`, `historical`, `watchlist`, or `unverified`. |
| `town` | string | Municipality. |
| `state` | string | Two-letter state code. |
| `address` | string | Street address when verified. |
| `lat` | number | Optional geocode. |
| `lon` | number | Optional geocode. |
| `establishment_type` | string | Market, bakery, restaurant, dairy bar, supermarket bakery, caterer, etc. |
| `kosher_scope` | string | Examples: full establishment, marked packaged items only, bakery department only. |
| `supervision` | string | Certifier or supervising authority. |
| `certification_notes` | string | Important caveats. |
| `cuisine_tags` | string | Pipe-delimited tags. |
| `price_band` | string | `$`, `$$`, `$$$`, or unknown. |
| `hours_text` | string | Source text before normalization. |
| `phone` | string | Public contact number. |
| `website` | string | Official site or ordering page. |
| `source_ids` | string | Pipe-delimited source references. |
| `last_verified` | date | ISO date. |

## `menu_items.csv`

| Field | Type | Notes |
| --- | --- | --- |
| `menu_item_id` | string | Stable item identifier. |
| `establishment_id` | string | Foreign key to `establishments.csv`. |
| `item_name` | string | Raw menu item name. |
| `normalized_name` | string | Clean name for modeling. |
| `description` | string | Raw description. |
| `category_raw` | string | Original menu category. |
| `category_model` | string | Normalized ML class. |
| `price_raw` | string | Raw price text. |
| `price_usd` | number | Parsed price. |
| `kosher_tags` | string | Pipe-delimited tags such as dairy, pareve, meat, pas_yisroel, cholov_yisroel. |
| `dietary_tags` | string | Pipe-delimited tags such as vegetarian, vegan, gluten_free, nut_free. |
| `ingredients_text` | string | Optional extracted ingredient text. |
| `source_ids` | string | Source references. |

## `sources.csv`

| Field | Type | Notes |
| --- | --- | --- |
| `source_id` | string | Stable source identifier. |
| `source_type` | string | certifier, official_site, ordering_page, community_site, review_site, directory. |
| `title` | string | Source title. |
| `url` | string | Source URL. |
| `accessed_date` | date | ISO date. |
| `trust_tier` | integer | 1 is strongest. |
| `notes` | string | Caveats or conflicts. |

## `certifications.csv`

| Field | Type | Notes |
| --- | --- | --- |
| `certification_id` | string | Stable identifier. |
| `establishment_id` | string | Foreign key. |
| `certifier` | string | Certifying agency. |
| `scope` | string | What is covered. |
| `category` | string | meat, dairy, pareve, bakery, packaged, marked-items-only. |
| `start_date` | date | Optional. |
| `end_date` | date | Optional. |
| `status` | string | active, expired, unknown. |
| `evidence_source_id` | string | Source backing the record. |
