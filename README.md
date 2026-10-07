# DAC-12 Data Lab

The DAC-12 Data Lab is the controlled dataset repository for the
DAC-12 — Data Analyst Convenience Series.

It provides realistic, deliberately imperfect datasets used to:

- Develop DAC-12 tools
- Test data-cleaning algorithms
- Validate expected results
- Benchmark performance
- Reproduce bugs
- Simulate real-world analyst workflows

## Repository Structure

```text
datasets/
├── raw/          # Original and intentionally messy datasets
├── expected/     # Expected results for test datasets
└── generated/    # Programmatically generated datasets

schemas/          # Dataset schemas and structural definitions
scenarios/        # Real-world data problems and test scenarios
benchmarks/       # Performance and accuracy benchmarks
documentation/    # Dataset documentation
