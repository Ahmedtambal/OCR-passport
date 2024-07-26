# OCR-passport

This project implements an Optical Character Recognition (OCR) system for extracting text and bounding box coordinates from images containing English text. Additionally, it includes functionality for extracting specific passport data from images using EasyOCR and Tesseract.

## Features

- Extract text from images using Tesseract OCR.
- Draw bounding boxes around detected text and return their coordinates.
- Extract specific passport data (e.g., name, date of birth, issuing authority) using EasyOCR.
- Process and visualize images in both grayscale and RGB.

## Installation
1. **Install the required dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

    The `requirements.txt` file should include:
    ```
    opencv-python
    matplotlib
    pytesseract
    passporteye
    easyocr
    python-dateutil
    ```

2. **Download and set up Tesseract OCR:**

    - Follow the instructions to install Tesseract OCR from [here](https://github.com/tesseract-ocr/tesseract).
    - Ensure that the Tesseract executable is in your system's PATH.
  

Approach
Pre-processing Steps
Grayscale Conversion: Images are first converted to grayscale for better OCR performance.
Bounding Box Drawing: Bounding boxes are drawn around detected text segments to visualize the OCR results.
Libraries Used
OpenCV: For image processing and visualization.
Matplotlib: For plotting images and bounding boxes.
Tesseract OCR: For text extraction from images.
EasyOCR: For extracting passport data from MRZ zones.
PassportEye: For reading MRZ zones from passport images.
Dateutil: For parsing dates in various formats.
Json: For handling country codes and output data.
Rationale Behind Algorithmic Choices
Tesseract OCR: Chosen for its robustness and open-source nature, making it ideal for general OCR tasks.
EasyOCR: Selected for its pre-trained models on multiple languages, including English, making it suitable for passport data extraction.
PassportEye: Used for its specialized capabilities in reading MRZ zones from passport images, which is crucial for accurate data extraction.

