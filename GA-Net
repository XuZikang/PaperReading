# GA-Net: Guided Aggregation Net for End-to-end Stereo Matching(2019)
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