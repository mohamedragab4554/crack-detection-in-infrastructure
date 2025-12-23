# Crack Detection in Civil Infrastructure Using Computer Vision

## Overview
This project applies deep learning–based computer vision techniques to
automatically detect cracks in civil infrastructure, supporting the
digital transformation of structural health monitoring (SHM).

The work is based on my MSc dissertation at Ulster University and
benchmarks state-of-the-art YOLO-based segmentation models and a U-Net
architecture for accurate crack localisation and pixel-level segmentation.

## Civil Engineering Problem
Manual visual inspection remains the dominant approach for identifying
cracks in concrete structures. However, it is labour-intensive,
time-consuming, subjective, and often exposes inspectors to hazardous
conditions such as working at height or near traffic.

Automated crack detection using computer vision offers a safer,
repeatable, and scalable alternative for infrastructure inspection and
asset management.

## Objectives
- Detect cracks in concrete infrastructure from inspection images
- Compare detection-based and segmentation-based deep learning models
- Evaluate robustness under real-world site conditions
- Assess suitability for integration into digital inspection workflows

## Methodology
The crack detection pipeline consists of:
- Image preprocessing and augmentation
- Crack detection using YOLO-based segmentation models (YOLOv8x-seg,
  YOLO11n-seg, YOLO11x-seg)
- Pixel-accurate crack segmentation using U-Net with a ResNet-50 backbone
- Quantitative evaluation using Precision, Recall, F1-score, IoU, and mAP
- External validation using real inspection images from live projects

## Models and Tools
- Python 3.11
- PyTorch
- OpenCV
- Ultralytics YOLO (segmentation variants)
- U-Net with ResNet-50 encoder
- Albumentations for data augmentation

## Dataset
- Crack-Seg benchmark dataset (Ultralytics)
- Real-world inspection images provided by industry partner (Amphora)

Due to data ownership and size restrictions, only representative sample
images are included in this repository.

## Results
- YOLO-based models achieved high recall and reliable crack localisation
  on curated datasets
- YOLO11x-seg demonstrated improved robustness and fewer false positives
  during field validation
- U-Net produced cleaner, pixel-accurate crack masks with superior
  boundary continuity under complex lighting and surface conditions

Example predictions and visual outputs are provided in the `results/`
folder.

## Engineering Impact
- Reduces inspection time from days to minutes
- Improves inspector safety by limiting site exposure
- Enhances repeatability and objectivity of crack assessment
- Supports integration with BIM and digital-twin environments

## Limitations and Future Work
- Performance is affected by domain shift between curated and site images
- Thin crack classes remain challenging under severe class imbalance
- Future work includes higher-resolution training, domain adaptation,
  and deployment on UAV-based inspection platforms

## Author
Mohamed Ragab  
MSc Research – Ulster University  
Computer Vision for Structural Health Monitoring
