# Verification evidence

Archive inspected on **2026-11-06**, source snapshot `75963177ec0f0c61e0228ac96c2e310348e330b0`. No EDA verification was rerun.

| Evidence | Observation | Limit |
|---|---|---|
| Controller geometry report, dated 2026-05-05 | Reports no DRC violations | Innovus geometry check; not proof of full foundry signoff or LVS |
| CPU geometry report, dated 2026-05-06 | Reports no DRC violations | Exact saved-state association still needs confirmation |
| Timing-loop report | Contains a timing-loop warning and cut timing arc | Requires investigation before timing claims |
| Native schematic/layout views | Files present across core hierarchy | Binary contents were not semantically decoded or verified |
| Integration screenshot | Repeated layout and connections visible | Visual evidence only; no correctness certificate |
| Course test infrastructure | Reference benches, monitors, and program inputs present | Infrastructure is not a passing student test result |

Some reports are located under the course release tree, which also contains apparent run outputs. Directory location does not resolve authorship or whether the files are staff examples versus student-generated outputs. Treat the report observations as provisional until provenance is confirmed.

## Required verification record

For each approved claim, record the design revision, tool/version, command or check configuration, timestamp, test/check name, expected result, actual result, and artifact hash. Keep sensitive run paths and licensed decks outside this repository.

- DRC and LVS for cells, register file, ALU, and final datapath.
- Instruction tests and coverage, with shift-extension results separated.
- Controller/datapath interface and reset checks.
- Investigation of timing loops, constraints, and any intentionally cut arcs.
- Timing, area, or power results only with method, corners, constraints, and source reports.

No missing result is represented as a pass. No simulation of a conceptual model would substitute for checking the actual custom design.
