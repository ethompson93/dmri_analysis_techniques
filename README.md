# Analysis Techniques for Diffusion MRI 🧠
### Materials for ISMRM workshop on 40 years of diffusion MRI
### 🎓 Educational Bootcamp, 16th Feb 2025, Kyoto
**Ellie Thompson and Anna Schroder, UCL Hawkes Institute**


## 📂 Data
The data you will need for the practicals is included in the [data](https://github.com/ethompson93/dmri_analysis_techniques/tree/main/data) folder. We will be using the [Fibercup phantom](https://tractometer.org/fibercup/home/) for all the practicals.

## Exercise 1 - The Diffusion Tensor
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ethompson93/dmri_analysis_techniques/blob/main/DTI_Estimation.ipynb)

In this exercise we fit the diffusion tensor model to phantom data using non-linear least squares. You will code up the model from scratch and visualise the results.

**Key references:**
- [P.J. Basser, J. Mattiello, D. Lebihan, Estimation of the Effective Self-Diffusion Tensor from the NMR Spin Echo, Journal of Magnetic Resonance, Series B,
Volume 103, Issue 3,
(1994)](https://www.sciencedirect.com/science/article/abs/pii/S1064186684710375) - the first paper introducing the diffusion tensor
- [O'Donnell LJ, Westin CF. An introduction to diffusion tensor image analysis. Neurosurg Clin N Am. 2011 Apr;22(2):185-96, viii. doi: 10.1016/j.nec.2010.12.004.](https://pmc.ncbi.nlm.nih.gov/articles/PMC3163395/#R5) - a nice overview of the technique and its applications

- [docs for scipy's non-linear least squares optimiser](https://docs.scipy.org/doc/scipy-1.15.0/reference/generated/scipy.optimize.least_squares.html)


## Exercise 2 - Ball and Stick Model
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ethompson93/dmri_analysis_techniques/blob/main/ball_and_stick.ipynb)

In this exercise we fit a simple compartment model: the ball-and-stick model. As in the previous exercise, you will code the model from scratch and fit it to the data using non-linear least squares.

**Key references:**
- [Behrens, T.E.J. et al. (2003), Characterization and propagation of uncertainty in diffusion-weighted MR imaging. Magn. Reson. Med., 50: 1077-1088. https://doi.org/10.1002/mrm.10609](https://onlinelibrary.wiley.com/doi/full/10.1002/mrm.10609) - paper introducing the ball and stick model, as part of a Bayesian framework for uncertainty estimation of the estimated parameters
- [Behrens, T.E.J. et al. (2007), Probabilistic diffusion tractography with multiple fibre orientations: What can we gain? NeuroImage, 34.1: 144-155. https://doi.org/10.1016/j.neuroimage.2006.09.018.](https://www.sciencedirect.com/science/article/pii/S1053811906009360?via%3Dihub) - extension of the ball and stick model to multiple fibres. The number of fibres in each voxel is estimated from the data by automatic relevance determination.
- [Panagiotaki, E. et al. (2012), Compartment models of the diffusion MR signal in brain white matter: A taxonomy and comparison. NeuroImage, 59.3: 2241-2254, https://doi.org/10.1016/j.neuroimage.2011.09.081.](https://www.sciencedirect.com/science/article/pii/S1053811911011566) - a taxonomy of different compartment models

## Exercise 3 - Constrained Spherical Deconvolution
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ethompson93/dmri_analysis_techniques/blob/main/constrained_spherical_deconvolution.ipynb)

In this exercise we will use tools from [DIPY](https://dipy.org) to obtain the voxel-wise fibre orientation function by performing constrained spherical deconvolution on our dataset. The practical draws on the example from the DIPY workshop: [Reconstruction with Constrained Spherical Deconvolution](https://workshop.dipy.org/documentation/1.6.0./examples_built/reconst_csd/).

**Key references:**
- [Dell'Acqua F, Tournier JD. (2019) Modelling white matter with spherical deconvolution: How and why? NMR in Biomedicine.; 32:e3945. https://doi.org/10.1002/nbm.3945](https://analyticalsciencejournals.onlinelibrary.wiley.com/doi/full/10.1002/nbm.3945) - thorough introduction to the topic of spherical deconvoluion in dMRI
- [Tournier, J. D., Calamante, F., & Connelly, A. (2007). Robust determination of the fibre orientation distribution in diffusion MRI: non-negativity constrained super-resolved spherical deconvolution. NeuroImage, 35(4), 1459–1472. https://doi.org/10.1016/j.neuroimage.2007.02.016](https://pubmed.ncbi.nlm.nih.gov/17379540/) - initial paper introducing the CSD method
- [Jeurissen, B. et al. (2014) Multi-tissue constrained spherical deconvolution for improved analysis of multi-shell diffusion MRI data. NeuroImage, Volume 103: 411-426, https://doi.org/10.1016/j.neuroimage.2014.07.061.](https://www.sciencedirect.com/science/article/pii/S1053811914006442) - extension to multi-tissue CSD


