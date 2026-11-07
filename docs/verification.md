# Release verification record

Preparation date: 2026-11-06. Scope: arithmetic and disclosure checks against
preserved local records. This is not external peer review or vendor attestation.

## Checks performed for this release

- PASS: clean tracked checkout inspected; ignored later research packages
  identified separately from Git history.
- PASS: 8/87, 22/254 and 67/770 session/event counts; distinct selected dates;
  all 2,222 existing signed horizon outcomes match stored candle arithmetic.
- PASS: event-close availability, evaluation window, complete forward coverage,
  pooled means, medians, sample SDs and overlap counts reconcile.
- PASS: selected archived output digests and three completion seals match;
  frozen source and replay digests match the freeze record.
- PASS: January raw January-2 omission, Experiment C full/January-2 omission
  contrasts, and all 67 Experiment D raw omissions reconcile.
- PASS: all included text/CSV/JSON/metadata reviewed; no copied source reports,
  embedded images, executable code, private paths, credentials, databases,
  infrastructure identifiers, raw market data or private Git history included.

## Sensitivity findings, kept distinct

January raw means change from -0.109195/+2.149425 to
-4.925000/-2.037500 points when January 2's seven events
are omitted (80 events remain). This is outcome-only sample composition.

Experiment C v2's all-event event-minus-baseline contrasts are
1.553777/3.662562 points at 5m/15m. Omitting
January 2 as both origin and donor gives
-4.056250/-1.491667 points.
These baseline contrasts are not the raw returns in the cohort CSV. Seven
donors become six under omission. The archived fixed 34-event subset's 15m
contrast stays positive under single-session omissions; this is a reported
sensitivity result, not an independently validated edge. That subset result
was reviewed in preserved reports, not freshly recomputed for this release.

Experiment D's raw single-session deletion means range from
-0.968956 to -0.228391 at 5m, and
-0.049541 to 0.570623 at 15m. Omitting
2025-11-20 produces the negative 15m endpoint,
so its small positive full-cohort 15m mean does not survive every omission.
These are raw outcome-only deletions with no baseline donors.

Overlap-origin counts at 5m/15m are January 51/86 of 87, Phase 2 144/245 of
254, and Experiment D 433/760 of 770. These are counts of affected origins,
not counts of independent windows or event pairs.

## Status qualifications

The January validation audit supports a reproducible exploratory Python pilot.
Phase 2's preserved review addendum reports PASS for arithmetic/file integrity;
it corrects overstated selection-order proof and a figure whisker caption.
Neither correction changes results. No figures from that package are included
here. Its manual editorial final metadata step limits byte-identical rebuilding.

Experiment D is recorded as completed for independent review, not independently
reviewed. This release's read-only arithmetic check adds a bounded verification
record; it does not establish detector correctness, independent market provenance
or prospective validity. Source reports contain archived software test results;
the test suites were not rerun for this documentation release.

Experiment C v2 corrects one session sign-count classification in a category/
omission scenario, not raw outcomes or means. Its numerical-zero rule is a
floating-point classification policy, not statistical significance. Use v2 when
interpreting those private summaries.

No new signals, research experiments, statistical tests, production operations,
Git commits, remote repositories or public URLs were created in preparation.
