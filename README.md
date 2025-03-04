:heavy_exclamation_mark:**DISCLAIMER**: this is a fork of [Anomaly-Transformer repository](https://github.com/thuml/Anomaly-Transformer) adjusted to run [FIREMAN](https://github.com/5uperpalo/FIREMAN-project) datasets.
# Setup environment
How to setup python venv to run the code on linux machine:
```bash
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get install python3.6
sudo apt-get install python3.6-venv
mkdir ~/.venvs
python3.6 -m venv ~/.venvs/anomaly-transformer
source ~/.venvs/anomaly-transformer/bin/activate
pip install torch==1.4.0 sklearn pandas pillow
```

# Anomaly-Transformer (ICLR 2022 Spotlight)
Anomaly Transformer: Time Series Anomaly Detection with Association Discrepancy

Unsupervised detection of anomaly points in time series is a challenging problem, which requires the model to learn informative representation and derive a distinguishable criterion. In this paper, we propose the Anomaly Transformer in these three folds:

- An inherent distinguishable criterion as **Association Discrepancy** for detection.
- A new **Anomaly-Attention** mechanism to compute the association discrepancy.
- A **minimax strategy** to amplify the normal-abnormal distinguishability of the association discrepancy.

<p align="center">
<img src=".\pics\structure.png" height = "350" alt="" align=center />
</p>

## Get Started

1. Install Python 3.6, PyTorch 1.4.0. (Note: Higher PyTorch version may cause error.)
2. Download data. You can obtain four benchmarks from [Tsinghua Cloud](https://cloud.tsinghua.edu.cn/d/9605612594f0423f891e/). **All the datasets are well pre-processed**. For the SWaT dataset, you can apply for it by following its official tutorial.
3. Train and evaluate. We provide the experiment scripts of all benchmarks under the folder `./scripts`. You can reproduce the experiment results as follows:
```bash
bash ./scripts/SMD.sh
bash ./scripts/MSL.sh
bash ./scripts/SMAP.sh
bash ./scripts/PSM.sh
bash ./scripts/LLFault.sh
bash ./scripts/SinglePhaseSag.sh
bash ./scripts/ThreePhaseGridFault.sh
bash ./scripts/ThreePhaseSensorFault.sh
```

## Main Result

We compare our model with 15 baselines, including THOC, InterFusion, etc. **Generally,  Anomaly-Transformer achieves SOTA.**

<p align="center">
<img src=".\pics\result.png" height = "450" alt="" align=center />
</p>

## Citation
If you find this repo useful, please cite our paper. 

```
@inproceedings{
xu2022anomaly,
title={Anomaly Transformer: Time Series Anomaly Detection with Association Discrepancy},
author={Jiehui Xu and Haixu Wu and Jianmin Wang and Mingsheng Long},
booktitle={International Conference on Learning Representations},
year={2022},
url={https://openreview.net/forum?id=LzQQ89U1qm_}
}
```

## Contact
If you have any question, please contact xjh20@mails.tsinghua.edu.cn, whx20@mails.tsinghua.edu.cn.
