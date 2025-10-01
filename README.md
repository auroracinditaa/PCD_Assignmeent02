# Image Enhancement Implementation using OpenCV

This project implements **image enhancement techniques** in Python using OpenCV.  
The program takes an input image, simulates degraded versions (blurred, dark, bright, and low-contrast), and then applies suitable enhancement methods to restore them.

---

## 🔹 Code Overview

1. **Upload and Read Image**
   - The image is uploaded using Google Colab’s `files.upload()` and then read with OpenCV (`cv2.imread`).

2. **Degradation Simulation**
   - `make_blurred`: applies Gaussian Blur to simulate a blurred image.  
   - `make_dark`: reduces brightness using `convertScaleAbs`.  
   - `make_bright`: increases brightness using `convertScaleAbs`.  
   - `make_low_contrast`: decreases image contrast.

3. **Enhancement Functions**
   - **Blurred → Sharpening filter** (kernel convolution).  
   - **Dark → Gamma correction (brightening)**.  
   - **Bright → Gamma correction (darkening)**.  
   - **Low-contrast → Histogram Equalization** on the Y channel in YCrCb color space.

4. **Visualization**
   - The results are displayed in a grid using Matplotlib.  
   - Each row shows a degraded image (input) and its enhanced result (output).  
   - The first row shows the original image (unchanged).

---

## 🔹 Output

The program produces a figure with 5 rows × 2 columns:

- Row 1: Original vs Original (unchanged)  
- Row 2: Blurred Image → Enhanced (Sharpened)  
- Row 3: Dark Image → Enhanced (Brightened)  
- Row 4: Bright Image → Enhanced (Darkened)  
- Row 5: Low-contrast Image → Enhanced (Equalized)

This demonstrates how different enhancement techniques can improve image quality depending on the type of degradation.

---

## 📖 References
- [GeeksforGeeks - Image Enhancement Techniques](https://www.geeksforgeeks.org/machine-learning/image-enhancement-techniques-using-opencv-python/)
