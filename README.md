# Scaled-YOLOv4-HarDNet
## Installation
```
# install mish-cuda, if you use different pytorch version, you could try https://github.com/thomasbrandon/mish-cuda
cd /
git clone https://github.com/JunnYu/mish-cuda
cd mish-cuda
python setup.py build install
```
## Train
```
cd Scaled-YOLOv4-HarDNet/
#need to add data.yaml
python train.py --img 416 --batch 72 --epochs 300 --data ../data.yaml --cfg ./models/yolov4-csp.yaml --weights '' --name yolov4-hardnet-results-1 --cache
```
## Detect
```
python detect.py --weights ./runs/yolov4-hardnet-results-1/weights/best_yolov4-hardnet-results-1.pt --img 416 --conf 0.4 --source ../test/images --output inference/output/yolov4/p7v3 --save-txt
```
