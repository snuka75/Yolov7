Face Mask Detection with YOLOv7

In this project, we fine-tuned the YOLOv7 object detection framework to perform face mask compliance detection across three categories: Correctly Worn Mask, Incorrectly Worn Mask, and No Mask. I collaborated with Yashwanth to bring this project to life.

We began by training YOLOv7 on the COCO dataset to build a strong general object recognition foundation. After successfully completing that phase, we transitioned into custom training by sourcing a raw face mask dataset from Kaggle. We manually annotated this dataset using the Computer Vision Annotation Tool (CVAT) to ensure high-quality, labeled data suited for our specific task.

Our fine-tuning process involved modifying the YOLOv7 architecture for a three-class setup, adjusting training configurations, and optimizing hyperparameters. Training was performed with an image size of 640x640, a batch size of 8, SGD optimizer with momentum, and advanced augmentations like Mosaic and random flips. We closely monitored the model's performance through TensorBoard visualizations.

The results were strong: the model achieved a mean Average Precision (mAP@0.5) of approximately 74%, and a mAP@0.5:0.95 of around 48%, indicating consistent detection performance across strict IoU thresholds. Precision reached over 85%, and recall climbed above 70%, demonstrating the model’s ability to make accurate and reliable detections.

To replicate or build upon this project, clone the repository, install the required dependencies, and follow the training and inference scripts provided. Training can be started with the prepared configurations, and detections can be run on new images easily through the detect.py script.
