# Self-supervised Learning Model Zoo
## Pretrained models

### MAE

Pretrained on **ImageNet** dataset.

| Config                                                       | Backbone | Params<br>(backbone/total) | Flops | inference time(V100)<br>(ms/img) | Epochs | Download                                                     |
| ------------------------------------------------------------ | -------- | -------------------------- | ----- | -------------------------------- | ------ | ------------------------------------------------------------ |
| [mae_vit_base_patch16_8xb64_400e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mae/mae_vit_base_patch16_8xb64_400e.py) | ViT-B/16 | 85M/111M                   | 9.8G  | 8.03                             | 400    | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-b-400/pretrain_400.pth) |
| [mae_vit_base_patch16_8xb64_1600e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mae/mae_vit_base_patch16_8xb64_1600e.py) | ViT-B/16 | 85M/111M                   | 9.8G  | 8.03                             | 1600   | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-b-1600/pretrain_1600.pth) |
| [mae_vit_large_patch16_8xb32_1600e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mae/mae_vit_large_patch16_8xb32_1600e.py) | ViT-L/16 | 303M/329M                  | 20.8G | 16.30                            | 1600   | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-l-1600/pretrain_1600.pth) |

### Fast ConvMAE

Pretrained on **ImageNet** dataset.

| Config                                                       | Backbone        | Params<br/>(backbone/total) | Flops | inference time(V100)<br/>(ms/img) | Epochs | Download                                                     |
| ------------------------------------------------------------ | --------------- | --------------------------- | ----- | --------------------------------- | ------ | ------------------------------------------------------------ |
| [fast_convmae_vit_base_patch16_8xb64_50e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/fast_convmae/fast_convmae_vit_base_patch16_8xb64_50e.py) | ConvViT-B/16 | 88M/115M                    | 45.1G | 6.88                              | 50     | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/FastConvMAE/pretrained/epoch_50.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/FastConvMAE/pretrained/20220617_110501.log.json) |

> The flops of Fast ConvMAE is about four times of MAE, because the mask of MAE only retains 25% of the tokens each forward, but the mask of Fast ConvMAE adopts a complementary strategy, dividing the mask into four complementary parts with 25% token each part. This is equivalent to learning four samples at each forward, achieving 4 times the learning effect.

### DINO

Pretrained on **ImageNet** dataset.

| Config                                                       | Backbone  | Params<br/>(backbone/total) | inference time(V100)<br/>(ms/img) | Epochs | Download                                                     |
| ------------------------------------------------------------ | --------- | --------------------------- | --------------------------------- | ------ | ------------------------------------------------------------ |
| [dino_deit_small_p16_8xb32_100e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/dino/dino_deit_small_p16_8xb32_100e_tfrecord.py) | DeiT-S/16 | 21M/88M                     | 6.17                              | 100    | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/dino_deit_small/epoch_100.pth) |

### MoBY

Pretrained on **ImageNet** dataset.

| Config                                                       | Backbone  | Params<br/>(backbone/total) | Flops | inference time(V100)<br/>(ms/img) | Epochs | Download                                                     |
| ------------------------------------------------------------ | --------- | --------------------------- | ----- | --------------------------------- | ------ | ------------------------------------------------------------ |
| [moby_deit_small_p16_4xb128_300e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/moby/moby_deit_small_p16_4xb128_300e_tfrecord.py) | DeiT-S/16 | 21M/26M                     | 18.6G | 6.17                              | 300    | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/moby_deit_small_p16/epoch_300.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/moby_deit_small_p16/log.txt) |
| [moby_swin_tiny_8xb64_300e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/moby/moby_dynamic_swin_tiny_8xb64_300e_tfrecord.py) | Swin-T    | 27M/33M                     | 18.1G | 9.74                              | 300    | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/moby_dynamic_swin_tiny/epoch_300.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/moby_dynamic_swin_tiny/log.txt) |

### MoCo V2

Pretrained on **ImageNet** dataset.

| Config                                                       | Backbone | Params<br/>(backbone/total) | Flops | inference time(V100)<br/>(ms/img) | Epochs | Download                                                     |
| ------------------------------------------------------------ | -------- | --------------------------- | ----- | --------------------------------- | ------ | ------------------------------------------------------------ |
| [mocov2_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mocov2/mocov2_rn50_8xb32_200e_tfrecord.py) | ResNet50 | 23M/28M                     | 8.2G  | 8.59                              | 200    | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mocov2_r50/epoch_200.pth) |

