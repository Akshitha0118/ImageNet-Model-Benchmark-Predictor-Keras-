# 🧠 ImageNet Model Benchmark Predictor(Keras) 

An end-to-end deep learning project that performs **image classification using multiple pretrained CNN architectures** from **Keras Applications**, with an **interactive frontend** and **CPU vs GPU performance benchmarking**.

---

## 🚀 Project Overview

This project provides a unified framework to run inference on images using **multiple ImageNet-trained deep learning models** through a **single, reusable pipeline**.  
Users can upload an image, select a model, and instantly receive top predictions along with execution time.

---

## 🧩 Supported Models

- VGG16, VGG19  
- ResNet50, ResNet50V2, ResNet101, ResNet101V2, ResNet152, ResNet152V2  
- InceptionV3, InceptionResNetV2, Xception  
- MobileNet, MobileNetV2  
- DenseNet121, DenseNet169, DenseNet201  
- NASNetMobile, NASNetLarge  
- EfficientNet (B0–B7)  
- EfficientNetV2 (B0–B3, S, L)  
- ConvNeXt (Tiny, Small, Base, Large)

---

## 🖥️ Frontend

The project includes an **interactive Gradio-based frontend** that allows:
- Image upload
- Model selection via dropdown
- Real-time prediction results
- User-friendly interface for demos and deployment

---

## ⚙️ Code Flow

1. **Model Registry**  
   All supported models are stored in a centralized dictionary with:
   - Model loader  
   - Input image size  
   - Preprocessing function  
   - Decoder logic  

2. **Dynamic Model Selection**  
   A single function loads the selected model dynamically.

3. **Image Preprocessing**  
   Input images are resized and normalized based on the selected architecture.

4. **Prediction Pipeline**  
   - Forward pass  
   - Top-k ImageNet class decoding  

5. **Performance Tracking**  
   - Per-model inference time  
   - Total execution time measurement  

---

## ⏱️ Performance Comparison (CPU vs GPU)

| Platform | Total Execution Time |
|--------|----------------------|
| VS Code (CPU) | ~ 6–12 minutes (model dependent) |
| Google Colab (GPU) | **4.93 seconds** |

> GPU acceleration significantly improves inference speed, especially for large models such as VGG19, NASNetLarge, and EfficientNet variants.

---

## 🚧 Challenges & Solutions

| Challenge | Solution |
|--------|---------|
Long inference time on CPU | Migrated benchmarking to GPU |
High memory usage | Dynamic model loading & session clearing |
Different preprocessing per model | Centralized model configuration |
Code duplication | Unified prediction function |
User accessibility | Added Gradio frontend |

---

## 🛠️ Tech Stack

- Python  
- TensorFlow / Keras  
- NumPy  
- Gradio  
- Google Colab  
- VS Code  

---

