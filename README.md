# DCT + DWT Hybrid Image Watermarking 🖼️🔒

This project implements a **hybrid image watermarking system** using **Discrete Wavelet Transform (DWT)** and **Discrete Cosine Transform (DCT)**.  
The objective is to embed a watermark image inside a host (cover) image so that it remains **invisible to the human eye** while being **robust to distortions** such as noise and compression.

---

## 🔧 How it Works
1. **Wavelet Decomposition (DWT):**  
   The host image is decomposed into subbands (LL, LH, HL, HH) using a 1-level Haar wavelet transform.  

2. **Frequency Transformation (DCT):**  
   The chosen subband is transformed using DCT to obtain frequency coefficients.  

3. **Watermark Embedding:**  
   The watermark is embedded into mid-frequency coefficients using a scaling factor (*alpha*).  

4. **Reconstruction:**  
   Inverse DCT and IDWT are applied to generate the **watermarked image**.  

5. **Watermark Extraction:**  
   The process is reversed to **recover the watermark** from the watermarked image.

---

## 📊 Evaluation
- **MSE (Mean Squared Error)** and **PSNR (Peak Signal-to-Noise Ratio)** are computed between the original and watermarked images.  
- A PSNR value **above 30 dB** typically indicates good imperceptibility (watermark is invisible).  

---

## ✅ Applications
- **Digital copyright protection** – secure image ownership with invisible marks.  
- **Tamper detection** – reveal modifications made to images.  
- **Robust storage** – hybrid DWT+DCT watermarking resists compression, noise, and filtering better than spatial-only methods.  

---

## 📉 Example Results
*(Replace with your own images/plots once generated)*

| Original Image | Watermarked Image | Extracted Watermark |
|----------------|-------------------|----------------------|
| ![Original](assets/original.png) | ![Watermarked](assets/watermarked.png) | ![Watermark](assets/recovered.png) |

---
