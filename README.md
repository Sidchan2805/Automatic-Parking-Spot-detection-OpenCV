# Automated Parking Vacancy Spot Detection

## Overview

This project utilizes computer vision and image processing techniques to detect available parking spots in a parking lot. The system employs both deep learning-based object detection and classical computer vision techniques to ensure robustness and accuracy across various environmental conditions. The goal is to provide a scalable and deployable solution that does not require complex infrastructure changes.

## Features

Real-time parking vacancy detection

YOLOv8 for object detection

Classical computer vision techniques (OpenCV, cvzone, image stitching, non-max suppression)

Handling occlusions and external factors

Integration with CCTV footage

Scalable and deployable solution

## Project Structure

├── data/                   # Dataset files (CNR Park, CNR ParkExt, additional parking videos)
├── models/                 # Trained model checkpoints
├── src/                    # Source code
│   ├── detection.py        # YOLOv8-based object detection
│   ├── cv_methods.py       # Classical computer vision methods
│   ├── stitching.py        # Image stitching for multiple perspectives
│   ├── tracking.py         # Parking space status tracking
│   └── utils.py            # Helper functions
├── notebooks/              # Jupyter notebooks for experimentation
├── results/                # Output images, logs, and quantitative results
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation

Installation

## Prerequisites

Please make sure you have Python 3.8+ installed along with the necessary dependencies.

Download the dataset (CNR Park & CNR ParkExt) and place it in the data/ directory.

Usage

Running Object Detection

python src/detection.py --input data/parking_lot_image.jpg --output results/detected_output.jpg

Running Classical CV Methods

python src/cv_methods.py --input data/parking_lot_image.jpg --output results/cv_output.jpg

## Methodology

### Data Collection:

Used open-source datasets (CNR Park, CNR ParkExt)

Collected additional parking lot videos

### Preprocessing:

Applied SIFT and manual image stitching to handle non-detected spaces

### Model Architecture:

Utilized YOLOv8 for object detection

Applied classical computer vision techniques for refinement

### Training Procedure:

Trained on labeled parking datasets

Fine-tuned using real-world CCTV footage

### Post-processing:

Used non-max suppression to refine bounding boxes

Implemented a manual polygon test function for additional accuracy

### Results

Quantitative Results

High accuracy in identifying vacant and occupied spaces

Improved detection using ensemble methods

### Qualitative Results

Bounding box refinement with non-max suppression

Enhanced detection of occluded objects

Future Scope

Implementing real-time tracking for parking duration estimation

Integrating with automated ticketing systems

Extending the solution to multi-level parking lots
