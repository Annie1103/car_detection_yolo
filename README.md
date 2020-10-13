# car_detection_yolo
`code`

## 1.Git clone darknet <br>

`! cd darknet; make`


## 2.下載訓練好的權重<br>

這裡使用yolov4訓練好的資料 [yolo4.weights](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights) <br>

## 3.用Python-PIL打開圖檔 <br>

`from PIL import Image`

`Image.open("/圖片路徑/")`
