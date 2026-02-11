The Canny method most widely used edge detector in Computer Vision to outline the edges of the Cardiomyocytes Cells. The Canny Edge Detection is a more advanced and robust edge detection algorithm compared to the Sobel Edge Detection. It provides better detection of edges, localization, and minimizes the response to noise. This makes it particularly suitable for analyzing contracting cardiac muscle cells, where accurate boundary detection is crucial for segmentation and analysis (Vijayarani and Vinupriya, 2013).

Steps Involved in Canny Edge Detection:

a.	Noise Reduction:
Gaussian Filtering: The first step in the Canny Edge Detection algorithm is to apply a Gaussian filter to smooth the image and reduce noise. This is essential because noise can lead to false edges.
 
where is the Gaussian kernel with standard deviation σ 
b.	Gradient Calculation:

Sobel Operator: The algorithm then computes the gradient intensity and direction of the smoothed image using Sobel operators. This step helps in identifying areas of the image with high spatial derivatives.
 
where Sx and Sy are Sobel Kernels in the x and y directions, respectively.
c.	Non-Maximum Suppression:
Thinning: Non-maximum suppression is applied to the gradient magnitude image to thin the edges. This step ensures that only the local maxima, which are the potential edges, are preserved.
Process: For each pixel, it is checked whether the pixel is a local maximum in its neighborhood along the gradient direction. Non-maxima are suppressed (set to zero).
d.	Double Thresholding:
Edge Classification: The algorithm uses two thresholds to classify the edges into strong, weak, and non-relevant pixels.
High and Low Thresholds: Pixels with gradient values above the high threshold are considered strong edges, those below the low threshold are suppressed, and those in between are considered weak edges.
e.	Edge Tracking by Hysteresis:
Edge Connectivity: Weak edges that are connected to strong edges are retained, while the others are suppressed. This step helps in suppressing noise and ensuring that edges are continuous.
Application in Cardiac Muscle Cell Analysis:
Edge Detection: The Canny Edge Detection algorithm can be used to detect the boundaries of contracting cardiac muscle cells (Vijayarani and Vinupriya, 2013). This is crucial for accurately segmenting individual cells from a cluster and analyzing their movement.
Noise Reduction: Given the often noisy nature of biological images, the initial Gaussian filtering step is particularly useful for reducing noise while preserving important structural details.
Gradient Information: By computing the gradient magnitude and direction, the method provides detailed information about the edges, which can be used to understand the orientation and movement of muscle cells.
Accurate Segmentation: The combination of non-maximum suppression and edge tracking by hysteresis ensures that only the most relevant edges are retained, leading to precise segmentation of cells.
