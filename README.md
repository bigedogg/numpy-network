# 三层神经网络分类器

这是一个使用纯Python和Numpy实现的三层神经网络分类器，数据集为Fashion-MNIST数据集，旨在进行图像分类任务。本模型支持自定义隐藏层大小、激活函数类型，并采用SGD优化器进行训练。

## 环境依赖

- Python 3.6+
- Numpy 1.19+

## 数据集

使用Fashion-MNIST数据集，可以从[Zalando的GitHub仓库](https://github.com/zalandoresearch/fashion-mnist)下载。数据应包括训练集和测试集。
请将下载的数据解压到项目目录中的'data/'文件夹下

## 使用说明

### 训练模型

要训练模型，您需要调用`train`函数。可以自定义隐藏层大小、激活函数类型、学习率等。

其中参数意义如下：
- `--hidden_size`：隐藏层的神经元数量。
- `--activation`：使用的激活函数类型（支持'relu'或'sigmoid'或'tanh'）。
- `--initial_learning_rate`：学习率。
- `--num_epochs`：训练周期数。
- `--reg_lambda`：L2正则化的强度。
- `--batch_size`：批量大小。

### 测试模型

训练完成后，模型权重将自动保存。使用`test`函数来评估模型在测试集上的性能：

### 参数调优

为了获得最佳性能，您可以使用`parameter_search`函数来调整超参数，如学习率和隐藏层大小：

该函数将使用不同的参数组合运行多次训练，并记录每种设置下的性能。最后返回最佳参数组合。
