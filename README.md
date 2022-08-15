# StrongSORT-Object-Tracking
This repository implements StrongSORT which is an upgraded version of DeepSORT, with YOLOv5 detections, which is fine tuned on custom dataset, to track cars in a parking lot. It has an additional security feature implemented which activates an alert as soon as a car moves from its position.

## Initialize repository 
%cd Yolov5_StrongSORT_OSNet

%pip install -qr requirements.txt  # install dependencies

## Start Tracking

!python track.py --yolo-weights  yolov5s.pt --strong-sort-weights osnet_x0_25_msmt17.pt --source test.mp4 --save-vid