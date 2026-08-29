# BSTVC production 3D assets

V15 loads the approved V04 Meshopt assets from `public/3d/bstvc/production/`:

- HQ: `bstvc-museum-treasure-hq-v04-meshopt.glb` — 18,179,224 bytes.
- Lite: `bstvc-museum-treasure-lite-v04-meshopt.glb` — 7,313,824 bytes.

The runtime slots live in `src/BSTVCSceneGLB.jsx`. V15 does not modify either GLB. It selects Lite before the request on compact/constrained desktop hardware and skips the complete Three.js path for reduced motion, Save-Data, compact/mobile viewports, explicit `?motion=static`, or missing WebGL2.

The static fallback is the transparent WebGL-derived frame `public/images/generated/bstvc-museum-treasure-transparent-v15.webp`, paired with the independent 2.5D plinth. This avoids the obsolete poster's opaque rectangle and duplicate pedestal.
