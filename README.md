# T2V-Bed-Fall-Detection-Dataset

This repository contains the **T2V-Bed-Fall-Detection-Dataset**, a specialized video/text dataset designed for training and evaluating vision-based models in detecting bed-related fall incidents, particularly focused on elderly care and healthcare environments.

## Table of Contents
- [Introduction](#introduction)
- [Dataset Features](#dataset-features)
- [Data Cleaning & Elimination Criteria](#data-cleaning--elimination-criteria)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [License](#license)

---

## Introduction
Bed-exit falls represent one of the most critical risks in hospitals and home care settings. This dataset provides annotated data tracking transitions from bed-lying to sitting, bed-exiting, and sudden fall events. It supports multi-modal tasks such as text-to-video (T2V) evaluation, action recognition, and anomaly detection.

## Dataset Features
- **Platform-Generated Content:** Both the **fall** and **non-fall** video datasets were fully generated and synthesized using the **Mage.space** AI platform.
- **Diverse Scenarios:** Covers multiple camera angles, lighting conditions, and bed types.

## Data Cleaning & Elimination Criteria
To ensure data quality, raw video clips underwent a rigorous filtering process based on the following **Elimination Criteria**:
1. **Kinematic Inconsistency:** Any generated or recorded sequences where the joint movements or skeletal trajectories were *kinematically inconsistent* or mathematically impossible for human body limits were immediately excluded.
   - *Note: Example clips of these rejected videos are provided in the `Elimination samples (Kinematically inconsistent)/` directory for reference and comparison.*
3. **Occlusion & Noise:** Clips with severe environmental occlusion where the subject was invisible for more than 40% of the sequence were removed.
4. **Mislabeled Transitions:** Sequences failing to demonstrate a clear semantic transition from bed-bound states to secondary actions were filtered out.

## Repository Structure
```text
├── fall/                      # Processed fall video clips (MP4 format)
├── non_fall/                  # Processed non-fall video clips (MP4 format)
├── Elimination samples (Kinematically inconsistent)/  
├── Detailed breakdown of prompts.csv                   
├── Fall_Generation_Log.csv
├── Non-Fall Generation Log.csv
└── README.md                  # Project documentation
```

## Getting Started

### Prerequisites
Ensure you have the following requirements installed before processing the dataset:
- Python 3.x
- OpenCV
- Pandas / NumPy

### Installation & Local Setup
Clone this repository to your local machine:
```bash
git clone https://github.com
cd T2V-Bed-Fall-Detection-Dataset
```

To update or upload changes from your local environment to this repository, use the following standard commands:
```bash
git add .
git commit -m "Add/Update dataset files"
git push origin main
```

## License
This dataset is openly and freely available to the public. You are welcome to use, modify, and distribute it for both academic and commercial purposes. 

Licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** License. 

* **Freedom to Use:** You can copy, redistribute, remix, and build upon the data for any purpose.
* **Attribution Required:** You must give appropriate credit, provide a link to this repository, and indicate if changes were made.
