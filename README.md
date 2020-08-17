# Random-Forest-MATLAB

随机森林工具包-MATLAB版

using MATLAB to achieve RF algorithm,and the decision tree is ID3 , C4.5 and CART.

I had achieve these by different ways.

此处复现的是 《MATLAB神经网络43个案例分析》中的第30章，基于随机森林思想的组合分类器设计（-乳腺癌诊断）中的随机森林实现

包括威斯康辛大学医学院的乳腺癌数据集，共包括569个病例，其中，良性357例，恶性212例。该次实现随机选取500组数据作为训练集，剩余69组作为测试集。

包括科罗拉多大学博尔德分校Abhishek Jaiantilal 开发的randomforest-matlab开源工具箱（下载地址https://code.google.com/p/randomforest-matlab/）
，其复现代码见 main.m 函数。

调用格式为：

model = classRF_train(X,Y,ntree,mtry,extra_options)

其中， X 为训练集的输入样本矩阵，其每一列表示一个变量（属性〉，其每一行表示一个样本； Y
为训练集的输出样本向量，其每一行表示 X 中对应的样本所属的类别 z ntree 为随机森林中决
策树的个数（默认值为 SOO) ;mtry 为分裂属性集中的属性个数（默认值 m =l v'MJ .M 为总的
属性个数，符号L . 」表示向下取整） ; extra_options 为可选的参数； model 为创建好的随机森林
分类器。

[Y-hat, votes] = classRF_predict(X,model,extra_options)

其中， X 为待预测样本的输入矩阵，其每一列表示一个变量（属性〉，其每一行表示一个样本；
model 为创建好的随机森林分类器； extra_options 为可选的参数 ； Y_hat 为待预测样本对应的
所属类别； votes 为朱格式化的待预测样本输出类别权重，即将待预测样本预测为各个类别的
决策树个数。
