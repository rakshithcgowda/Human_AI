# Multi-Stage Document Processing and OCR Pipeline

This repository contains a multi-stage pipeline for processing documents and extracting information using deep learning. The project includes the following modules:

1. **PDF to JPG Conversion:**  
   Converts PDF files into JPG images. Each page of a PDF is saved as a separate JPG image.

2. **JPG to Binary Mask Conversion:**  
   Processes JPG images to create corresponding binary mask images based on a simple thresholding method.

3. **Layout Segmentation with TransUNet:**  
   Implements a TransUNet model that uses a U-Net architecture with a transformer in the bottleneck for layout segmentation tasks (e.g., separating background from main text).

4. **Word Document to OCR Data Extraction:**  
   Extracts text from Microsoft Word documents (.docx) and renders each paragraph/page as an image and text file.

5. **OCR with a Hybrid CNN+Transformer Model:**  
   A hybrid deep learning model for optical character recognition (OCR) that combines a CNN backbone for spatial feature extraction with a Transformer encoder for sequence modeling. The model is trained with CTC loss and evaluated using Character Error Rate (CER) and Word Error Rate (WER).

## Repository Structure


## Requirements

Ensure you have Python 3.7 or higher installed. The following Python packages are required:

- `Pillow`
- `pdf2image`
- `torch`
- `torchvision`
- `python-docx`
- `numpy`
- `editdistance`
- `matplotlib`

You can install the required dependencies using `pip`:

```bash
pip install pillow pdf2image torch torchvision python-docx numpy editdistance matplotlib
