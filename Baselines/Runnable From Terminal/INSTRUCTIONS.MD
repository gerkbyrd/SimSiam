#MoCo:
Pre-training:
python main_moco.py

Evaluation (lin. classification):
python main_lincls.py --pretrained [your checkpoint path]/checkpoint_0199.pth.tar

#BYOL:
Pre-training:
python -m byol.main_loop \
  --experiment_mode=<'pretrain' or 'linear-eval'> \
  --worker_mode=<'train' or 'eval'> \
  --checkpoint_root=</path/to/the/checkpointing/folder> \
  --pretrain_epochs=<40, 100, 300 or 1000>
  
Evaluation (lin. classification):
  --experiment_mode='linear-eval' \
  --worker_mode=<'train' or 'eval'> \
  --checkpoint_root=</path/to/the/checkpointing/folder> \
  --pretrain_epochs=<40, 100, 300 or 1000>
