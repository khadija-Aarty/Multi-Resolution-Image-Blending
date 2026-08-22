<div align="center">

# 🖼️ Multi-Resolution Image Blending using Gaussian & Laplacian Pyramids

**Seamless image compositing through multi-scale pyramid decomposition**

</div>

---

## 📌 Overview

Multi-resolution image blending is a classic technique in digital image processing and computer vision for combining two images into a single, visually realistic composite. Instead of merging images directly at the pixel level — which tends to produce visible seams and abrupt transitions — this project blends images **across multiple scales** using **Gaussian and Laplacian pyramids**, producing smooth, natural-looking transitions while preserving fine edge details.

## 🎯 Objectives

- Implement image blending using Gaussian and Laplacian pyramids
- Produce smooth transitions between two images using a gradient mask
- Preserve edges and fine details throughout the blending process
- Compare pyramid-based blending against basic direct/pixel-level blending

## 🔍 How It Works

1. **Load & Preprocess** — Load two input images, resize to a common target size, and normalize pixel values
2. **Mask Creation** — Generate a gradient blending mask that defines how the two images transition into each other
3. **Gaussian Pyramids** — Build multi-level Gaussian pyramids for both images (repeated smoothing + downsampling) and for the mask
4. **Laplacian Pyramids** — Derive Laplacian pyramids from the Gaussian pyramids to capture edge and detail information at each scale
5. **Pyramid Blending** — Blend each corresponding level of the two Laplacian pyramids using the Gaussian pyramid of the mask
6. **Reconstruction** — Collapse the blended pyramid back into a single full-resolution image
7. **Comparison** — Compare the pyramid-blended result against a naive direct blend to demonstrate the reduction in visible seams and artifacts

## 📊 Result

The pyramid-based blend produces significantly smoother transitions and fewer visible seams compared to direct/basic blending, while preserving sharp edges and fine texture detail from both source images — demonstrating the core advantage of multi-scale image representation over single-scale pixel operations.

## 🛠️ Tech Stack

`Python` · `OpenCV` · `NumPy` · `Matplotlib` · `Google Colab`

## 🚀 How to Run

1. Open `multi_resolution_image_blending.ipynb` in Google Colab (or Jupyter Notebook)
2. Mount Google Drive / update the image paths to point to your own input images
3. Run all cells sequentially — the notebook is organized into clearly labeled steps (loading, preprocessing, pyramid construction, blending, reconstruction, and comparison)

## 📁 Repository Structure

```
Multi-Resolution-Image-Blending/
├── multi_resolution_image_blending.ipynb   # Full implementation and walkthrough
├── IEEE_Project_Report.pdf                 # Detailed project report (IEEE format)
└── README.md
```

## 👥 Team

Developed as a team project for an academic computer vision course.

Maintained here by: **Khadija Tul Kobra** — [GitHub](https://github.com/khadija-Aarty)
