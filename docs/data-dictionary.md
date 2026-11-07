# Cohort summary columns

Each row represents one of three separate cohorts at one horizon; it is not a
new sample. The same events appear at 5m and 15m.

| Column | Meaning |
| --- | --- |
| cohort | Separate historical sample identifier |
| selected_sessions | Passing selected sessions, not candidate count |
| events | Included historical event count |
| horizon_minutes | 5 or 15 minutes after the reference close |
| complete_outcomes | Existing outcomes with full intervening candle coverage |
| mean_signed_points | Event-weighted raw signed change, preserved decimal value |
| median_signed_points | Median of raw signed outcomes |
| sample_sd_signed_points | Sample SD using n-1; descriptive dispersion |
| sum_signed_points | Sum of existing signed outcomes; supports aggregate checks |
| overlapping_event_origins | Origins with another same-session origin strictly less than the horizon away |
| instrument_status | UNVERIFIED_NQ_CACHE; points are provisionally NQ-labeled |
| source_id | Source register identifier for the reviewed summary |

No baseline contrast or live observation is present in this CSV. Monetary
returns, trade fills, P&L, significance estimates and confidence intervals are
not represented by these columns.
