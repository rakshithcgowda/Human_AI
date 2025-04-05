# Text Recognition with Transformer Models


![Project Banner](External_Images/image.png)
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


You can install the required dependencies using `pip`. For example:

```bash
pip install torch torchvision pillow pdf2image streamlit pyngrok numpy matplotlib editdistance
```


### Prerequisites

- `Python 3.7+`
- `PyTorch and TorchVision`
- `PIL (Pillow)`
- `pdf2image`
- `Streamlit`
- `pyngrok`

**Installation**
- Other dependencies: numpy, matplotlib, editdistance
- Clone the repository:

**Installation**
- Other dependencies: numpy, matplotlib, editdistance
- Clone the repository:

```bash
git clone https://github.com/yourusername/Human_AI.git
cd Human_AI
```

## Results
- ### Specific Task 1 : *Layout Organization Recognition*

*Validation IoU* (Intersection over Union) = `96.66%`

-A higher IoU (closer to 1) indicates better segmentation performance. An IoU of 0.9666 means that 96.66% of the predicted mask aligns with the actual mask.

*Validation Dice Coefficient* = `98.27%`

-It is more sensitive to small segmentation errors. A Dice score of 0.9827 means that the predicted segmentation is 98.27% accurate in capturing the target regions.

- ### Specific Task 2 : *Optical Character Recognition*

-The OCR model was evaluated using Character Error Rate (CER), Word Error Rate (WER).

*CER = 0.293* → 29.3% of characters are incorrect. Lower is better.

*WER = 0.563* → 56.3% of words contain errors. Lower is better.



## **Running the Streamlit App**
- To launch the web app:

-Run the Streamlit app:

```bash
streamlit run app.py
```

**Ngrok Integration:**
If running in a notebook environment, the code in `app.py` automatically launches the Streamlit app and creates an ngrok tunnel. Update the ngrok auth token in the script with your own if necessary.


### The Streamlit app lets you upload an image, view its binary mask, and see the segmentation output predicted by the AdvancedTransUNet model.

-- **Specific Task I - Layout Organization Recognition**

![Project Banner](External_Images/gif_specific_1.gif)


- **Specific Task II - Optical Character Recognition (OCR)**

![Project Banner](External_Images/gif_specific_2.gif)




***Contributing:***
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

***License:***
This project is licensed under the [MIT License](LICENSE). See the LICENSE.txt file for details.




Simply copy this code block into your repository's `README.md` file.



