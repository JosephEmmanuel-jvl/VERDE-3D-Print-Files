# VERDE 3D Print Files

This repository contains the approved STL candidates for the VERDE thesis sensor rack, camera-visible aphid props, and an articulated cabbage-looper test prop.

## Files to print

### Sensor rack

Print **one copy of every STL** in `print/Sensor Rack/`:

1. `P01_RAIL_WITH_FOUR_DOVETAIL_SOCKETS.stl`
2. `P02_LEFT_RESERVOIR_WALL_BRACKET.stl`
3. `P03_RIGHT_RESERVOIR_WALL_BRACKET.stl`
4. `P04_LEFT_OUTSIDE_BACKING_PLATE.stl`
5. `P05_RIGHT_OUTSIDE_BACKING_PLATE.stl`
6. `P06_pH_SNUG_5_COMPLETE_CARTRIDGE.stl`
7. `P07_TDS_SNUG_3_COMPLETE_CARTRIDGE.stl`
8. `P08_WATER_TEMP_SNUG_1_COMPLETE_CARTRIDGE.stl`
9. `P09_TURBIDITY_SNUG_7_COMPLETE_CARTRIDGE.stl`

The intended installed station order is:

- pH: X = -90 mm
- Turbidity: X = -30 mm
- Water temperature (DS18B20): X = +30 mm
- EC/TDS: X = +90 mm

The pH and EC/TDS stations are separated by 180 mm. The nine files are separate printable parts so the rail, wall hardware, and sensor cartridges can be printed and replaced independently.

Recommended material: PETG for the rack parts. The mounting design uses through-bolts, large washers or backing plates, and nuts; it must not rely on screw threads biting directly into Styrofoam.

### Aphid props

Print both files once:

1. `print/Aphids/VERDE_APHIDS_WITH_LEGS_4X.stl` — contains four separate small aphid props. Each aphid is approximately 8.93 x 6.42 x 3.36 mm and includes six legs, two antennae, and two cornicles.
2. `print/Aphids/VERDE_LARGE_APHID_WITH_LEGS_PRINT_ONE.stl` — contains one detailed large aphid, approximately 82.57 x 114.99 x 117.90 mm.

Recommended small-aphid starting settings: PLA or PETG, 0.10-0.12 mm layer height, slow outer walls, and no support if the slicer preview shows all legs contacting the build plate. Use a brim if bed adhesion is weak.

For the large aphid, inspect the slicer preview carefully and use supports where required under the body, legs, and antennae. Confirm the approximately 118 mm height fits the printer before slicing.

### Cabbage-looper prop

Print one copy:

1. `print/Cabbage Looper/VERDE_CABBAGE_LOOPER_ARTICULATED_PRINT_IN_PLACE_60MM.stl`

This is a seven-section print-in-place articulated prop measuring approximately **60.0 x 9.80 x 6.74 mm**. It uses six side-to-side hinge joints with approximately 0.60 mm radial clearance.

Recommended first-print settings: PLA, 0.4 mm nozzle, 0.12-0.16 mm layer height, three walls, and the supplied flat orientation. **Disable generated supports**, and do not use a brim that bridges the moving-joint gaps. After the print has fully cooled, free each joint gently and individually.

The STL passed digital topology checks: seven closed components, zero boundary edges, and zero non-manifold edges. Actual printed movement, joint durability, and camera-detection performance still require physical testing.

## Important verification limits

- These are STL models, not G-code. The printer operator must slice them for the actual printer, nozzle, and material.
- Inspect every slicer preview for scale in millimetres, missing layers, unsupported features, and bed fit before printing.
- Holder sizes 1/3/5/7 were selected from the snug coupon set, but final fit still requires physical testing with the actual probes.
- Reservoir lid clearance, waterproofing, foam compression, fastener length, PETG strength, and final assembled load have not been physically validated.
- The aphids and cabbage looper are controlled visual test props. Detecting them does not by itself prove performance on real insects in field conditions.

## Integrity

`SHA256SUMS.txt` records the SHA-256 checksum of every included STL. No rejected or superseded models are included.

See `ATTRIBUTION.md` for the required credit for the large aphid model.
