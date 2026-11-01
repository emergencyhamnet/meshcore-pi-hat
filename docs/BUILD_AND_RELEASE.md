# Hardware Build And Release Record

Complete this record after adding the original project files. Entries below are pending,
not established specifications or manufacturing instructions.

## Design Identity

| Field | Value |
|---|---|
| PCB name and silkscreen revision | Pending |
| CAD tool and exact version | Pending |
| Native project entry file | Pending |
| Fabricated revision and date | Pending |
| Assembly options / unpopulated parts | Pending |
| Supported Pi models | Pending verification |
| Tested software release | Pending |
| Original fabrication package filename | Pending |
| Fabrication package SHA-256 | Pending |

## Design Review

- [ ] Native schematic and PCB files open with the documented CAD version.
- [ ] Symbols, footprints, models and library dependencies are available with their own licence notices.
- [ ] Schematic PDF matches the native design revision.
- [ ] BOM and placement files match the exact fabricated assembly.
- [ ] Connector pin numbering, orientation and board revision are documented.
- [ ] Supply ratings, radio drive limits and GPIO voltage levels are verified.
- [ ] Unresolved ERC/DRC results and assembly deviations are documented.
- [ ] Datasheets are linked where redistribution permission is unavailable.

## Validation

Record the actual board revision, equipment, measurement setup and results. Separate
operator observations from calibrated/certified claims. Include power-up checks, supply
behaviour, TXEN/RXEN operation, receive/transmit checks and fitted sensors where applicable.
Do not copy software test results as proof of every PCB's electrical behaviour.

## Publish A Fabrication Release

1. Remove private order/account details and files without redistribution permission.
2. Verify the CC BY-NC-SA 4.0 scope, fabrication permission and third-party exclusions.
3. Preserve the original fab-submitted package byte-for-byte and record its SHA-256.
4. Keep new exports in a separate, clearly identified revision rather than replacing originals.
5. Commit the matching editable sources, BOM, documentation and images.
6. Tag the reviewed hardware revision, for example `hardware-v1.0`, only if that matches
   the actual revision being released.
7. Attach the exact fabrication ZIP to the GitHub release and state whether it was built
   and tested, along with known issues and compatible software revisions.

In Windows PowerShell, obtain a package checksum with:

```powershell
Get-FileHash -Algorithm SHA256 "path-to-original-fabrication-package.zip"
```

Keep backups and source/export history. A GitHub release is not a substitute for checking
the fitted PCB revision and assembly options before ordering or powering a board.