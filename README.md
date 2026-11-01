# MeshCore Raspberry Pi HAT

Non-commercial shared hardware design and manufacturing files for the custom Raspberry Pi HAT using the
Ebyte E22-900M33S radio module. Software is maintained separately in
[meshcore-pi-port](https://github.com/emergencyhamnet/meshcore-pi-port).

## Hardware v1.0

[Hardware v1.0 release record](RELEASE.md) describes the original fabrication package
and the later PCB source revision. The original package produced working boards with
hand-soldered fuses; the revised fuse-pad layout has not been fabrication-tested.
Read the known issues before ordering or assembling boards.

## Design Files

- [KiCad project](design/Lora_pi_Hat.kicad_pro), [schematic](design/Lora_pi_Hat.kicad_sch)
	and [PCB](design/Lora_pi_Hat.kicad_pcb). The PCB file reports KiCad generator version 10.0.
- [Schematic PDF](design/circuit.pdf).
- [Hardware specification, Issue 1.0](design/MeshCore_Pi_HAT_Hardware_Spec_Issue_1_0.rtf).
- [Updated assembly BOM](design/updated-Lora_pi_Hat.csv); not a complete procurement list.
- [Original fab-submitted package](fabrication/LORA-PI_HAT-V1.zip), preserved unchanged.

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
