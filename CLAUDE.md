# 12-inch-rack

This project is for modifying community-made 10-inch rack mount models so they fit the user's 12-inch rack.

## Context

The user bought a 12-inch desktop rack. Existing available models for the TP-Link SG108E switch and Lenovo ThinkCentre Tiny M720q are 10-inch rack models, so they are too narrow for this rack.

Reference images and seller screenshots live in `context/`. Original community files live in `10-inch/`. Adapted files should be written to `12-inch/`.

## Target Dimensions

Use these 12-inch rack dimensions:

- Overall front panel width: `277.4 mm`
- Usable internal width: `255 mm`
- Height: `44.45 mm` / `1U`
- Center-to-center hole spacing: `268 mm`

The original 10-inch models are approximately `254 mm` wide. The adaptation used here adds `11.7 mm` to each side, producing `277.4 mm` overall width.

## Modeling Approach

Preserve the device fit. Do not scale the whole model.

Instead, extend the left and right rack-ear regions outward so the panel fits the 12-inch rack. Keep the central switch/ThinkCentre pocket unchanged.

For the ThinkCentre Tiny model, this means widening the two side support areas that hold the computer, not changing the computer cradle dimensions.

## Existing Generated Models

- `12-inch/TL-SG108E-V5-12-INCH-RACK-MOUNT.3mf`
- `12-inch/Tiny-Rack-Mount-no-Keystone-12-inch-light-v2.3mf`

These outputs target `277.4 mm` overall front width and preserve the original device geometry. Use the Bambu-oriented ThinkCentre 3MF for slicing when possible.

## PETG Print Profile

Recommended Bambu X1 Carbon PETG baseline:

- Filament: PETG / Generic PETG, mapped to the real AMS slot before printing.
- Nozzle: `250 C` for the initial layer, then `245 C` for other layers.
- Textured PEI bed: `75 C`.
- Layer height: `0.20 mm`.
- Walls: `4` for SG108E, `6` for the ThinkCentre Tiny mount.
- Sparse infill: `20% gyroid` for SG108E, `35% gyroid` for the ThinkCentre Tiny mount.
- Top shell layers: `5`.
- Top surface speed: `80 mm/s`.
- Outer wall speed: `100 mm/s`.
- Initial layer speed: `30 mm/s`; initial layer infill speed: `60 mm/s`.
- Inner wall speed: `160 mm/s`; sparse infill speed: `180 mm/s`; internal solid infill speed: `160 mm/s`.
- Brim: auto brim with `0.2 mm` brim-object gap. Use `5 mm` brim for SG108E and `10 mm` brim for the taller ThinkCentre mount.
- Support: off for the SG108E flat print. Use tree support for the ThinkCentre upright/compromise print.
- Keep flow calibration enabled when sending the print.

If the PETG surface is rough or stringy, dry the spool at `55-60 C` for `4-6 hours` before printing.
