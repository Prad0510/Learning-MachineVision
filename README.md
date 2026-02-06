# Learning-MachineVision
A collection of projects and experiments documenting my learning path in Machine Vision and Digital Image Processing. This repository tracks my progress from basic pixel manipulation to advanced image enhancement techniques.

<h2>📍 Current Progress: Image Preprocessing & Enhancement</h2>

The focus of this phase is understanding how to "clean" and "recover" visual information from real-world images that suffer from low light or sensor noise.
1. Image Acquisition & Histogram AnalysisGrayscale Conversion: Learning to convert BGR images to Gray to simplify the mathematical complexity of filters.Histogram Visualization: Using matplotlib to analyze the "mountain" of pixel intensities (0-255) to diagnose low contrast or lighting issues.
2. Spatial Domain Filtering (Smoothing)I experimented with various kernels to remove "sand-like" Gaussian noise:Mean Filter: Using simple averaging (cv2.blur) to reduce grain by calculating the mean of a $5 \times 5$ neighborhood.Gaussian Filter: Implementing weighted averages (cv2.GaussianBlur) for a more natural noise reduction that respects the center of the kernel.Median Filter: Exploring non-linear filtering (cv2.medianBlur) to remove sharp speckles while attempting to preserve edges.
3. Image Sharpening (High-Pass Filtering)Laplacian Operator: Using second-order derivatives to isolate high-frequency components (edges).
4. Image Reconstruction: Combining the smoothed image with the Laplacian edge map to produce a final, crisp output where details like mountain ridges and paths are clearly defined.

<h3>🛠️ Tools Used</h3>

<p><strong>Language:</strong> Python</p>

<p><strong>Libraries:</strong></p>
<ul>
  <li><strong>OpenCV:</strong> The primary engine for image math and filtering.</li>
  <li><strong>NumPy:</strong> For handling images as numerical matrices.</li>
  <li><strong>Matplotlib:</strong> For side-by-side visual comparisons and histogram plotting.</li>
</ul>

<h3>📂 Project Structure</h3>

<pre>
Plaintext
├── 01_Histogram_Analysis/      # Basic loading and intensity plotting
├── 02_Smoothing_Techniques/    # Comparisons of Mean, Gaussian, and Median filters
├── 03_Image_Sharpening/        # Laplacian edge detection and image enhancement
└── README.md
</pre>


<h3>📈 Future Goals</h3>

<ul>
  <li>Implementing Histogram Equalization for better lighting.</li>
  <li>Exploring Edge Detection (Canny, Sobel) for object recognition.</li>
  <li>Integrating these preprocessing steps into my AI-Driven Financial Intelligence Platform for document scanning.</li>
</ul>
