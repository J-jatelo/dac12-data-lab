# DAC-12 Cleaning Rules

## Philosophy

DAC-12 follows the principle:

> Detect aggressively. Correct conservatively.

The system should identify as many potential data-quality problems as possible,
while avoiding automatic changes when the correct interpretation is uncertain.

---

## Category A — Automatic Corrections

DAC-12 may automatically perform corrections when the intended result is
unambiguous.

### Whitespace

Example:

`" John Doe "` → `"John Doe"`

### Duplicate Records

Exact duplicate records may be removed.

### Standardized Categories

Known categorical values may be normalized.

Example:

`Kenya`, `kenya`, `KENYA` → `Kenya`

### Empty Strings

Whitespace-only values should be interpreted as missing values.

---

## Category B — Detect and Recommend

DAC-12 should identify these problems but require review before changing them.

Examples:

- Missing values
- `N/A` values
- Invalid email formats
- Mixed date formats
- Mixed data types
- Unknown categorical values
- Text inside numeric columns

DAC-12 should provide a recommended action without silently applying it.

---

## Category C — Manual Review

DAC-12 must not automatically modify potentially meaningful values.

Examples:

- Negative salaries
- Impossible or unusual ages
- Extreme numerical values
- Potentially valid outliers
- Ambiguous category mappings

These should be reported to the analyst for review.

---

## Core Principle

DAC-12 should prioritize data integrity over aggressive cleaning.

A detected anomaly does not automatically mean the value is wrong.
