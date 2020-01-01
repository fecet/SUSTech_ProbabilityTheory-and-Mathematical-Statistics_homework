# Mathematical Statistics and Data Analysis

# Parameter Estimation

## 11810105 谢泽健

### 5

#### a

$X$ 的一阶矩为
$$
E(X)=\theta+2(1-\theta)=2-\theta
$$
所以 $\theta$ 的矩估计为
$$
\hat{\theta}=2-\bar{X}
$$
由样本可得
$$
\bar{X}=2-\frac{1+2+2}{3}=\frac{1}{3}
$$

#### b

$$
L ( \theta ) = L \left( \theta ; X _ { 1 } , X _ { 2 } , \cdots , X _ { n } \right) = \prod _ { i = 1 } ^ { n } P \left( X _ { i } ; \theta \right)=\theta(1-\theta)^2
$$

#### c

求
$$
\max _ {  0\le\theta\le1 } L( \theta )=\theta(1-\theta)^2
$$
得
$$
\theta=\frac{1}{3}
$$

## 补充题

### 1

$$
E(X)=\int_{0}^{\theta}\frac { 2x } { \theta ^ { 2 } } ( \theta - x ) dx=\frac{\theta }{3}
$$

所以 $\theta$ 的矩估计为
$$
\hat{\theta}=3\bar{X}=\frac{3\sum_{i=1}^{n} X_i}{n}
$$

### 2

#### 1

$$
L(\theta)=\prod _ { i = 1 } ^ { n } \frac { \theta ^ { X_i } } { X_i ! } e ^ { - \theta }=\frac{\theta^{\sum_{i=1}^{n} X_i}}{\prod_{i=1}^{n} X_i!}e ^ { - n\theta }
$$

所以
$$
\max _ {  \theta>0 } L( \theta )=\theta^{\sum_{i=1}^{n} X_i}e ^ { - n\theta }
$$
令 $f(\theta)=\theta^{\sum_{i=1}^{n} X_i}e ^ { - n\theta }$ , 并记 $\sum_{i=1}^{n} X_i=t$, 可得
$$
f'(\theta)=t e^{\theta  (-n)} \theta ^{t-1}-n e^{\theta  (-n)} \theta ^t
$$
令 $f'(\theta)=0$, 得
$$
\theta=\frac{t}{n}=\frac{\sum_{i=1}^{n} X_i}{n}=\bar{X}
$$

#### 2

$$
L(\theta)=\prod _ { i = 1 } ^ { n } \theta \alpha X_i ^ { \alpha - 1 } e ^ { - \theta X ^ { \alpha } }=\theta^n \alpha^n e^{-n\theta\sum _ { i = 1 } ^ { n }X_i^{\alpha}}\prod _ { i = 1 } ^ { n }X_i^{\alpha-1}
$$

所以
$$
\max _ {  \theta\in \R } L( \theta )=\theta^n  e^{-n\theta\sum _ { i = 1 } ^ { n }X_i^{\alpha}}
$$
令 $f(\theta)=\theta^n  e^{-n\theta\sum _ { i = 1 } ^ { n }X_i^{\alpha}}$ , 并记 $\sum_{i=1}^{n} X_i^\alpha=t$, 可得
$$
f(\theta)=\theta^n  e^{-n\theta t}\\
f'(\theta)=n \theta ^{n-1} e^{\theta  (-n) t}-n t \log (e) \theta ^n e^{\theta  (-n) t}
$$
令 $f'(\theta)=0$, 解得
$$
\theta=\frac{1}{t}=\frac{1}{\sum_{i=1}^{n} X_i^\alpha}
$$

### 3

$$
\hat{\sigma^2}=\frac { 1 } { k } \sum _ { i = 1 } ^ { n - 1 } \left( X _ { i + 1 } - X _ { i } \right) ^ { 2 }
$$

$$
E(\hat{\sigma^2})=E(\frac { 1 } { k } \sum _ { i = 1 } ^ { n - 1 } \left( X _ { i + 1 } - X _ { i } \right) ^ { 2 })=\frac { 1 } { k }\sum _ { i = 1 } ^ { n - 1 } E( X _ { i + 1 } ^2+ X _ { i }^2-2X_{i+1}X_i)
$$

注意到
$$
E(X_{i+1}^2)=E(X_{i})^2=\sigma^2\\
E(2X_{i+1}X_i)=2E(X_{i+1})E(X_i)=0
$$
所以
$$
\frac { 1 } { k }\sum _ { i = 1 } ^ { n - 1 } E( X _ { i + 1 } ^2+ X _ { i }^2-2X_{i+1}X_i)=\frac { 1 } { k }\sum _ { i = 1 } ^ { n - 1 } 2\sigma^2=\frac { 1 } { k }2(n-1)\sigma^2
$$

要使得估计值无偏, 则
$$
\frac { 1 } { k }2(n-1)\sigma^2=\sigma^2
$$
所以
$$
k=2(n-1)
$$

### 4

$$
E(Y)=a\bar{X_1}+b\bar{X_2}=aE(\bar{X_1})+b(\bar{X_2})
$$

因为均值 $\bar{X_1}$ 和 $\bar{X_2}$ 均为 $\mu$ 的无偏估计:
$$
E(Y)=(a+b)\mu=\mu
$$

$$
Var(Y)=a^2Var(\bar{X_1})+b^2Var(\bar{X_2})+2abCov(\bar{X_1},\bar{X_2})
$$

由于 $X_1$ 和 $X_2$ 相互独立
$$
Cov(\bar{X_1},\bar{X_2})=0
$$
所以
$$
Var(Y)=a^2Var(\bar{X_1})+b^2Var(\bar{X_2})=\frac{a^2\sigma^2}{n_1}+\frac{b^2\sigma^2}{n_2}
$$
求导得
$$
\min_{a,b}\frac{a^2\sigma^2}{n_1}+\frac{b^2\sigma^2}{n_2}=\frac{1}{n_1+n_2}
$$
其中
$$
a=\frac{n_1}{n_1+n_2}\\
b=\frac{n_2}{n_1+n_2}
$$
