# Lab 8 - Edge Detection

ARTI403 - Image Processing

## Objective

Apply and compare edge detection methods using Python and OpenCV, and see how changing the parameters affects the detected edges.

## Files

| File | Description |
|------|-------------|
| `Lab8_Task.ipynb` | Jupyter notebook with the solution and outputs |
| `Lab8_Task.pdf` | PDF version of the notebook |
| `coffee.png` | Image used in the task |

## Task 1: Apply Edge Detection Methods

I used a new image (a coffee cup on a wooden table) and applied:

- Sobel Edge Detector
- Prewitt Edge Detector
- Canny Edge Detector

The original image and the three edge maps are shown together in the notebook.

**Notes:**
- Sobel and Prewitt give very similar results (thick edges). Sobel is slightly stronger because of the higher weight in the middle of the kernel.
- Canny gives thin, clean, binary edges. The cup, saucer and spoon outlines are very clear, but it also picks up the wood texture.

## Task 2: Effect of Canny Thresholds

| Low | High | Edge pixels |
|-----|------|-------------|
| 30  | 90   | ~41,700 |
| 50  | 150  | ~31,300 |
| 100 | 200  | ~20,400 |

- Low thresholds detect more edges and more details, but also a lot of noise (wood texture).
- Higher thresholds keep only the strong edges (cup rim, saucer border) and remove noise, but some fine details are lost.

## Requirements

```
pip install opencv-python numpy matplotlib
```

## How to Run

1. Keep `coffee.png` in the same folder as the notebook.
2. Open `Lab8_Task.ipynb` in Jupyter / VS Code.
3. Run all cells.
