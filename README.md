# About

A texture reconverter for my [VRChat 3D Model Loader](https://github.com/vr-voyage/vrchat-3d-model-loader-tablet),
setup as a single HTML file with no dependencies and no
network requests !

You can use it offline without any server !  
This doesn't send any data anywhere.

# Usage

* Open the HTML file with a browser.
* Click "Initialize" at the bottom.
* Drag & drop the VRM or GLB file to convert in the "Drop" section".
* Use the downloaded `reconverted.glb` file.

# Technical details

Currently convert textures inside GLB models to BC7.

Inside the JSON, this :
* replaces the reconverted `"images"` mimetype to `"image/raw"`
* adds my custom extension `EXT_voyage_exporter` which contains
  three fields : `width`, `height` and `format`.

This uses [gputex](https://github.com/verekia/gputex) under the hood.

AI was used to :
* convert and stuff `gputex` into a single HTML file
* make the "UI"

The GLB manipulation code is mine, so I still know what it does.

BC3 (DXT5) was added into the mix by the coding agent, but I haven't tested it yet.
