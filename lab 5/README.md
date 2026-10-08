# Lab 5: Spatial Filtering – Smoothing and Sharpening

**Course:** ARTI404 – Image Processing  
**Student:** Mohammed Moayed Alquriniy (2240007325)  
**University:** Imam Abdulrahman Bin Faisal University – Department of Computer Engineering

---

## Overview
This lab applies spatial filters to images using OpenCV. It covers **smoothing** (box and Gaussian filters) and **sharpening** (unsharp masking and the Laplacian filter).

## Tasks

| Task | Description | Image |
|------|-------------|-------|
| Procedural Step | Unsharp masking (Gaussian blur, `sigma = 2`, `amount = 1.5`) | `Coffee.png` |
| Task 1 | Convolve the image with a **7×7 box filter**, then show the original and smoothed images side by side | `Cat.png` |
| Task 2 | Apply a **5×5** and a **21×21 Gaussian filter**, then show the three images side by side | `Astronaut.png` |
| Task 3 | Sharpen the image with a **3×3 Laplacian filter** using `np.clip(image_float - laplacian, 0, 1)` | `Moon.png` |

## Folder Structure
```
Lab 5/
├── Lab5.ipynb          # Jupyter notebook (solved, with outputs)
├── Lab5_Report.pdf     # Report: code + output
├── requirements.txt    # Required libraries
├── README.md
└── images/
    ├── Coffee.png
    ├── Cat.png
    ├── Astronaut.png
    └── Moon.png
```

## How to Run
1. Install the requirements:
   ```bash
   pip install -r requirements.txt
   ```
2. Open `Lab5.ipynb` from inside the `Lab 5` folder, so the relative `images/` paths resolve.
3. Run all cells.

## Libraries
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## Key Takeaways
- **Box filter:** gives equal weight to every neighbour, which produces a uniform blur.
- **Gaussian filter:** weights neighbours by distance from the centre; a larger kernel means a larger sigma and a stronger blur.
- **Unsharp masking:** `original + amount × (original − blurred)` boosts fine details.
- **Laplacian:** a second-derivative operator that detects edges; subtracting it from the image sharpens it.

## References
- [OpenCV – Smoothing Images](https://docs.opencv.org/4.x/d4/d13/tutorial_py_filtering.html)
- [Data Carpentry – Blurring Images](https://datacarpentry.github.io/image-processing/06-blurring.html)
