# Object_Detection_CustomDataset_YOLOV8

The The objective is to identify 10 objects within a series of images. The objects to detect are,

Phone
Laptop
Mouse
Keyboard
Satellite Dish
Server Rack
Magnifying Glass
Keys
USB Stick
Router

The steps involved in creating the object detction project are

1. Collecting Images
2. Annotating Images
3. Preprocessing Images
4. Generating Images in YOLOV8 format
5. YOLOV8 Model Training
6. Validation and Testing
7. Detecting objects from the series of images

## 1. Collecting Images
Images were collected by using Fatkun Batch Image Downloader. The dataset was cleaned manually, removed images with unsupported formats.

## 2. Annotating Images
The cleaned images were formed as a dataset of representative images with bounding box annotations around the objects that need to be detected. 
This is done by using Roboflow application, https://roboflow.com/ .

## 3. Preprocessing Images
The images were preprocessed by applying Auto-orient and Resize steps to the dataset.

## 4. Generating Images in YOLOV8 format
The annotated dataset was generated fro the format of YOLOV8 model.

## 5. Training
Experimented with different pretrained Yolov models with our custom dataset such as YOLOV5s, YOLOV5x6, YOLOV7 and YOLOV8s, YOLOV8m, YOLOV8l and YOLOV8x. After training with different models YOLOV8x showed better performance than the other models.

The model was initially trained with all the default parameters. To improve the performance of the model the custom dataset experimented with different number of epochs 50, 100, 200, 300 and with batch size of 8, 16.

Finally, YOLOV8x model is trained to detect the custom dataset for 300 epochs with batch size of 16. The image size parameter has been reduced from the default setting 640 to 224, because most of the images in the custom dataset has dimension lesser than the default dimension.

## 6. Validation and Testing
YOLOV8x model was then validated and tested using the validation and test datasets. The model obtained a higher mAP value of 0.77.

## 7. Detecting objects from the series of images
From the series of images all the 10 objects were detected successfully.

