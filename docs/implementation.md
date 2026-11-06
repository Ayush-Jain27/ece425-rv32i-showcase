# Implementation

## Custom-cell foundation

The project starts with transistor-level logic, multiplexing, and storage cells. The retained library contains schematic, layout, symbol, and abstract views. These cells form the building blocks for the higher-level datapath.

The useful design discipline here is consistency: a cell must have a logical interface that can be composed and a physical interface that can be connected. A finished-looking view alone is not evidence of correctness; the corresponding checks belong in the verification record.

## Hierarchical datapath

The design hierarchy includes an ALU, adder, comparator, register file, registers, and multi-input multiplexers. A bit slice groups the logic needed for one position in a wider datapath. Repeating the slice keeps the structure regular while making the inter-slice carry, comparison, and control connections explicit design concerns.

The base datapath and shift extension have separate saved hierarchies. The extension includes shifter-related cells; its existence is distinct from demonstrated instruction-test coverage.

## Physical integration

The retained deliverables include controller and CPU project saves, physical-design scripts, and Liberty/LEF exchange files. The course flow explores both a standard-cell implementation and an implementation using a register-file macro.

Liberty describes timing behavior for synthesis and timing analysis. LEF describes the physical abstraction needed for placement and routing. These interfaces connect the custom-design work to the automated flow without requiring the tools to treat each macro as transistor-level geometry.

The integration screenshot was inspected during documentation preparation. It shows a repeated datapath region connected to an upper logic region. Design images cannot be shared, so this repository uses conceptual illustrations rather than that screenshot.

## Evidence boundary

The student implementation is Ayush Jain's individual work; the controller and reference architecture originate in course material. Native design databases were inventoried but not opened or reverified during documentation preparation. The [verification record](verification.md) separates available artifacts from confirmed results.
