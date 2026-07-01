# 12-inch-rack Project Context

This workspace adapts community-made 10-inch rack mount models so they fit the user's 12-inch desktop rack.

## Goal

Convert existing 10-inch rack mount models, eg:

- TP-Link TL-SG108E / SG108E switch
- Lenovo ThinkCentre Tiny M720q

The adapted models should fit the user's 12-inch rack while preserving the device-specific cradle/pocket geometry from the original community models.

## Important Rack Dimensions

Use these target rack dimensions unless the user provides updated measurements:

- Overall front panel width: `277.4 mm`
- Usable internal width: `255 mm`
- Height: `44.45 mm` / `1U`
- Center-to-center mounting hole spacing: `268 mm`

The original 10-inch models measured about `254 mm` wide. The current conversion target adds `23.4 mm` total width, or `11.7 mm` per side.

## Directory Layout

- `10-inch/`: original community 10-inch rack mount source models.
- `12-inch/`: generated 12-inch adaptations.
- `context/`: reference photos and screenshots of the user's rack and seller-provided dimensions.

## Editing Guidance

Prefer preserving the central device geometry and extending only the rack-ear/side-support geometry outward.

Do not uniformly scale the models. Uniform scaling would distort the switch or ThinkCentre fit.

For models like the ThinkCentre Tiny mount, widening should effectively thicken/extend the two side supports while leaving the M720q cradle unchanged.

For rack fit, prioritize:

1. `277.4 mm` overall front width.
2. `268 mm` center-to-center mounting hole spacing.
3. `44.45 mm` 1U height.
4. Device pocket dimensions from the original model.

## Current Outputs

The current generated files are:

- `12-inch/TL-SG108E-V5-12-INCH-RACK-MOUNT.3mf`
- `12-inch/Tiny-Rack-Mount-no-Keystone-12-inch-light-v2.3mf`

The ThinkCentre `light-v2` files keep the same `277.4 mm` outside width while reducing how much side-holder mass is moved outward. The Bambu-oriented file uses slicer-friendly axes: width on X, depth on Y, and 1U height on Z.

The SG108E V5 white output was generated from `10-inch/TL-SG108E+V5+10i+RM.3mf`.

## PETG Print Profile

Baseline Bambu X1 Carbon PETG settings for these rack mounts:

- Filament: PETG / Generic PETG, mapped to the actual AMS slot before printing.
- Nozzle: `250 C` initial layer, `245 C` other layers.
- Textured PEI bed: `75 C` initial layer and other layers.
- Layer height: `0.20 mm`.
- Walls: `4` for SG108E, `6` for the taller ThinkCentre Tiny mount.
- Sparse infill: `20% gyroid` for SG108E, `35% gyroid` for the ThinkCentre Tiny mount.
- Top shell layers: `5`.
- Top surface speed: `80 mm/s`.
- Outer wall speed: `100 mm/s`.
- Initial layer speed: `30 mm/s`; initial layer infill speed: `60 mm/s`.
- Inner wall speed: `160 mm/s`; sparse infill speed: `180 mm/s`; internal solid infill speed: `160 mm/s`.
- Brim: auto brim, `5 mm` width and `0.2 mm` brim-object gap for SG108E; `10 mm` brim for the taller ThinkCentre mount.
- Support: off for the SG108E flat orientation. Use tree support for the ThinkCentre upright/compromise orientation.
- Flow calibration: keep enabled when sending the print.

If PETG is stringy or rough, dry the spool at `55-60 C` for `4-6 hours`. Avoid using PLA as PETG support material unless it is only a dedicated interface and the slicer purge strategy is understood.
