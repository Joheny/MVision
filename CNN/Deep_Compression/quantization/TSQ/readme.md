# TSQ Two-Step Quantization 两步量化策略  激活编码 + 权重量化转换
[Wang_Two-Step_Quantization_for_CVPR_2018](http://openaccess.thecvf.com/content_cvpr_2018/papers/Wang_Two-Step_Quantization_for_CVPR_2018_paper.pdf)

# 也属于 增量型量化 的方式 Incremental quantization 
      增量型量化的基本思路是，部分的对参数或者激活函数进⾏量化处理，使得整个量化过程更
      加平稳。这⾥的 部分 可以有多种层⾯，可以是数量上的部分，也可以是程度上的部分。

# 简介 这里
      在量化神经网络的硬件设计中，每一点都很重要。
      然而，极低的位表示通常会导致较大的精度下降。
      因此，如何训练 高精度的极低比特 神经网络 具有重要的意义。
      大多数现有的网络量化方法同时学习变换（低比特权重）以及编码（低比特激活）。
      这种紧密耦合使得优化问题变得困难，从而防止网络学习最优表示。
      在本文中，我们提出了一个简单但有效的两步量化（TSQ）框架，
      通过将网络量化问题分解为两个步骤：
          激活的编码学习 和 权重的变换函数学习。
      对于第一步，我们提出了稀疏量化的编码学习方法。
      第二步可以表述为具有 低比特约束 的 非线性最小二乘回归问题，它可以以迭代的方式有效地求解。
      
|Object     |        Name命名     |    Method方法|
|low-bit weights 权重  | transformations 变换 |non-linear least square regression problem 非线性最小二乘方法|
low-bit activations 激活| encodings 编码 |sparse suantization 稀疏-半波高斯量化 (HWGQ) |