### SwAV

Pretrained on **ImageNet** dataset.

| Config                                                       | Backbone | Params<br/>(backbone/total) | Flops | inference time(V100)<br/>(ms/img) | Epochs | Download                                                     |
| ------------------------------------------------------------ | -------- | --------------------------- | ----- | --------------------------------- | ------ | ------------------------------------------------------------ |
| [swav_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/swav/swav_rn50_8xb32_200e_tfrecord.py) | ResNet50 | 23M/28M                     | 12.9G | 8.59                              | 200    | [model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/swav_r50/epoch_200.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/swav_r50/log.txt) |

## Benchmarks

For detailed usage of benchmark tools, please refer to benchmark [README.md](../../benchmarks/selfsup/README.md).

### ImageNet Linear Evaluation

| Algorithm | Linear Eval Config                                           | Pretrained Config                                            | Top-1 (%) | Download                                                     |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------- | ------------------------------------------------------------ |
| SwAV      | [swav_resnet50_8xb2048_20e_feature](../../benchmarks/selfsup/classification/imagenet/swav_r50_8xb2048_20e_feature.py) | [swav_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/swav/swav_rn50_8xb32_200e_tfrecord.py) | 73.618    | [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/imagenet_linear_eval/swav_r50_linear_eval/20220216_101719.log.json) |
| DINO      | [dino_deit_small_p16_8xb2048_20e_feature](../../benchmarks/selfsup/classification/imagenet/dino_deit_small_p16_8xb2048_20e_feature.py) | [dino_deit_small_p16_8xb32_100e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/dino/dino_deit_small_p16_8xb32_100e_tfrecord.py) | 71.248    | [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/imagenet_linear_eval/dino_deit_small_linear_eval/20220215_141403.log.json) |
| MoBY | [moby_deit_small_p16_8xb2048_30e_feature](../../benchmarks/selfsup/classification/imagenet/moby_deit_small_p16_8xb2048_30e_feature.py) | [moby_deit_small_p16_4xb128_300e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/moby/moby_deit_small_p16_4xb128_300e_tfrecord.py) | 72.214    | [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/imagenet_linear_eval/moby_deit_small_p16_linear_eval/20220414_134929.log.json) |
| MoCo-v2   | [mocov2_resnet50_8xb2048_40e_feature](../../benchmarks/selfsup/classification/imagenet/mocov2_r50_8xb2048_40e_feature.py) | [mocov2_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mocov2/mocov2_rn50_8xb32_200e_tfrecord.py) | 66.8      | [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/imagenet_linear_eval/mocov2_r50_linear_eval/20220214_143738.log.json) |

### ImageNet Finetuning

