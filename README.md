# GeometryEstimation

[MoGe](https://arxiv.org/abs/2410.19115_) is a powerful model for recovering 3D geometry from monocular open-domain images. The model consists of a ViT encoder and a convolutional decoder. It directly predicts an affine-invariant point map as well as a mask that excludes regions with undefined geometry (e.g., sky), from which the camera shift, camera focal length and depth map can be further derived.

## Features

- **Accurately** estimate 3D geometry in point map or mesh format from a **single** image.
- Support various image resolutions and aspect ratios, ranging from **2:1** to **1:2**.
- Capable of producing an extensive depth range, with distances from nearest to farthest reaching up to **1000x**.
- **Fast** inference, typically **0.2s** for a single image.

### Prerequisite

- Clone this repository.

  ```bash
  git clone https://github.com/Tox1cCoder/GeometryEstimation.git
  cd GeometryEstimation
  ```

- Make sure that `pytorch` and `torchvision` are installed. Then install the rest of the requirements.
  ```bash
  pip install -r requirements.txt
  ```

### Using [scripts/app.py](scripts/app.py) for a web demo

Make sure that `gradio` is installed and then run the following command:

```bash
python scripts/app.py

```

### Using [scripts/infer.py](scripts/infer.py)

Run the script `scripts/infer.py` via the following command:

```bash
# Save the output [maps], [glb] and [ply] files
python scripts/infer.py --input IMAGES_FOLDER_OR_IMAGE_PATH --output OUTPUT_FOLDER --maps --glb --ply

# Show the result in a window (requires pyglet < 2.0, e.g. pip install pyglet==1.5.29)
python scripts/infer.py --input IMAGES_FOLDER_OR_IMAGE_PATH --output OUTPUT_FOLDER --show
```
