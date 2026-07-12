# 12-inch rack conversions

Generated from the original `10-inch/` models for the rack shown in `context/`.

- Target front width: `277.4 mm`
- Usable internal width: `255 mm`
- Original model width: `254.0 mm`
- Added width: `11.7 mm` per side
- Center-to-center rack hole spacing: `268 mm`
- Height: `44.45 mm` / `1U`
- Method: moved the outer rack-ear geometry outward and kept the central device pocket unchanged.

Files:

- `TL-SG108E-V5-12-INCH-RACK-MOUNT.3mf`
- `Tiny-Rack-Mount-no-Keystone-12-inch-light-v2.3mf`
- `m920q-12-INCH-RACK-MOUNT.3mf` — converted from `10-inch/m720q_rack.3mf` ("m920q rack v8"); only the flat rack ear panel is extended (the front face with M5 mounting slots), the device bracket arms are unchanged. Bambu project format, white eSUN PETG profile, face-down print orientation. Panel width **277.4 mm**, M5 slot outer edge C-C **268.0 mm** exactly.

For the ThinkCentre Tiny mount, this effectively thickens/extends the two side support sections while leaving the M720q cradle dimensions unchanged.

Use `Tiny-Rack-Mount-no-Keystone-12-inch-light-v2.3mf` for Bambu Studio. This version uses slicer-friendly axes: width on X, depth on Y, and the 1U height on Z.

`light-v2` keeps the same `277.4 mm` outside width but reduces how much of the ThinkCentre side-holder mass is moved outward. Its solid mesh volume is about `386.8 cm3`, compared with about `493.9 cm3` for the first 12-inch conversion and `301.6 cm3` for the original 10-inch model.

`TL-SG108E-V5-12-INCH-RACK-MOUNT.3mf` was generated from `10-inch/TL-SG108E+V5+10i+RM.3mf`. It targets `277.4 mm` overall width, includes a white material color in the 3MF, and uses a `4.0 mm` rack/base plate thickness.
