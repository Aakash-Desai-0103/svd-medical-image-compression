# Medical Image Compression using SVD

Linear Algebra Mini Project (UE24MA241B)  
PES University | April 2026  

---

## 📌 Overview

This project demonstrates the application of **Singular Value Decomposition (SVD)** for compressing medical images while preserving important visual information.

We apply core Linear Algebra concepts such as:
- Matrix representation
- Rank and RREF
- Orthogonality
- Projection
- Eigenvalues and diagonalization

---

## 📊 Dataset

- Total images: 18  
- Categories:
  - Chest X-rays (6)
  - CT Scans (6)
  - MRI Images (6)
- All images resized to **512 × 512 grayscale**

---

## ⚙️ Methodology

The compression pipeline:

1. Convert images to matrix form  
2. Perform RREF and analyze rank  
3. Apply SVD: `A = UΣVᵀ`  
4. Select optimal rank (`k = 50`)  
5. Verify orthogonality of U and V  
6. Project onto lower-dimensional space  
7. Apply least squares approximation  
8. Perform eigenvalue analysis  

---

## 📈 Results

- Compression Ratio: ~10×  
- Energy Retained: ~95%+  
- Reconstruction Error: ~10⁻¹⁰ (≈ 0%)  
- PSNR: ~33 dB  
- SSIM: ~0.96  

The compressed images retain almost all important features with minimal loss.

---

## 🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook
Open:

notebooks/Master_DEMO.ipynb

Run all cells.
```
---

## 👥 Team

- Aakash Desai: Data Loading, RREF  
- Abhinav Agraharam: SVD, Space Analysis  
- Aadhavan Muthusamy: Orthogonalization, Projection  
- Adarsh Rajesh: Eigenvalues, Final Metrics  

---

## 📌 Conclusion

SVD enables efficient compression of medical images by removing redundancy while maintaining high visual quality.
This demonstrates how theoretical Linear Algebra concepts can be applied to real-world problems.

---
