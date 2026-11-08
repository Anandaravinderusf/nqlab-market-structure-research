# What can be reproduced

> November 8 update: the sections below preserve the initial November 6 release
> record. See the [post-event path package](../results/post-event-path-v1-20261107/README.md)
> for the November 7 extension, fresh internal verification, definitions, and
> continuing limitations. The initial record is not a claim that later work was
> independently scientifically validated.

## From this public package

Readers can inspect the methodology, limitations, six cohort/horizon aggregate
rows and verification record. For each CSV row, `sum_signed_points / events`
agrees with `mean_signed_points` within decimal rounding. README values are
rounded to six decimal places. The file manifest supports payload integrity
checking. These checks do not reconstruct event-level outcomes or validate data
provenance; aggregate signed sums do not substitute for source observations.

## Checked privately during release preparation

Read-only checks reconstructed all 2,222 existing 5m/15m signed outcomes from
preserved event identities and stored candle closes: 174 January, 508 Phase 2,
and 1,540 Experiment D. Counts, pooled means, medians, sample SDs, timing,
complete windows, disjoint selected dates and overlap counts agree with the
preserved summaries. Existing January raw omission, Experiment C all-event full
and January-2 origin/donor omission contrasts, and all Experiment D raw
single-session omissions were checked. Signals were not regenerated and no new
experiment, statistical test or outcome definition was run.

Archived run/final output hashes and completion seals were checked for the
selected B/C, Phase 2/addendum and Experiment D packages. Frozen source/replay
hashes match the freeze record. The current package check does not independently
validate every market-data input, rerun the historical test suites or certify all
archived validation claims. Historical test counts remain archived evidence.

## Required for external replication in a future release

- Reviewed event records with sign/type, origin, modeled/actual availability,
  reference price and full 5m/15m outcomes; exact cohort and exclusion manifests.
- Authorized one-minute OHLCV histories including warm-up and outcome buffer,
  source hashes, date/instrument mapping, units, timestamp semantics, correction
  handling, aggregation and missing-data rules. The January chart-only subset
  omits warm-up and is insufficient to regenerate its events.
- Reviewed frozen detector implementation/configuration and replay; importer,
  event-study, baseline and reporting code; exact B/C subset membership and donor
  windows; test fixtures and per-stage hashes.
- A portable dependency/environment record and commands that write only fresh
  outputs. Private manifests contain machine-specific paths and require careful
  extraction rather than direct publication.

The preserved expansions record Python 3.13.16 with pandas 2.3.3, NumPy 2.3.4,
PyArrow 23.0.1 and tzdata 2025.2. The private dependency file also pins plotting
and supporting packages. These are recorded historical versions, not an install
recipe for this release; no runtime dependency file is included because no
replication software is shipped. Timezone databases, fonts, image metadata and
manual editorial packaging can affect artifact portability. Phase 2's addendum
documents a manual final-report metadata step, so a fully scripted byte-identical
report rebuild is not established even where arithmetic is reproducible.

## Not established

Original vendor/exchange provenance, full raw-market reconstruction, independently
verified selection chronology, universal warm-up sufficiency, independent Pine
runtime parity and prospective predictive validity remain outside the verified
scope. Resolving scientific provenance is separate from the owner's publication
authorization. Future data/code releases require their own confidentiality and
reuse-permission review and must preserve these historical checkpoints.
