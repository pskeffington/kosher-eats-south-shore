# Social media helper for eating kosher

## Working concept

The social media helper is a community-facing layer for `kosher-eats-south-shore`. Its purpose is to make kosher food discovery easier, friendlier, and more shareable while preserving careful source standards around kashrut claims.

The helper should not behave like a generic restaurant app. It should act like a community connector:

- Help families find verified kosher options.
- Help visitors understand what is available before traveling.
- Help synagogues and community groups share reliable local food information.
- Help small kosher-friendly businesses become discoverable.
- Help users create respectful social posts that support local community life.

## Core user stories

### Family looking for food

A family wants to know what options are available near Canton, Sharon, Stoughton, Plymouth, or Cape Cod. The helper should return verified options first, explain caveats, and suggest a shareable post such as:

> Looking for verified kosher breakfast or bakery options on the South Shore? Here are the currently verified nodes we found, with source notes and certification caveats.

### Visitor planning a trip

A visitor heading toward Plymouth or the Cape wants to know whether kosher food is available along the route. The helper should distinguish between verified establishments, marked supermarket bakery items, and watchlist towns where no active supervised establishment has been confirmed.

### Community organization sharing a resource

A synagogue, school, or local group wants to post a useful update. The helper should produce a clear, source-linked summary without overstating certification scope.

### Small business visibility

A local kosher business or supervised food department should be easier to find. The helper can generate business-friendly blurbs while keeping certification details factual.

## Content types

### 1. LinkedIn posts

Purpose: show practical machine learning for community connection.

Tone: thoughtful, civic, technical but human.

Example angle:

> Most AI demos chase scale. This one starts small: helping people find kosher food across the South Shore of Massachusetts. By turning fragmented public information into structured, source-linked data, we can support families, visitors, synagogues, and small businesses with a practical community tool.

### 2. Facebook community posts

Purpose: useful local sharing.

Tone: warm, concise, neighborhood-centered.

Example angle:

> We are building a source-linked guide to kosher food options on the South Shore. The first verified cluster is around Canton, Sharon, and Stoughton. Plymouth-to-Cape is being tracked as a watchlist until more active supervised options are confirmed.

### 3. Instagram carousel captions

Purpose: visual, simple education.

Tone: friendly and accessible.

Carousel sequence:

1. Eating kosher on the South Shore
2. Verified options first
3. Certification scope matters
4. Bakeries and marked items can count, but only when source-backed
5. Plymouth-to-Cape is a watchlist zone
6. Help us keep the map accurate

### 4. Community update blurbs

Purpose: synagogue newsletters, school groups, local email lists.

Tone: practical and trusted.

Example angle:

> A new community data project is mapping verified kosher food access across the South Shore. The project combines careful source review with simple menu classification tools so local families and visitors can better understand available options.

## ML-assisted helper features

### Post generator

Inputs:

- Audience: LinkedIn, Facebook, Instagram, synagogue newsletter, local email list
- Topic: verified options, new listing, menu highlight, travel planning, holiday prep, community request
- Location: town or route
- Certification strictness: high, moderate, exploratory
- Tone: professional, warm, celebratory, cautious, technical

Outputs:

- Short post
- Long post
- Suggested title
- Hashtags
- Caveat sentence
- Source note

### Menu explainer

Inputs:

- Establishment
- Menu items
- Certification scope
- Dietary tags

Outputs:

- Human-readable menu summary
- Suggested family use case
- Suggested travel use case
- Items requiring verification

### Community connector

Inputs:

- User location
- Destination
- Occasion
- Time window
- Dietary needs

Outputs:

- Verified nearby options
- Watchlist notes
- Suggested post asking for community confirmation
- Business or synagogue contact suggestions, when sourced

### Accuracy guardrail

The helper must include one of these labels in every generated food recommendation:

- Verified active
- Verified limited scope
- Watchlist
- Historical
- Unverified lead

## Recommended data fields for social content

Add these optional fields to establishment and menu records:

- `share_title`
- `share_summary`
- `community_use_case`
- `route_relevance`
- `holiday_relevance`
- `family_friendly_score`
- `visitor_friendly_score`
- `confidence_label`
- `recommended_caveat_text`

## LinkedIn positioning

The best public frame is:

> Practical AI for community infrastructure.

Supporting points:

- This is a small, local data project.
- Kosher food discovery is a real coordination problem.
- The hard part is not the model; it is trustworthy data.
- Menu machine learning becomes useful when it respects community rules and source evidence.
- The project can help local institutions and small businesses become more discoverable.

## Hashtag bank

- #Kosher
- #SouthShoreMA
- #CommunityData
- #MachineLearning
- #ResponsibleAI
- #LocalBusiness
- #FoodAccess
- #JewishCommunity
- #CivicTech
- #DataForGood

## Product direction

The first product should be a content assistant, not a public ranking engine. Ranking can come later after the data is stronger.

Phase 1:

- Source-linked establishment records
- Simple post templates
- Manual review before publication

Phase 2:

- Menu item extraction
- Category and dietary tagging
- Route-based helper prompts

Phase 3:

- Recommendation prototype
- Community submission form
- Verification workflow

Phase 4:

- Public map or microsite
- Social sharing cards
- Newsletter export
