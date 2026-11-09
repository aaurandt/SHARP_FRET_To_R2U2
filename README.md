# SHARP FRET to R2U2

This repository contains the SHARP requirements in FRET and the corresponding exports for R2U2.

## Folder Layout

- `INSPECTA_SHARP_No_Rewrites/` contains the requirements and exports before the MLTL rewrite rules are applied.
- `INSPECTA_SHARP_With_Rewrites/` contains the corresponding version with the rewrite rules applied.

Each folder has a `fretRequirementsVariables.json` file containing the FRET requirements and variable mappings. It also has a subfolder for each SHARP component: `RX_Firewall`, `TX_Firewall`, `MAVLink_Firewall`, `Flight_Safety_Monitor`, and `Mode_Manager`. Each component folder is the R2U2 export such that it contains a C2PO specification (`.c2po`), an example CSV trace header (`.csv`), and a signal mapping file (`.map`).

## FRET Import and Export

To open a version in FRET, use FRET's project import button (down arrow) and select that version's `fretRequirementsVariables.json`. To regenerate the R2U2 files, review the component's Variable Mapping in the Analysis Portal, select R2U2 as the export language, and export the component.