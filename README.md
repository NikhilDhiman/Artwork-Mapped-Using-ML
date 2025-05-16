# 🎨 Artwork Mapped Using ML

This project visualizes thousands of artwork images in a 3D space based on their **visual similarity**, using **deep learning** for feature extraction and **unsupervised learning** for dimensionality reduction and clustering.

Explore art visually and intuitively without relying on text or metadata.

Live Demo: [https://3d-umap-cs5660.vercel.app/](https://3d-umap-cs5660.vercel.app/)

---

## 📁 Dataset

[WikiArt 120K Dataset on Kaggle](https://www.kaggle.com/datasets/antoinegruson/-wikiart-all-images-120k-link)

---

## ⚙️ Software Requirements

- Python 3.8+
- pip
- GPU (Recommended for faster feature extraction)

### Install Dependencies

Create a virtual environment and install required libraries:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

**requirements.txt**:
```txt
tensorflow
numpy
pandas
matplotlib
plotly
opencv-python
scikit-learn
tqdm
umap-learn
h5py
Pillow
```

---

## 🚪 Environment Setup

1. **Download Dataset:** Extract WikiArt images to:

   ```bash
   /home/<your_username>/CS5660/data/wikiart_images
   ```

2. **Update Paths in Notebook:**

   Update the following variables in the notebook if needed:
   ```python
   IMAGES_DIR = "/your/path/wikiart_images"
   PROJ_DIR = "/your/project/folder"
   ```

3. **Create Directory for Features:**
   ```bash
   mkdir -p extracted_features_batched_artwork
   ```

---

## 🚀 How to Run

### Via Jupyter Notebook

1. Launch Jupyter:
   ```bash
   jupyter notebook
   ```

2. Open `Artwork Mapped Using ML.ipynb`

3. Run cells in order:

   - Data Cleaning: Duplicate and corrupt image filtering
   - Feature Extraction: Using ResNet50
   - Dimensionality Reduction: PCA + UMAP
   - Clustering: HDBSCAN
   - Save Embeddings: For visualization

---

## 🔹 Visualization

Final output (3D coordinates + image references) is used by a [Three.js](https://threejs.org/) web app:

Live Interface: [https://3d-umap-cs5660.vercel.app/](https://3d-umap-cs5660.vercel.app/)

Update `data.json` in the web repo with your new outputs to visualize custom embeddings.

---

## 👥 Authors

- Nikhil Dhiman  
- Yamini Mandadi  
- Akash Saraf


