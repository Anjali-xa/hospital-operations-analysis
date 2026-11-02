# Hospital Operations KPI Framework

## Purpose
This framework defines a consistent starting point for analysing hospital capacity, patient flow, and service efficiency. Populate metrics only after confirming the dataset's field definitions and reporting period.

## Core KPIs
| KPI | Suggested definition | Validation |
|---|---|---|
| Admissions | Count of distinct admission IDs | Check duplicate IDs and cancelled records |
| Average length of stay | Total inpatient days / completed discharges | Exclude ongoing stays or report separately |
| Bed occupancy rate | Occupied bed-days / available bed-days | Confirm staffed-bed capacity and date grain |
| Readmission rate | Eligible readmissions / eligible discharges | State the readmission window and exclusions |
| Average waiting time | Total waiting minutes / completed visits | Check negative values and unit consistency |

## Data-quality checklist
- Confirm patient and encounter identifiers are de-identified.
- Standardise admission, discharge, and visit timestamps.
- Flag discharge dates earlier than admission dates.
- Distinguish missing values from zero counts.
- Check whether transfers create multiple encounter rows.
- Document exclusions and denominator choices.

## Analysis questions
1. How does patient volume vary by day, month, and department?
2. Which departments show the longest waiting times?
3. How does occupancy vary against available staffed beds?
4. Are length-of-stay patterns different by admission type?

## Reporting notes
Show numerator, denominator, period, and exclusions alongside each rate. Do not infer clinical quality or causation from operational measures alone.