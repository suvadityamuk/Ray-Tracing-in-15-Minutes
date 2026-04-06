# Ray Tracing in 15 Minutes

A minimal ray-tracing project built with **PyTorch** to display a Sphere.

This repository walks through the core ideas behind a very simple ray tracer: generating one ray per pixel, intersecting those rays with a sphere, and shading the result with a basic Phong lighting model.

It is meant to be approachable rather than exhaustive, and is a nice starting point if you want to understand how ray tracing works without diving into a full rendering engine.

## What's in this repo

- `ray_tracing.py` — a standalone Python script that renders a shaded sphere
- `PyTorch_Ray_Tracing.ipynb` — the notebook version with step-by-step explanations

Run this notebook on [Google Colab here](https://colab.research.google.com/drive/1BcDNndy7wgRxqkQF5XTxVGVVt3RX4MA4)

## What it covers

- scene setup
- camera and image plane setup
- ray generation
- ray-sphere intersection
- surface normals
- Phong shading
- image rendering and saving

## Requirements

You'll need Python 3 plus these packages:

```bash
pip install torch matplotlib pillow
```

The script automatically uses:

- CUDA if available
- Apple Metal (`mps`) if available
- CPU otherwise

## Run it

```bash
python ray_tracing.py
```

This will generate:

- `raytrace_sphere.png`

and also display the image in a matplotlib window.

## Why PyTorch?

PyTorch makes it easy to express the entire render as tensor operations, which keeps the implementation short and makes the math easier to follow. The same ideas can also be translated to NumPy or other numerical computing libraries.

## If you want to extend it

A few natural next steps:

- add more spheres or other primitive types
- add shadows
- add reflections
- experiment with camera position and field of view
- try different materials, colors, and lighting setups

## Credits

Created by [Suvaditya Mukherjee](https://suvadityamuk.com).

Inspired by the spirit of *Ray Tracing in One Weekend*, but kept intentionally small and beginner-friendly.
