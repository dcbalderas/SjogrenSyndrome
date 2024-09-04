![Alt text](/photos/sjogren_example.jpg "Sjogren Dataset")

<div align="center">
    <img src="/photos/sjogren_example.jpg" width="400px"</img> 
</div>

# SjogrenSyndrome: An Open-Access Dataset for Instance Segmentation

This repository makes available the source code and public dataset for the work, "Sjogren's Syndrome Dataset, an open-access dataset for computer Instance Segmentation, published with open access by Scientific Reports: https://www.. The SjogrenSyndrome dataset consists of TODO images capturing four different parts of the x-ray images of people glands that might be infected with the Sjogren's Syndrome. In our work, the dataset was classified to an average accuracy of TODO:... without Data Augmentation the Yolov8 deep convolutional neural network.

The source code, images and annotations are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) license. The contents of this repository are released under an [Apache 2](LICENSE) license.

## Images Sources
The SjogrenSyndrome repository contains a collection of photographs of x-ray images of people infected with the symdrome which can be used to train a image classifiers or be used in machine learning projects. A variety of categories have been provided to ensure a diverse selection of images for the best and most accurate results.

These images were taken from different setup environment using the following rules:
1. TODO
2. TODO 

## Stats
There are **TODO** images that included **4** clases.

Class | Type of Segment | Label 
------ | ------ | ------ 
0   | Submaxillary Gland  | GS       
1   | Parotid Gland  | GP       
2   | Vessel | V     
3   | Cyst | Q         

## Data organization

Images are assigned unique filenames with increasing ID number. The images were taken for TODO n patients over the period of n months. The format is like so: ```xxxxx.jpg```, where the ID is simply an integer from 0 to the current number of image.

The images are placed in a single train folder using the COCO JSON (Instance Segmentation) folder format.

** train - Labeled images

## Images labeling

The TODO file assigns species labels to each image. It is a comma separated text file in the TODO Pascal VOC (Visual Object Classes) format. Example:

```
<annotation>
    <folder></folder>
    <filename>000001.jpg</filename>
    <path>000001.jpg</path>
    <source>
        <database>tomate_rugoso</database>
    </source>
    <size>
        <width>500</width>
        <height>375</height>
        <depth>3</depth>
    </size>
    <segmented>0</segmented>
    <object>
        <name>helmet</name>
        <pose>Unspecified</pose>
        <truncated>0</truncated>
        <difficult>0</difficult>
        <occluded>0</occluded>
        <bndbox>
            <xmin>179</xmin>
            <xmax>231</xmax>
            <ymin>85</ymin>
            <ymax>144</ymax>
        </bndbox>
    </object>
    <object>
        <name>helmet</name>
        <pose>Unspecified</pose>
        <truncated>0</truncated>
        <difficult>0</difficult>
        <occluded>0</occluded>
        <bndbox>
            <xmin>112</xmin>
            <xmax>135</xmax>
            <ymin>145</ymin>
            <ymax>175</ymax>
        </bndbox>
    </object>
</annotation>
```

## Training

## Models

We provide the most successful YoloV8 models saved in *.pt* model format. The model provided was trained for **1,000** epochs with the following hyperparameters. 
```
lr0=0.01, lrf=0.1, momentum=0.937, weight_decay=0.0005, warmup_epochs=3.0, warmup_momentum=0.8, warmup_bias_lr=0.1, box=0.05, cls=0.3, cls_pw=1.0, obj=0.7, obj_pw=1.0, iou_t=0.2, anchor_t=4.0, fl_gamma=0.0, hsv_h=0.015, hsv_s=0.7, hsv_v=0.4, degrees=0.0, translate=0.2, scale=0.9, shear=0.0, perspective=0.0, flipud=0.0, fliplr=0.5, mosaic=1.0, mixup=0.15, copy_paste=0.0, paste_in=0.15, loss_ota=1
```

The models trained are: 

```
models/best_00.pt
```

### First Model
The first model provided is the Yolov8 trained using the trained folder. It consist of TODO images which were splitted in 70-10-20, resulting in training **TODO**, testing **TODO** and validation **TODO** images. The resulting number of labels where *TODO*
 all        | TODO
 ------ | ------
 GS     | TODO
 GP     | TODO
 V     | TODO
 Q     | TODO 

The resulting model was saved in models/best_00.pt

## BibTeX (TODO: Update)
```
@article{TomatoRugoso2024,
  author = {David Balderas-Silva and
    Pedro Ponce Cruz and 
    Arturo Molina},
  title = {{TomatoRugoso: Tomato brown fruit virus, an open-access Tomatoes Rugoso’s dataset for computer visual inspection}},
  journal = {TODO:...},
  year = 2024,
  number = TODO:...,
  month = TODO:...,
  volume = TODO:...,
  issue = TODO:...,
  day = TODO:...,
  url = "https://doi.org/TODO:...",
  doi = "TODO:..."
}

```
