### GA-Net: Guided Aggregation Net for End-to-end Stereo Matching(2019)
+ End-End 视觉匹配算法的基本流程：
    + Feature Extraction：使用多层CNN进行特征提取（沙漏结构）
    + Match Cost Aggregation：
    + Disparity Prediction：
+ 现有的方法：
    + DispNet
    + GC-Net
    + PSMNet
    + SGM
+ 优化了原有的SGM算法，提出了SGA(Semi-global Guided Aggregation)和LGA(Local Guided Aggregation)，代替原有方法中耗时长的3D-CNN方法，去除了人为设置的参数，使得原有的SGM方法可以使用BP方法进行训练
+ 主要工作：修改SGM中Cost Aggregation的计算方法
+ 网络结构：
    + Feature Extraction
    + Cost Aggregation for the 4D cost volume
    + Guidance subnet
    + Disparity regression
+ 数据集：
    + Scene Flow
    + KITTI
---
反思：
+ 用神经网络做图像识别很大程度上都是基于现有的经典模型，然后去微调结构，而损失函数之类的也基本上是有限的那几种。而神经网络用在立体匹配上，更需要根据立体匹配的经典算法来重新设计网络结构，算是一种转化的过程，将经典算法变成可被训练的结构
下一步计划：
+ 阅读DispNet, GC-Net, PSMNet, SGM的相关论文
+ 学习立体匹配的基础知识
