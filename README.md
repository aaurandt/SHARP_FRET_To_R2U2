# SHARP FRET to R2U2

This repository contains the SHARP requirements in FRET, the corresponding R2U2 exports before and after MLTL rewrites, and documentation for those rewrite rules.

## Folder Layout

- `INSPECTA_SHARP_No_Rewrites/` contains the requirements and exports before the MLTL rewrite rules are applied.
- `INSPECTA_SHARP_With_Rewrites/` contains the corresponding version with the rewrite rules applied.
- [`rewrites.pdf`](rewrites.pdf) documents the MLTL rewrite rules used by FRET.

Each folder has a `fretRequirementsVariables.json` file containing the FRET requirements and variable mappings. It also has a subfolder for each SHARP component: `RX_Firewall`, `TX_Firewall`, `MAVLink_Firewall`, `Flight_Safety_Monitor`, and `Mode_Manager`. Each component folder is the R2U2 export such that it contains a C2PO specification (`.c2po`), an example CSV trace header (`.csv`), and a signal mapping file (`.map`).

## MLTL Rewrite Rules

The [rewrite rule reference](rewrites.pdf) lists 160 rules implemented in FRET to reduce the resources required by exported R2U2 monitors. It groups the rules into Boolean, next operator, temporal operator and interval, when in/not in scope, and EqSat-derived rewrites. The two export folders show the SHARP requirements before and after these rules are applied.

## FRET Import and Export

To open a version in FRET, use FRET's project import button (down arrow) and select that version's `fretRequirementsVariables.json`. To regenerate the R2U2 files, review the component's Variable Mapping in the Analysis Portal, select R2U2 as the export language, and export the component.
