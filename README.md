# VASAD: a Volume and Semantic dataset for Building Reconstruction from Point Clouds
**VASAD: a Volume and Semantic dataset for Building Reconstruction from Point Clouds<br>**
P-A. Langlois, A. Boulch, and R. Marlet. VASAD: Volumetric and Semantic Reconstruction, ICPR, 2022.
![Project banner](https://raw.githubusercontent.com/palanglois/palanglois.github.io/main/images/vasaad_ban.png)

## Dataset download

You can download VASAD [on Kaggle](https://www.kaggle.com/datasets/palanglois/vasad-volume-and-semantic-for-buildings).

## Dataset description

Each folder contains the data for a given building. We provide the following files:
- model.obj: the raw file where each component of the building is represented separately.
- colored\_triangles.obj: each class of the dataset is colored for visualization purpose.
- ptView.json: a set of simulated camera locations 
- samplesWithLabel.obj: a simulated Lidar scan (from the point of views in ptView.json) with a class label for each point.
- pov.obj: the list of point of views from which each point of samplesWithLabel.obj was taken from.

We also provide a labelled point cloud with features computed from [FKAConv](https://github.com/valeoai/LightConvPoint):
- lcpSamplesWithLabel.obj: a simulated Lidar scan (from the point of views in ptView.json with a FKAConv feature for each
- lcpPov.obj: the list of point of views from which each point of samplesWithLabel.obj was taken from.
- lcpVis.obj: a colored version of lcpSamplesWithLabel.obj using a argmax function on the features for visualization purpose.

The following classes are represented in the dataset: 

- pillar
- railing
- roof
- stair
- window
- beam
- door
- partition
- slab
- bearing wall
- ceiling
