
## Features

- **PDF to JPG Conversion:**  
  Process PDFs one page at a time to reduce memory usage, saving each page as a separate JPG.

- **JPG to Mask Conversion:**  
  Generate binary masks from JPG images using a customizable threshold. This is useful for preprocessing before segmentation.

- **AdvancedTransUNet Segmentation Model:**  
  An enhanced U-Net variant that incorporates residual double convolution blocks, attention-based skip connections, and a transformer bottleneck for improved layout segmentation.

- **OCR Pipeline:**  
  A hybrid CNN+Transformer architecture designed for OCR tasks, complete with training, evaluation (using CER/WER), and visualization of error distributions.

- **Streamlit Web App:**  
  An interactive interface to upload images, convert them to binary masks, and run segmentation predictions using a pretrained AdvancedTransUNet model. The app also supports ngrok tunneling for public access.

## Setup

### Prerequisites

- Python 3.7+
- PyTorch and TorchVision
- PIL (Pillow)
- pdf2image
- Streamlit
- pyngrok
- Other dependencies: numpy, matplotlib, editdistance

You can install the required dependencies using `pip`. For example:

```bash
pip install torch torchvision pillow pdf2image streamlit pyngrok numpy matplotlib editdistance
Installation
Clone the repository:

bash
Copy
git clone https://github.com/yourusername/advanced-document-processing.git
cd advanced-document-processing
Set up the environment:
It is recommended to use a virtual environment.

bash
Copy
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
pip install -r requirements.txt  # If you have a requirements file.
Usage
PDF to JPG Conversion
Run the script to convert PDFs located in a specified folder into JPG images:

bash
Copy
python pdf_to_jpg.py
Make sure to update the pdf_folder and jpg_folder paths in the script as needed.

JPG to Binary Mask Conversion
Run the following script to convert your JPG images into binary masks:

bash
Copy
python jpg_to_mask.py
Ensure the directory paths are correctly set before execution.

Training the AdvancedSegmentation Model
The segmentation_model.py file contains the training and evaluation routines for the AdvancedTransUNet model. You can run it directly:

bash
Copy
python segmentation_model.py
This script loads images and corresponding masks, trains the model, and saves the trained weights as advanced_transunet_model.pth.

Training the OCR Model
The OCR model and its training routine are defined in ocr_model.py. To train the OCR model, run:

bash
Copy
python ocr_model.py
This script prepares the dataset, trains the Hybrid CNN+Transformer model using CTC loss, and evaluates the model using CER and WER metrics.

Running the Streamlit App
To launch the web app:

Run the Streamlit app:

bash
Copy
streamlit run app.py
Ngrok Integration:
If running in a notebook environment, the code in app.py automatically launches the Streamlit app and creates an ngrok tunnel. Update the ngrok auth token in the script with your own if necessary.

The Streamlit app lets you upload an image, view its binary mask, and see the segmentation output predicted by the AdvancedTransUNet model.

Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

License
This project is licensed under the MIT License. See the LICENSE file for details.

csharp
Copy

Simply copy this code into your `README.md` file in your repository.





