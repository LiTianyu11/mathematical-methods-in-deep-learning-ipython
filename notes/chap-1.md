下面涵盖了机器学习中从**模型表示**到**损失函数计算**

---

### 1. 线性模型的向量化表示

此公式展示了如何将线性方程转化为矩阵/向量的点积形式。

$$y(x_0, x_1) = w_0 x_0 + w_1 x_1 + b = \begin{bmatrix} w_0 & w_1 \end{bmatrix} \begin{bmatrix} x_0 \\ x_1 \end{bmatrix} + b = w^{\text{T}} x + b \tag{1.3}$$

---

### 2. 监督学习数据集

表示包含 $N+1$ 个样本的训练集，每个样本由特征向量和真实标签组成。

$$\left( \boldsymbol{x}^{(0)}, y_{\text{gt}}^{(0)} \right), \left( \boldsymbol{x}^{(1)}, y_{\text{gt}}^{(1)} \right), \dots, \left( \boldsymbol{x}^{(N)}, y_{\text{gt}}^{(N)} \right)$$

---

### 3. 单个样本的预测值

$$y_{\text{predicted}}^{(i)} = \boldsymbol{w}^{\text{T}} \boldsymbol{x}^{(i)} + b$$

---

### 4. 误差平方与总损失 (Loss & Cost Function)

这段文字描述了如何衡量预测值与真实值（Ground Truth）之间的差异。

**单个训练实例的误差平方：**


$$e_i^2 = \left( y_{\text{predicted}}^{(i)} - y_{\text{gt}}^{(i)} \right)^2$$

**整个训练数据集上的总损失：**


$$E^2 = \sum_{i=0}^{i=N} e_i^2 = \sum_{i=0}^{i=N} \left( y_{\text{predicted}}^{(i)} - y_{\text{gt}}^{(i)} \right)^2 = \sum_{i=0}^{i=N} \left( \boldsymbol{w}^{\text{T}} \boldsymbol{x}_i + b - y_{\text{gt}}^{(i)} \right)^2$$

---

### 💡 术语小贴士：

* **$y_{\text{gt}}$**: 这里的 `gt` 代表 **Ground Truth**（真实值/标准答案）。
* **$E^2$**: 通常被称为 **SSE (Sum of Squared Errors)**，是优化模型参数时最常用的目标函数之一。

你是在学习如何推导 **梯度下降 (Gradient Descent)** 算法吗？我可以继续为你展示如何对这些公式求导。