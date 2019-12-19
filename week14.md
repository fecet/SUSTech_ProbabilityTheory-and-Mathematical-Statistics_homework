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
L(\theta)=\prod _ { i = 1 } ^ { n } \frac { \theta ^ { x_i } } { x_i ! } e ^ { - \theta }=\frac{\theta^{\sum_{i=1}^{n} X_i}}{\prod_{i=1}^{n} X_i!}e ^ { - n\theta }
$$

所以
$$
\max _ {  \theta>0 } L( \theta )=\theta^{\sum_{i=1}^{n} X_i}e ^ { - n\theta }
$$
令 $f(\theta)=\theta^{\sum_{i=1}^{n} X_i}e ^ { - n\theta }$ 

