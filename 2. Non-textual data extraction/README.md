CBIR-Based Basketball Jersey Retrieval System

📌 Project Overview

This project implements a Content-Based Image Retrieval (CBIR) system to identify and compare basketball jerseys based on visual features. Unlike traditional retrieval methods that rely on metadata, CBIR analyzes the actual visual content of images, making it suitable for applications in pattern recognition, computer vision, and multimedia retrieval.

This system utilizes two key descriptors:

Smart Histogram Descriptor: Measures color similarity between images.

HOG + Harris Descriptor: Captures shape and structural patterns of the jerseys.

A two-step retrieval approach is used where images are first ranked using one descriptor and then refined using the second descriptor to improve accuracy.

🎯 Objectives

Develop a toy CBIR system capable of retrieving similar basketball jerseys.

Implement and compare two different feature descriptors (Smart Histogram and HOG + Harris).

Experiment with different distance metrics for similarity computation.

Combine both descriptors for improved retrieval results.

Provide a visualization of the retrieved images ranked by similarity.

🛠️ Setup & Installation

Prerequisites

Make sure you have Python 3.8+ and install the required dependencies:

Running the CBIR System

Place your basketball jersey images in the data/ directory.

The system will:

Extract features using Smart Histogram and HOG + Harris.

Rank images based on combined similarity scores.

Display the top 5 most similar jerseys.

📝 Implementation Details

1️⃣ Smart Histogram Descriptor

Uses color histograms to compare jerseys based on color distribution.

Works on different color spaces (RGB, HSV).

Distance metrics used: Chi-Square, Bhattacharyya, Correlation.

2️⃣ HOG + Harris Descriptor

HOG (Histogram of Oriented Gradients) captures shape-based features.

Harris Corner Detection extracts structural patterns of jersey text and numbers.

Distance metric: Euclidean distance.

🔄 Combined Approach

Smart Histogram first → HOG + Harris second

Initial filtering using color similarity.

Shape and texture analysis for fine-tuning results.

HOG + Harris first → Smart Histogram second

Structural matching before color comparison.

More robust retrieval for jerseys with different shades but similar patterns.

📊 Results & Performance

The combination of both descriptors improves retrieval accuracy.

The two-step approach refines the search results compared to using only a single descriptor.

The final similarity score is computed as:



Where  and  determine the weight of each descriptor (experimentally adjusted).

🖼️ Sample Output

When querying a jersey image, the system displays the most similar jerseys:

Query Image: Lakers #23
Top Matches:
1. Lakers #6 - Similarity: 0.85
2. Suns #23 - Similarity: 0.82
3. Warriors #30 - Similarity: 0.79
...

📌 References

Datta, R., Joshi, D., Li, J., & Wang, J. Z. (2008). Image retrieval: Ideas, influences, and trends of the new age.

Jain, A. K., Duin, R. P., & Mao, J. (2000). Statistical pattern recognition: A review.

🎯 Future Improvements:

Experiment with deep learning-based feature extraction.

Implement faster indexing techniques for large datasets.

Explore different feature fusion strategies for better accuracy.
