# Decoding Photographic Composition with Geometric Machine Learning

## Motivation and Background
The composition of a photograph is critical to its aesthetic appeal. However, evaluating composition quality often relies on subjective human judgment. This project aims to objectify this evaluation using Geometric Machine Learning, particularly focusing on manifold learning with annotated composition elements to decipher the geometrical underpinnings that constitute well-composed images.

Traditionally, models predicting the aesthetic appeal of an image rely on black box approaches, lacking transparency about the influence of geometric features on compositional success. Unlike these models, this project delves deeper into establishing objective geometrical relationships that define good photographic composition. By focusing on interpretability, actionable insights contributing to enhanced composition in images can be identified.

## Approach
Extracting geometric features from composition elements, such as subject size and placement, leading line orientation, forms the basis of this approach. These features, combined with qualitative image annotations, such as exposure, color harmony, object emphasis, depth of field, and others, create feature vectors for each image. Manifold learning techniques are then applied to embed these vectors into a lower-dimensional space, revealing clusters and patterns correlated with high composition scores.

For more details, explore the corresponding notebooks.

## Data 
The project utilizes the [Image Composition Assessment DataBase (CADB)](https://github.com/bcmi/Image-Composition-Assessment-Dataset-CADB), offering over 10,000 images with detailed composition category labels, annotations for main subjects and leading lines, and human-assigned composition scores.

## Project Structure

Below is the overview of the directory structure of the project:

```
photo_composition/
│
├── notebooks/                               # Jupyter notebooks for data analysis and exploration
│   ├── eda.ipynb                            # Preprocessing the data and analyzing distribution
│   ├── feature_engineering.ipynb            # Creating new features that comprise a high-dimensional
│   │                                        # embedding for each image
│   └── modeling.ipynb                       # Applying manifold learning techniques to extract patterns
│
├── src/                                     # Source code for the project
│   └── data/                                # Scripts/modules for data loading and manipulation
│       └── visualize_cadb_annotation.py     # Visualizing annotations of composition score,  
│                                            # scene category, and composition element
│
├── .gitignore                               # Specifies intentionally untracked files to ignore
└── README.md                                # Project overview, setup, and usage instructions
```

## Usage

- Navigate to the `notebooks/` directory and open the Jupyter notebooks to inspect exploratory data analysis results, 
feature engineering steps, and manifold learning techniques applied to high-dimensional image representations to learn 
patterns.

- To execute code, you'll need to download the dataset listed above and put it in the folder `data/` in the root of 
the project. 
