# Historical event-study methodology

The research baseline is frozen SDR v0.11. Preserved Python replay outputs label
bullish/bearish displacement (diamond) and bullish/bearish R events. R events
relate to preceding setups, adding dependence. This release describes event-study
measurement and selection; it does not disclose a complete detector specification
or provide executable detector code. Source implementation and configuration
require a separate provenance and confidentiality review before release.

## Cohorts and selection

- January: eight coverage-selected chronological mornings, January 2, 3, 6, 7,
  8, 10, 13 and 14, 2025; 87 events. This is the original exploratory pilot.
- Phase 2: third Wednesday of January, April, July, October and December in
  2021-2025: 25 calendar candidates, 22 passing sessions, 254 events. Three
  candidates were excluded without replacement for missing or malformed data.
- Experiment D: first/third Tuesday and Thursday of February, May, August and
  November in 2021-2025: 80 calendar candidates, 67 passing sessions, 770 events.
  Thirteen candidates were excluded without replacement for data/warm-up gates.
  These selected sessions are disjoint from January and Phase 2.

Calendar rules and local seals are consistent with declared selection before
new replay. They are not an independent timestamped preregistration or proof of
historical ordering. Passing occupancy gates conditions the samples further;
neither expansion is a random sample of trading sessions. Excluded/not-run
sessions are not zero-event observations. No cohorts are pooled in this release.

## Bars, state and availability

Stored UTC timestamps are treated as one-minute bar opens and converted using
America/New_York. Event bar opens are in [09:30, 11:00) New York time. Historical
events become available at their modeled candle close, one minute after open;
09:30 markers therefore become known at 09:31. Bars opening from 11:00 through
11:14 provide outcome buffer, not additional study events.

Minute aggregation uses first open, maximum high, minimum low, last close and
summed volume in occupied buckets, with no gap filling/interpolation. Occupancy
does not prove complete trade capture or validate the vendor's original clock
semantics. Passing expansion sessions have all 105 morning/buffer buckets and
at least 120 contiguous pre-open minutes under the preserved gates. Prior-day
and current-day histories provide warm-up. Python state depends on history;
tested warm-up agreement is not a universal sufficiency guarantee. The January
audit found that starting only at 09:30 changes events on all eight dates.

## Raw signed outcome

Let t be the event candle's opening time, C(t) its closing price, d be +1 for a
bullish event or -1 for a bearish event, and h be 5 or 15 minutes:

`signed_change(h) = d * [C(t + h minutes) - C(t)]`.

The outcome candle closes exactly h minutes after the reference candle closes.
Both horizons require all intervening minute candles. All included events in
these three cohorts have both outcomes. Results are unnormalized price-point
changes, provisionally NQ-labeled; they are not percentage returns or trade P&L.
Reference-close availability does not guarantee an executable fill at that close.
Pooled means weight events equally; equal-session means are different statistics.

## Retrospective baseline and sensitivity

Experiment C v2 concerns the January pilot only. Each event has seven other-day
controls at the same New York reference-close minute and the same sign. Controls
are averaged within each event before the event-minus-baseline contrasts are
aggregated. Donor windows may contain SDR events, overlap, be reused, and come
from dates later than the origin. This is a retrospective descriptive benchmark.
It is not the generic event-neighborhood-excluding baseline used by another code
path. No cross-year matched baseline was executed for Phase 2 or Experiment D.

Experiment C session omission removes a day as both event origin and control
donor, recomputing donor means while retaining original subset membership.
Raw January and Experiment D omission diagnostics remove event origins only;
they do not use baseline donors. These are composition sensitivities, not
confidence intervals, significance tests or independent replications.

## Live evidence is separate

Historical Python-generated availability is modeled; it is not an observed
TradingView trigger or webhook receipt. Genuine live observations retain actual
activation, trigger and receipt evidence and require separately matched prices.
Live delivery can verify collection without validating historical signal parity
or prospective predictive performance. No live records or live outcomes are
included in this package.
