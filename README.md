
# Image Processing in C/C++

This repository contains a C/C++ program for processing raw images using file input/output operations (`fopen`, `fread`, `fwrite`, `fclose`) in the C/C++ library.

## Overview

The program takes a raw image file (`unesco750-1.raw`), performs three different processing operations on it, and saves the processed images to separate raw files. The operations performed are:

1. Reversing intensity: `255 - f(x, y)`
2. Adding 20 to every pixel value
3. Adding 100 to every pixel value

## File Structure

- `image_processing.cpp`: The main C++ source file containing the image processing code.
- `unesco750-1.raw`: The input raw image file.
- `reverse_intensity.raw`: Output file after reversing intensity.
- `add_20pixel.raw`: Output file after adding 20 to every pixel.
- `add_100pixel.raw`: Output file after adding 100 to every pixel.
- `README.md`: This README file providing an overview of the project.

## Usage

To compile and run the program:

1. Compile the C++ code: `g++ image_processing.cpp -o image_processing`
2. Run the compiled program: `./image_processing`

## Requirements

- C/C++ compiler (e.g., GCC)
- Adobe Photoshop or similar software for converting raw files to JPEG format (optional)

## Author

Shubham Vats

