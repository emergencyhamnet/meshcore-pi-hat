# MeshCore Raspberry Pi HAT

Non-commercial shared hardware design and manufacturing files for the custom Raspberry Pi HAT using the
Ebyte E22-900M33S radio module. Software is maintained separately in
[meshcore-pi-port](https://github.com/emergencyhamnet/meshcore-pi-port).

## Repository Status

This is a repository scaffold. Design files, board photographs, CAD tool/version,
board revision, and fabrication history have not yet been added or verified here.
Do not fabricate from this scaffold. No hardware release has been published.

## Add Your Files

| Directory | Contents |
|---|---|
| `design/` | Editable schematic/PCB project, required symbols, footprints and libraries |
| `docs/` | Schematic PDF, pinout, electrical limits and assembly/test instructions |
| `bom/` | Bill of materials with quantities and manufacturer part numbers |
| `fabrication/` | Exact fab-submitted ZIP, Gerbers, drill files and placement files |
| `mechanical/` | STEP models, board outlines and enclosure drawings |
| `images/` | Board photographs and renders |

Keep the original fabrication package unchanged. Do not mix its files with regenerated
outputs from a newer design. Preserve the supplier BOM as submitted; the CSV template in
`bom/` is optional and contains no actual parts.

## Before Publishing

Follow [the build and release checklist](docs/BUILD_AND_RELEASE.md). Record the CAD software
and version, fitted PCB revision, tested assembly options and any known discrepancies.
Review [the licence scope and fabrication permission](LICENSING.md) before adding files.
Do not assume third-party footprints, models or datasheets can be redistributed.

## Licence

Original project hardware design files, documentation and images use
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/): attribution,
non-commercial use and ShareAlike. This is non-commercial shared hardware, not
open-source hardware. [LICENSING.md](LICENSING.md) includes a separate permission to
pay a fabrication service for your own non-commercial builds. Commercial uses outside
those permissions require separate agreement. Third-party assets and software retain
their own licences.

## Software Compatibility

The Pi software's `v0.2.0-alpha5` release includes physical TXEN/RXEN GPIO control and
settings-save corrections for the tested E22 HAT. This does not certify all assemblies or
PCB revisions. Record the exact board and software revisions used for each hardware test.
The software TX-power setting represents requested SX1262 chip output, not final antenna
power; module-specific drive limits and RF compliance require verification.

## Electrical Safety

Disconnect all Pi, HAT and UPS power before fitting or removing the board. Verify supply
voltage, polarity, current capacity, GPIO logic levels and the fitted radio's specifications.
Use an appropriate antenna or RF load before transmitting. Analyzer connections require
suitable attenuation and power ratings. Observe applicable RF rules.