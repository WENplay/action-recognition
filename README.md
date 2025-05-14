# STGT: An Intra-Stream Evolution Feature Extraction Method for Event Camera Action Recognition

## The pipeline of STGT

![](/pipeline.png)

## Key steps for replicating experiments

### Dataset preparation:

1. Action Recognition Dataset [PAF](https://github.com/CrystalMiaoshu/PAFBenchmark)

2. Standard [THU<sup>E-ACT</sup>-50](https://github.com/lujiaxuan0520/THU-EACT-50)

3. Challenging [THU<sup>E-ACT</sup>-50 CHL](https://github.com/lujiaxuan0520/THU-EACT-50)

### Python environment setup with Conda

```bash
conda create -n stgt python=3.10
conda activate stgt

conda install pytorch=1.13 torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia
conda install pyg=2.2 -c pyg -c conda-forge
pip install pyg-lib -f https://data.pyg.org/whl/torch-1.13.0+cu117.html
 
conda install openbabel fsspec rdkit -c conda-forge

pip install pytorch-lightning yacs torchmetrics
pip install performer-pytorch
pip install tensorboardX
pip install ogb
pip install wandb

conda clean --all
```

### Trainning
```bash
conda activate stgt

python main.py --cfg configs/STGT/THU-EACT-50.yaml  wandb.use False

```

### Test

```bash
On the dataset THU<sup>E-ACT</sup>-50.

```
The code will be open sourced after the paper is officially published.
