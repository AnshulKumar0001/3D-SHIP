# Ship & Lighthouse — Computer Graphics Project

An interactive Three.js scene with a moving ship, a lighthouse on a rocky island, and a rotating beacon. The models are made from built-in Three.js geometries, and the water surface animates in real time.

## Run locally

The project uses ES modules and an import map, so serve the folder over HTTP instead of opening `index.html` directly.

1. Open this folder in VS Code.
2. Start the **Live Server** extension from `index.html`, or run `python -m http.server 8000` in the project folder.
3. Visit `http://localhost:8000`.

Three.js is loaded from jsDelivr, so an internet connection is needed on the first load.

## Controls

- **Start / Pause / Resume / Reset** control the vessel animation and restore the scene.
- Use the directional pad or **W A S D / arrow keys** to translate the ship.
- Use the curved-arrow buttons to rotate the ship around its vertical axis.
- Choose the vessel or lighthouse and drag the scale slider to resize it.
- Orbit the camera by dragging in the scene, scroll to zoom, or use the camera buttons.
- Toggle environment lighting to compare the scene with its base lighthouse beacon.
- Adjust animation speed with the speed slider. Press **Space** to pause or resume.

## Computer graphics concepts

- **Modelling:** meshes assembled from primitive geometries form the ship, island, lighthouse, and clouds.
- **Translation and rotation:** vessel movement and heading controls update its position and Y rotation.
- **Scaling:** the selected vessel or lighthouse is uniformly resized.
- **Viewing transformation:** `OrbitControls` manipulates the perspective camera.
- **Lighting and shading:** hemisphere, directional, point, and rotating spotlight sources illuminate the scene; the directional light casts shadows.
- **Animation:** `requestAnimationFrame` updates a procedurally displaced ocean, ship bob, and lighthouse beam.

The source is organized as `index.html`, `styles.css`, and `src/main.js`. No build step is required.
