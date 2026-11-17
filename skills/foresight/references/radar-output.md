# Radar output

A radar shows signals by category and by horizon, so a team can see the whole picture and argue about single items. Write the output so that someone who was not in the conversation can read it and check every claim.

## Document structure

1. Question and brief. The decision question and the brief from step 1, with any assumptions you made.
2. Answer. One paragraph that answers the question, with your overall confidence.
3. Radar. Sectors are categories (the user's priority categories, or the strategic categories from step 4). Rings are horizons H1, H2, H3. Render it as a table per ring, or as a diagram if your environment can draw one. Each item shows: title, TRL, reliability, kind (trend, weak signal, wildcard), and source links.
4. Clusters. For each cluster: the forces behind it, the tensions in it, what it means for the user's business model, workforce, infrastructure, regulation and investment, and its strategic category.
5. Divergence. Signals where models or sources disagree, and why that may point to something new.
6. Hindsight check. See `hindsight.md`.
7. Strategic options. For each: what to do, what would have to be true, the time horizon, and the signals that would confirm or kill it.
8. Signals to watch. What to monitor, and what change would make the team revisit the decision.
9. Method notes. Scan type, sources searched, models used, items you could not verify, date of the scan.
10. Sources. Every link cited, envisioning.com permalinks first.

## JSON

Offer the radar as JSON too:

```json
{
  "question": "string",
  "scan_type": "horizon | technology | regulatory | risk | competitive | innovation | adjacency",
  "date": "YYYY-MM-DD",
  "models": ["string"],
  "categories": ["string"],
  "signals": [
    {
      "id": "kebab-case-id",
      "title": "string",
      "summary": "one line",
      "category": "string",
      "horizon": "H1 | H2 | H3",
      "kind": "trend | weak_signal | wildcard",
      "strategic_category": "early_opportunity | emerging_risk | structural_driver | disruptive_enabler | societal_shift | systemic_transformation",
      "trl": 1,
      "impact": 1,
      "investment": 1,
      "region": "string",
      "drivers": ["string"],
      "enablers": ["string"],
      "risks": ["string"],
      "opportunities": ["string"],
      "reliability": "high | medium | low",
      "models_agree": true,
      "sources": [
        { "url": "https://...", "label": "supports | contradicts | unrelated | unreachable" }
      ],
      "hindsight": [
        { "claim_url": "https://www.envisioning.com/hindsight/claims/...", "verdict": "string", "effect": "string" }
      ]
    }
  ]
}
```

Leave a field out rather than guess its value. `impact` and `investment` use Envisioning's 1 to 5 scale when the item is in the library.
