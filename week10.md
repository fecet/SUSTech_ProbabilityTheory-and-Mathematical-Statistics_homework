# 54

$$
\operatorname{Cov}(U, V)=\operatorname{Cov}(Z+X, Z+Y)=\operatorname{Cov}(Z, Z)+\operatorname{Cov}(Z, Y)+\operatorname{Cov}(X, Z)+\operatorname{Cov}(X, Y)
$$

分别计算得
$$
\operatorname{Cov}(Z, Z)=\operatorname{Var}(Z)=\sigma_Z^2
\\
\operatorname{Cov}(Z, Y)=0
\\
\operatorname{Cov}(X, Z)=0
\\
\operatorname{Cov}(X, Y)=0
$$
所以
$$
\operatorname{Cov}(U, V)=\sigma_Z^2
$$
相关系数为
$$
\rho(U, V)=\frac{\operatorname{Cov}(U, V)}{\sqrt{\operatorname{Var}(U) \cdot \operatorname{Var}(V)}}
$$

$$
\operatorname{Var}(U)=\operatorname{Var}(Z+X)=\operatorname{Cov}(Z+X,Z+X)=\operatorname{Var}(Z)+\operatorname{Var}(X)+2 \cdot \operatorname{Cov}(Z, X)=\sigma_{X}^{2}+\sigma_{Z}^{2}
$$

同理可得
$$
\operatorname{Var}(V)=\operatorname{Var}(Z+Y)=\operatorname{Var}(Z)+\operatorname{Var}(Y)+2 \cdot \operatorname{Cov}(Z, Y)=\sigma_{Y}^{2}+\sigma_{Z}^{2}
$$
代入得
$$
\rho(U, V)=\frac{\sigma_{Z}^{2}}{\sqrt{\left(\sigma_{X}^{2}+\sigma_{Z}^{2}\right) \cdot\left(\sigma_{Y}^{2}+\sigma_{Z}^{2}\right)}}=\frac{1}{\sqrt{\left(1+\sigma_{X}^{2}\right) \cdot\left(1+\sigma_{Y}^{2}\right)}}
$$

# 60

$$
E(XY)=E(SY^2)=E(SY^2|S=1)P(S=1)+E(SY^2|S=-1)P(S=-1)=\frac{E(Y^2)+E(-Y^2)}{2}=0
$$

$$
E(SY)=E(SY|S=1)P(S=1)+E(SY|S=-1)P(S=-1)=\frac{E(Y)+E(-Y)}{2}=0
$$

所以
$$
\operatorname{Cov}(X, Y)=E(X \cdot Y)-E(X) \cdot E(Y)=E\left(S \cdot Y^{2}\right)-E(S \cdot Y) \cdot E(Y)=0-0=0
$$

$$
F_{X}(x)=P(X \leq x)=P(S \cdot Y \leq x)=\iint_{s \cdot y \leq x} f_{S, Y}(s, y) d s d y=\iint_{s \cdot y \leq x} f_{S}(s) \cdot f_{Y}(y) d s d y
$$

注意到
$$
P(S \cdot Y \leq x)=P(S \cdot Y \leq x|S=1)P(S=1)+P(S \cdot Y \leq x|S=-1)P(S=-1)
$$

$$
P(S \cdot Y \leq x|S=1)=P(Y\le x)=F_Y(x)\\
P(S \cdot Y \leq x|S=-1)=P(Y\ge -x)=1-F_Y(-x)
$$

所以
$$
F_{X}(x)=\frac{1}{2} \cdot\left(1-F_{Y}(-x)\right)+\frac{1}{2} \cdot F_{Y}(x)=\frac{1}{2} \cdot F_{Y}(x)-\frac{1}{2} \cdot F_{Y}(-x)+\frac{1}{2}
$$
由于 Y  的密度函数关于 $y$ 轴对称
$$
f_{Y}(x)=f_{Y}(-x)
$$
所以
$$
f_{X}(x)=F_{X}^{\prime}(x)=\left(\frac{1}{2} \cdot F_{Y}(x)-\frac{1}{2} \cdot F_{Y}(-x)+\frac{1}{2}\right)^{\prime}=\frac{1}{2} \cdot f_{Y}(x)+\frac{1}{2} \cdot f_{Y}(-x)=f_Y(x)
$$
然而
$$
f_{X | Y}(x | y)=\left\{\begin{array}{ll}{\frac{1}{2},} & {x=\pm y} \\ {0,} & {\text { 其他 }}\end{array}\right.
$$
所以
$$
f_{X | Y}(x | y) \neq f_{X}(x)
$$
这表明 $X$ 和 $Y$ 不独立

# 补充题

## 1.

$$
E(X)=\int_{-\infty}^{\infty}xf(x) dx=\int_{-\infty}^{0}\frac{xe^{x}}{2} dx+\int_{0}^{\infty}\frac{xe^{-x}}{2} dx=\left.\frac{e^{x} (x-1)}{2}\right|_{-\infty}^{0}+\left.\frac{e^{-x} (-x-1)}{2}\right|_{0} ^{\infty}=-\frac{1}{2}+\frac{1}{2}=0
$$

$$
E(X^2)=\int_{-\infty}^{\infty}x^2f(x) dx=\int_{-\infty}^{0}\frac{x^2e^{x}}{2} dx+\int_{0}^{\infty}\frac{x^2e^{-x}}{2} dx=\\
\left.\frac{e^{x} (x^2-2 x+2)}{2}\right|_{-\infty}^{0}+\left.\frac{e^{-x} (-x^2-2 x-2)}{2}\right|_{0} ^{\infty}=1+1=2
$$

所以
$$
D(X)=E(X^2)-E(X)^2=2-0^2=2
$$

## 2.

不独立, 考虑事件 $X>1$ 和 $|X|\ge1$
$$
P(X\ge1)=\int_1^{\infty } \frac{ e^{-x}}{2} \, dx=\frac{1}{2e}
$$

$$
P(|X|\ge1)=P(X \ge 1)+P(X \le -1)=\frac{1}{e}
$$

而
$$
P(X\ge 1,|X|\ge1)=P(X\ge1)=\frac{1}{2e}\neq P(X\ge 1)P(|X|\ge1)
$$

### 3.

由于 $X$ 和 $|X|$ 不独立, 所以它们一定相关



