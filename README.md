# NQ/LAB: Market-Structure Research

An independent exploratory study of algorithmically detected market-structure
events and short-term price behavior in historical data provisionally associated
with Nasdaq-100 futures. Historical baseline: frozen SDR v0.11.

**Research question:** Do signed 5-minute and 15-minute post-event price changes
show a consistent descriptive pattern across separate selected historical cohorts?

This curated documentation and aggregate-results package was prepared for VIZN
Horizons 2026. The November 8 update adds the November 7 exploratory post-event
path findings and a revised publication PDF. It contains reviewed summaries and
an explicit record of internal arithmetic verification.
Event-level observations, price data, executable replication scripts and full
detector source are **not included**. External end-to-end replication is not yet
possible from this package.

## Main findings

Event-weighted raw mean signed close changes, in provisional NQ-labeled points:

| Separate historical cohort | Selected sessions | Events | 5 minutes | 15 minutes |
| --- | ---: | ---: | ---: | ---: |
| January 2025 pilot | 8 | 87 | -0.109195 | +2.149425 |
| Phase 2 cross-year | 22 | 254 | -2.182087 | -2.600394 |
| Experiment D | 67 | 770 | -0.445130 | +0.346753 |

The initial positive 15-minute mean did not recur consistently across the
separate selected cohorts. Session composition and retrospective benchmark
construction affect the summaries. These observations do not identify a regime
effect or model degradation.

These are descriptive historical results. They do not demonstrate alpha,
profitability, statistical significance, causality or independent prospective
predictive validation. Overlapping windows and shared session conditions make
events dependent. No execution or trading-cost model is applied.

Historical instrument/contract identity, rollover/adjustment mapping and original
timestamp semantics remain unresolved. The internal data label is
`UNVERIFIED_NQ_CACHE`; numerical agreement does not establish TradingView/Pine
runtime parity. Genuine live webhook observations are a separate evidence stream
and are not pooled with these historical cohorts.

## November 7 post-event path update, released November 8

In Experiment D's 770 events, median maximum favorable/adverse excursions over
15 subsequent candles were 23.500/23.375 provisional NQ-labeled points.
At least 10 favorable points were reached by 594/770 (77.1%), adverse points by
572/770 (74.3%), and both sides by 396/770 (51.4%). Favorable reach is not
prediction accuracy. No non-event benchmark was run.

- [Findings, summary CSVs, and aggregate figure](results/post-event-path-v1-20261107/README.md)
- [Follow-up methods and limitations](results/post-event-path-v1-20261107/methodology.md)
- [Fresh internal verification and replication limits](results/post-event-path-v1-20261107/verification.md)
- [Publication PDF: release note plus the approved 18-slide presentation](publication/NQLAB-Post-Event-Publication.pdf)

The update reproduces stored arithmetic. Experiment D remains completed for
independent review, not independently reviewed as a complete scientific package.
Original historical provenance and independent Pine runtime parity remain unresolved.

## Read the evidence

- [Methodology and timing](docs/methodology.md)
- [Scientific limitations](docs/limitations.md)
- [Reproducibility scope and missing materials](docs/reproducibility.md)
- [Reviewed sources and provenance](docs/research-sources.md)
- [Cohort summaries and column definitions](results/cohort-summary.csv),
  [data dictionary](docs/data-dictionary.md)
- [Release checks and sensitivity findings](docs/verification.md)
- [File manifest](release-manifest.json)

The source reports remain private; the source register identifies the reviewed
versions by digest. Hashes identify bytes and do not make unavailable evidence
independently inspectable or certify market-data provenance.

## Citation and reuse

See [citation instructions](CITATION.md) and [CITATION.cff](CITATION.cff).
No open-source code or data license has been selected for this initial package;
see [reuse status](REUSE.md). Public availability is separate from permission to
redistribute underlying data or unpublished implementation.
