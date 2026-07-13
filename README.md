# demo1 rolling object indoor floor 10k

Generated on remote machine 1 under allowed paths only.

Data layout:
- `archives/`: tar.gz batches of single-object rolling/sliding episodes.
- `metadata/archive_index.jsonl`: archive ranges, sizes, and checksums.
- `metadata/generation_config.json`: simulation, rendering, object, and batching settings.
- `code/`: collection script and pipeline snapshot.
- `status.json`: latest generation/push status.

Each episode contains one object only. Object sources include RobotWin mesh models and builtin/procedural geometry models: cube, sphere, flat cylinder, L-shape, tetrahedron, and rectangular bar. The same source family is used for visual rendering and collision/physics representation. The indoor-floor scene uses RTX/RaytracedLighting videos and records trajectory, pose, velocity, angular velocity, momentum, angular momentum, mass, center of mass, inertia, friction, disturbance force/torque, contact, and metadata fields. Each episode also contains per-view raw renderer RGB PNG frames packed as `*_frames.tar.gz`, `state_replay_validation.json`, mesh_assets/mesh_assets_manifest.json plus visual_mesh.obj and collision_mesh.obj for the episode object, and replay_state_exports/<episode>/replay_state.npz plus replay_state_manifest.json exported by the validator for IsaacSim PhysX import verification.