| Algorithm | Fintune Config                                               | Pretrained Config                                            | Top-1 (%) | Download                                                     |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------- | ------------------------------------------------------------ |
| **MAE**   | [mae_vit_base_patch16_8xb64_100e_lrdecay075_fintune](../../benchmarks/selfsup/classification/imagenet/mae_vit_base_patch16_8xb64_100e_lrdecay075_fintune.py) | [mae_vit_base_patch16_8xb64_400e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mae/mae_vit_base_patch16_8xb64_400e.py) | 83.13     | [fintune model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-b-400/fintune_400.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-b-400/20220126_171312.log.json)|
|           | [mae_vit_base_patch16_8xb64_100e_lrdecay065_fintune](../../benchmarks/selfsup/classification/imagenet/mae_vit_base_patch16_8xb64_100e_lrdecay065_fintune.py) | [mae_vit_base_patch16_8xb64_1600e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mae/mae_vit_base_patch16_8xb64_1600e.py) | 83.55     | [fintune model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-b-1600/fintune_1600.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-b-1600/20220426_101532.log.json)|
|           | [mae_vit_large_patch16_8xb16_50e_lrdecay075_fintune](../../benchmarks/selfsup/classification/imagenet/mae_vit_large_patch16_8xb16_50e_lrdecay075_fintune.py) | [mae_vit_large_patch16_8xb32_1600e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mae/mae_vit_large_patch16_8xb32_1600e.py) | 85.70     | [fintune model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-l-1600/fintune_1600.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/mae/vit-l-1600/20220427_150629.log.json)|
| **Fast ConvMAE** | [fast_convmae_vit_base_patch16_8xb64_100e_fintune](https://github.com/alibaba/EasyCV/tree/master/benchmarks/selfsup/classification/imagenet/fast_convmae_vit_base_patch16_8xb64_100e_fintune.py) | [fast_convmae_vit_base_patch16_8xb64_50e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/fast_convmae/fast_convmae_vit_base_patch16_8xb64_50e.py) | 84.37     | [fintune model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/FastConvMAE/imagenet_finetune/epoch_100.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/FastConvMAE/imagenet_finetune/20220621_160255.log.json) |

### COCO2017 Object Detection

| Algorithm | Eval Config                                                  | Pretrained Config                                            | mAP (Box) | mAP (Mask) | Download                                                     |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------- | ---------- | ------------------------------------------------------------ |
| **Fast ConvMAE** | [mask_rcnn_conv_vitdet_50e_coco](https://github.com/alibaba/EasyCV/tree/master/benchmarks/selfsup/detection/coco/mask_rcnn_conv_vitdet_50e_coco.py) | [fast_convmae_vit_base_patch16_8xb64_50e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/fast_convmae/fast_convmae_vit_base_patch16_8xb64_50e.py) | 51.3 | 45.6 | [eval model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/FastConvMAE/maskrcnn_coco_finetune/epoch_50.pth) |
| SwAV      | [mask_rcnn_r50_fpn_1x_coco](https://github.com/alibaba/EasyCV/tree/master/benchmarks/selfsup/detection/coco/mask_rcnn_r50_fpn_1x_coco.py) | [swav_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/swav/swav_rn50_8xb32_200e_tfrecord.py) | 40.38     | 36.48      | [eval model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/detection/mask_rcnn_r50_fpn/mocov2_r50/epoch_12.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/detection/mask_rcnn_r50_fpn/mocov2_r50/20220510_164934.log.json) |
| MoCo-v2   | [mask_rcnn_r50_fpn_1x_coco](https://github.com/alibaba/EasyCV/tree/master/benchmarks/selfsup/detection/coco/mask_rcnn_r50_fpn_1x_coco.py) | [mocov2_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mocov2/mocov2_rn50_8xb32_200e_tfrecord.py) | 39.9     | 35.8      | [eval model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/detection/mask_rcnn_r50_fpn/swav_r50/epoch_12.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/detection/mask_rcnn_r50_fpn/swav_r50/20220513_142102.log.json) |
| MoBY | [mask_rcnn_swin_tiny_1x_coco](https://github.com/alibaba/EasyCV/tree/master/benchmarks/selfsup/detection/coco/mask_rcnn_swin_tiny_1x_coco.py) | [moby_swin_tiny_8xb64_300e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/moby/moby_dynamic_swin_tiny_8xb64_300e_tfrecord.py) | 43.11 | 39.37 | [eval model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/detection/swin_tiny/moby/epoch_12.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/detection/swin_tiny/moby/20220523_114410.log.json) |

### VOC2012 Aug Semantic Segmentation

| Algorithm | Eval Config                                                  | Pretrained Config                                            | mIOU  | Download                                                     |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----- | ------------------------------------------------------------ |
| SwAV      | [fcn_r50-d8_512x512_60e_voc12aug](https://github.com/alibaba/EasyCV/tree/master/benchmarks/selfsup/segmentation/voc/fcn_r50-d8_512x512_8xb4_60e_voc12aug.py) | [swav_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/swav/swav_rn50_8xb32_200e_tfrecord.py) | 63.91 | [eval model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/segmentation/swav_fcn_r50/epoch_60.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/segmentation/swav_fcn_r50/20220525_171032.log.json) |
| MoCo-v2   | [fcn_r50-d8_512x512_60e_voc12aug](https://github.com/alibaba/EasyCV/tree/master/benchmarks/selfsup/segmentation/voc/fcn_r50-d8_512x512_8xb4_60e_voc12aug.py) | [mocov2_resnet50_8xb32_200e](https://github.com/alibaba/EasyCV/tree/master/configs/selfsup/mocov2/mocov2_rn50_8xb32_200e_tfrecord.py) | 68.49 | [eval model](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/segmentation/mocov2_fcn_r50/epoch_60.pth) - [log](http://pai-vision-data-hz.oss-cn-zhangjiakou.aliyuncs.com/EasyCV/modelzoo/selfsup/benchmarks/segmentation/mocov2_fcn_r50/20220525_211410.log.json) |
