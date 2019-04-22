### Practical Deep Stereo (PDS): Toward applications-friendly deep stereo matching(NIPS2018)
+ 现有的方法
    + PSM
    + CRL
    + iResNet-i2
    + DispNet-corr1D
    + LRCR
    + GC
+ Pipeline
    + Embedding
    + Matching: cost volume for every disparity
    + Regularization: a hourglass network with shortcut connections between the concracting and the expanding parts
    + Refinement: refines the initial lowresolution disparity relying on attention map
+ 主要工作
    + 用于推理的新颖的超像素MAP近似，其以最小匹配成本计算差异周围的均值
    + 相较于文献中的`modest-size image patches`，使用`train on full-size images`
    + A novel bottleneck matching module -> Decrease memory footprint
    + Training阶段，使用`sub-pixel criterion`
+ 提供了一个以往方法在KITTI上的3PE和Time天梯图
---
反思：
+ 应该先看一看视觉匹配的基础知识，了解例如disparity, cost volume的概念，才能更好的理解文章的意思