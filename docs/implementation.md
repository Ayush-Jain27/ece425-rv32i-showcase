# Implementation breakdown

## Custom cells

The custom-cell library contains views for logic gates, muxes, a latch, a flip-flop, and transmission gates. Schematic, layout, symbol, and abstract views appear in the archive. The presence of these views supports a hierarchical custom-design workflow; individual authorship and correctness are pending confirmation.

## Datapath hierarchy

The saved datapath library includes arithmetic, comparison, storage, multiplexing, and shift-related cells. Base and shift-extension top levels are separate. This organization is consistent with the course's bit-sliced target. No native OpenAccess database is copied here, and no claim is made that the database was opened or checked during this portfolio preparation.

## Physical integration

The archive includes controller and two CPU project saves, Tcl scripts, Liberty/LEF exchange files, and screenshots. The course distinguishes a standard-cell CPU flow from a register-file-macro flow. File names align with those deliverables; that correspondence alone does not verify macro use or final correctness.

The integration screenshot was visually reviewed and shows a large repeated datapath region connected to an upper logic region in Virtuoso. It is withheld pending course, contributor, and image-sharing review. Native files and tool interface screenshots are not assumed to be prohibited simply because Cadence produced them; their actual provenance and applicable terms must be checked.

## Engineering evidence still needed

Confirm the author's exact contributions, final database revision, DRC/LVS results, executed tests, and any measured timing/area/power results before converting this draft into a first-person accomplishment narrative.
