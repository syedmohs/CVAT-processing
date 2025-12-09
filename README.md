📘 README – CVAT Annotation Visualization
This repository contains a Python script that visualizes CVAT polyline annotations on top of the original images.
The script reads your annotations.xml, overlays all annotation polylines on the corresponding image files, and saves the output.

📦 Folder Structure

Organize your project like this:

project/
│
├── annotations.xml
│
├── images/
│     ├── scene00001.png
│     ├── scene00006.png
│     ├── scene00011.png
│     └── ... (all image frames)
│
└── overlay.ipynb

▶️ How to Use
1. Install Requirements

Make sure you have OpenCV installed:

pip install opencv-python


(Optional but recommended)

pip install numpy

2. Run the Script

Save the visualization script as annotate_cvat.py, then run:

python annotate_cvat.py

3. Output

Annotated images will be saved inside:

annotated_output/


Each output image will have green polylines showing your "liver annotation".

🧠 Script Overview

The script:

Loads annotations.xml

Extracts all <image> tags

Reads their name field (e.g., "scene00001.png")

Parses each <polyline> associated with that image

Draws the polylines on the image using OpenCV

Saves them to annotated_output/
