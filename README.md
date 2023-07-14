# Reconstructing Spatiotemporal Data with C-VAEs
---

<p align="center">
<img src="assets/CIIC_logo.png" width="1000px"/>
</p>

---
<div align="center">

 [Dataset](https://zenodo.org/record/7944963#.ZGYoxHbMIQ8) | [Dataset Citation](#burnedareauav-dataset-citation) 
 
</div>

![Visitors](https://api.visitorbadge.io/api/visitors?path=https%3A%2F%2Fgithub.com%2FCIIC-C-T-Polytechnic-of-Leiria%2FReconstr_CVAE_paper&label=Visitors&countColor=%23263759&style=plastic)
### Description

The continuous representation of spatiotemporal data commonly relies on using abstract data types, such as *moving regions*, to represent entities whose shape and position continuously change over time. Creating this representation from discrete snapshots of real-world entities requires using interpolation methods to compute in-between data representations and estimate the position and shape of the object of interest at arbitrary temporal points. Existing region interpolation methods often fail to generate smooth and realistic representations of a region's evolution. However, recent advancements in deep learning techniques have revealed the potential of deep models trained on discrete observations to capture spatiotemporal dependencies through implicit feature learning.

In this work, we explore the capabilities of Conditional Variational Autoencoder (C-VAE) models to generate smooth and realistic representations of the spatiotemporal evolution of moving regions. We evaluate our proposed approach on a sparsely annotated dataset on the burnt area of a forest fire. We apply compression operations to sample from the dataset and use the C-VAE model and other commonly used interpolation algorithms to generate in-between region representations. To evaluate the performance of the methods, we compare their interpolation results with manually annotated data and regions generated by a U-Net model. We also assess the quality of generated data considering temporal consistency metrics.

### Burned Area 2D Moving Region 

<div align="center">
<img src="assets/mov_region.png" width="1000px"/>
<p>Continuous representation model requires a method to recreate the spatiotemporal evolution of a region, such as the progression of the burned area.</p>
</div>

### C-VAE Architecture

<div align="center">
<img src="assets/CVAE_training_inference.png" width="1000px"/>
<p><strong>Employed C-VAE Architecture.</strong>  a) each region stored in WKT
format is converted to raster image to be processed by the model b) a new image
is generated conditioned by a label and converted to WKT format.</p>
</div>

### Summary of Results 

<div align="center">
<img src="assets/tab_similarity.png" width="600px"/>
<p><strong>Similarity Evaluation.</strong> Comparison of JI and HD for U-Net Samples and BurnedAreaUAV test set using periodic and distance-based sampling.</p>
</div>

<div align="center">
<img src="assets/table_tc.png"width="500px"/>
<p><strong>Temporal Consistency Comparison.</strong> Average temporal consistency across different algorithms for periodic and distance-based sampling.</p>
</div>

<div align="center">
<img src="assets/area_evolution.png" width="1000px"/>
<p>Representation of the evolution burned area.</p>
</div>

<div align="center">
      <a href="https://www.youtube.com/watch?v=9gHSvj8vwTI">
     <img 
      src="assets/play_video.png" 
      alt="Comparison of Interpolation from Distance-Based Sampling" 
      style="width:75%;">
      </a>
      <p>Comparison of Interpolation from Distance-Based Sampling</p>
 </div>

### TL;DR

The C-VAE algorithm performed competitively against the best-performing algorithm (Shape-Based) in terms of similarity metrics and also achieved superior temporal consistency and generated a relatively realistic and smooth representation of the phenomenon evolution, suggesting that C-VAE models may be a viable alternative to modelling the spatiotemporal evolution of 2D moving regions.


### Data Download

- [*BurnedAreaUAV* Dataset](https://zenodo.org/record/7944963#.ZGYoxHbMIQ8)
- [U-Net Samples File](https://drive.google.com/file/d/1Lmh3jY0qMQd8kpiX9fkIFNGKvXjab_bp/view?usp=sharing)

### *BurnedAreaUAV* Dataset Citation
```bibtex
@misc{ba_uav_ribeiro_dataset,
  author       = {Ribeiro, Tiago F. R. and Silva, Fernando and Moreira, José and Costa, Rogério Luís de C.},
  title        = {BurnedAreaUAV Dataset (v1.1)},
  month        = may,
  year         = 2023,
  publisher    = {Zenodo},
  version      = {1.1},
  doi          = {10.5281/zenodo.7944963},
}
```
### Paper Citation
```
Under review 🔍
```
### Acknowledgements
This work is partially funded by FCT - Fundação para a Ciência e a Tecnologia, I.P., through projects MIT-EXPL/ACC/0057/2021 and UIDB/04524/2020, and under the Scientific Employment Stimulus - Institutional Call - CEE/CINST/00051/2018.

