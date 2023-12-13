**CS 771: Learning based Methods of Computer Vision - Final Project**

Thi project is based on the [transReID](https://arxiv.org/pdf/2102.04378.pdf) model which is used to perfom Object Re-identification task. Here, we first test the model and understand what are the key modules present in it.It has an important module, the Jigsaw Patch Module, which consists of hyperparameters that could be tuned to increase its performance. Then we explore two options with the aim of enhancing the model and present all results in our Final Report.


**Hyper-parameter Tuning with TransReID**
With the TRansREID model with a backbone of DeIT base model, we changed the JPM parameters _C.MODEL.SHIFT_NUM, and _C.MODEL.SHUFFLE_GROUP in the config file defaults.py. We then rained and evaluated this model on the Market-1501 dataset and present our results. The config file can be found at /TransReID/configs/Market/deit_transreid_stride.yml

**Gaussian Noise and Zero Masking**
We replaced the JPM with Gaussian Noise addition and Zero Masking techniques to further analyze the performance of the model. For this we made changes in the TransReID/model/make_model.py.

**Self Supervised Pre-training with DINO**
We used the /Dino to pre-train ViT-S model with DINO methodology.This code is publicly available. We then gave this pre-trained model as the backbone of our TransReID model and evaluated its performance on the Market-1501 dataset and present its results.
