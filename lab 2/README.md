# Lab 2 - Image Processing

ARTI 403 - Image Sampling, Quantization, Arithmetic and Set Operations.

## What's in this lab

- Sampling and quantization on an image
- Adding/subtracting two images
- Adding a constant value to an image
- Set operations on two images (union, intersection, difference, symmetric difference)


## How to run

Open lab2.ipynb and run all cells. Needs opencv-python, numpy, matplotlib, pillow, scikit-image.

If the images folder is empty, the first cell will generate sample images automatically so the notebook still runs.

## Notes

Task 1: tried different sampling factors and quantization levels to see the effect on the image.

Task 2: subtraction, addition with constant (175), and the three set operations (difference, symmetric difference, intersection) are all done using bitwise operations.
