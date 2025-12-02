High-resolution aeromagnetic map through  transformer and CNNs



### :tada::tada: News :tada::tada:

ABSTRACT
Given the diversity of optimization techniques available for super-resolution, the quality of reconstructed outputs often varies substantially with the characteristics of the input data. Identifying the most suitable optimization strategy for a given dataset is therefore crucial. In the case of aeromagnetic surveys, accuracy is especially important, as high-fidelity reconstructions are essential for producing robust geological interpretations.
Several studies have explored the use of perceptual loss functions and adversarial optimization to enhance aeromagnetic resolution. Although these GAN-based approaches can generate visually appealing results, they suffer from notable limitations. Perceptual losses are designed to align with human visual preferences, yet they often fail to preserve pixel-level fidelity resulting in degraded quantitative performance in metrics such as PSNR and SSIM. This mismatch between visual realism and numerical accuracy poses a challenge for geological applications, where structural precision is indispensable. we examine a broad range of learning and optimization strategies implemented across multiple architectures for aeromagnetic super-resolution. Through a comparative analysis, we assess the ability of Transformer-based models and convolutional neural networks (CNNs) to recover high-frequency geological information. Our goal is to determine whether attention-driven architectures and residual CNN designs can mitigate the limitations inherent to adversarial methods achieving both pixel fidelity and realistic visualisation. For this purpose, we implement four state-of-the-art architectures that incorporate attention mechanisms and residual learning to generate highly consistent super-resolution aeromagnetic maps. Our findings indicate that even well-designed, relatively simple CNNs can outperform carefully optimized GAN models. Networks trained with adversarial objectives consistently achieved lower validation metrics. This behavior is primarily caused by the nature of their objective function and the dynamics of adversarial optimization, which tend to prioritize fooling a discriminator overachieving stable, generalizable feature representations. In contrast, Transformer-based architectures particularly hybrid attention models outperformed all other approaches, producing highly accurate reconstructions and superior recovery of high-frequency geological structures.

 
## 🧩 Install
```
git clone https://github.com/XY-boy/TTST.git
```

## Environment
 > * CUDA 11.1
 > * Python 3.9.13
 > * PyTorch 1.9.1
 > * Torchvision 0.10.1
 > * basicsr 1.4.2 

## 🎁 Dataset
Please download the following remote sensing benchmarks:
| Data Type | [AID](https://captain-whu.github.io/AID/) | [DOTA-v1.0](https://captain-whu.github.io/DOTA/dataset.html) | [DIOR](https://www.sciencedirect.com/science/article/pii/S0924271619302825) | [NWPU-RESISC45](https://ieeexplore.ieee.org/abstract/document/7891544)
| :----: | :-----: | :----: | :----: | :----: |
|Training | [Download](https://captain-whu.github.io/AID/) | None | None | None |
|Testing | [Download](https://captain-whu.github.io/AID/) | [Download](https://captain-whu.github.io/DOTA/dataset.html) | [Download](https://drive.google.com/drive/folders/1UdlgHk49iu6WpcJ5467iT-UqNPpx__CC) | [Download](https://onedrive.live.com/?authkey=%21AHHNaHIlzp%5FIXjs&id=5C5E061130630A68%21107&cid=5C5E061130630A68&parId=root&parQt=sharedby&o=OneUp)
## 🧩 Usage
### Quick Test
[Download Pre-trained Model](https://github.com/XY-boy/TTST/blob/main/saved_models/ttst_4x.pth)
- **Step I.**  Use the structure below to prepare your dataset.

/xxxx/xxx/ (your data path)
```
/GT/ 
   /000.png  
   /···.png  
   /099.png  
/LR/ 
   /000.png  
   /···.png  
   /099.png  
```
- **Step II.**  Change the `--data_dir` to your data path.
- **Step III.**  Run the eval_4x.py
```
python eval_4x.py
```
### Train
```
python train_4x.py
```

## 🖼️ Results
### Quantitative
 ![image](/fig/red.png)

### Visual
 ![image](/fig/dota.png)

## Acknowledgments
Our TTST mainly borrows from DRSFormer (https://github.com/cschenxiang/DRSformer) and [SKNet](https://github.com/implus/SKNet).  
Thanks for these excellent open-source works!

## Contact
If you have any questions or suggestions, feel free to contact me.  
Email: xiao_yi@whu.edu.cn; xy574475@gmail.com

## Citation
If you find our work helpful in your research, please consider citing it. We appreciate your support！😊

```
# Super-resolution Aeromagnetic Data

High-resolution aeromagnetic map through Transformer and CNNs

### Quantitative
![High-resolution aeromagnetic map](fig/QuebecHRLR_MagneticMap.png)

### Visual
![Loss curve](fig/Loss - Copy.png)

## Requirements
- Python 3.8
- tensorlayer>=2.0.0
- imgaug>=0.2.5
- h5py==2.10.0
- tensorflow-gpu==2.0.0
- CUDA 10.1
- cuDNN 7.4

## Usage
### Quick Test
- Step I: Prepare your dataset

