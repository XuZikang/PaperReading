### Pyramid Stereo Matching Network(CVPR2018)
+ 现有方法依赖于基于补丁的Siamese网络，缺乏利用上下文信息来寻找对应区域中的对应关系的手段
+ 很多病态区域如遮挡区域、重复出现的表象、低纹理区域、反射表面等。需要全局上下文信息进行整合
+ SPP和膨胀卷积用来扩大感受野，使得PSM-Net可以将像素级的特征扩展至多尺度区域级的特征
+ 全局信息和局部信息结合形成cost volume，再用3D卷积的方式融合多通道信息，正则化cost volume，最终预测视差图
+ PSMNet: Exploit global context information in stereo matching **语义分割**
    + Spatial pyramid pooling：融合不同位置和尺度的信息
    + 3D CNN: Regularize cost volume using stacked multiple hourglass networks
+ 算法优化的两个方向：
    + Accurately compute the matching cost using CNNs and how to apply SGM to refine the disparity map
    + Post-processing of the disparity map
![1](F://学习资料/文献/显微重建/PaperReading/PSM-Net.png)
+ MC-CNN and GC-Net approaches concatenate the left and right features to learn matching cost estimation using deep network.
+ Cost Volume: 4D Volume(height x width x disparity x feature size)
+ Disparity Regression:
    + $ \hat{d}=\sum_{d=0}^{D_{\max }} d \times \sigma\left(-c_{d}\right) $
+ Loss Function:
    + $ L(d, \hat{d})=\frac{1}{N} \sum_{i=1}^{N} \operatorname{smooth}_{L_{1}}\left(d_{i}-\hat{d}_{i}\right) $
    + $ \operatorname{smooth}_{L_{1}}(x)=\left\{\begin{array}{ll}{0.5 x^{2},} & {\text { if }|x|<1} \\ {|x|-0.5,} & {\text { otherwise }}\end{array}\right. $
+