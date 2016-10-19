# Faster-RCNN_TF

This is an experimental Tensorflow implementation of Faster RCNN - a convnet for object detection with a region proposal network.
For details about R-CNN please refer to the paper [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks](http://arxiv.org/pdf/1506.01497v3.pdf) by Shaoqing Ren, Kaiming He, Ross Girshick, Jian Sun.


### Requirements: software

1. Requirements for Tensorflow (see: [Tensorflow](https://www.tensorflow.org/))

2. Python packages you might not have: `cython`, `python-opencv`, `easydict`

### Requirements: hardware

1. For training the end-to-end version of Faster R-CNN with VGG16, 3G of GPU memory is sufficient (using CUDNN)

### Installation (sufficient for the demo)

1. Clone the Faster R-CNN repository
  ```Shell
  # Make sure to clone with --recursive
  git clone --recursive https://github.com/smallcorgi/Faster-RCNN_TF.git
  ```

2. Build the Cython modules
    ```Shell
    cd $FRCN_ROOT/lib
    make
    ```

### Demo

*After successfully completing [basic installation](#installation-sufficient-for-the-demo)*, you'll be ready to run the demo.

To run the demo
```Shell
cd $FRCN_ROOT
./tools/demo.py --model model_path
```
The demo performs detection using a VGG16 network trained for detection on PASCAL VOC 2007.


### Training Results

Download model training on PASCAL VOC 2007 [here](https://drive.google.com/open?id=0ByuDEGFYmWsbZ0EzeUlHcGFIVWM).

| Classes       | AP     |
|-------------|--------|
| aeroplane   | 0.698 |
| bicycle     | 0.788 |
| bird        | 0.657 |
| boat        | 0.565 |
| bottle      | 0.478 |
| bus         | 0.762 |
| car         | 0.797 |
| cat         | 0.793 |
| chair       | 0.479 |
| cow         | 0.724 |
| diningtable | 0.648 |
| dog         | 0.803 |
| horse       | 0.797 |
| motorbike   | 0.732 |
| person      | 0.770 |
| pottedplant | 0.384 |
| sheep       | 0.664 |
| sofa        | 0.650 |
| train       | 0.766 |
| tvmonitor   | 0.666 |
| mAP        | 0.681 |


### Download pre-trained ImageNet models

If you want to train the model by yourself, and you can download the pre-trained ImageNet models [here](https://drive.google.com/open?id=0ByuDEGFYmWsbNVF5eExySUtMZmM).
