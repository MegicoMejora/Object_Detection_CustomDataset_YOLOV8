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
From the series of images all the 10 objects were detected successfully with higher confidence.

![image](https://user-images.githubusercontent.com/80173980/229173655-c47d1d23-a24b-4d42-b4e1-87785321a925.png)
![image](https://user-images.githubusercontent.com/80173980/229173865-0cb62a13-e8c8-4f00-ac30-ed9c7ffc4433.png)
![image](https://user-images.githubusercontent.com/80173980/229173950-9d05eab8-0375-4541-98e2-3e262495c1e1.png)
![image](https://user-images.githubusercontent.com/80173980/229174046-b457c960-df4f-4989-81e3-589096336b29.png)
![image](https://user-images.githubusercontent.com/80173980/229174111-2114e8d5-0922-4841-9d84-3566625ca8d8.png)
![image](https://user-images.githubusercontent.com/80173980/229174235-de9e5502-00d4-4477-b85d-9450b19f023b.png)
![image](https://user-images.githubusercontent.com/80173980/229174355-afa7e7b3-0307-4aaa-94d3-6bf6742851bd.png)
![image](https://user-images.githubusercontent.com/80173980/229174417-23f23615-45e0-469d-805b-3bb24b51e3e3.png)
![image](https://user-images.githubusercontent.com/80173980/229174481-f0dddd9c-59ee-4efa-9239-239758aabff4.png)
![image](https://user-images.githubusercontent.com/80173980/229174555-b409472e-6606-47f9-8b5c-b3927b967cdd.png)










