# Base body rigging prototype

The original Meshy download is preserved unchanged in `../base-body-v01.glb`.

## Deliverables

- `base-body-prototype.blend`: editable working mesh, 22-bone skeleton, skin weights, and four static pose-check actions. This is the primary working asset.
- `base-body-prototype.fbx`: candidate interchange export. Structural and all-bone pose reimport checks passed. Unity validation is still pending.
- Four PNGs: rendered bind pose, squat, sideways leg extension and arm reach.
- `preparation-report.json`: geometry and rig statistics.
- `fbx-validation.json`: export reimport checks and original-file checksum.

The working mesh has 9,000 vertices and 18,000 triangles, with up to four weights per vertex and no unweighted vertices. After welding and reduction it has one connected component, no boundary edges and no nonmanifold edges.

## Visual assessment and limitations

The Blender renders show bending knees, a sideways leg extension and arm reach. Shorts hems and hip deformation need cleanup. The mesh is a triangle-decimated prototype, not production joint-loop retopology. Shorts remain fused to the body; there is no complete underlying body beneath them for arbitrary clothing swaps. Fingers are not independently rigged. No UVs or texture bake are provided.

The four clips are held QA poses, not skating, puck handling or shooting animations. The squat and extension test range of motion; they are not approved hockey technique or balance.

FBX reimport preserved the mesh, 22 bones, weights and four actions. The earlier hip translation problem is resolved: pose displacement now lives on Root, so connected hips created during import cannot suppress it. All 22 bone positions and rotations were compared for all four clips; maximum position error was below 0.000004 m, with no measured quaternion angle difference. No Unity or mobile-device performance validation has been performed.

A separate `stance/hockey-stance-blockout.blend` adds two independently skinned skate blockouts, a separate stick and puck, a held crouched reach pose, and perspective/top-down previews. The stance uses a reversible body mask to hide feet beneath the equipped skates. These are size and silhouette placeholders. Fingers remain open, grip contact is not validated, and this is not a skating animation.

## Next production steps

1. Refine hips, knees and shoulders with animation-friendly topology and weight painting; repair shorts hems and decide on clothing/body masking.
2. Add finger control sufficient for a stable two-hand stick grip.
3. Refine the separate skate/stick blockouts; establish blade-ground and hand-stick contact.
4. Validate the FBX skeleton and clips in Unity.
5. Author a short skating loop, then puck handling and wrist shot; inspect all at the actual top-down gameplay camera.
6. Add independently replaceable equipment bound to the shared skeleton, UVs, textures and measured mobile LODs.
