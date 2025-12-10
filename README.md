High-resolution aeromagnetic map through  transformer and CNNs
This is Originally code from : https://github.com/XY-boy/TTST

ABSTRACT:
This study investigated deep learning–based super-resolution methods for enhancing the resolution of magnetic data from Quebec (Canada). We evaluated recent learning approaches, including attention mechanisms and residual architectures, to address the limited generalization typically observed in GAN-based models. we adapted four architcetures including EDSR, RCAN, HAT and TTST. 
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
🎁 Dataset

Please download the following remote sensing benchmark:

Data Type	Link[https://github.com/Biondokin-92/Super-resolution-aeromagnetic-data/tree/main/AID-tiny/Train]

Dataset Structure

The downloaded folder contains two subfolders:

GT : Ground Truth (high-resolution images)

LR : Low-Resolution images
Each image must be in PNG format, with the following naming convention:
/GT/
000_GT.png
001_GT.png
...
/LR/
000_LR.png
001_LR.png
...

|Training | [Download](https://captain-whu.github.io/AID/) | None | None | None |
|Testing | [Download](https://captain-whu.github.io/AID/) | [Download](https://captain-whu.github.io/DOTA/dataset.html) | [Download](https://drive.google.com/drive/folders/1UdlgHk49iu6WpcJ5467iT-UqNPpx__CC) | [Download](https://onedrive.live.com/?authkey=%21AHHNaHIlzp%5FIXjs&id=5C5E061130630A68%21107&cid=5C5E061130630A68&parId=root&parQt=sharedby&o=OneUp)
## 🧩 Usage
### Quick Test
[Download Pre-trained Model](https://github.com/XY-boy/TTST/blob/main/saved_models/ttst_4x.pth)
- **Step I.**  Use the structure below to prepare your dataset.

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
### Aaeromagnetic map 

![High-resolution aeromagnetic map](fig/QuebecHRLR_MagneticMap.png)
![Example of generated maps from different models](fig/Results_1_SR.png)
![Vertical derivation](fig/VD.png)
![Loss](fig/Loss.png)
![Cross-plot](fig/CrossPlot_ALL.png)
![PSNR/SSIM Comparison](fig/psnr_ssim_comparison_7.png)


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

