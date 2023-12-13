**CS 771: Learning based Methods of Computer Vision - Final Project**

Tasks performed as a part of this project:

**Hyper-parameter Tuning with TransReID**
We changed the JPM parameters _C.MODEL.SHIFT_NUM, and _C.MODEL.SHUFFLE_GROUP in the file /TransReID/config/defaults.py. We trained and evaluated the model using DeIT base model. The config file can be found at /TransReID/configs/Market/deit_transreid_stride.yml

**Gaussian Noise and Zero Masking**
We added some code in /TransReID/model/make_model.py, for Gaussian Noise addition and Zero Masking.

**Self Supervised Pre-training with DINO**
We used the /Dino to pre-train ViT-S model with DINO methodology. This code is publicly available. We then gave this pre-trained model as input to TransReID. The config file can be found here: /TransReID/configs/Market/vit_small_ics.yml
