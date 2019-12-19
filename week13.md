# Mathematical Statistics and Data Analysis

# Limit theorem

## 11810105 谢泽健

### 3

$$
\bar{X}=\frac{\sum_{i=1}^{16} X_i}{16}
$$

所以
$$
\frac{16X}{4}\sim N(0,1)
$$

$$
P(\bar{X} |<c)=P(-c<X<c)=P(-4c<4X<4c)=2\Phi(4c)-1=0.5
$$

解得
$$
c=0.168622
$$

### 6

依题意, 存在独立的随机变量 $Z,U$ 使得
$$
T=\frac{Z}{\sqrt{\frac{U}{n}}}
$$
其中 $Z \sim N(0,1), U \sim \chi_{n}^{2}$

所以
$$
T^2=\frac{Z^2}{\frac{U}{n}}=\frac{Z^2/1}{U/n}
$$
因为 $Z^2$ 是自由度为 $1$ 的卡方随机变量, 这满足了 $F$ 分布的定义, 所以
$$
T^2 \sim F_{1,n}
$$

### 8

对于一个伽马分布 $Gamma(\alpha, \lambda)$, 当 $\alpha=1$ 时, 伽马分布退化为指数分布, 所以
$$
X, Y \sim Gamma(1,1)
$$
所以, 
$$
f_X(t)=f_Y(t)=e^{-t}
$$
记 $Z=\frac{X}{Y}$
$$
f_{\frac{X}{Y}}(z)=\int_{-\infty}^{+\infty} f_{Y}(y) \cdot f_{X}(z \cdot y) \cdot|y| d y
$$
所以
$$
f_{Z}(z)=\int_{-\infty}^{+\infty} f_{Y}(y) \cdot f_{X}(z \cdot y) \cdot|y| d y=\int_{0}^{+\infty} e^{-y} \cdot e^{-zy} \cdot y d y=\frac{1}{(1+z)^{2}}
$$
另一方面, $F_{2,2}$ 的密度为
$$
f(x)=1/(1 + x)^2
$$
所以
$$
\frac{X}{Y} \sim F_{2,2}
$$

## 补充题

### 1

设第一个样本均值为 $\bar{X_1}$, 第二个为 $\bar{X_2}$, 则
$$
\bar{X_1} \sim N(240, \frac{20^2}{36})\\
\bar{X_2} \sim N(240, \frac{20^2}{49})
$$
所以 $\bar{X_1}-\bar{X_2}$ 满足
$$
\bar{X_1}-\bar{X_2} \sim N(0,\frac{20^2}{36}+\frac{20^2}{49})
$$
所以
$$
P(|\bar{X_1}-\bar{X_2}|\le10)=P(-10\le\bar{X_1}-\bar{X_2}\le10)=P(\frac{-10}{\sqrt {\frac{20^2}{36}+\frac{20^2}{49}}}\le\frac{Z}{\sqrt {\frac{20^2}{36}+\frac{20^2}{49}}}\le\frac{10}{\sqrt {\frac{20^2}{36}+\frac{20^2}{49}}})
$$
其中 $Z \sim N(0,1)$, 所以
$$
P(|\bar{X_1}-\bar{X_2}|\le10)=2\Phi(2.27777)-1=0.97726
$$

### 2

因为 
$$
X_1, X_2,\cdots, X_{10} \sim N(0,0.3^2)
$$
所以 $\frac{10X_i}{3}\sim N(0,1)$, 于是
$$
\frac{100}{9}\sum_{i=1}^{10}X_i^2\sim\chi_{10}^{2}
$$
所以
$$
P(\sum_{i=1}^{10}X_i^2\le C)=P(\frac{100}{9}\sum_{i=1}^{10}X_i^2\le \frac{100}{9}C)
$$
解
$$
P(\chi_{10}^{2}\le\frac{100}{9}C)=0.95
$$
得
$$
C=1.64763
$$

### 3

#### 1

易知
$$
X_1-X_2,X_1+X_2\sim N(0, \sqrt 2 \sigma)
$$
根据定理

> 随机变量 $\bar{X}$ 和 随机向量 $\left(X_{1}-\bar{X}, X_{2}-\bar{X}, \ldots, X_{n}-\bar{X}\right)$ 是独立的

这可以推出 $2 \bar{X}=X_1+X_2$ 和 $2(X_{1}-\bar{X})=X_1-X_2$ 是相互独立的

注意到
$$
(\frac{X_1-X_2}{\sqrt 2\sigma})^2\sim \chi_1^{2}
$$
所以
$$
\frac{\left(X_{1}-X_{2}\right)^{2}}{\left(X_{1}+X_{2}\right)^{2}}=\frac{(\frac{X_1-X_2}{\sqrt 2\sigma})^2}{(\frac{X_1-X_2}{\sqrt 2\sigma})^2}\sim F_{1,1}
$$

#### 2

$$
P\left\{\frac{\left(X_{1}+X_{2}\right)^{2}}{\left(X_{1}+X_{2}\right)^{2}+\left(X_{1}-X_{2}\right)^{2}}>k\right\}=P(\frac{\left(X_{1}+X_{2}\right)^{2}+\left(X_{1}-X_{2}\right)^{2}}{\left(X_{1}+X_{2}\right)^{2}}<\frac{1}{k})
$$

即
$$
P(\frac{\left(X_{1}-X_{2}\right)^{2}}{\left(X_{1}+X_{2}\right)^{2}}<\frac{1}{k}-1)=P(F_{1,1}<\frac{1}{k}-1)=0.1
$$
解得
$$
k=0.975528
$$
