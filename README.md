# Resnet_Classification_CIFAR100

## 包含的文件夹介绍

train.py 用于训练网络和测试；

Data_augmentation_vis.ipynb 为数据集及结果的可视化工作；

utils文件夹包含data augmentation所需的一些函数和类；

checkpoints包含已完成训练的模型，模型的下载链接：

model文件夹提供可选择的网络结构（可更改args.model），本次实验选择的网络结构为Resnet-18。

## 模型的运行指令
- 运行baseline的命令：

  ```
  python train.py --method baseline --dataset cifar100 --model resnet18 --epochs 200
  ```

- 运行cutout的命令：

  ```
  python train.py --method cutout --dataset cifar100 --model resnet18 --data_augmentation --epochs 200
  ```

- 运行mixup的命令：

  ```
  python train.py --method mixup --dataset cifar100 --model resnet18 --data_augmentation --epochs 200
  ```

- 运行cutmix的命令：

  ```
  python train.py --method cutmix --dataset cifar100 --model resnet18 --data_augmentation --epochs 200  --cutmix_prob 0.1
  ```
