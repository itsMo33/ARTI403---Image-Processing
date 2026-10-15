# ARTI403 – Image Processing | Lab 6: Frequency Domain

**Name:** Mohammed Moayed Alquriniy
**Student ID:** 2240007325
**Course:** ARTI403 – Image Processing (Department of Computer Engineering, IAU)
**Academic Year:** 2026 – 2027

---

## Overview
This lab covers **filtering in the frequency domain** using the 2D Fast Fourier Transform (FFT).
An image is transformed to the frequency domain, multiplied by a filter, and transformed back to the spatial domain with the inverse FFT.

## Tasks

### Procedural Task #1 – Laplacian Filter in the Frequency Domain
- Loaded the Cameraman image (`skimage.data.camera()`) and resized it to 256 × 256.
- Built the Laplacian filter directly in the frequency domain: `H(u, v) = −4π² (u² + v²)`.
- Multiplied the image spectrum by the filter and applied the inverse FFT to get the edge-enhanced image.

### Assessment Task #1 – Sobel Filters in the Frequency Domain
- Defined the Sobel X and Sobel Y kernels.
- Zero-padded and centred each kernel to the image size, then used `ifftshift` so the kernel centre sits at (0, 0) before the FFT.
- Multiplied the image FFT by each Sobel FFT, applied the inverse FFT, and computed the gradient magnitude `G = √(Gx² + Gy²)`.
- Visualised the frequency responses of both Sobel filters.
- **Verified** the result against spatial-domain circular convolution (`scipy.ndimage.convolve`, `mode='wrap'`): the maximum difference is ~1e-15, confirming the convolution theorem.

## Folder Structure
```
Lab 6/
├── Lab6.ipynb      # Jupyter notebook (all cells executed, outputs visible)
├── Lab6.pdf        # PDF export of the notebook
├── README.md       # This file
└── images/         # Images used and produced in the lab
    ├── cameraman.png                        # Original input image
    ├── task1_laplacian_frequency.png        # Task 1: Laplacian results
    ├── task2_sobel_frequency_responses.png  # Sobel X / Y frequency responses
    ├── task2_sobel_frequency_results.png    # Assessment: Sobel results
    └── task2_frequency_vs_spatial.png       # Verification vs. spatial domain
```

## Requirements
- Python 3
- NumPy, Matplotlib, scikit-image, SciPy

```bash
pip install numpy matplotlib scikit-image scipy
```

## How to Run
1. Open `Lab6.ipynb` in Jupyter / VS Code.
2. Run all cells (**Run All**). The `images/` folder is created automatically and the result figures are saved into it.

## Results
| Laplacian (Task 1) |
|---|
| ![Laplacian](images/task1_laplacian_frequency.png) |

| Sobel in the Frequency Domain (Assessment) |
|---|
| ![Sobel](images/task2_sobel_frequency_results.png) |

## Key Takeaways
- Multiplication in the frequency domain is equivalent to convolution in the spatial domain.
- Both the Laplacian and Sobel filters remove the DC component, so they act as high-pass (edge-detecting) filters.
- Sobel X detects vertical edges, Sobel Y detects horizontal edges, and the magnitude combines them into a full edge map.
