# ComfyUI TotoroUI Sarpify

A trimmed TotoroUI/ComfyUI-derived runtime used for Sarp's Flux and image-generation experiments.

## What is included

- Core node definitions in `nodes.py`
- Model and folder path helpers in `folder_paths.py`
- Totoro model/runtime modules under `totoro/`
- Extra node packs under `totoro_extras/`

## Requirements

- Python 3.10+
- PyTorch compatible with your hardware
- Pillow, NumPy, safetensors, and the model-specific dependencies used by the nodes you run

## Usage

This repo is intended to be used as a local runtime/library component rather than a standalone packaged app. Install the dependencies required by your workflow, place model weights in the expected `models/` subdirectories, then import or run the workflow code that uses these nodes.

## Artifact policy

Do not commit downloaded checkpoints, generated outputs, local inputs, or cache directories. The `.gitignore` file excludes the common large artifact paths (`models/`, `checkpoints/`, `output/`, `outputs/`, `input/`, `temp/`, etc.).
