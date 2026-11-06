# Public-release review — not cleared

Keep this repository private until each applicable item has dated evidence and Ayush approves the exact release commit.

| Review | Status | Evidence needed |
|---|---|---|
| Course permission | OPEN | Spring 2026 policy or instructor permission covering the actual summary, diagrams, and any later code/images |
| Collaboration | OPEN | Individual contribution map and permission for any shared work |
| Technology provenance | OPEN | Exact PDK/model/library versions and their actual license files |
| EDA output sharing | OPEN | Applicable institutional/vendor terms for any screenshots or native outputs proposed for release |
| Technical claims | OPEN | Final revision and attributable simulation, LVS/DRC, and timing evidence |
| Sanitization | PARTIAL | Clean documentation-only history; recheck complete history and attachments before release |
| User release approval | OPEN | Approval of the final audited commit |

## Current inclusion decision

New prose and high-level conceptual diagrams are staged privately for review. All 958 tracked source files are withheld from this showcase, including instructional assets, HDL/test infrastructure, native databases, Liberty/LEF, environment configuration, screenshots, and raw reports. This conservative decision is not a claim that every source file is legally restricted.

The initial audit inventoried and hashed every tracked file, screened textual content, inspected selected documentation/reports, and visually reviewed the integration screenshot. Binary databases were not semantically audited; the shallow source checkout does not establish full historical provenance. The detailed file manifest remains local and is not included in this repository.

## Policy references checked 2026-11-06

- [UIUC ECE academic integrity guidance](https://ece.illinois.edu/academics/ugrad/advising-tips/academic-honesty): instructor-specific rules matter. This is not explicit ECE 425 publication permission.
- [UIUC Grainger academic integrity](https://grainger.illinois.edu/academics/online/current-students/academic-integrity): general academic-integrity context; not a course-specific release grant.
- [NC State FreePDK45](https://eda.ncsu.edu/freepdk/freepdk45/): upstream describes Apache licensing, with historical license changes. Verify the exact installed distribution and included components before redistribution.

The Spring 2026 course webpage could not be retrieved during this review. No course-specific publication authorization or applicable Cadence agreement was found in the inspected materials. No third-party license conclusion is inferred from file extensions or product names.
