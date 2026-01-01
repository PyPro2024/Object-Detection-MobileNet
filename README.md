# Object Detection with TensorFlow Hub

![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat&logo=tensorflow)
![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![TF Hub](https://img.shields.io/badge/TF%20Hub-Pretrained%20Models-blueviolet)

##  Project Overview
This project implements an **Object Detection** system using pre-trained models hosted on **TensorFlow Hub**. Unlike training a model from scratch, this approach leverages "Transfer Learning" to achieve high-accuracy detection with minimal setup and computational cost.

The goal is to load a robust pre-trained model (e.g., SSD MobileNet) and perform inference on arbitrary images to detect, classify, and localize objects with bounding boxes.

##  Model & Approach
* **Source:** TensorFlow Hub (Repository of trained machine learning models).
* **Architecture:** Utilizes Single Shot Multibox Detector (SSD) architectures (like MobileNet or Inception) trained on the **COCO Dataset**.
* **Advantage:** Allows for immediate deployment without the need for massive datasets or days of training time.

## Tech Stack
* **Deep Learning:** TensorFlow, TensorFlow Hub
* **Image Processing:** OpenCV, Pillow (PIL)
* **Visualization:** Matplotlib
* **Data Handling:** NumPy

##  Capabilities
1.  **Image Loading:** Preprocesses local images into the required tensor format.
2.  **Inference:** Runs the image through the pre-trained graph to obtain:
    * **Detection Boxes:** Coordinates of the object $(ymin, xmin, ymax, xmax)$.
    * **Detection Scores:** Confidence level of the prediction (0.0 to 1.0).
    * **Detection Classes:** The label index (mapped to COCO class names).
3.  **Visualization:** Draws labeled bounding boxes on the original image for verification.

## How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/PyPro2024/Object-Detection-MobileNet.git]
    ```
2.  **Install dependencies:**
    ```bash
    pip install tensorflow tensorflow-hub matplotlib numpy opencv-python
    ```
3.  **Run the Notebook:**
    Open `Object_Det_PretrainedModel.ipynb` in Jupyter Notebook or Google Colab.
    * *Note: Ensure you have an image named `cat.png` (or update the path) to test the inference.*

##  Results
The model successfully identifies objects in complex scenes.
* **Example:** Inputting an image of a cat results in a bounding box labeled "Cat" with high confidence (>90%).

---
*If you find this project helpful, feel free to ⭐ the repo!*
