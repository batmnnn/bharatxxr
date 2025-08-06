# bharatxxr

**bharatxxr** is an Augmented Reality (AR) project powered by [A-Frame](https://aframe.io/) and [MindAR](https://hiukim.github.io/mind-ar-js-doc/). It recognizes custom image targets and displays 3D or 2D overlays using WebXR in your browser.

## Features

- Marker-based AR using MindAR.
- 3D model and image overlays when scanning the specified image target.
- Mobile-friendly, web-based—no app installation required.

## Demo

Open `index.html` in a browser supporting WebXR and camera access. When you point your camera at the image configured as a target, you will see the overlay (provided as `nocap.png` or the referenced 3D model).

## How it Works

- **A-Frame** is used for WebXR 3D rendering.
- **MindAR** provides marker image detection and tracking.
- When the target image (`targets.mind`) is detected, the AR overlay (plane with `nocap.png` and/or 3D model) appears.

## Usage

1. Clone the repository or download the files.
2. Serve the project via a local web server (due to browser camera permissions). For example, using Python:
   ```sh
   python3 -m http.server
   ```
   Then visit `http://localhost:8000` in your browser.

3. Place your custom image targets in `targets.mind`, and update references (if needed) in `index.html`.

## File Structure

| File          | Description                                     |
|---------------|-------------------------------------------------|
| index.html    | Main AR web application                         |
| nocap.png     | Sample overlay image (displayed on target)      |
| targets.mind  | MindAR target database                          |
| LICENSE       | MIT License                                     |

## Dependencies

- [A-Frame 1.5.0](https://aframe.io/releases/1.5.0/aframe.min.js)
- [MindAR 1.2.5](https://cdn.jsdelivr.net/npm/mind-ar@1.2.5/dist/mindar-image-aframe.prod.js)

## License

This project is licensed under the MIT License.
