# Introduction

Slightly modified [Pytorch-Yolov4 repository](https://github.com/Tianxiaomo/pytorch-YOLOv4) with better darknet to onnx support.

## How to modify from darknet to onnx

``` shell
# pytorch-YOLOv4 repo의 root directory에서...
python demo_darknet2onnx.py .\yolov4-csp-leaky-vmd.cfg .\yolov4_vehicle.names .\yolov4-csp-leaky-vmd_final.weights ex_img.jpg 1
  
# More general format is:
# python demo_darknet2onnx.py <cfgFile> <namesFile> <weightFile> <imageFile> <batchSize>
```

## Tested model conversions

- yolov4_csp
- yolov3_spp
- yolov7_tiny

## Other notes

Use `add_nms_to_graph.py` if you have to add nms plugin for tensorrt!