# Measurement and limitations

Use accepted preserved events from frozen SDR v0.11. No signals were regenerated,
tuned, or selected anew. January, Phase 2, and D remain separate cohorts of
8/87, 22/254, and 67/770 selected sessions/events. All 1,111 accepted events
have a reference close and complete forward coverage. No accepted event was
excluded or substituted in this follow-up calculation.

The reference is each event's own completed candle close. If its opening time is t,
modeled availability is t+60 seconds. Observe the next 15 one-minute candles,
excluding the original event candle's high and low. For bullish events, favorable
excursion is max(0, subsequent high minus reference) and adverse excursion is
max(0, reference minus subsequent low). Bearish events reverse the sides.
MFE and MAE are the maxima across the window. These are nonnegative provisional
NQ-labeled point magnitudes, not trade returns or executable exits.

Thresholds are inclusive 10, 25, and 50 points, evaluated with exact rational
arithmetic on decimal inputs. First crossing means the first subsequent candle
whose high/low reaches the relevant level. Detected minute k bounds the crossing
within [k-1,k] minutes. OHLC cannot resolve within-candle sequence or fills.
Both sides first detected in one candle are always ambiguous. One side reached
and the other censored gives that side first within the window. Neither reached
is a separate category. Both reached can occur in different candles.

An unreached side is administratively censored at 15 minutes, not a hit at 15.
Reach fractions include all complete events in the denominator. Conditional time
quantiles summarize hits only. All-event median detected minute is blank if fewer
than half reached the threshold. Minute percentiles interpolate upper bounds and
do not imply subminute precision.

Each cohort has nine overlapping group views: all, displacement, r, bullish,
bearish, and four signed event types. n and sessions identify each denominator.
Statistics are event weighted. sample_sd uses n-1. Excursion and reached-only
minute percentiles interpolate at (n-1)p. Fractions are on a 0-to-1 scale.
First-crossing category counts partition n; favorable/adverse reach rates overlap.
not_yet_reached_n at minute 15 is the censored count.

## Scientific limits

This exploratory extension followed known endpoint findings. Its local protocol
seal is not externally attested preregistration. No non-event comparator,
uncertainty interval, hypothesis test, normalization, or execution/cost model was
run. Overlapping windows, shared sessions, setup/R relationships, selected dates,
and small type cells limit inference. Absolute point comparisons can reflect
volatility, price scale, session composition, and unresolved instrument mapping.

Historical vendor provenance, original clock semantics, contract identity, and
roll/adjustment mapping remain unresolved. Independent TradingView/Pine runtime
parity is unavailable. Experiment D remains completed for independent review,
not independently reviewed as a complete scientific package. Reproduction of
stored arithmetic does not resolve these limitations. The public package cannot
establish unusual conditional movement, sustained prediction, alpha, or profit.

Future designs require advance owner approval. Untouched dates, appropriate
comparators, provenance and dependence controls would be needed for stronger
claims. These observations must not be relabeled a holdout after inspection.
