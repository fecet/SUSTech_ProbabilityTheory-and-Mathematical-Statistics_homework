# 6.

## a.

$$
E(X)=\int_{0}^{1} x \cdot f(x) d x=\int_{0}^{1} x \cdot 2 x d x=2 \cdot \int_{0}^{1} x^{2} d x=\left.2 \cdot\left(\frac{x^{3}}{3}\right)\right|_{0} ^{1}=2 \cdot \frac{1}{3}=\frac{2}{3}
$$

## b

概率质量函数为:
$$
f_Y(y)=f_X[x(y)]x'(y)=f_X(\sqrt y)\frac{1}{2\sqrt{y}}=1, \quad 0\le y\le1
$$
所以
$$
E(Y)=\int_{0}^{1} y \cdot f_{Y}(y) d y=\int_{0}^{1} y \cdot 1 d y=\left.\frac{y^{2}}{2}\right|_{0} ^{1}=\frac{1}{2}
$$

## c

$$
E\left(X^{2}\right)=\int_{0}^{1} x^{2} \cdot f_{X}(x) d x=\int_{0}^{1} x^{2} \cdot 2 x d x=2 \cdot \int_{0}^{1} x^{3} d x=\left.2 \cdot\left(\frac{x^{4}}{4}\right)\right|_{0} ^{1}=2 \cdot \frac{1}{4}=\frac{1}{2}
$$

### d.

根据定义
$$
\operatorname{Var}(X)=E\left[(X-E(X))^{2}\right]=E\left[\left(X-\frac{2}{3}\right)^{2}\right]=\int_{0}^{1}\left(2 x^{3}-\frac{8}{3} x^{2}+\frac{8}{9} x\right) d x=\frac{1}{18}
$$
根据定理
$$
\operatorname{Var}(X)=E\left(X^{2}\right)-[E(X)]^{2}=\frac{1}{2}-\left(\frac{2}{3}\right)^{2}=\frac{1}{2}-\frac{4}{9}=\frac{1}{8}
$$

# 15.

