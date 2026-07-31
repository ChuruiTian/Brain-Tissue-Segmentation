# Brain MRI Tissue Segmentation with 2D U-Net

## Overview

This project implements a 2D U-Net for multiclass brain MRI tissue
segmentation using the IBSR dataset. The model is built with MONAI and
PyTorch and evaluated using Dice score, IoU, and pixel accuracy.

## Dataset

-   **Dataset:** IBSR Brain Tissue Segmentation
-   **Input:** Brain MRI volumes (48 × 192 × 192)
-   **Output:** Four-class segmentation masks
-   **Training:** 14 patients (672 slices)
-   **Validation:** 6 patients (288 slices)

## Methodology

-   Visualized MRI volumes and segmentation masks.
-   Converted 3D MRI volumes into 2D axial slices.
-   Trained a 2D U-Net implemented with MONAI.
-   Optimized the model using DiceCELoss and Adam.
-   Evaluated segmentation with Dice score, IoU and pixel accuracy.

## Results

  Metric             Result
  ---------------- --------
  Pixel Accuracy      94.5%
  Mean Dice           0.660

  Class           Dice
  ------------ -------
  Background     0.996
  Class 1        0.174
  Class 2        0.777
  Class 3        0.707

## Repository Structure

``` text
Brain-Tissue-Segmentation/
├── brain_seg.ipynb
├── UNET_draft_sketch.pdf
└── README.md
```

## Limitations

-   The model uses 2D slices and does not exploit full 3D spatial
    information.
-   The dataset contains only 20 MRI volumes, limiting generalisation.
-   Class imbalance results in lower segmentation performance for Class
    1.
