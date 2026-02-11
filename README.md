# Automated Image Processing Pipeline

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square\&logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=flat-square\&logo=opencv)
![Pytest](https://img.shields.io/badge/Testing-Pytest-yellow?style=flat-square\&logo=pytest)

## Project Overview

This project is a Python-based image processing automation tool designed to streamline the application of various computer vision techniques. The system monitors an `input/` directory, detects valid image files, and processes them through a pipeline of five distinct filters before saving the results to an `output/` directory.

This application was developed as a school assignment to demonstrate modular Python programming, file system manipulation, image processing using OpenCV, automated testing using PyTest, and basic DevOps automation through GitHub Actions.

## Key Features

The application automatically applies the following techniques to every image found in the input directory:

1. **Median Blur:** Reduces noise while effectively preserving edges.
2. **Grayscale Conversion:** Converts color images to black and white for structural analysis.
3. **Canny Edge Detection:** Identifies strong structural edges within the image.
4. **Emboss Filter:** Creates a 3D shadow effect, highlighting high-frequency details.
5. **Bilateral Filter:** Smoothes images while keeping edges sharp (advanced noise reduction).

## Project Structure

```text
Project/
├── .github/workflows       # GitHub Actions workflow configuration
├── input/                  # Place raw images here (.jpg, .png, etc.)
├── output/                 # Processed images will appear here
├── module/                 # Image processing modules
│   ├── median_blur.py
│   ├── grayscale.py
│   ├── canny_edge.py
│   ├── emboss_filter.py
│   ├── bilateral_filter.py
│   └── combine_filters.py
├── process_image.py        # Main execution script
├── test_script.py          # Ensures automation works properly
├── requirements.txt        # Project dependencies
└── README.md               # Project documentation
```

## Setup & Installation

### Prerequisites

* **Python 3.10+** (Recommended)
* **pip** (Python package manager)
* **Git**

### Installation Steps

1. **Clone the Repository**

```bash
git clone <repository_url>
cd automated-image-processing
```

2. **Install Dependencies**

```bash
pip install -r requirements.txt
```

or

```bash
python -m pip install -r requirements.txt
```

## Usage

1. **Add Images:**
   Place your raw images (`.jpg`, `.png`, `.jpeg`, `.bmp`, or `.tiff`) inside the `input/` folder.

2. **Push Changes to Trigger the CI Pipeline:**

```bash
git add .
git commit -m "your-image-name-here"
git push origin main
```

3. **View Results:**
   Processed images will appear inside the `output/` folder (e.g., `image_canny.jpg`, `image_median_blur.jpg`, etc.).

## Automation

This repository includes a GitHub Actions workflow that automatically runs the project whenever changes are pushed to the `main` branch.

The workflow:

1. Installs required dependencies
2. Runs the test script
3. Runs the image processing script
4. Saves generated output files
5. Commits updates if changes are detected

Workflow file location:

```text
.github/workflows/ci.yml
```

## DevOps Concepts Applied

* **Version Control**
* **GitHub Repository Hosting**
* **Continuous Integration**
* **Automated Testing**
* **Virtual Environment**
* **Deterministic and Reproducible Image Processing Pipeline**

## Academic Integrity

This project was developed as a school assignment.

For Students: Please use this code for reference and learning purposes only. Do not copy the code directly to submit as your own work.

## Authors

- **Asuncion, Andrei T.** – Developer 
- **De Leon, John Eron R.** – DevOps  
- **Apolonio, Lanz Matthew B.** – Automated QA Tester  
- **Ponelas, Joshua Efraim O.** – Presenter