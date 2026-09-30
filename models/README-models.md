# 3D Models

## Workshop (core): your own model

1. Download a `.glb` from [poly.pizza](https://poly.pizza/).
2. Put it in `models/custom/`.
3. Ask the agent (see `PROMPTS.md`) to wire it up, or edit `index.html`:
   - Add `<a-asset-item id="custom-model" src="./models/custom/YOUR-FILE.glb"></a-asset-item>`
   - Set `gltf-model="#custom-model"` on `#active-model`

## Bundled fallbacks

If your download fails, switch `gltf-model` to one of:

`#robot-model` · `#crystal-model` · `#satellite-model` · `#trophy-model` · `#plant-model`

Double-tap in AR cycles the bundled models (and your custom model if you add it to the `models` array).

## Take-home: your own image target

1. Generate a QR that points at your GitHub Pages URL (e.g. Canva).
2. Run: `npx @8thwall/image-target-cli@latest`
3. Paste the JSON into `targetData` in `index.html` and update `name=` on `xrextras-named-image-target`.
