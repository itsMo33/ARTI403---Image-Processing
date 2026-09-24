# Lab 3 - Image Manipulations using OpenCV

ARTI 403 - Image Processing

## What's in this lab

- Reading and saving images with OpenCV
- Loading an image in grayscale
- Converting between color spaces (grayscale, YUV)
- Geometric transformations: resize, rotate, shear
- Intensity transformations: negative, log, power law (gamma)

## Files

- `Lab3.ipynb` - the notebook with all the code
- Uses the images from the shared `../images/` folder (lena_gray_256.tif and cameraman.tif)

## How to run

Open `Lab3.ipynb` and run all cells. Needs opencv-python, numpy, matplotlib.

## Notes

The steps (reading, saving, color spaces) are done on lena_gray_256.tif. Task 1 (resize, rotate, shear) and Task 2 (negative, log, gamma) are done on cameraman.tif.

For the log transform I picked c so the brightest pixel maps to 255. For gamma I used 2, since gamma > 1 increases contrast.
