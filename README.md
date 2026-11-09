# Avicennia marina Morphometric Dataset (GCC)

This repository contains the processed dataset and analysis pipeline used in the study:

"Leaf morphological variation in Avicennia marina across the Gulf Cooperation Council: a quantitative morphometric analysis"

## Dataset contents

- Morphometric shape descriptors
- Elliptic Fourier coefficients
- Binary leaf masks
- Leaf outline coordinates
- Analysis scripts

## Note on image licensing

Original leaf images were obtained from public biodiversity platforms (iNaturalist, GBIF) and field observations. Due to copyright restrictions, original images are not redistributed in this repository. Metadata is provided to enable retrieval from the original sources.

## Run order

Run the scripts in this order, from the folder that holds the input files:

python 01_efd_analysis.py

python 02_shape_pca_permanova_classification.py

python 03_sensitivity_checks.py <folder containing basic_shape_features.csv>

## Software

Python 3.10 with NumPy, SciPy, pandas, scikit-learn, scikit-bio, statsmodels, seaborn, matplotlib and pyefd. Script 03 uses its own NumPy/SciPy implementation of PERMANOVA (Anderson, 2001) and does not need scikit-bio.

## Reproducibility notes
All random procedures use seed 42. Permutation p-values and Monte-Carlo percentages in Table V can differ slightly between software implementations and platforms.
Image source was retained as specimen-level metadata but was not modeled as a PERMANOVA factor, because field and repository sampling were not balanced across countries (see the manuscript, Study limitations).
The original images are not redistributed because of platform licensing; source identifiers are in the metadata files.

## License

This dataset is distributed under the MIT License.
