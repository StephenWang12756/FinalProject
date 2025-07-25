HomeS

HomeS or Home Security is a project which uses AI to detect intruders. HomeS is also used for facial recognition. People who have access for example people who live in your home or friends that visit often. 

HomeS uses Jetson Orin Nano, Ultralytics and yolov8n.



## Installation


1. To install Yolov8

```bash
  pip install ultralytics
```
2. This command trains the AI and Epochs=50 makes the AI go through the AI 50 times

```bash
yolo task=classify mode=train model=yoolov8n-cls data=dataset epochs=50 imgsz=224
```
3. This command checks the accuracy of the AI
```bash
yolo task=classify mode=val model=/home/nvidia12/FinalProject/runs/classify/trsin5/weights/best.pt data=/home/nvidia12/FinalProject/dataset/test
```

4. This will make predictions
```bash
yolo task=classify mode=predict model=/home/nvidia12/FinalProject/runs/classify/train5/weights/best.pt source=/home/nvidia12/FinalProject/dataset/test
```

5. This allows the user to use in an app or website
```bash
yolo export model=/home/nvidia12/FinalProject/runs/classify/train5/weights/best.pt
```