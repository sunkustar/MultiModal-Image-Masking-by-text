# Text-Based Image Masking

This project focuses on a **multimodal task** where the goal is to mask regions of an image based on textual descriptions. The model combines image and text modalities to generate accurate masks that align with the given instructions.

---

## Dataset

The **Magic Brush** dataset is used for training and evaluation. This dataset provides diverse images and associated text descriptions, making it ideal for this multimodal image masking task.

![image](https://github.com/user-attachments/assets/d131fe20-db05-4aef-b1bb-02e6168c2244)


---

## Architecture

The architecture integrates both image and text modalities through a hybrid design:

- **Image Encoder**: A Customized CNN-based backbone ( ResNet50 ) extracts high-level image features.
- **Text Encoder**: A transformer-based model (e.g., BERT or CLIP) encodes the textual description.
- **Fusion Module**: Combines encoded features from both modalities through cross attention
- **Masking Head**: Outputs a pixel-wise segmentation mask based on the combined features.

Below is a diagram of the architecture:

![Architecture]![image](https://github.com/user-attachments/assets/aedd75c7-005d-43f0-aaeb-4d7df3999c6e)


---

## Training Results

After training the model on the Magic Brush dataset for 200 epochs, the following performance metrics were achieved:

![image](https://github.com/user-attachments/assets/f8195aae-1e8a-43a8-8f03-efe25d6b167b)

- **Mean Intersection over Union (mIoU)**: 96.1%

we also tried with some other achitectures and loss functions details are mentioned in the report.pdf


## Sample Results

Sample Result:
![image](https://github.com/user-attachments/assets/0996ca8f-3077-4619-9724-e33176cf0b28)
![image](https://github.com/user-attachments/assets/03e57903-892b-4ffa-8ccb-bf026f90ec3d)
![image](https://github.com/user-attachments/assets/a54218e0-ed84-4e73-ab82-c01bac5097e5)


## Try it 

download the models from drive link given models.txt
use environment.yml to create compatable conda env


## Acknowledgments

We thank the creators of the **Magic Brush** dataset and open-source frameworks like PyTorch and Hugging Face Transformers for enabling this work.


