* [简介]()
* [阅读指南](read_guide.md)
* 2\. 预备知识
   <!-- * [2.1 环境配置](chapter02_prerequisite/2.1_install.md) -->
   * [2.2 数据操作](chapter02_prerequisite/2.2_tensor.md)
   * [2.3 自动求梯度](chapter02_prerequisite/2.3_autograd.md)
* 3\. 深度学习基础
   * [3.1 线性回归](chapter03_DL-basics/3.1_linear-regression.md)
   * [3.2 线性回归的从零开始实现](chapter03_DL-basics/3.2_linear-regression-scratch.md)
   * [3.3 线性回归的简洁实现](chapter03_DL-basics/3.3_linear-regression-pytorch.md)
   * [3.4 softmax回归](chapter03_DL-basics/3.4_softmax-regression.md)
   * [3.5 图像分类数据集（Fashion-MNIST）](chapter03_DL-basics/3.5_fashion-mnist.md)
   * [3.6 softmax回归的从零开始实现](chapter03_DL-basics/3.6_softmax-regression-scratch.md)
   * [3.7 softmax回归的简洁实现](chapter03_DL-basics/3.7_softmax-regression-pytorch.md)
   * [3.8 多层感知机](chapter03_DL-basics/3.8_mlp.md)
   * [3.9 多层感知机的从零开始实现](chapter03_DL-basics/3.9_mlp-scratch.md)
   * [3.10 多层感知机的简洁实现](chapter03_DL-basics/3.10_mlp-pytorch.md)
   * [3.11 模型选择、欠拟合和过拟合](chapter03_DL-basics/3.11_underfit-overfit.md)
   * [3.12 权重衰减](chapter03_DL-basics/3.12_weight-decay.md)
   * [3.13 丢弃法](chapter03_DL-basics/3.13_dropout.md)
   * [3.14 正向传播、反向传播和计算图](chapter03_DL-basics/3.14_backprop.md)
   * [3.15 数值稳定性和模型初始化](chapter03_DL-basics/3.15_numerical-stability-and-init.md)
   * [3.16 实战Kaggle比赛：房价预测](chapter03_DL-basics/3.16_kaggle-house-price.md)
* 4\. 深度学习计算
   * [4.1 模型构造](chapter04_DL_computation/4.1_model-construction.md)
   * [4.2 模型参数的访问、初始化和共享](chapter04_DL_computation/4.2_parameters.md)
   * [4.3 模型参数的延后初始化](chapter04_DL_computation/4.3_deferred-init.md)
   * [4.4 自定义层](chapter04_DL_computation/4.4_custom-layer.md)
   * [4.5 读取和存储](chapter04_DL_computation/4.5_read-write.md)
   * [4.6 GPU计算](chapter04_DL_computation/4.6_use-gpu.md)
* 5\. 卷积神经网络
   * [5.1 二维卷积层](chapter05_CNN/5.1_conv-layer.md)
   * [5.2 填充和步幅](chapter05_CNN/5.2_padding-and-strides.md)
   * [5.3 多输入通道和多输出通道](chapter05_CNN/5.3_channels.md)
   * [5.4 池化层](chapter05_CNN/5.4_pooling.md)
   * [5.5 卷积神经网络（LeNet）](chapter05_CNN/5.5_lenet.md)
   * [5.6 深度卷积神经网络（AlexNet）](chapter05_CNN/5.6_alexnet.md)
   * [5.7 使用重复元素的网络（VGG）](chapter05_CNN/5.7_vgg.md)
   * [5.8 网络中的网络（NiN）](chapter05_CNN/5.8_nin.md)
   * [5.9 含并行连结的网络（GoogLeNet）](chapter05_CNN/5.9_googlenet.md)
   * [5.10 批量归一化](chapter05_CNN/5.10_batch-norm.md)
   * [5.11 残差网络（ResNet）](chapter05_CNN/5.11_resnet.md)
   * [5.12 稠密连接网络（DenseNet）](chapter05_CNN/5.12_densenet.md)
