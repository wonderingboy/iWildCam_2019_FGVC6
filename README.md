# iWildCam_2019_FGVC6
top 3% (10/344)  solution for [iWildCam 2019](https://www.kaggle.com/c/iwildcam-2019-fgvc6/overview) competition (Categorize animals in the wild), which is as part of the  [FGVC6](https://sites.google.com/view/fgvc6/home) workshop at [CVPR 2019](http://cvpr2019.thecvf.com/)

### Requirements
* Python 3.6
* pytorch 1.1.0

### About the Code

#### 1. Download the Data
Download the competition data accoring to [here](data/README.md)

#### 2. Detect and Crop the Image 
```
python detect_crop_image.py
```
In my method, I first run object detection and crop the bounding box for classification. 
#### 3. Train the Model
```
python train_model.py
```
#### 4. Prediction

```
python infer.py
```

### About the Method

I got the best single model predicion (f1=0.224 in private lb) with following configuration .

model: efficientnet_b0

image augmentation: Traditional image augmentation + cutout + mixup + label smoothing

 Please view the detailed report  in [iwildcam_2019.pdf](iwildcam_2019.pdf)