# Lab_Task_10_DIP

# *Task 10: Image Compression Using DCT & Huffman Coding*

*Roll Number:* 2023-SE-02

### *Prompt*

*"Implement a complete image compression workflow in Python using OpenCV, NumPy, and Matplotlib, compatible with Google Colab. The program should:

* Allow interactive image upload (JPEG/PNG) in Colab.
* Perform JPEG-like DCT compression on each color channel using an 8×8 block size and a standard JPEG quantization matrix (allow scaling for visible compression).
* Apply Huffman coding to the quantized DCT coefficients of each channel and generate bitstreams.
* Compute compression metrics:

  * Compression Ratio (CR)
  * Mean Squared Error (MSE)
  * Peak Signal-to-Noise Ratio (PSNR)
  * Rate Distortion (RD)
* Display: Original image, Compressed image, Amplified difference image between original and compressed.
* Print all computed metrics.
* Ensure the code is robust, fully Colab-compatible, handles color images, and clearly separates all steps. Use amplified differences to highlight compression artifacts."*

---

## *Objective*

The objective of this task is to implement a *JPEG-like image compression workflow* using *DCT (Discrete Cosine Transform)* and *Huffman coding*, and evaluate the compression performance using key metrics (CR, MSE, PSNR, RD). Additionally, visual differences between the original and compressed image are highlighted to analyze artifacts.

---

## *Methodology / Approach*

1. Upload a color image (JPEG/PNG) safely in Google Colab.
2. Split the image into *RGB channels* and perform block-wise (8×8) *DCT compression*:

   * Center pixel values around 0.
   * Apply standard JPEG quantization matrix (scalable).
   * Quantize, dequantize, and apply *inverse DCT* to reconstruct each channel.
3. Merge reconstructed channels to form the *compressed color image*.
4. Apply *Huffman coding* to each channel’s quantized DCT coefficients to generate compressed bitstreams.
5. Compute key *compression metrics*:

   * *Compression Ratio (CR):* Original bits / Compressed bits
   * *Mean Squared Error (MSE):* Pixel-wise error
   * *PSNR:* Signal-to-noise ratio in dB
   * *Rate Distortion (RD):* Compressed bits per unit MSE
6. Create an *amplified difference image* to visualize compression artifacts.
7. Display original image, compressed image, and difference image side by side for visual comparison.
8. Print computed metrics to evaluate compression performance.

---

## *Results / Observations*

* *Original vs Compressed:* Compressed image visually preserves most details with slight loss depending on quantization scale.
* *Difference Image (Amplified):* Highlights compression artifacts, mostly in high-frequency regions.
* *Compression Metrics:*
