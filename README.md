# CSRNet_Implement
Please give this git a star if it helps
## Take an Overview
I believe that for the most of the people who are new to the CSRNet may have not understand this model totally yet, therefore I made the ```overview.ipynb```, which will show the image in the dataset and its ground truth density map randomly, moreover, after you have your own weight after training, overview.ipynb can also present the estimated counting and the density map generated by the network and the result will store in the ```overview_img``` automatically.

## Dataset
This model need the dataset ```ShanghaiTech_Crowd_Counting_Dataset``` which you can download from the link below
ShanghaiTech_Crowd_C ounting_Dataset was first introduced in ```Single-Image Crowd Counting via Multi-Column Convolutional Neural Network, in IEEE 2016```, which is a new large-scale crowd counting dataset named Shanghaitech which contains 1198 annotated images, with a total of 330,165 people with centers of their heads annotated.
https://drive.google.com/file/d/16dhJn7k4FWVwByRsQAEpl9lwjuV03jVI/view?usp=sharing

## Replace
Be sure to downlaoad dataset and run replace.py before all, ```replace.py``` will help you replacing all the root in the codes with your own path to the dataset.

## Ground Truth
Before the training, you need to set the grounde truth up through ```make_dataset.py``` and this process may cost you a while, and this is one of the reason why we need CSRNet.

## Training
Use ```python train.py train.json val.json 0 0``` to start, and be sure to take a look about the parses in ```train.py```

## Differece
After you got your own weight, ```speed_test.ipynb``` can show how fast is the network, and will let you understand why we need the CSRNet. Note that you need to put your images waiting to be estimated in the ```Img_to_estimate``` folder, and the result will store in the ```After_estimation``` folder.

## Estimation
With your best weight, ```estimate.ipynb``` can help you present your performance.

## Prerequisities
Python: ```2.7``` , PyTorch: ```0.4.0``` , CUDA: ```9.2```

## Reference
```
@inproceedings{li2018csrnet,
  title={CSRNet: Dilated convolutional neural networks for understanding the highly congested scenes},
  author={Li, Yuhong and Zhang, Xiaofan and Chen, Deming},
  booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  pages={1091--1100},
  year={2018}
} 
```
```
@inproceedings{zhang2016single,
  title={Single-image crowd counting via multi-column convolutional neural network},
  author={Zhang, Yingying and Zhou, Desen and Chen, Siqin and Gao, Shenghua and Ma, Yi},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={589--597},
  year={2016}
}
```
