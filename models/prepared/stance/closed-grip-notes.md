# Closed hockey grip blockout

Open `hockey-closed-grip.blend`. This separate revision preserves the earlier stance scene and base-body files.

- Two independent glove objects, each with four curled fingers, an opposing thumb, palm and cuff.
- Gloves rigidly skinned to the existing Hand.L / Hand.R bones.
- Original open hands hidden by a reversible body mask; the original mesh is preserved.
- Stick repositioned closer to the body; both wrist IK targets reached without bone stretching. See `grip-report.json` for measured errors.
- Stick attached to the upper hand. The lower hand is posed for this static stance only.
- Perspective, top-down and close-up PNGs show the actual Blender scene.

This is a geometric glove-grip prototype, not a new articulated bare-hand rig. Finger segments are not separately animated. Animated two-hand contact, wrist deformation cleanup, detailed glove design and Unity export remain pending. The prior base-body FBX has not been overwritten with this equipment scene.