记从第一种彩票中获得的奖金为 $R_1$, 从第二种彩票中获得的为 $R_2$, 那么奖金期望为
$$
E(R_1+R_2)=E(R_1)+E(R_2)
$$
从一种彩票中购买两张, 不失一般性, 假设购买两张第一种彩票
$$
E(R_1+R_2)=E(R_1)+E(R_2)=\frac{2}{n}+0=\frac{2}{n}
$$ {\operatorname{Var}(X)=E\left(X^{2}\right)-[E(X)]^{2}=\frac{1}{2}-\left(\frac{2}{3}\right)^{2}=\frac{1}{2}-\frac{4}{9}
若从两种彩票中各买一张
$$
E(R_1+R_2)=E(R_1)+E(R_2)=\frac{1}{n}+\frac{1}{n}=\frac{2}{n}
$$
因此两种购买方式在期望收入上没有差别

# 20

设 $X$ 服从参数为 $\lambda$ 的泊松分布
$$
E(\frac{1}{X+1})=\sum_{x=0}^{\infty}\frac{f(x)}{x+1}=\sum_{x=0}^{\infty}\frac{e^{-\lambda } \lambda ^x}{(x+1)!}
$$
 注意到
$$
\sum_{j=0}^{\infty}\left(\frac{\lambda^{j} }{ j !}\right)=\mathrm{e}^{\lambda}
$$
所以
$$
\sum_{x=0}^{\infty}\frac{e^{-\lambda } \lambda ^x}{(x+1)!}=\frac{1}{\lambda}\sum_{x=0}^{\infty}\frac{e^{-\lambda } \lambda ^{x+1}}{(x+1)!}=\frac{1}{\lambda}e^{-\lambda}(e^\lambda-1)=\frac{1-e^{-\lambda }}{\lambda }
$$


# 21

$$
E(X^2)=\int_0^1 x^2f(x)=E(X^2)=\int_0^1 x^2=\frac{1}{3}
$$

# 31

$$
E(\frac{1}{X})=\int_1^2{\frac{f(x)}{x}}=\int_1^2{\frac{1}{x}}=\ln2
$$

$$
E(X)=\int_1^2{xf(x)}=\int_1^2{x}=\frac{3}{2}
$$

所以
$$
\frac{1}{E(x)}=\frac{2}{3}\neq E(\frac{1}{X})
$$

# 49

## a

$$
E(Z)=E[\alpha X+(1-\alpha) Y]=\alpha \cdot E(X)+(1-\alpha) \cdot E(Y)=\alpha \cdot \mu+(1-\alpha) \cdot \mu=\mu
$$

## b

$$
\operatorname{Var}(Z)=\operatorname{Var}[\alpha X+(1-\alpha) Y]=\operatorname{Var}(\alpha X)+\operatorname{Var}[(1-\alpha) Y]=\alpha^{2}  \operatorname{Var}(X)+(1-\alpha)^{2}  \operatorname{Var}(Y)
$$

所以
$$
\operatorname{Var}(Z)=f(\alpha)=\alpha^{2} \cdot \sigma_{X}^{2}+(1-\alpha)^{2} \cdot \sigma_{Y}^{2}
$$
求导得
$$
f^{\prime}(\alpha)=2 \alpha \cdot \sigma_{X}^{2}-2(1-\alpha) \cdot \sigma_{Y}^{2}
$$
令
$$
f^{\prime}(\alpha)=0
$$
解得
$$
\alpha=\frac{\sigma_{Y}^{2}}{\sigma_{X}^{2}+\sigma_{Y}^{2}}
$$

## c

当使用平均数优于单独使用 $X$ 和 $Y$ 时,  这意味着 $\frac{X+Y}{2}$ 的方差较小
$$
\alpha^{2}\sigma_{X}^{2}+(1-\alpha)^{2} \sigma_{Y}^{2}<\min(\sigma_X^2,\sigma_Y^2)
$$
其中 $\alpha=\frac{1}{2}$, 所以
$$
\frac{1}{4} \cdot\left(\sigma_{X}^{2}+\sigma_{Y}^{2}\right)<\sigma_{X}^{2} \Longleftrightarrow \sigma_{Y}^{2}<3 \sigma_{X}^{2}
$$

$$
\frac{1}{4} \cdot\left(\sigma_{X}^{2}+\sigma_{Y}^{2}\right)<\sigma_{Y}^{2} \Longleftrightarrow \sigma_{X}^{2}<3 \sigma_{Y}^{2}
$$

综上, 当 $\frac{1}{3}<\frac{\sigma_{X}^{2}}{\sigma_{Y}^{2}}<3$ 时, 使用平均数优于单独使用 $X$ 和 $Y$.

# 50

$$
E(\bar{X})=E\left(\frac{1}{n}  \sum_{i=1}^{n} X_{i}\right)=\frac{1}{n} \sum_{i=1}^{n} E\left(X_{i}\right)=\frac{1}{n}  \sum_{i=1}^{n} \mu=\frac{1}{n}  n \mu=\mu
$$

$$
\operatorname{Var}(\bar{X})=\operatorname{Var}\left(\frac{1}{n}  \sum_{i=1}^{n} X_{i}\right)=\frac{1}{n^{2}}\operatorname{Var}\left(\sum_{i=1}^{n} X_{i}\right)=\frac{1}{n^{2}}\sum_{i=1}^{n} \operatorname{Var}\left(X_{i}\right)=\frac{n\sigma^2}{n^2}=\frac{\sigma^2}{n}
$$

# 55

$$
E(T)=\sum_{k=1}^{n}kE( X_k)=\sum_{k=1}^{n}k\mu=\frac{n(n-1)\mu}{2}
$$

$$
\operatorname{Var}(T)=\sum_{k=1}^{n}k^2\operatorname{Var}( X_k)=\frac{n(n+1)(2n+1)\sigma^2}{6}
$$

