# Post-event price paths: exploratory v1

Analysis: November 7, 2026. Curated public release: November 8, 2026.
The owner authorized public use of these selected aggregate findings. This is a
separate sanitized release, not the private experiment package or an open data license.

Across separate historical cohorts, paths frequently moved with and against the
event direction. The small endpoint means conceal substantial two-way movement.
The expansion cohorts do not show a consistent favorable-path advantage across
thresholds and event types. No non-event benchmark was run.

| Separate cohort | Sessions | Events | Median favorable excursion | Median adverse excursion |
| --- | ---: | ---: | ---: | ---: |
| January pilot | 8 | 87 | 54.000 | 41.000 |
| Phase 2 | 22 | 254 | 19.000 | 23.375 |
| Experiment D | 67 | 770 | 23.500 | 23.375 |

Units: provisional NQ-labeled points over the 15 subsequent one-minute candles.
The medians are separate marginal summaries and need not describe the same event.

In D, 594/770 (77.1%) reached at least 10 points favorably and 572/770 (74.3%)
reached at least 10 points adversely. Both opposing levels were reached by
396/770 (51.4%). The categories overlap. Same-minute first-detection ambiguity
occurred for 27/770 events at this threshold, a different quantity from both reached.
The preserved 15-minute signed endpoint mean remains +0.346753 points
(sample SD 43.259098). A favorable reach rate is not directional prediction accuracy.

## Contents

- [Methods, definitions, and limitations](methodology.md)
- [Verification and replication scope](verification.md)
- [Excursion distributions](excursion-summary.csv)
- [Threshold reach and censor summaries](threshold-summary.csv)
- [Opposing first-crossing summaries](first-crossing-summary.csv)
- [Cumulative minute summaries](time-to-threshold.csv)
- [Summary figure](opposing-first-crossing.png) and [caption](figure-caption.md)
- [Publication PDF](../../publication/NQLAB-Post-Event-Publication.pdf)

Group views overlap. Do not add groups or pool cohorts as independent samples.
The public files omit event rows, original price data, session-level dated tables,
the ECDF, detector and analysis source, original reports, environment metadata,
private history, and live records. Full external replication remains unavailable.
No significance, causality, alpha, prospective predictive validity, or profitability
is established. See the repository [reuse disclosure](../../REUSE.md).
