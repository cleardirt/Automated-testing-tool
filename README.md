# 项目介绍

该项目复现了《The Limitations of Deep Learning in Adversarial Settings》中提出的雅可比显著图(Jacobian Saliency Map) 的攻击样本生成方法。

# 项目结构

```
JSMA
│  jsma.py //主函数文件
│  mnist_net_all.pkl //MNIST数据集的pkl文件
└─mnist
    └─MNIST //MNIST数据集
        └─raw
                t10k-images-idx3-ubyte
                t10k-images-idx3-ubyte.gz
                t10k-labels-idx1-ubyte
                t10k-labels-idx1-ubyte.gz
                train-images-idx3-ubyte
                train-images-idx3-ubyte.gz
                train-labels-idx1-ubyte
                train-labels-idx1-ubyte.gz
```



## 引用库和版本

| 库          | 版本   |
| ----------- | ------ |
| matplotlib  | 3.4.3  |
| numpy       | 1.21.4 |
| torch       | 1.7.1  |
| torchvision | 0.10.0 |

## 项目启动

1.运行main函数，如无数据集则自动下载，如有则直接运行

2.项目绘制对抗性样本的图像后的图像，和图像测试扰动前识别的数字和识别后的数字

## 项目功能概述

首先加载模型，选择测试样本，并通过perturbation_single方法生成对抗性样本，最后绘制对抗性样本的图像