# car_detection_yolo

利用YOLOv4協助辨識圖檔
=
<建立環境>
-
1.環境：[GoogleColab](https://colab.research.google.com/notebooks/intro.ipynb#recent=true) (在執行YOLOv4之前，首先先檢查Colab的GPU環境）<br>
-
    ! nvidia-smi 
    
2.查看Makefile並修改參數加速GPU
-
#### 打開Makefile
    
    ! head darknet/Makefile
    
#### 使用以下程式修改參數
    
    ! sed -i "s/GPU=0/GPU=1/g" /content/darknet/Makefile
    ! sed -i "s/CUDNN=0/CUDNN=1/g" /content/darknet/Makefile
    ! sed -i "s/OPENCV=0/OPENCV=1/g" /content/darknet/Makefile
    
3.從Github上clone darknet 
-
    ! git clone https://github.com/AlexeyAB/darknet.git
    
4.下載訓練好的權重
-
#### 這裡使用yolov4訓練好的資料 [yolo4.weights](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights) <br>

5.將yolo4.weight上傳到Colab環境
-
    
6.將YOLOv4編譯成可執行檔
-
    ! cd darknet; make

<開始準備辨識>
-
1.建立一個資料夾並上傳要辨識的圖檔
-
2.用Python-PIL打開要辨識的圖片 
-
    from PIL import Image

    Image.open("/圖片路徑/")


2.開始辨識(注意YOLOv4的路徑）
-
    ! cd /content/darknet; ./darknet detect /content/darknet/cfg/yolov4.cfg /content/yolov4.weights /content/cartraining/car001.JPG
    
3.查看辨識後的圖片
-
    from PIL import Image

    Image.open("/content/darknet/predictions.jpg")
