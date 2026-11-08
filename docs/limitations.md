# Scientific and reproducibility limitations

> November 8 update: the sections below preserve the initial November 6 release
> record. See the [post-event path package](../results/post-event-path-v1-20261107/README.md)
> for the November 7 extension, fresh internal verification, definitions, and
> continuing limitations. The initial record is not a claim that later work was
> independently scientifically validated.

1. **Instrument and data provenance.** Dated contract identity, rollover and
   adjustment mapping, vendor event/correction semantics, original timestamps
   (including exchange versus receipt and interval start versus end), full trade
   capture and certified exchange-calendar context remain unresolved. The
   historical data label is UNVERIFIED_NQ_CACHE. Plausible prices, quarter-point
   increments, occupancy and continuity screens do not establish instrument
   identity or equivalence to a TradingView continuous contract.
2. **Selection and development.** These are selected retrospective cohorts,
   conditioned on calendar rules and available morning data. Local hashes and
   timestamps do not independently establish preregistration. Expansion after
   observing the pilot is not prospective independent validation. Excluded
   sessions were not silently replaced or treated as zero events.
3. **Dependence.** Overlapping forward windows, common sessions, setup/R relations
   and reused baseline controls preclude independent-event interpretation.
   Non-overlap selection changes category/time composition and does not remove
   shared-session dependence. Session omissions reuse most observations.
4. **Instability and comparison.** Means differ across the separate cohorts and
   are sensitive to session mix. Absolute points are unnormalized for volatility
   or price level. These differences cannot identify regime effects, degradation
   or a generalizable trading rule. No significance or causal claim is made.
5. **Execution and prospective evidence.** Close-to-close changes assume no
   executable entry. Spread, fees, slippage, latency, position sizing and P&L are
   absent. Live webhook receipt and historical Python replay are separate
   evidence streams. No independent prospective predictive validation is shown.
6. **Runtime validation.** Preserved Python prefix, state and warm-up checks are
   software evidence on tested inputs. They are not genuine TradingView/Pine
   execution parity. The historical audit also found bounded box-helper display
   differences outside the event-study calculation; full-indicator parity is not
   established. No same-contract/same-candle Pine runtime oracle was available.
7. **Public reproducibility.** This release omits event-level data, candles,
   detector source and executable replication scripts. Source hashes alone
   cannot enable external numerical replication. Experiment D's original report
   says it was completed for independent review, not independently reviewed;
   current arithmetic checks do not replace a full independent scientific audit.

The owner confirmed relevant data-use and publication permissions for this
release during its preparation. This owner authorization is recorded separately
from unresolved scientific provenance and is not represented as independently
verified vendor documentation. Older private reports retain narrower historical
permission statements. No vendor license, vendor attribution, data-redistribution
grant or open-source reuse license is invented here. Underlying datasets and
implementation are not distributed.
