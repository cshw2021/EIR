## Towards Extreme Image Rescaling with Generative Prior and Invertible Prior

Hao Wei, Chenyang Ge, Zhiyuan Li, Xin Qiao, Pengchao Deng.

Institute of Artificial Intelligence and Robotics, Xi’an Jiaotong University

<p align="center">
 <img src="assets/framework.pdf">
 </p>

 if VQIR is helpful for you, please help star this repo. Thanks.

### Updates
- **2024-09-08**: The code is released.
- **2023-12-25**: Repo is released.
- **2023-12-24**: The paper is accepted by IEEE Transactions on Circuits and Systems for Video Technology.

### Installation
```bash
pip install -r requirements.txt
```

### Inference
Download the pretrained weights of VQIR ([16x and 32x](https://drive.google.com/drive/folders/1NRJfaSShSXs2SZ0O0lzCoP4pl6mYKWun?usp=share_link)) and put them into `vqir/pretrained'.
```bash
python vqir/test.py -opt vqir/options/test/test_vqir_stage2.yml
```

### Train
Download the training dataset [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/) and pretrained weights of [VQGAN](https://heibox.uni-heidelberg.de/d/8088892a516d4e3baf92/?p=%2F) which put into `vqir/pretrained/vqgan'
- stage 1: train the IFRM
```bash
python vqir/train.py -opt vqir/options/train/train_vqir_stage1.yml
```
- stage 2: train the MSRM
```bash
python vqir/train.py -opt vqir/options/train/train_vqir_stage2.yml
```

### Acknowledgement
This work is based on [VQGAN](https://github.com/CompVis/taming-transformers), [IRN](https://github.com/pkuxmq/Invertible-Image-Rescaling), and [BasicSR](https://github.com/XPixelGroup/BasicSR). Thanks for their awesome work.

### Contact
If you have any questions, please feel free to reach me out at haowei@stu.xjtu.edu.cn.
