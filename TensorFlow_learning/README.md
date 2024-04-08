## 安装虚拟环境
### Ubuntu
创建虚拟环境
`python3 -m venv --system-site-packages ./venv`
激活虚拟环境
`source ./venv/bin/activate #sh,bash or zsh`
退出虚拟环境
`deactivate`

### Windows
创建虚拟环境
`python -m venv --system-site-packages .\venv`
激活虚拟环境
`.\venv\Scripts\activates`
退出虚拟环境
`deactivate`

><a href="https://www.bilibili.com/video/BV1FW4y1b7WM/">从入门到精通：TensorFlow全套教程</a>
## 基本概念
机器学习->深度学习
机器学习过程
- 数据获取
- 特征工程
- 建立模型
- 评估与应用
其中**特征工程**是最为重要的部分.

特征工程的作用：
- 数据特征决定了模型的上限
- 预处理和特征提取是最核心的
- 算法与参数选择决定了如何逼近这个上限

深度学习解决的问题是如何提取特征.

### 前向传播
#### 得分函数

K`(KNN)`近邻算法`参考K个近邻，预测结果`
K近邻无法区分背景和主体，不适用于视觉学习，需要有一个得分函数.

以CIFAR-10为数据库为例
- 10标签
- 50000训练数据
- 10000测试数据
- 大小均为32\*32

一种线性模型$$f(X,W)_{10\times1}=W_{10\times3072}X_{3072\times1}+b_{10\times1}$$
其中W为权重参数，b为微调参数`各自类别，各自微调`.

训练的过程就是修改W的过程.

#### 损失函数
- 衡量分类的结果

一种模型$$L_i=\sum_{j\neq y_i}{\max(0,s_j-s_{y_i}+\Delta b)}$$
$\Delta b$为容忍程度，存在是为了更加准确，避免偶然和混淆.

损失函数=数据损失+正则化惩罚项$$L=\underbrace{\frac{1}{N}\sum_{i=1}^{N}{\sum_{j\neq y_i}{\max(0,f(X_i,W)_j-f(X_i,W)_{y_i}+\Delta b)}}}_{data\_loss}+\underbrace{\lambda R(W)}_{正则化惩罚项}$$
可以令$$R(W)=\sum_k\sum_lW^2_{k,l}$$
通常希望模型不要太复杂，不期望过拟合模型，$\lambda$可能会比较高

softmax分类器$$data\rightarrow x\overset{exp}{\longrightarrow}e^x\overset{normalize}{\longrightarrow}probability$$
计算损失值$$L_i=-\log{P(Y=y_i|X=x_i)}$$
### 反向传播

## 神经网络
### 整体结构
- 层次结构
	- 会有一个input layer,多个hidden layer,和一个output layer
- 神经元
	- 过多会导致过拟合
- 全连接
- 非线性

### 激活函数
Sigmoid(梯度消失)$$\sigma(x)=\frac{1}{(1+e^{-x})}$$
Relu$$\sigma(x)=\max(0,x)$$
Tanh

### 预处理
参数初始化（尽量小）

### DROP-OUT
训练阶段每次每层随机停用一部分神经元
