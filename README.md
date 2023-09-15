# Jittor Large Scale Unsupervised Semantic Segmentation (PASS + SAM)
	
## Introduction
![image](https://user-images.githubusercontent.com/20515144/196449430-5ac6a88c-24ea-4a82-8a45-cd244aeb0b3b.png)

Baseline:PASS, containing four steps. 1) A randomly initialized model is trained with self-supervision of pretext tasks。 2) A pixel-attention-based clustering scheme to obtain pseudo categories and assign generated categories to each image pixel. 3) Fine-tune the pre-trained model with the generated pseudo labels to improve the segmentation quality. 4) During inference, the LUSS model assigns generated labels to each pixel of images, same to the supervised model. 

This repo provides four solutions to improve mIoU score based on PASS model and Segment Anything Model. 

## Visualization
<img src="https://github.com/20throokie/SAMPASS-jittor/blob/master/vis/visualization.png">

Results in th first line comes from PASS baseline. After improvement, object localization is more accurate and multiple objects can be detected.

## Description

**Adapter**
<img src="https://github.com/20throokie/SAMPASS-jittor/blob/master/vis/adapter.png">
**Saliency map**
<img src="https://github.com/20throokie/SAMPASS-jittor/blob/master/vis/saliency.png">
**Progressive upsampling**
<img src="https://github.com/20throokie/SAMPASS-jittor/blob/master/vis/progressive_upsampling.png">
**Semantic voting**
<figure class="half">
    <img src="https://github.com/20throokie/SAMPASS-jittor/blob/master/vis/sam1.png">
    <img src="https://github.com/20throokie/SAMPASS-jittor/blob/master/vis/sam2.png">
</figure>


## Citation
```
@article{gao2022luss,
  title={Large-scale Unsupervised Semantic Segmentation},
  author={Gao, Shanghua and Li, Zhong-Yu and Yang, Ming-Hsuan and Cheng, Ming-Ming and Han, Junwei and Torr, Philip},
  journal=TPAMI,
  year={2022}
}
```

## Acknowledgement

This codebase is build based on the [SwAV codebase](https://github.com/facebookresearch/swav).

If you have any other question, open an issue or email us via shgao@live.com


