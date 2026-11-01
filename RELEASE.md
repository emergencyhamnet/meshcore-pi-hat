# Hardware v1.0 - MeshCore Raspberry Pi HAT

Release tag: `hardware-v1.0`. Publication date: 2026-11-01.
Issue 1.0 fabrication package with a later, unverified fuse-pad source revision.

## Included Files

- Editable KiCad project, schematic and PCB under `design/`.
- Schematic PDF and the original Issue 1.0 hardware specification.
- Updated supplier-assembly BOM; module and connectors require separate provisioning.
- Original `fabrication/LORA-PI_HAT-V1.zip`, attached to this release unchanged.

The ZIP contains four copper-layer Gerbers, front/back mask, paste and silkscreen
Gerbers, board outline, plated/non-plated drill files, a Gerber job file and
`Final-Parts_list-Lora_pi_Hat.csv`. No pick-and-place position file was found in this
ZIP. Confirm any additional assembly information required by your supplier.

Original fabrication ZIP SHA-256:

```text
21a498d4de875e38e6807e7811565f76d953818853760e1482d7fb8e9389a636
```

## Revision Status And Known Issues

1. The owner reports working boards made from the original fabrication package. The
   three fuses had unsuitable footprints for automated placement and were hand-soldered
   with the owner's approval. This workaround must not be overlooked when reordering.
2. The current editable PCB source has revised fuse pads, but has not been tested at
   fabrication. It does not reproduce the original package's revision. Review the pads
   and regenerate a matching set of manufacturing files before using that revision.
3. The updated BOM identifies U1 as E22-900M30S, while the tested Pi HAT/software path
   uses E22-900M33S. Confirm the intended module and footprint before procurement. The
   module and connectors are excluded from supplier assembly; the BOM is not complete.
4. The updated BOM groups F1/F2/F3 with quantity 1. Confirm three fitted fuses and the
   intended supplier quantity before ordering; the supplied CSV has not been altered.
5. The original hardware spec is historical, not proof of every fitted component or
   current electrical value. Confirm the fitted board and later documented corrections
   against the current schematic, BOM and actual assembly.

## Software And Validation

Use [MeshCore Pi port alpha5](https://github.com/emergencyhamnet/meshcore-pi-port/releases/tag/v0.2.0-alpha5)
or later for the E22 GPIO and settings-save corrections. Software TX power is requested
SX1262 drive, not final antenna power; module-specific limits and local RF rules apply.

The PCB file reports KiCad generator version 10.0. Independent CAD opening, library
availability, ERC/DRC, Gerber-to-source comparison and full electrical certification
were not performed for this publication. This is a documented hardware source release,
not an assertion that the revised source is production-qualified.

## Licence

Original project design files and documentation use CC BY-NC-SA 4.0. See `LICENSE` and
`LICENSING.md` for scope, third-party exclusions and the separate permission for paid
fabrication of non-commercial builds. Review third-party rights before redistribution.