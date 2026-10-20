# Edge Detection Using Convolution

## Overview

This project implements image edge detection from scratch using **2D convolution-style operations and Sobel filters** in Python.

Edge detection is a fundamental technique in computer vision used to identify boundaries and regions of significant intensity changes in an image. The project demonstrates how convolution kernels extract directional image features and how their outputs can be combined to estimate edge strength.

## How It Works

The algorithm consists of the following steps:

1. **Image loading:** Load an image and convert it to grayscale.
2. **Kernel definition:** Define the horizontal and vertical Sobel filters.
3. **Convolution:** Slide each kernel across the image, multiply corresponding elements, and sum the results.
4. **Gradient magnitude:** Combine the two directional gradients to estimate edge strength.
5. **Visualization:** Display the original image, horizontal gradient, and detected edges.

### Sobel Filters


The horizontal gradient kernel is:

### Sobel Filters

The horizontal gradient kernel (Gx):

```text
Gx = [-1   0   1]
     [-2   0   2]
     [-1   0   1]
```

The vertical gradient kernel (Gy):

```text
Gy = [-1  -2  -1]
     [ 0   0   0]
     [ 1   2   1]
```

The edge magnitude is calculated as:

```text
G = sqrt(Gx² + Gy²)
```

Larger gradient magnitudes indicate stronger intensity changes and therefore potential edges.


Larger gradient magnitudes indicate stronger intensity changes and therefore potential edges.


## Technologies Used

- **Python**
- **NumPy** — matrix operations and numerical calculations
- **Matplotlib** — image visualization
- **Pillow (PIL)** — image loading and grayscale conversion

## Installation

Install the required libraries:

```bash
pip install numpy matplotlib pillow
```

## Usage

1. Clone or download this repository.
2. Place an image named `image.jpg` in the project directory.
3. Run the Python script:

```bash
python edge_detection.py
```

Replace `image.jpg` with your image filename if necessary.

The program displays the original image, the horizontal gradient, and the resulting edge map.



This project is available for educational and personal use.
