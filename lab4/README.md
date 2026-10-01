# Lab 4: Intensity Transformations and Filtering – Spatial Domain

**Course:** ARTI404 – Image Processing
**University:** Imam Abdulrahman Bin Faisal University – College of Computer Science and Information Technology
**Student:** Mohammed Moayed Alquriniy (2240007325)
**Academic Year:** 2025 – 2026

## Overview

This lab implements fundamental image processing algorithms in the spatial domain: thresholding, contrast stretching, histogram equalization, and histogram matching.

## Folder Contents

| File | Description |
|------|-------------|
| `Lab4.ipynb` | Jupyter notebook with all procedural steps and assessment tasks, including outputs |
| `Lab4_Report.pdf` | Lab report with code, results, and observations |
| `Parrot.png` | Image used for thresholding |
| `moon.png` | Moon image (`skimage.data.moon`) used for contrast stretching and equalization |
| `rocket.png` | Rocket image (`skimage.data.rocket`) used as the reference for histogram matching |
| `chelsea.png` | Chelsea image (`skimage.data.chelsea`) used as the source for histogram matching |

## Tasks

### Procedural Steps

**Task 1: Thresholding.** The Parrot image is converted to grayscale and thresholded with `cv2.threshold` using the values 0, 50, 100, 150, and 200.

**Task 2: Histogram Processing.** The moon image is contrast stretched with `exposure.rescale_intensity` using the 2nd and 98th percentiles. The original and stretched images are displayed with their histograms.

### Assessment

**Task 1: Contrast Stretching (3rd – 80th percentiles).** The moon image is stretched using the 3rd percentile (87) and the 80th percentile (118). About 20% of the pixels saturate at 255.

**Task 2: Histogram Equalization.** `exposure.equalize_hist` flattens the histogram of the moon image and spreads the gray levels over the full range.

**Task 3: Histogram Matching.** `exposure.match_histograms` matches the histogram of the Chelsea image (source) to the rocket image (reference) for each RGB channel.

## Requirements

- Python 3
- Jupyter Notebook
- OpenCV, NumPy, scikit-image, Matplotlib

```bash
pip install opencv-python numpy scikit-image matplotlib
```

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/itsMo33/ARTI403---Image-Processing.git
   ```
2. Make sure `Parrot.png` is in the shared `images/` folder at the root of the repository, because the notebook loads it from `../images/Parrot.png`.
3. Open `Lab4.ipynb` in Jupyter or VS Code and run all cells from top to bottom.

The moon, rocket, and Chelsea images are loaded directly from `skimage.data`, so they do not need to be in the `images/` folder.
