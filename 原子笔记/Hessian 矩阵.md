# Hessian 矩阵

## 一、详细讲解

### 1. 它解决什么问题

梯度描述一阶变化，Hessian 描述梯度如何继续变化，也就是函数的二阶局部曲率。它是多变量版本的二阶导数。

### 2. 核心定义与形式

若 $f:\mathbb R^n\to\mathbb R$ 二阶可导，则 Hessian 为

$$
\nabla^2f(x)
=
\begin{bmatrix}
\frac{\partial^2f}{\partial x_1^2}
&
\cdots
&
\frac{\partial^2f}{\partial x_1\partial x_n}
\\
\vdots&\ddots&\vdots\\
\frac{\partial^2f}{\partial x_n\partial x_1}
&
\cdots
&
\frac{\partial^2f}{\partial x_n^2}
\end{bmatrix}.
$$

若二阶混合偏导连续，则 Hessian 对称。

### 3. 核心推导 / 原理

二阶局部近似为

$$
f(x+\Delta x)
\approx
f(x)
+\nabla f(x)^T\Delta x
+\frac12\Delta x^T\nabla^2f(x)\Delta x.
$$

因此 Hessian 决定局部二次曲率。

### 4. 一个最小例子

$$
f(x_1,x_2)=x_1^2+3x_1x_2+2x_2^2.
$$

则

$$
\nabla^2f=
\begin{bmatrix}
2&3\\
3&4
\end{bmatrix}.
$$

### 5. 易错点与理解要点

- Hessian 是矩阵。
- 二次函数的 Hessian 是常数矩阵。
- Hessian 对称需要适当的二阶可微条件。

## 二、快速查阅

### 一句话理解

> Hessian 是多变量函数的二阶曲率矩阵。

### 核心公式

$$
\nabla^2f(x)=
\left[
\frac{\partial^2f}{\partial x_i\partial x_j}
\right]
$$

### 易错点

- Hessian 不是梯度的长度，而是梯度的导数矩阵。

## 相关知识

- 梯度
- 二阶凸性判据
