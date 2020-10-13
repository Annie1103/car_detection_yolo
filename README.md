# car_detection_yolo

#### 利用yolov4協助辨識圖檔<br>
#### 環境：[GoogleColab](https://colab.research.google.com/notebooks/intro.ipynb#recent=true) (在執行yolov4之前，首先先檢查Colab的GPU環境）<br>

    ! nvidia-smi


## 1.Git clone darknet <br>

    ! cd darknet; make

## 2.下載訓練好的權重<br>

這裡使用yolov4訓練好的資料 [yolo4.weights](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights) <br>

## 3.將yolo4.weight上傳到Colab環境

## 4.用Python-PIL打開要辨識的圖檔 <br>

    from PIL import Image

    Image.open("/圖片路徑/")

## 5.上傳
