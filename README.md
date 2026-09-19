# AI-Powered Bag Surveillance System

## Overview
This project is an AI-driven video surveillance tool designed to detect people and objects. It uses YOLOv8 for object detection and calculates spatial overlap (IoU) . 

## What It Does
* **Object Detection:** Identifies people, vehicles, and bags in a video feed using a customized YOLOv8 configuration.
* **Spatial Association:** Uses Intersection over Union (IoU) logic to pair people with the bags they are carrying.
* **Event Timeline Generation:** Automatically logs a cleaned, chronological timeline of when specific subjects appear in the frame (e.g., "A Person with a backpack appeared").
* **RAG Integration:** Packages the chronological timeline events into structured documents (with timestamps and video sources) ready for Retrieval-Augmented Generation (RAG) pipeline.

## Quick Start

**1. Install Dependencies**
Ensure your environment has the required packages installed[cite: 1]:
`pip install ultralytics opencv-python-headless torch`

**2. Run the Pipeline**
Execute the main script via the command line by passing your input video and desired output path[cite: 1]:
`python main.py --video sample_data/your_video.mp4 --output outputs/annotated.mp4`