* 6\. 循环神经网络
   * [6.1 语言模型](chapter06_RNN/6.1_lang-model.md)
   * [6.2 循环神经网络](chapter06_RNN/6.2_rnn.md)
   * [6.3 语言模型数据集（周杰伦专辑歌词）](chapter06_RNN/6.3_lang-model-dataset.md)
   * [6.4 循环神经网络的从零开始实现](chapter06_RNN/6.4_rnn-scratch.md)
   * [6.5 循环神经网络的简洁实现](chapter06_RNN/6.5_rnn-pytorch.md)
   * [6.6 通过时间反向传播](chapter06_RNN/6.6_bptt.md)
   * [6.7 门控循环单元（GRU）](chapter06_RNN/6.7_gru.md)
   * [6.8 长短期记忆（LSTM）](chapter06_RNN/6.8_lstm.md)
   * [6.9 深度循环神经网络](chapter06_RNN/6.9_deep-rnn.md)
   * [6.10 双向循环神经网络](chapter06_RNN/6.10_bi-rnn.md)
* 7\. 优化算法
   * [7.1 优化与深度学习](chapter07_optimization/7.1_optimization-intro.md)
   * [7.2 梯度下降和随机梯度下降](chapter07_optimization/7.2_gd-sgd.md)
   * [7.3 小批量随机梯度下降](chapter07_optimization/7.3_minibatch-sgd.md)
   * [7.4 动量法](chapter07_optimization/7.4_momentum.md)
   * [7.5 AdaGrad算法](chapter07_optimization/7.5_adagrad.md)
   * [7.6 RMSProp算法](chapter07_optimization/7.6_rmsprop.md)
   * [7.7 AdaDelta算法](chapter07_optimization/7.7_adadelta.md)
   * [7.8 Adam算法](chapter07_optimization/7.8_adam.md)
* 8\. 计算性能
   * [8.1 命令式和符号式混合编程](chapter08_computational-performance/8.1_hybridize.md)
   * [8.2 异步计算](chapter08_computational-performance/8.2_async-computation.md)
   * [8.3 自动并行计算](chapter08_computational-performance/8.3_auto-parallelism.md)
   * [8.4 多GPU计算](chapter08_computational-performance/8.4_multiple-gpus.md)
* 9\. 计算机视觉
   * [9.1 图像增广](chapter09_computer-vision/9.1_image-augmentation.md)
   * [9.2 微调](chapter09_computer-vision/9.2_fine-tuning.md)
   * [9.3 目标检测和边界框](chapter09_computer-vision/9.3_bounding-box.md)
   * [9.4 锚框](chapter09_computer-vision/9.4_anchor.md)
   * [9.5 多尺度目标检测](chapter09_computer-vision/9.5_multiscale-object-detection.md)
   * [9.6 目标检测数据集（皮卡丘）](chapter09_computer-vision/9.6_object-detection-dataset.md)
   * 9.7 单发多框检测（SSD）
   * [9.8 区域卷积神经网络（R-CNN）系列](chapter09_computer-vision/9.8_rcnn.md)
   * [9.9 语义分割和数据集](chapter09_computer-vision/9.9_semantic-segmentation-and-dataset.md)
   * 9.10 全卷积网络（FCN）
   * [9.11 样式迁移](chapter09_computer-vision/9.11_neural-style.md)
   * 9.12 实战Kaggle比赛：图像分类（CIFAR-10）
   * 9.13 实战Kaggle比赛：狗的品种识别（ImageNet Dogs）
* 10\. 自然语言处理
   * [10.1 词嵌入（word2vec）](chapter10_natural-language-processing/10.1_word2vec.md)
   * [10.2 近似训练](chapter10_natural-language-processing/10.2_approx-training.md)
   * [10.3 word2vec的实现](chapter10_natural-language-processing/10.3_word2vec-pytorch.md)
   * [10.4 子词嵌入（fastText）](chapter10_natural-language-processing/10.4_fasttext.md)
   * [10.5 全局向量的词嵌入（GloVe）](chapter10_natural-language-processing/10.5_glove.md)
   * [10.6 求近义词和类比词](chapter10_natural-language-processing/10.6_similarity-analogy.md)
   * [10.7 文本情感分类：使用循环神经网络](chapter10_natural-language-processing/10.7_sentiment-analysis-rnn.md)
   * [10.8 文本情感分类：使用卷积神经网络（textCNN）](chapter10_natural-language-processing/10.8_sentiment-analysis-cnn.md)
   * [10.9 编码器—解码器（seq2seq）](chapter10_natural-language-processing/10.9_seq2seq.md)
   * [10.10 束搜索](chapter10_natural-language-processing/10.10_beam-search.md)
   * [10.11 注意力机制](chapter10_natural-language-processing/10.11_attention.md)
   * [10.12 机器翻译](chapter10_natural-language-processing/10.12_machine-translation.md)