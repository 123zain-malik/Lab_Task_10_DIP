# Lab_Task_10_DIP

2023-SE-02_Lab_Task_10_DIP

Implement a complete image compression workflow in Python using OpenCV, NumPy, and Matplotlib, compatible with Google Colab. The program should:
Allow interactive image upload (JPEG/PNG) in Colab.
Perform JPEG-like DCT compression on each color channel using an 8×8 block size and a standard JPEG quantization matrix (allow scaling for visible compression).
Apply Huffman coding to the quantized DCT coefficients of each channel and generate bitstreams.
Compute compression metrics:
Compression Ratio (CR)
Mean Squared Error (MSE)
Peak Signal-to-Noise Ratio (PSNR)
Rate Distortion (RD)
Display:
Original image
Compressed image
Amplified difference image between original and compressed
Print all computed metrics.
Ensure the code is robust, fully Colab-compatible, handles color images, and clearly separates all steps. Use amplified differences to highlight compression artifacts.
