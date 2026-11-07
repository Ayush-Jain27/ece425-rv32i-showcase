# RISC-V Datapath

**Custom digital design, from transistor-level cells to processor integration.**

I designed the schematics and layouts for a bit-sliced RISC-V datapath in Cadence Virtuoso, then worked through the physical-design flow connecting custom blocks with synthesized logic.

The central challenge was hierarchy: designing one reusable slice, connecting arithmetic and comparison across slices, and keeping the physical interfaces consistent as the design grew into a complete datapath.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/design-hierarchy-dark.svg">
  <img src="assets/design-hierarchy.svg" alt="Conceptual datapath showing the register file, operand selection, ALU, memory interface, and writeback loop" width="960">
</picture>

*Selected data paths, drawn for this showcase. This is a conceptual overview, not an extracted schematic.*

## My work

- **Custom cells:** transistor-level schematic and layout work for logic, selection, and storage elements.
- **Datapath construction:** a register file, arithmetic and logic blocks, comparison logic, multiplexers, and supporting state elements organized into repeated bit slices.
- **Shift extension:** a separate hierarchy containing shifter-related cells and an extended datapath.
- **Physical integration:** controller and CPU place-and-route work, including library exchange files and a register-file macro flow.

The processor reference RTL, controller, specifications, and test infrastructure were supplied. My contribution was the individual implementation and physical-design work; the reference architecture and supplied infrastructure are not my original designs.

## Design approach

| Stage | Engineering focus |
|---|---|
| Transistors → cells | Build reusable logic and storage elements with consistent physical interfaces |
| Cells → blocks | Compose arithmetic, comparison, selection, and register-file structures |
| Blocks → datapath | Repeat a one-bit slice and connect shared control and inter-slice signals |
| Datapath → integration | Bring custom geometry and synthesized logic together through defined interfaces |

The architecture uses a 32-bit datapath with separate instruction and data memory interfaces. The diagrams in this repository explain the organization at a conceptual level; they are not extracted schematics or layout images.

## Tools and flow

**Cadence Virtuoso · Cadence Innovus · Synopsys synthesis and simulation infrastructure · Calibre checking flow · FreePDK45**

The project connects custom schematic/layout work with the standard-cell flow through Liberty timing and LEF geometry interfaces. Tool-specific databases, underlying implementation source, and design images are not distributed in this repository.

## Technical documentation

- [Architecture](docs/architecture.md): functional organization and design boundaries.
- [Implementation](docs/implementation.md): custom-cell hierarchy and physical integration.
- [Verification](docs/verification.md): available evidence, check scope, and unresolved results.
- [Reproducibility](docs/reproducibility.md): dependencies and the authorized design environment.
- [Attribution](ATTRIBUTION.md): individual work and supplied components.

## Verification status

The retained archive includes schematic/layout views, physical-design saves, and historical geometry reports. Two reports record no DRC violations; their association with the final design state still needs confirmation. A timing report also contains a loop warning. Full simulation/LVS completion and timing closure are not claimed here; the [verification notes](docs/verification.md) explain the evidence precisely.

## About this repository

This is a technical project showcase, not a distributable processor implementation. It contains original documentation and conceptual diagrams. Underlying implementation source, design screenshots, native databases, technology libraries, and licensed dependencies are excluded. See the [sharing notes](docs/release-review.md) for publication boundaries and the release review.

**Ayush Jain** · [GitHub](https://github.com/Ayush-Jain27) · [Portfolio](https://ayush-jain.dev)
