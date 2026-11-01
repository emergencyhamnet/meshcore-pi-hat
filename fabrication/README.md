# Fabrication Files

`LORA-PI_HAT-V1.zip` is the original package submitted to the fabrication supplier.
The project owner reports that it produced working boards. Its BOM covers supplier
assembly only: the E22 module and connectors are omitted and must be supplied separately.

The three fuses had incorrect footprints for automated assembly. The owner authorised
hand-soldering those fuses, and the boards were completed using that workaround.

The PCB source in `design/` includes revised fuse pads. That layout has not been tested
at fabrication and is not the same revision as the original ZIP. Do not assume the
updated sources and original Gerbers are interchangeable.

See [the release record](../RELEASE.md) for package contents, checksum and known issues.
