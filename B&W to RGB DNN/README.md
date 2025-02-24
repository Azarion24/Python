# Image Colorization Tool

A Python application that automatically colorizes black and white images using a pre-trained deep learning model.

## Overview

This tool uses the Zhang et al. colorization model implemented in OpenCV to add realistic color to grayscale images. The colorization process works by:

1. Converting the image to the LAB color space
2. Predicting the 'a' and 'b' color channels using a pre-trained CNN
3. Recombining all channels to produce a full-color image

## Features

- Simple and easy-to-use implementation
- Uses a state-of-the-art model from the paper "Colorful Image Colorization" by Zhang et al.
- Built with OpenCV and NumPy for efficient processing
- Works with any standard image format

## Prerequisites

- Python 3.x
- OpenCV (cv2)
- NumPy

## Model Files

The application requires the following model files that should be placed in a `/models` directory:
- `colorization_deploy_v2.prototxt`
- `colorization_release_v2.caffemodel`
- `pts_in_hull.npy`

These files can be downloaded from [the original GitHub repository](https://github.com/richzhang/colorization).

## Usage

1. Place your black and white image as `zdjecie.jpg` in the root directory
2. Run the script
3. The original and colorized images will be displayed

## How It Works

The code loads a pre-trained CNN model that understands how to predict color based on visual features. It processes the luminance channel from the LAB color space and predicts the corresponding 'a' and 'b' color channels. These are then merged back together to create a colorized version of the original image.

## Acknowledgments

This implementation uses the model from:
- [Colorful Image Colorization](https://github.com/richzhang/colorization) by Richard Zhang, Phillip Isola, and Alexei A. Efros
