# StrongSORT-Object-Tracking
This repository implements StrongSORT which is an upgraded version of DeepSORT, with YOLOv5 detections, which is fine tuned on custom dataset, to track cars in a parking lot. It has an additional security feature implemented which activates an alert as soon as a car moves from its position.

## Initialize repository 
%cd Yolov5_StrongSORT_OSNet

%pip install -r requirements.txt  # install dependencies

## Initialize torchreid
git clone https://github.com/KaiyangZhou/deep-person-reid.git

cd deep-person-reid

pip install -r requirements

python setup.py develop

cd ../

## Initialize yolov5 repositrory
!git clone https://github.com/ultralytics/yolov5


## Start Tracking
!python track.py --yolo-weights  yolov5s.pt --strong-sort-weights osnet_x0_25_msmt17.pt --source test.mp4 --save-vid
