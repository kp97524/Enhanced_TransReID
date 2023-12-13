# Self-Supervised Vision Transformers with DINO
We modify the code from [DINO](https://github.com/facebookresearch/dino). You can refer to the original repo for more details.

## Training
Please set `--data_path`, `filter_path`, `output_dir` and `--keep_num` in the shell files. 
You can set `--keep_num` to 2090122 (50%) or 2508146 (60%) for the conditional training.
60% pre-training data achieves better performance, while 50% pre-training data makes a trade-off between the performance and the computational cost.

- Training ViT-S
```bash
python -W ignore -m torch.distributed.launch --nproc_per_node=8 main_dino.py \
--arch vit_small \
--data_path /home/michuan.lh/datasets/LUP \
--output_dir ./log/dino/lup/vit_small_full_lup \
--height 256 --width 128 \
--crop_height 128 --crop_width 64 \
--epochs 100 \
```

- Training ViT-S+ICS
```bash
python -W ignore -m torch.distributed.launch --nproc_per_node=8 main_dino.py \
--arch ours_vit_small \
--data_path /home/michuan.lh/datasets/LUP \
--output_dir ./log/dino/lup/vit_small_ics_full_lup \
--height 256 --width 128 \
--crop_height 128 --crop_width 64 \
--epochs 100 \

```
