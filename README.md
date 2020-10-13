# car_detection_yolo

利用YOLOv4協助辨識圖檔
==
#### 環境：[GoogleColab](https://colab.research.google.com/notebooks/intro.ipynb#recent=true) (在執行YOLOv4之前，首先先檢查Colab的GPU環境）<br>

    ! nvidia-smi 
    


## 從Github上clone darknet <br>

    git clone https://github.com/AlexeyAB/darknet.git
    
## 將YOLOv4編譯成可執行檔<br>

    ! cd darknet; make

## 下載訓練好的權重<br>

#### 這裡使用yolov4訓練好的資料 [yolo4.weights](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights) <br>

## 將yolo4.weight上傳到Colab環境

## 用Python-PIL打開要辨識的圖檔 <br>

    from PIL import Image

    Image.open("/圖片路徑/")

## 上傳
