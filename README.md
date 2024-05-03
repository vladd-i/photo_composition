# Evaluation Photo Composition with Geometric Representation Learning

## Motivation and Background
The composition of a photograph is critical to its aesthetic appeal. However, evaluating composition quality often relies on subjective human judgment. This project aims to objectify this evaluation using Geometric Machine Learning, particularly focusing on manifold learning with annotated composition elements to decipher the geometrical underpinnings that constitute well-composed images.

There are a variety of models that can predict the aesthetic appeal of an image. ChatGPT can analyze an uploaded photograph and provide an evaluation of its composition in text format. Other models use deep convolutional neural nets or various heuristics, including those related to color and contrast, to evaluate aesthetic appeal. Unlike the existing models that predict compositional success through a black box approach, this project delves deeper into establishing objective geometrical relationships that define good photographic composition. By focusing on interpretability, I aim to identify actionable insights that contribute to enhanced composition in images.

## Approach
I plan to extract geometric features from the composition elements of each image, such as the size of the subject and its placement, the orientation and positioning of leading lines. These features, combined with scene category and composition rule annotations, will form a feature vector for each image. Applying manifold learning techniques, I plan to embed these vectors into a lower-dimensional space, revealing clusters and patterns that correlate with high composition scores. This analysis will not only reveal what constitutes well-composed images, but also provide a roadmap for compositional improvement by identifying pathways on the manifold that lead to higher scores.

## Data 
I am using the [Image Composition Assessment DataBase (CADB)](https://github.com/bcmi/Image-Composition-Assessment-Dataset-CADB), which provides over 10,000 images with detailed composition category labels, annotations for the main subjects and leading lines, and human-assigned composition scores.

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
├── requirements.txt                         # TODO: Project dependencies
├── .gitignore                               # Specifies intentionally untracked files to ignore
└── README.md                                # Project overview, setup, and usage instructions
```

## Setup and Installation

1. Clone this repository:
    ```
    git clone git@github.com:vladd-i/photo_composition.git
    ```
2. Install required dependencies:
    ```
    pip install -r requirements.txt
    ```

## Usage

- Navigate to the `notebooks/` directory and open the Jupyter notebooks to inspect exploratory data analysis results, 
feature engineering steps, and manifold learning techniques applied to high-dimensional image representations to learn 
patterns.