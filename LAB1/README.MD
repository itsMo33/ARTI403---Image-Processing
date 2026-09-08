# ARTI403 - Lab 1: Image Processing

Quick lab notebook for loading, showing, and saving images in Python with OpenCV, PIL, and NumPy.

## What you need

Python 3, plus these packages:

pip install opencv-python pillow matplotlib numpy


## Before you run it

Put `cameraman.tif` and `lena_gray_256.tif` inside an `images` folder next to the notebook. The real Lena image is copyrighted, so `lena_gray_256.tif` here is just a substitute grayscale image - if your instructor gave you the actual file, drop it in instead, the code doesn't change.

## What's in it

- Loading an image with OpenCV and with PIL, and showing it with matplotlib
- Fixing the color issue OpenCV gives you (it reads images as BGR, not RGB)
- Saving an image back to disk with both OpenCV and PIL
- Turning an image into a NumPy array and printing its shape and values
- A few practice exercises at the end: min/max/mean pixel value, cropping, flipping, and thresholding

## Running it

Open the notebook in Jupyter and run the cells top to bottom.
