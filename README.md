# 📘 CVAT Annotation Visualization

This repository contains a **Python script** designed to visualize **CVAT polyline annotations** overlaid on the original image files.

The script reads your `annotations.xml` file, overlays all annotation polylines onto the corresponding images, and saves the output.

---

## 📦 Folder Structure

Organize your project files in the following structure for the script to run correctly:

project/

│

├── annotations.xml         <-- Your CVAT output file

│

├── images/                 <-- All the image frames go here

│     ├── scene00001.png

│     ├── scene00006.png

│     ├── scene00011.png

│     └── ... (and so on)

│

└── overlay.ipynb           <-- The visualization script/notebook

---

## ▶️ How to Use

### 1. Install Requirements

Ensure you have the necessary libraries installed.

# Required: OpenCV for image manipulation and drawing
pip install opencv-python

# Optional but Recommended: NumPy for efficient array handling
pip install numpy
bash

# Run the script: python annotate_cvat.py

# Output: annotated_output/

# script overview
The script performs the following steps:

Loads the annotations.xml file.

Extracts all <image> tags.

Reads the name field (e.g., "scene00001.png") to find the corresponding image file.

Parses each <polyline> associated with that image to get the coordinate data.

Draws the polylines on the image using OpenCV functions.

Saves the annotated image to the annotated_output/ directory.
