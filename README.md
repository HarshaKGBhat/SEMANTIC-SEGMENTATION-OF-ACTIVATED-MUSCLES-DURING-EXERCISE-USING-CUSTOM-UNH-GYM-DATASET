🏋️# SEMANTIC-SEGMENTATION-OF-ACTIVATED-MUSCLES-DURING-EXERCISE-USING-CUSTOM-UNH-GYM-DATASET
This is an Academic Project of Deep Learning course . Contributors are Gururaj Somanna and Harsha Keladi Ganapathi
📌 Overview
This project implements a U-Net based semantic segmentation model with a ResNet-34 encoder to detect and segment activated muscle regions during various exercises. The dataset was collected from the University of New Haven (UNH) gym, annotated using Roboflow, and consists of images showing biceps, triceps, and calf muscle activation.

The model can help in:

Sports science & fitness tracking

Injury prevention

Anatomical analysis

📂 Dataset
The dataset consists of:

Total images: 520 (256×256 resolution)

Classes:

0 – Background

1 – Activated Biceps

2 – Activated Triceps

3 – Activated Calf

📎 Dataset link: https://app.roboflow.com/jim-ps1mt/jim_sem/browse?queryText=&pageSize=50&startingIndex=0&browseQuery=true

Images were annotated pixel-wise and augmented with flips, shearing, grayscale, Gaussian blur, and random noise to improve generalization.

⚙️ Methodology
Model Architecture
Encoder: ResNet-34 backbone (pretrained on ImageNet)

Decoder: U-Net style with skip connections

Output: 4-channel segmentation mask (background + 3 muscle classes)

Training Details
Loss Function: Cross-Entropy Loss

Optimizer: Adam

Learning Rate Scheduler: StepLR

Best Hyperparameters:

Learning rate: 1e-4

Batch size: 16

Epochs: 30

📊 Results
Training Accuracy: 94.5%

Validation Accuracy: 92.3%

mIoU: 0.51

Qualitative results show good alignment between predictions and ground truth, especially for clear muscle boundaries.

Metric	Train Set	Val Set
Loss	0.13	0.17
Pixel Acc	94.5%	92.3%
mIoU	0.58	0.51

🚀 Deployment
The trained model is deployed via Gradio for interactive testing on images and videos.
Users can upload exercise images and see the segmented muscle activation regions in real-time.

📦 Installation & Usage
bash
Copy
Edit
# Clone the repository
git clone https://github.com/yourusername/muscle-activation-segmentation.git
cd muscle-activation-segmentation

# Install dependencies
pip install -r requirements.txt

# Train the model
python train.py

# Run inference
python inference.py --image path/to/image.jpg
🔗 References
Human Pose Estimation Using MediaPipe

Neural Muscle Activation Detection

INet: Biomedical Image Segmentation

👨‍💻 Authors
Harsha Keladi Ganapathi

Gururaj Somanna
