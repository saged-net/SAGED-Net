# 📂 Dataset Preparation

SAGED-Net is evaluated on four public histopathology benchmarks. Below are the download links and the required directory structure for training.

## 1. Download Links

| Dataset     | Description                                      | Download Link                                                                                        |
| :---------- | :----------------------------------------------- | :--------------------------------------------------------------------------------------------------- |
| **TNBC**    | Triple Negative Breast Cancer (50 images)        | [Link](https://www.kaggle.com/datasets/mahmudulhasantasin/tnbc-nuclei-segmentation-original-dataset) |
| **CPM-15**  | MICCAI 2015 Comp. Precision Medicine (15 images) | [Link](https://www.kaggle.com/datasets/ashutoshnaik67/hovernetdataset)                               |
| **CPM-17**  | MICCAI 2017 Comp. Precision Medicine (32 images) | [Link](https://www.kaggle.com/datasets/ashutoshnaik67/hovernetdataset)                               |
| **PanNuke** | 19 Tissue Types (~7,900 patches)                 | [Link](https://www.kaggle.com/datasets/theredlad/pannuke-dataset-experimental-data)                  |

---

## 2. Dataset Descriptions

### 1. Triple Negative Breast Cancer (TNBC)

- **Source:** Curated by Naylor et al. from the Curie Institute.
- **Content:** Contains **50 H&E stained images** (512×512 pixels) at 40x magnification.
- **Characteristics:** This dataset is characterized by high cellularity, significant overlap between nuclei, and dense clustering. It serves as a rigorous benchmark for separating touching instances in homogeneous tissue.
- **Annotations:** ~4,000 annotated nuclei boundaries.

### 2. CPM-15 (MICCAI 2015)

- **Source:** Computational Precision Medicine (CPM) Challenge 2015.
- **Content:** Contains **15 training images** and 15 testing images derived from TCGA.
- **Characteristics:** Includes samples from two diverse cancer types:
  - Lower Grade Glioma (LGG)
  - Non-Small Cell Lung Cancer (NSCLC)
- **Challenge:** The main difficulty lies in the variability of nuclear appearance (shape, size, and chromatin texture) across different organs.

### 3. CPM-17 (MICCAI 2017)

- **Source:** Computational Precision Medicine (CPM) Challenge 2017.
- **Content:** Contains **32 training images** and 32 testing images.
- **Characteristics:** Extends the diversity of CPM-15 by including four distinct cancer cohorts:
  - Head and Neck Squamous Cell Carcinoma (HNSCC)
  - Glioblastoma Multiforme (GBM)
  - Lower Grade Glioma (LGG)
  - Non-Small Cell Lung Cancer (NSCLC)
- **Challenge:** Tests the model's ability to generalize across multi-organ tissues with varying stain intensities.

### 4. PanNuke (Large-Scale Dataset)

Semi automatically generated nuclei instance segmentation and classification dataset with exhaustive nuclei labels across 19 different tissue types. The dataset consists of 481 visual fields, of which 312 are randomly sampled from more than 20K whole slide images at different magnifications, from multiple data sources. In total the dataset contains 205,343 labeled nuclei, each with an instance segmentation mask. Models trained on PanNuke can aid in whole slide image tissue type segmentation, and generalize to new tissues. PanNuke demonstrates one of the first successfully semi-automatically generated datasets.

- **Source:** Gamper et al., University of Warwick.
- **Content:** A massive dataset comprising **~7,901 image patches** (256×256 pixels) from 19 different tissue types.
- **Characteristics:** PanNuke is one of the few semi-automatically generated datasets that provides multiclass nuclei segmentation labels.
- **Classes:**
  - Neoplastic cells
  - Inflammatory cells
  - Connective/Soft tissue cells
  - Dead Cells
  - Epithelial cells
- **Challenge:** Extreme class imbalance and high intra-class variation across 19 tissues.
