# 🏥 FedGDA – Federated Medical Image Segmentation

A research-oriented federated learning framework for multi-organ medical image segmentation using Attention U-Net and FedGDA (Federated Server-Guided Dynamic Alignment).

This project focuses on improving segmentation performance under non-IID client data distributions in federated learning environments while preserving data privacy.

---

# 📌 Project Overview

Medical image segmentation plays a critical role in healthcare applications such as:
- Organ localization
- Disease diagnosis
- Surgical planning
- Treatment monitoring

Traditional centralized deep learning approaches require transferring sensitive medical data to a central server, raising privacy and security concerns.

This project explores:
- Federated Learning for distributed medical segmentation
- Attention U-Net architecture
- Non-IID client data simulation
- FedAvg baseline comparison
- Server-guided data alignment (FedGDA)
- Federated vs centralized performance evaluation

---

# 🧠 Objectives

The project focuses on:

✅ Multi-organ CT image segmentation  
✅ Federated learning under non-IID settings  
✅ Comparison of centralized and federated learning  
✅ Improving federated segmentation performance using FedGDA  
✅ Dice score evaluation and visualization  

---

# 🏗 System Architecture

```text
Client CT Data
      ↓
Local Attention U-Net Training
      ↓
Federated Aggregation (FedAvg / FedGDA)
      ↓
Global Model Update
      ↓
Segmentation Prediction
      ↓
Performance Evaluation (Dice Score)
```

---

# 🛠 Technologies Used

- Python
- PyTorch
- NumPy
- Matplotlib
- Federated Learning
- Attention U-Net
- Medical Image Processing
- CT Image Segmentation
- Jupyter Notebook

---

# 🧪 Model Architecture

## Attention U-Net

The project uses an Attention U-Net architecture for accurate multi-organ segmentation from CT scans.

### Key Features
- Encoder-decoder segmentation architecture
- Attention gates for region-focused learning
- Multi-class organ segmentation
- Dice + BCE combined loss function

---

# 📂 Dataset

The project uses abdominal CT image slices for multi-organ segmentation.

### Segmented Organs
- Liver
- Spleen
- Left Kidney
- Right Kidney
- Pancreas

---

# ⚙️ Training Workflow

## 1️⃣ Data Preprocessing
- CT slice normalization
- Mask preparation
- Multi-organ label generation
- Dataset partitioning across clients

---

## 2️⃣ Centralized Training
A centralized Attention U-Net baseline was trained using combined client datasets.

### Results
- Mean Dice Score: **0.9069**

---

## 3️⃣ Federated Learning Setup
Federated learning was implemented using:
- Multiple simulated clients
- Local model updates
- Federated averaging (FedAvg)
- Non-IID data distribution

---

## 4️⃣ FedGDA Alignment
FedGDA was introduced to improve federated segmentation performance through server-guided data alignment.

### Purpose
- Reduce client distribution mismatch
- Improve generalization
- Stabilize federated training

---

# 📊 Training Performance

## Training History

### Combined Dice + BCE Loss
- Training and validation loss decreased consistently during training.
- Stable convergence observed across epochs.

### Mean Dice Score
- Dice score improved steadily and exceeded the target threshold of **0.75**.
- Final validation Dice score achieved approximately **0.90** during centralized training.

---

# 📈 Federated Learning Results

## Federated Training Analysis

### Average Client Loss
Federated client loss decreased gradually across communication rounds, indicating stable optimization.

### Dice Score Across Rounds
- Best Federated Dice Score: **0.851**
- Centralized Dice Score: **0.909**

The federated model achieved strong segmentation performance despite non-IID client distributions.

---

# 🖼 Visualization Outputs

The project includes:

✅ Training curves  
✅ Dice score progression  
✅ Federated learning convergence plots  
✅ Prediction visualizations  
✅ Centralized vs federated comparisons  
✅ Ground truth vs predicted segmentation overlays  

---

# 🔬 Centralized vs Federated Comparison

The segmentation outputs demonstrate:

- Centralized training achieves slightly higher segmentation accuracy.
- Federated learning maintains competitive performance while preserving data privacy.
- FedGDA alignment improves stability and prediction consistency under non-IID settings.

---

# 🧠 Segmentation Prediction Results

The model successfully segmented:
- Liver
- Spleen
- Kidneys
- Pancreas

Prediction outputs show strong overlap with ground truth masks across multiple CT slices.

---

# 📊 Performance Summary

| Model | Dice Score |
|---|---|
| Centralized Attention U-Net | 0.9069 |
| Federated Learning (Best) | 0.851 |

---

# 💻 Training Environment

The model was trained using Jupyter Notebook with GPU acceleration.

### Hardware Configuration
- GPU: NVIDIA DGX A100 (10 GB GPU Memory)
- CPU: 8 vCPUs
- RAM: 32 GB

### Framework
- PyTorch with CUDA acceleration

# 📁 Project Structure

```bash
fedgda-medical-image-segmentation/
│
├── notebooks/
│   └── my_training.ipynb
│
├── outputs/
│   ├── centralized_vs_federated.png
│   ├── federated_predictions_aligned.png
│   ├── federated_vs_baseline.png
│   ├── predictions.png
│   └── training_curves.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# 📌 Key Learnings

Through this project, I learned:

- Federated learning workflows
- Medical image segmentation
- Attention U-Net implementation
- Handling non-IID client distributions
- Federated averaging (FedAvg)
- Dice score evaluation
- Multi-organ segmentation
- Federated model comparison and visualization

---

# 🚀 Future Improvements

Possible future enhancements include:

- Advanced FedGDA optimization
- Communication-efficient federated learning
- Transformer-based medical segmentation
- Differential privacy integration
- Real multi-hospital federated deployment
- 3D volumetric segmentation
- Adaptive client weighting strategies

---

# 👩‍💻 Author

## Sanjana R

- GitHub: https://github.com/r-sanjana
