# Data Augmentation Impact on Average Pooling in CNNs

## Overview
This project presents an empirical analysis of how common data augmentation techniques affect **average pooling outputs** in Convolutional Neural Networks (CNNs). The study demonstrates that average pooling is **not invariant** to transformations such as rotation, flipping, scaling, cropping, and illumination changes.

## Objective
To evaluate whether average pooling preserves spatial and intensity consistency when input images undergo various augmentations, and to understand the role of data augmentation in improving CNN robustness.

## Key Experiments
The following transformations were applied to input images before average pooling:
- Rotation (90°, 180°, 270°)
- Horizontal and vertical flipping
- Scaling (zoom and resize)
- Cropping (horizontal and vertical)
- Brightness variations (maximum and minimum intensity)

Each transformed image was resized to a fixed dimension and passed through a 2×2 average pooling operation for comparison.

## Key Findings
- Average pooling preserves **local intensity statistics**, not spatial orientation.
- Pooled outputs change significantly under rotation, reflection, and scaling.
- Cropping causes permanent information loss in pooled representations.
- Extreme brightness collapses spatial information entirely.
- CNN robustness arises from **learned features via data augmentation**, not from pooling operations.

## Conclusion
Average pooling should be viewed as a **dimensionality reduction and smoothing operation**, not a mechanism for transformation invariance. Effective CNN generalization depends on diverse augmented training data and robust feature learning.

## Technologies Used
- Python
- NumPy
- OpenCV
- Matplotlib

## Use Cases
- Academic research on CNN behavior
- Understanding pooling limitations
- Computer vision and deep learning education
- Final year engineering project reference

## Author
Soham Chogale

## License
This project is intended for academic and educational use.

