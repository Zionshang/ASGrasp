# ASGrasp: Generalizable Transparent Object Reconstruction and 6-DoF Grasp Detection from RGB-D Active Stereo Camera
This repository contains the source code for our paper:
[ASGrasp: Generalizable Transparent Object Reconstruction and 6-DoF Grasp Detection from RGB-D Active Stereo Camera](https://arxiv.org/pdf/2405.05648.pdf)

For more information, please visit our [**project page**](https://pku-epic.github.io/ASGrasp/).

## Requirements
The code has been tested with `Python 3.8`, `PyTorch 1.9.1` and `Cuda 11.1`

## Installation

```
sudo apt-get install libopenblas-dev
```

It is recommended to run this project with Python 3.8.

```
conda create -n asgrasp python==3.8
conda activate asgrasp
```

Install the corresponding torch (>=1.8) version that matches your CUDA version; for example, CUDA 11.8:

```bash
pip install torch==2.0.0
```

Install GSNet dependencies
```bash
cd gsnet
pip install -r requirements.txt
```

Compile and install pointnet2 operators.
```bash
cd gsnet/pointnet2
python setup.py install

```
Compile and install knn operator.
```bash
cd gsnet/knn
python setup.py install
```

Install GraspNetAPI dependencies
```bash
cd graspnetAPI
pip install -r requirements.txt
```

## Checkpoints
Please download the [checkpoints](https://drive.google.com/drive/folders/1omayRF-kl_HzkHRs9Ln7Dfn8L7dRUT9S?usp=sharing) to 'checkpoints/'

## Testing
Please run
```
python infer_mvs_2layer_gsnet.py
```

## Acknowledgement
Our code is based on these wonderful repos, we appreciate their great works!

* [RAFT-Stereo](https://github.com/princeton-vl/RAFT-Stereo)
* [IterMVS](https://github.com/FangjinhuaWang/IterMVS)
* [GraspNet](https://github.com/graspnet)
* [graspness_implementation](https://github.com/rhett-chen/graspness_implementation)
* [DREDS](https://github.com/PKU-EPIC/DREDS)

## Contact
If you have any questions, please open a github issue or contact us:

Jun Shi: jun7.shi@samsung.com, Yong A: yong.a@samsung.com, He Wang: hewang@pku.edu.cn
