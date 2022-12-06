# Cell Projection Plots (CPP): a novel visualization of bone marrow aspirate cytology
Here are sample codes used in the paper titled; _Cell projection plots: a novel visualization of bone marrow aspirate cytology_

A sample CPP is shown here that shows orderly neutrophil maturation in a normal bone marrow aspirate. CPPs were evaluated by hematopathologists to check their descriptive value. 

![Neutrophil Maturation](https://github.com/TahDeh/Cell_Projection_Plot/blob/main/images/cellplot_neutrophil.jpg)


## Feature Extraction

Tissue tiles were analyzed by a YOLO model to detect cells and extract deep features. A deep feature vector was produced for each detected cell from
the corresponding region on the feature map, i.e., the first output of the model’s backbone. Average pooling was applied on the corresponding region to construct a deep feature vector of size 256 for each detected cells. These deep feature vectors represent cells.

![Feature Extraction](https://github.com/TahDeh/Cell_Projection_Plot/blob/main/images/overview%20Yolo%20features.jpg)

## Cell Detection Model
A pre-trained YOLO model were repurposed to be used in this study. The model's weights can be found [here](https://zenodo.org/record/6373429#.Y4_DUHbMKUk). 
