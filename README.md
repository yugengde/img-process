# img-process
# 图像处理

### 图片的平滑 (图片平滑也称为滤波)
#### 常用的处理平滑的算法:
- 基于二维离散卷积的高斯平滑，均值平滑；
- 基于统计学的中值平滑；
- 具备保持边缘作用的双边滤波，导向滤波。

### 阈值分割
- 阈值分割是基于区域的，简单的通过灰度值信息来提取形状的技术
- 阈值分割后的输出图像只有两种灰度值: 255,0
- 阈值分割处理又常称为图像的二值化处理

### 形态学处理
- 腐蚀: 图像的腐蚀与中值平滑操作类似，它是取每个位置的矩形区域的最小值作为该位置的输出灰度值
- 膨胀: 图像的腐蚀与中值平滑操作类似，它是取每个位置的矩形区域的最大值作为该位置的输出灰度值
- 注意的是这里的邻域不再单纯是矩形区域(可以是椭圆，十字交叉结构，在大多数书中的定义是结构元,它同样需要指定一个锚点)

### 边缘检测
- 图像的边缘指的是灰度值发生急剧变化的位置，可以理解为物理信号的中的高频成分
- 边缘是通过检查每个像素的领域并对灰度变化进行量化的，这种灰度变化的量化相当于微积分里连续函数中方向导数或者离散数列的差分
- 边缘检测大多是通过基于方向导数掩码(梯度方向导数)求卷积的方法

