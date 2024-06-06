# Image-Mosaicing-

This repository contains the code and documentation for  image mosaicing. The process involves combining multiple images with overlapping fields of view to create a segmented panorama or a high-resolution image.

## Introduction
Image mosaicing is extensively used in fields such as satellite imaging, medical imaging, microscopy, and computer vision. It allows for the creation of larger images with higher resolution than is possible with a single camera. The process involves:

1. Determining camera motion between images using features like points, edges, or textures.
2. Finding correspondences between images.
3. Applying geometrical transformations to warp images into a common coordinate system.
4. Using blending techniques to smooth intensity variations in overlapping regions.

## Challenges
1. Varying illumination conditions.
2. Images with moving objects.
3. Parallax effects.
4. Lens distortion.
   
Advanced techniques like bundle adjustment are used to refine camera parameters and produce visually consistent mosaics free from ghosting, blurring, and visible seams.

## Datasets
Four datasets with varying percentages of overlap were collected for this lab:

Dataset 1: Overlapping of more than 50%

Dataset 2: Overlapping of about 50%

Dataset 3: Overlapping of about 15%

Dataset 4: Overlapping of 50%

These datasets were used to create panoramic mosaics using the Harris Corner Detection method to detect and align interest points.

## Methodology
Harris Corner Detection
The Harris Corner Detector algorithm is used to detect interest points or corners in images, which are crucial for feature matching, image stitching, and object recognition.

## Interest Points Detection: Set the maximum number of interest points (N) to 1000.
Feature Matching: Match specific features and estimate the transformation between adjacent image pairs.

Image Alignment: Align all the extracted feature descriptors for each interest point.

Blending Techniques: Blending techniques are used to smooth intensity variations in the overlap region, ensuring a seamless mosaic.

## Results
### Dataset 1: Latino Students Centre (Overlapping > 50%)
Interest Points: Detected and aligned using N=1000.

### Dataset 2: Brick Wall at Ruggles T-Station (Overlapping ~50%)
Interest Points: Detected and aligned using N=1000.
Observations: The mosaic's alignment is less accurate due to similar features causing confusion during alignment.

### Dataset 3: Mural on Ruggles Wall (Overlapping ~15%)
Interest Points: Initially set to N=1000, later increased to N=2000 for better accuracy.
Panoramic Mosaic (N=1000)
Panoramic Mosaic (N=2000)

Observations: Increasing N improves the stitching accuracy.

### Dataset 4: Mural on Ruggles Wall (Overlapping ~50%)
Interest Points: Detected and aligned using N=1000.
