# Mint Discretely Integrable Moments for Symmetric Frame Fields
# TLDR
本文提出的方法能够自动恢复具有复杂拓扑的场，其能够对于实际中的复杂几何构造参数化。

#
we show that discrete (local) integrability of a symmetric frame field on a tetrahedral volume mesh can be expressed as `linear constraints` on `certain tensor representations of the field` (where the entries of these tensors are polynomials in the natural representation of a frame field, as 9 DOFs per point).


# 标架场和八面体群
Frame field是一个 $2^3$ 向量场（ $2^3$ -vector field），对于属于三维空间 $\mathbb{R}^3$ 的区域 $\Omega$ 中每个点 $p$ 的一个三维标架场可以如下表示：

$$
\{f_1(p),f_2(p),f_3(p)\}
$$

记矩阵 $\mathrm{F}\in \mathbb{R}^{3\times 3}$ 中的每一列保存了 $f_i$

记 $\mathcal{O}$ 为一个八面体群（octahedral group），那么其中每一个元素 $g\in \mathcal{O}$ 可以表示为两个矩阵的乘积 $g=\mathrm{DP}$ ，其中：
- $\mathrm{D}$ 是一个对角阵，对角线元素为 $\pm1$
- $\mathrm{P}$ 是一个排列矩阵，

一个八面体群通过右乘，作用在一个矩阵上，会改变这个矩阵列的**顺序**，也会改变列的**符号**

给定2个矩阵：

$$
\mathrm{F}=[f_1,f_2,f_3] \quad \mathrm{G}=[g_1,g_2,g_3]
$$

如果存在一个 $g$ 满足 $\mathrm{F}=\mathrm{G}g$ ，那么 $F$ 和 $G$ 表示的是同一个标架场，记做 $\mathrm{F}\sim\mathrm{G}$ 

用 $\mathbb{R}^{3\times3}/\mathcal{O}$ 表示3对称方向标架（3-symmetric direction frames）的商空间（quotient space）， $GL(3)/\mathcal{O}$ 表示上述空间的非退化的空间（即线性无关的）。
>注意， $GL(3)/\mathcal{O}$ 虽然在局部邻域上是欧式空间的，但是其的三个方向 $f_i$ 每个都有不同的尺度，所以该空间并非流形。所以，每个  $2^3$ 向量场是 $\Omega \times \mathbb{R}^{3\times3}/\mathcal{O}$ 中的一个片段 $\Gamma$ 。

在远离奇异点和奇异线的区域，可以局部梳理（comb）标架场，即在邻域内的每个点上找到3个满足 $\mathrm{C}\sim\mathrm{F}$ 的向量场 $c_i$ 。但是，由于标架场奇异线上存在`拓扑位错`，一般不可能将这种局部梳理（combing）推广到全局分裂为3个光滑的向量场。

> 注意，八面体标架（octahedral frames）是八面体群（octahedral group）的子集。

之前有许多工作使用八面体标架（octahedral frames）来处理hex，可以减少高各向异性的标架、退化的标架（共面或者0维的）产生。但是八面体标架不利于积分。一个可以积分的标架意味着存在一个局部共形参数化。

即使施加很轻微的约束（比如对其标架至边界）， 都无法找到一个可积的八面体标架，因为三维的共形变换很少（只有Möbius transformations）。







