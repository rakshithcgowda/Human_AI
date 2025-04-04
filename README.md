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


  ## Challenges and Learning

- **Data Quality and Preprocessing:**  
  Managing varying image quality and artifacts was challenging, which led to extensive experimentation with preprocessing techniques to ensure robust performance.

- **Balancing Model Complexity and Efficiency:**  
  Integrating advanced components like transformer bottlenecks and attention mechanisms improved segmentation accuracy but required careful tuning to maintain feasible training times and resource usage.

- **Handling OCR Variability:**  
  The OCR pipeline faced challenges with diverse fonts, layouts, and noise in input images, prompting iterative improvements to reduce Character Error Rate (CER) and Word Error Rate (WER).

- **Deployment and Integration:**  
  Creating a seamless Streamlit web app with ngrok tunneling for public access required overcoming hurdles related to model loading, inference speed, and user interface design.

- **Debugging and Iterative Learning:**  
  The project involved continuous debugging and refinement, which deepened understanding of both traditional CNNs and modern transformer architectures in computer vision tasks.


## High Level Design
![OCR Demo](External_Images/hig_level_design.png)



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

*Validation IoU* (Intersection over Union) = `98.31%`

-A higher IoU (closer to 1) indicates better segmentation performance. An IoU of 0.9831 means that 98.31% of the predicted mask aligns with the actual mask.

*Validation Dice Coefficient* = `99.15%`

-It is more sensitive to small segmentation errors. A Dice score of 0.9915 means that the predicted segmentation is 99.15% accurate in capturing the target regions.

- ### Specific Task 2 : *Optical Character Recognition*

-The OCR model was evaluated using Character Error Rate (CER), Word Error Rate (WER).

*CER = 0.293* → 29.3% of characters are incorrect. Lower is better.

*WER = 0.545* → 54.5% of words contain errors. Lower is better.



## **Running the Streamlit App**
- To launch the web app:

-Run the Streamlit app:

```bash
streamlit run app.py
```

**Ngrok Integration:**
If running in a notebook environment, the code in `app.py` automatically launches the Streamlit app and creates an ngrok tunnel. Update the ngrok auth token in the script with your own if necessary.


### The Streamlit app lets you upload an image, view its binary mask, and see the segmentation output predicted by the AdvancedTransUNet model.

## Preview

- **Specific Task I - Layout Organization Recognition**

![Project Banner](External_Images/gif_specific_1.gif)


- **Specific Task II - Optical Character Recognition (OCR)**

![Project Banner](External_Images/gif_specific_2.gif)




***Contributing:***
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

***License:***
This project is licensed under the [MIT License](LICENSE). See the LICENSE.txt file for details.




Simply copy this code block into your repository's `README.md` file.



