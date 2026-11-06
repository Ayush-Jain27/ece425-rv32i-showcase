# Implementation breakdown

## Custom cells

The custom-cell library contains views for logic gates, muxes, a latch, a flip-flop, and transmission gates. Schematic, layout, symbol, and abstract views appear in the archive. Ayush confirms sole authorship of the student implementation; correctness remains subject to verification evidence.

## Datapath hierarchy

The saved datapath library includes arithmetic, comparison, storage, multiplexing, and shift-related cells. Base and shift-extension top levels are separate. This organization is consistent with the course's bit-sliced target. No native OpenAccess database is copied here, and no claim is made that the database was opened or checked during this portfolio preparation.

## Physical integration

The archive includes controller and two CPU project saves, Tcl scripts, Liberty/LEF exchange files, and screenshots. The course distinguishes a standard-cell CPU flow from a register-file-macro flow. File names align with those deliverables; that correspondence alone does not verify macro use or final correctness.

The integration screenshot was visually reviewed and shows a large repeated datapath region connected to an upper logic region in Virtuoso. Ayush confirmed that design images cannot be shared, so it is excluded. The original conceptual diagrams in this showcase explain hierarchy without reproducing the screenshot or detailed circuitry.

## Engineering evidence still needed

Confirm the final database revision, DRC/LVS results, executed tests, and any measured timing/area/power results before making completion or performance claims. Student implementation ownership is confirmed by the author; reference-design attribution remains separate.
