# Comparison of Faster RCNN vs Yolovx

The goal of this assignment is train both models on custom annotated dataset. 

1. Take photos of your environment of two or more objects. (at least 100 instances between all objects) 

2. Annotate them on roboflow. 

3. Train a Faster RCNN model using detectron2

4. Train Yolov4/5/6/7/8 (only one of them of choice) the smallest size

5. Evaluate both models based on mAP and speed and size.


# Taking photos

I desided to detect spoon and fox. So here are example images:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/fox.png" alt="Fox" width="1200"/>

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/spoon.png" alt="Spoon" width="1200"/>

# Annotation with roboflow

This is very easy to annotate obhject detection dataset. Here is a screenshot from the roboflow ui:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/annotation.png" alt="Annotation" width="1200"/>

# Faster RCNN using detectron2

Based on official documentation of detectron2 and roboflow I was able to train Faster RCNN with detectron2. 

Sample predictions:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/rcnn-preds-1.png" alt="preds" width="1200"/>

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/rcnn-preds-2.png" alt="preds" width="1200"/>

# Yolov8

With the usage of yolo client it was super smooth to train yolov8s on custom dataset: 

Sample predictions:

<img src="https://raw.githubusercontent.com/AlekseyKorshuk/aml-faster-rcnn-vs-yolovx/main/docs/yolo-preds.png" alt="preds" width="1200"/>

# Comparison

- Mean Average Precision
  - Faster RCNN: 72%
  - Yolov8: 84.3%
- Speed:
  - Yolo is a lot faster and such speed gives a lot of betefits despite its size
  - Yolo training for 24 epochs done in 4 minutes, but Faster RCNN in 55 minutes
- Size:
  - Fater RCNN model size: 796.5 Mb
  - Yolov8 model size: 21.46 Mb





