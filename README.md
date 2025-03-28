# LGN waveform classification from [Sun et al., 2024](https://doi.org/10.1101/2023.11.22.568065)

[![DOI](https://img.shields.io/badge/DOI-10.1101/2023.11.22.568065-blue)](https://doi.org/10.1101/2023.11.22.568065)

## Description
Python (Jupyter) scripts to replicate the macaque LGN waveforms analysis results presented in "Unveiling the Diversity of Functional Responses and Extracellular Signals in Awake Monkey LGN", [Sun et al., 2024](https://doi.org/10.1101/2023.11.22.568065).

The classification technique used here is called WaveMAP by [Lee et al., 2021](https://doi.org/10.7554/eLife.67490), which uses Uniform Manifold Approximation and Projection (UMAP) for dimensionality reduction and the Louvain method for cluster identification (Blondel et al., 2008). As in [Lee et al. (2021)](https://doi.org/10.7554/eLife.67490), before WaveMAP classification, the mean waveform of each single unit was normalized so that the maximum of its absolute value was 1. Mean waveforms are stored in data/waveforms_mean.mat.

## Steps
1. Open jupyter notebooks
   1. Open terminal (i.e., Anaconda)
   2. pip install notebook (if not already installed)
   3. cd path_to_folder (change directory to where this folder is located)
   4. jupyter notebook
2. Run the Jupyter notebooks in the following order
   1. 0_install_packages
   2. 1_wavemap_analysis
      - performs primary analysis on waveforms_mean.mat and outputs the cluster classifications and umap into umap_clustering_norm.csv
   3. 2_wavemap_bootsrap
      - bootstraps the primary analysis to output confidence scores in condifence_scores.csv
3. Analysis output will be saved into /analysis_output folder

## Contact
Scott Sun - shsun@mgh.harvard.edu
John Pezaris - pezaris.john@mgh.harvard.edu


