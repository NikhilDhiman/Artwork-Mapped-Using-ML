# Artwork-Mapped-Using-ML
Artwork Mapped Using ML

An interactive 3D landscape of thousands of artworks, visualized using Machine Learning and dimensionality reduction. This project organizes artworks based solely on visual similarity—no metadata, artist names, or titles involved.

## Project Summary
This project explores visual similarity among thousands of artworks by mapping them into a 3D space using deep learning and unsupervised learning techniques. The result is a navigable, web-based visualization where users can explore artworks from any perspective.

## Key Features
Visual Similarity Mapping: Artworks that look similar are placed closer together in 3D space.

Image-Only Analysis: No metadata or text—just raw pixel data.

Deep Learning Embeddings: Pre-trained models (like InceptionV3 or ResNet50) are used for image feature extraction.

Dimensionality Reduction: UMAP reduces the high-dimensional embeddings into a 3D space.

Web Visualization: A Three.js interface allows exploration of the 3D artwork landscape.

##  How It Works
#### Image Preprocessing

Recursively loads images from a specified directory, ignoring non-image files and corrupt files (logged).

#### Feature Extraction

Uses TensorFlow’s ResNet50 (pre-trained on ImageNet) without the top layer.

Outputs 2048-dimensional embeddings for each image.

Images are resized to 224x224 and preprocessed using preprocess_input().

#### Batch Processing & Storage

Embeddings are generated in batches (BATCH_SIZE = 32) and saved in HDF5 format.

Corresponding image filenames are saved in a .npy file.

#### Dimensionality Reduction

You can apply UMAP separately to the HDF5 feature data to reduce it to 3D for visualization.




