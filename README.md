# Knowledge Distillation for Brain Tumor Segmentation
This code was written for participation in the [Brain Tumor Segmentation Challenge](http://braintumorsegmentation.org/) (BraTS) 2019.
The code is based on [the corresponding paper](TBD), where we employ knwoledge distillation for automatic brain tumor segmentation.
This repository contains the code for inferencing the distilled model.

## Network achitecture
<img src="media/ResUNet.png" alt="drawing" height="230"/>

### Results

<img src="media/test.png" alt="drawing" height="250"/><br/>


| Data        | WT           | ET  | TC |
| ------------- |:-------------:| :-----:|:----:|
| Cascaded UNet Val 2019 | 0.9      |    0.731 |0.833|
| Distilled Val 2019 | 0.904      |    0.756 |0.842|
| Distilled Test 2019 | 0.887      |    0.794 |0.829|



## Pre-trained model
Download checkpoint with the following [link](https://drive.google.com/file/d/1YX5B3fV_g7eDMIr2Ow5cN0CGNNIYn4Y0/view?usp=sharing), where models directory name is 'models_sm_1' and model itself has the name 'only_seg'.


## How to perform prediction
1. Download BraTS data
2. Download pretrained model
3. Setup directory hierarchy
4. Run the script


Run the following command. Models root directory is a repository for all models. Change the output directory in the script.
```
python test.py --name=brain-tumor-segmentation-0002  --models_path=<model's root dir>
```

## Requirements
```
dicom                  0.9.9.post1
h5py                   2.9.0
jupyter-client         5.2.4      
jupyter-core           4.5.0      
jupyterlab             1.0.1      
jupyterlab-server      1.0.0    
matplotlib             3.1.1  
nibabel                2.4.1
numpy                  1.16.4      
opencv-python-headless 4.1.0.25    
openpyxl               2.6.2
pandas                 0.24.2
pickleshare            0.7.5      
Pillow                 6.1.0
protobuf               3.8.0
pydicom                1.2.2      
Pygments               2.4.2
PyWavelets             1.0.3
scikit-image           0.15.0      
scikit-learn           0.21.2      
scipy                  1.3.0      
seaborn                0.9.0
SimpleITK              1.2.0      
six                    1.12.0      
sklearn                0.0 
tensorboardX           1.8
torch                  1.2.0      
torchvision            0.4.0
tqdm                   4.32.2x`
```

##Citation
TBD