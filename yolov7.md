### yolov7
#### 前言
- 在不同的edge device上速度优化
- edge CPU：MCUNet、NanoDet
- GPU：YOLOX、YOLOR
- CPU：MobileNet、ShuffleNet、GhostNet
- GPU：ResNet、DarkNet、DLA、CSPNet
#### 贡献点
- trainable bag-of-freebies methods
- re-parameterized module和dynamic label assignment strategy
- “extend” and “compound scaling” methods
#### 相关工作
- 重参数化：
- 模型层重参数化
  - 1、使用不同数据训练多个模型，使其参数平均化
  - 2、参数平均化不同迭代周期的模型
- 模块层重参数化
  - 在训练时，一个模块分成相同或不同的模块分支，在推理阶段集成等效模块
- 模型缩放：
  - 分辨率：输入图片尺寸
  - 深度：网络层的数量
  - 宽度：channel的数量
  - stage：特征金字塔的数量
