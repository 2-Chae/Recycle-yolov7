# Recycle Detecion using YOLOv7

Our code is based on [YOLOv7](https://github.com/WongKinYiu/yolov7).  
Details of implementation- [YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://arxiv.org/abs/2207.02696)

## Installation

#### Requirements
- python 3.7+
- PyTorch 1.12.1
- TorchVision 0.13.1
- Details are specified in [requirements.txt](./requirements.txt).

`pip install -r requirements.txt` before you run the code.

</details>


## Training

``` shell
python train.py --workers 8 --device 0 --batch-size 64 --data data/recycle.yaml --img 640 640 --cfg cfg/training/yolov7.yaml --weights 'yolov7_training.pt' --hyp data/hyp.scratch.p5.yaml --epochs 100 --project recycle_yolov7 
```


## Test
```shell
python test.py --data data/recycle.yaml --img 640 --batch 32 --conf 0.001 --iou 0.65 --device 0 --weights recycle_yolov7/Aug26_01-00-42/weights/last.pt --name yolov7_640_val

```
