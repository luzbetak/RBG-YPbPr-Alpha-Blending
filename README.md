RBG-YPbPr-Alpha-Blending
========================
A project dedicated to blending RGB and YPbPr color spaces using alpha blending techniques.

## Introduction
The RBG-YPbPr-Alpha-Blending project aims to provide a seamless way of blending images or visuals in RGB and YPbPr color spaces. This is achieved using alpha blending techniques, which ensure smooth transitions between overlapping visuals.

## Code Description

### Package and Imports
- The code belongs to the `graphics4` package.
- Necessary classes for image handling (`BufferedImage`), file operations (`File`), and exceptions (`IOException`) are imported. Additionally, a class for reading and writing images (`ImageIO`) is also imported.

### Class Declaration
- The class `Graphics4` is defined.

### Member Variables
- `numberOfImages` is an integer set to 30, likely representing the number of processed images to be generated.

### Main Method
- An instance of the `Graphics4` class is instantiated.
- The `RGB_ColorSpace()` method is invoked to process the image in RGB color space.

### RGB_ColorSpace Method
1. Reads an image named `rose.png` from a specific path.
2. Extracts the Red, Green, and Blue (RGB) components of each pixel in the image.
3. Initiates a new empty image buffer.
4. Processes the image 30 times (as determined by `numberOfImages`) to blend it with its grayscale version, each time with a varying alpha (transparency) value. This creates a series of images transitioning from the original to grayscale.
5. Each processed image is saved to disk with sequential filenames (e.g., `rose00.png`, `rose01.png`, ...).

### YPbPr_ColorSpace Method
1. Reads the `rose.png` image from the specified path.
2. Extracts the RGB components for each pixel.
3. Transforms the RGB values of each pixel into the YPbPr color space.
4. Generates a new empty image buffer.
5. Processes the image 30 times (similar to the `RGB_ColorSpace` method), blending it with its grayscale version in the YPbPr color space.
6. Saves each processed image with sequential filenames.
7. Converts the YPbPr values back to RGB (though the final saving in this format is commented out).

### Summary
The program processes an input image (`rose.png`) in two distinct ways:
1. By blending the image with its grayscale counterpart in the RGB color space.
2. By transitioning it to the YPbPr color space, blending it with its grayscale version, and subsequently converting it back to RGB.

The result from each processing step is a series of images that transition from the original image to grayscale, saved with sequential filenames.

