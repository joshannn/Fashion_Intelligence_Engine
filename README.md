# Fashion_Intelligence_Engine
 Fashion Intelligence Engine

A Python-based pipeline designed to transform raw Instagram data into structured fashion insights using Computer Vision.
The Vision
The ultimate goal of this project is to build a Fashion Intelligence Engine. By combining visual recognition with social media metadata, the system aims to:

Decode clothing styles from images using AI
Identify dominant fashion categories in the digital landscape
 Provide data-driven insights into trend popularity
 Analyze fashion trends at scale across social media platforms


Project Overview
This pipeline takes Instagram profile data and automatically categorizes clothing items into 60+ distinct fashion categories, from casual streetwear to revealing evening wear, from traditional ethnic attire to athletic sportswear.
# Fashion Intelligence Engine

A compact Python pipeline that turns social-media images into structured fashion insights using CLIP-based image understanding.

## Quick summary

- Purpose: Automatically detect and categorize clothing across 60+ fashion categories from Instagram images.
- Key tech: OpenAI CLIP (ViT-B/32) for zero-shot image understanding, with GPU acceleration and automatic CPU fallback.
- Output: Organized folders per category and a classification report for downstream analysis.

## Quick start

Prerequisites: Python 3.9+ and a machine with GPU (optional).

Install dependencies:

```bash
pip install -r requirements.txt
```

Run (example):

```bash
python instagram_downloader.py --user joshannn
python clothing_classifier.py --input data/joshannn --output reports/joshannn
```

## Features

- Zero-shot clothing classification (60+ categories)
- Intelligent non-clothing filtering (screenshots, food, landscapes)
- Auto-organization into category folders
- GPU acceleration with CPU fallback and basic error handling

## Project layout

- `instagram_downloader.py` — download images for a profile
- `clothing_classifier.py` — CLIP-based classification and filtering
- `requirements.txt` — Python dependencies
- `data/` — downloaded and organized images

## How it works (high level)

1. Download images from an Instagram profile
2. Encode images with CLIP and filter non-clothing content
3. Match clothing images to 60+ textual category prompts
4. Move images into category folders and generate a report

## Technical notes

- Expected throughput: ~2–3 img/s on GPU, ~0.5 img/s on CPU (depends on hardware)
- Typical accuracy: ~85–90% on clear, well-lit clothing photos

## Limitations

- Performance degrades on heavily edited or low-quality images
- CLIP may confuse context (mannequins, studio shots)
- Biases inherited from CLIP's training data




