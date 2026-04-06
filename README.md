
# 🏥 Medical Image Compression using SVD

**Linear Algebra Mini Project (UE24MA241B)**

---

## 🎯 Project Overview

This project demonstrates a complete **Linear Algebra pipeline** applied to real-world medical images.
We use **Singular Value Decomposition (SVD)** to compress images while preserving diagnostic quality.

### 🔄 Workflow:

* Data preprocessing
* Matrix analysis (RREF, rank, nullity)
* SVD-based decomposition
* Projection and reconstruction
* Final evaluation using quality metrics

---

## 📁 Notebook-wise Breakdown

---

### 🔹 Notebook 1: Data Processing & RREF Analysis (Person 1)

#### ✅ Key Tasks:

* Load and preprocess medical images
* Convert images into **512 × 512 grayscale matrices**
* Perform **RREF analysis** on submatrices
* Compute **rank and nullity**
* Generate dataset metadata

#### 💡 Key Insight:

* Rank < dimension ⇒ **redundancy exists**
* Confirms that **compression is possible**

#### 📤 Output:

* Processed image dataset
* RREF results (rank, nullity, pivot columns)
* Metadata summary
* Saved as: `person1_data.pkl`

---

### 🔹 Notebook 2: SVD & Space Analysis (Person 2)

#### ✅ Key Tasks:

* Perform SVD decomposition:

  ```
  A = U Σ Vᵀ
  ```
* Analyze singular value spectrum
* Compute cumulative energy
* Select optimal k values (90%, 95%, 99%)

#### 💡 Key Insight:

* Rapid decay of singular values ⇒ **high redundancy**
* Most image information captured in **few components**

#### 📤 Output:

* Singular values
* Energy plots
* Optimal k values for compression

---

### 🔹 Notebook 3: Orthogonalization & Projection (Person 3)

#### ✅ Key Tasks:

* Verify orthogonality of U and V

* Perform low-rank projection

* Reconstruct compressed images using:

  ```
  A_k = U_k Σ_k V_kᵀ
  ```

#### 💡 Key Insight:

* Projection reduces dimensionality
* Maintains important features while removing redundancy

#### 📤 Output:

* Reconstructed (compressed) images
* Error maps
* Orthogonality validation

---

### 🔹 Notebook 4: Evaluation & Final Metrics (Person 4)

#### ✅ Key Tasks:

* Evaluate compression quality using:

  * PSNR (Peak Signal-to-Noise Ratio)
  * SSIM (Structural Similarity Index)
* Compute compression ratio
* Perform eigenvalue analysis

#### 💡 Key Insight:

* SVD provides **optimal low-rank approximation**
* High PSNR & SSIM ⇒ **quality preserved after compression**

#### 📤 Output:

* Quality metrics for all images
* Final comparison results
* Saved as: `person4_data.pkl`

---

## 📊 Final Results

* Compression ratio: **~10×**
* Energy retained: **>95%**
* Average PSNR: **~33 dB**
* Average SSIM: **~0.96**

👉 Indicates **high-quality compression with minimal loss**

---

## 💡 Key Takeaways

* Medical images contain **significant redundancy**
* SVD efficiently captures dominant patterns
* Compression–quality tradeoff can be controlled using **k**
* Linear Algebra concepts have strong **real-world applications**

---

## 🏥 Applications

* Telemedicine (faster image transfer)
* Medical data storage optimization
* Mobile diagnostics
* Healthcare cloud systems

---

## 👥 Team Contribution

| Member   | Contribution                       |
| -------- | ---------------------------------- |
| Aakash Desai | Data preprocessing, RREF, metadata |
| Abhinav A | SVD decomposition, energy analysis |
| Aadhavan Muthusamy | Projection, reconstruction         |
| Adarsh Rajesh | Metrics, evaluation, results       |

---

If you want one last upgrade:
👉 I can compress this into a **“30-sec README pitch”** (what you say if prof asks *“Summarize your project”*) 💯
