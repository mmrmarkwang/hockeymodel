# Corrected prototype v02

This revision preserves the original GLB and all earlier working models.

## Knee correction

- Knee rest pivots moved from Y=-0.025 m to Y=+0.040 m, into the leg cross section (Z=0.555 m retained).
- Leg pose construction uses an analytic forward-bending solution with minimum-swing rotations, avoiding pole-induced 180-degree thigh/shin twists.
- Replaced irregular automatic weights around each knee with a smooth thigh/shin transition blended into the surrounding weights.
- Standard linear skinning retained; no Blender-only dual-quaternion or corrective modifier is required for these results.
- Same 9,000 vertices / 18,000 triangles, 22 bones, maximum four influences. This is a rig/weight correction, NOT production retopology.

`knee-before-front.png`, `knee-after-front.png`, and corresponding side images use matching camera/lighting. The sharp front collapse is reduced; remaining faceting, rear-knee compression, shorts hems and other body deformation still need production cleanup.

`base-body-prototype.blend` and `.fbx` contain bind, squat, side-extension and arm-reach QA actions. `fbx-validation.json` records successful structural and all-bone pose round-trip checks. Unity and device tests remain pending.

## Grip correction

Approved visual reference: `design/characters/player-v02/approved/left-shot-grip-approved.png` from the repository root.

`stance/hockey-grip-v02.blend` is a separate actual 3D blockout revision. It uses opposing palm normals: right/top hand displays the padded back; left/lower hand displays tan palm leather. Palms are shorter, wrist locations and elbow directions are solved without bone stretching. The shaft is held diagonally across the body for comparison with the approved pose; this is not an on-ice puck-control stance.

Gloves remain simplified rigid modules; this does not add an articulated finger skeleton. Bare hands are reversibly masked, and the stick follows the right hand. Lower-hand sliding/contact during animation, detailed glove anatomy, wrist/forearm skin refinement and production equipment assets remain pending. Do not treat this static blockout as a finished animation or as user-approved 3D geometry.
