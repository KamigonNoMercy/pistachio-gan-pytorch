# 🌰 Pistachio GAN with FID Evaluation (PyTorch)

This project implements a **Generative Adversarial Network (GAN)** using **PyTorch** to generate pistachio images.  
The goal is to train a generator that can create realistic pistachio images, while the discriminator learns to distinguish real from fake.  
The quality of generated images is measured with the **Frechet Inception Distance (FID)**.

---

## 🎥 Analysis Video
Watch the analysis walkthrough here:  
👉 https://drive.google.com/file/d/1uE5f2D5-Q1tFESeJnCoWw2HQpAmH7s-u/view?usp=sharing

---

## 📊 Dataset

The dataset consists of **pistachio images** with a black background.  
All images are in **.jpg format** and of consistent dimensions.

### Preprocessing
- Images split into **train/test** sets (`train_test_split`).  
- Resized and normalized to `[0, 1]` for GAN input.  
- Loaded into PyTorch `Dataset` and `DataLoader`.

---

## ✨ Highlights

- **Model Architecture**
  - **Generator**: takes random latent vectors (`z`) and produces synthetic pistachio images.  
  - **Discriminator**: binary classifier distinguishing real from generated images.  

- **Training Setup**
  - Framework: **PyTorch** (`torch.nn`, `torch.optim`)  
  - Loss: Binary Cross-Entropy (BCE)  
  - Optimizer: Adam  
  - Training loop alternates generator & discriminator updates.  

- **Evaluation**
  - **Frechet Inception Distance (FID)** computed via `torchmetrics.image.FrechetInceptionDistance`.  
  - Lower FID → generated images closer to real distribution.  
  - Visual comparison of **real vs generated samples**.

---

## 📂 Repository Layout
```
pistachio-gan-pytorch/
├─ notebook/
│ └─ pistachio-gan.ipynb
├─ README.md
├─ requirements.txt
├─ LICENSE
└─ .gitignore
```
---

## 🛠 Environment

Install dependencies:
```bash
pip install -r requirements.txt
```

## 🚀 Run the Notebook
```
jupyter notebook notebook/pistachio-gan.ipynb
```
