## 67

记 $Y$ 为长方形的高度, 依题意
$$
E(Y | X)=\frac{X}{2}\\
E(X)=\frac{1}{2}
$$

## 周长

$$
E(2(X+Y))=2E(X+Y)
$$

根据定理, 这等于
$$
2E(X+Y)=2E(E(X+Y|X))
$$
考虑 $E(X+Y|X)$
$$
E(X+Y|X)=X+E(Y|X)=\frac{3X}{2}
$$
所以周长的期望为
$$
2E(\frac{3X}{2})=3E(X)=\frac{3}{2}
$$

## 面积

$$
E(XY)=E(E(XY|X))
$$

考虑 $E(XY|X)$
$$
E(XY|X)=XE(Y|X)=\frac{X^2}{2}
$$
所以面积的期望为
$$
E(XY)=E(\frac{X^2}{2})=\frac{1}{2}\int_0^1x^2dx=\frac{1}{6}
$$

# 77

## a

### 协方差

$$
f_{X}(x)=\int_{x}^{+\infty} f(x, y) d y=\int_{x}^{+\infty} e^{-y} d y=-\left.e^{-y}\right|_{x} ^{+\infty}=e^{-x}
$$

$$
f_{Y}(y)=\int_{0}^{y} f(x, y) d x=\int_{0}^{y} e^{-y} d x=y \cdot e^{-y}
$$

所以
$$
E(X)=\int_{0}^{+\infty} x \cdot f_{X}(x) d x=\int_{0}^{+\infty} x \cdot e^{-x} d x=1
$$

$$
E(Y)=\int_{0}^{+\infty} y \cdot f_{Y}(y) d y=\int_{0}^{+\infty} y^{2} \cdot e^{-y} d y=2
$$

又

$$
E(X \cdot Y)=\int_{0}^{+\infty}\left(\int_{x}^{+\infty} x \cdot y \cdot f(x, y) d y\right) d x=\int_{0}^{+\infty}\left(\int_{x}^{+\infty} x \cdot y \cdot e^{-y} d y\right) d x=3
$$

所以
$$
\operatorname{Cov}(X, Y)=3-2 \cdot 1=1
$$

### 相关系数

$$
E\left(X^{2}\right)=\int_{0}^{+\infty} x^{2} \cdot f_{X}(x) d x=\int_{0}^{+\infty} x^{2} \cdot e^{-x} d x=2
$$

$$
E\left(Y^{2}\right)=\int_{0}^{+\infty} y^{2} \cdot f_{Y}(y) d y=\int_{0}^{+\infty} y^{3} \cdot e^{-y} d y=6
$$

所以
$$
\operatorname{Var}(X)=2-1^{2}=1\\
\operatorname{Var}(Y)=6-2^{2}=2
$$
从而
$$
\rho(X, Y)=\frac{1}{\sqrt{1 \cdot 2}}=\frac{\sqrt 2}{2}
$$

## b

$$
f_{X | Y}(x | y)=\frac{f_{X, Y}(x, y)}{f_{Y}(y)}=\frac{e^{-y}}{y \cdot e^{-y}}=\frac{1}{y}
$$

$$
f_{Y | X}(y | x)=\frac{f_{X, Y}(x, y)}{f_{X}(x)}=\frac{e^{-y}}{e^{-x}}=e^{x-y}
$$

所以
$$
E(X | Y=y)=\int_{0}^{y} x \cdot f_{X | Y}(x | y) d x=\int_{0}^{y} x \cdot \frac{1}{y} d x=\frac{1}{y} \cdot \int_{0}^{y} x d x=\frac{y}{2}
$$

$$
E(Y | X=x)=\int_{x}^{+\infty} y \cdot f_{Y | X}(y | x) d y=\int_{x}^{+\infty} y \cdot e^{x-y} d y=x+1
$$

## c

令
$$
U=E(X|Y)=\frac{Y}{2}\\
V=E(Y|X)=X+1
$$
所以
$$
f_U(u)=y(u) \cdot e^{-y(u)} \cdot y'(u)=4 ue^{-2 u} \quad u\ge0
$$

$$
f_V(v)=e^{-x(v)} \cdot x'(v)=e^{1-v}\quad v\ge1
$$

