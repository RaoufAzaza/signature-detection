#PDF Signature Detection for Subscribers

This project aims to detect and highlight specific signatures in PDF documents, focusing on those that belong to subscribers. The final page of the provided PDF is processed, and only relevant signatures matching specific criteria are displayed on the annotated output image.

#Features

Extracts and processes the last page of a PDF document for signature detection.

Utilizes advanced machine learning models via the Roboflow API for signature detection.

Filters detections to retain only those matching specific characteristics (e.g., aspect ratio, size, confidence).

Annotates detected signatures directly on the image and displays the results.

Provides detailed coordinates of detected signatures for further analysis.

#How It Works

PDF Conversion

The last page of the input PDF is converted into an image using the pdf2image library.

Signature Detection

The image is sent to a pretrained signature detection model hosted on the Roboflow platform.

Detections are filtered based on:

Confidence level: > 60%.

Aspect ratio: Between 2.0 and 6.0.

Size constraints: Height between 50px and 300px.

#Result Visualization

Detected signatures are annotated on the image with red rectangles.

Coordinates and confidence scores for each signature are printed.

#Output

Annotated image is displayed using Matplotlib.

A detailed log of detected signatures is provided in the console.

#Technologies Used

Python for scripting and automation.

OpenCV for image processing and annotation.

Matplotlib for visualization.

Roboflow API for inference with a pretrained signature detection model.

pdf2image and Poppler for PDF to image conversion.
