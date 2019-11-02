# Mathematical Statistics and Data Analysis

## Joint Distributions

## 11810105 谢泽健

### 3

记三个玩家赢得比赛的局数分别为 $X_1,X_2,X_3$, 则 $X_1,X_2,X_3$ 满足多项分布, 其公式为:
$$
p\left(y_{1}, y_{2}, \ldots, y_{k}\right)=\frac{n !}{y_{1} ! y_{2} ! \ldots y_{k} !} p_{1}^{y_{1}} p_{2}^{y_{2}} \ldots p_{k}^{y_{k}}
$$
所以
$$
p\left(x_{1}, x_{2}, x_{3}\right)=\frac{10 !}{x_{1} ! x_{2} ! x_{3} !}\left(\frac{1}{3}\right)^{x_{1}}\left(\frac{1}{3}\right)^{x_{2}}\left(\frac{1}{3}\right)^{x_{3}}
$$

### 补充题

依题意
$$
X \sim B(3,\frac{1}{2})\\
Y=|X-(3-x)|=|2x-3|
$$

|         | X=0  | X=1  | X=2  | X=3  |
| ------- | ---- | ---- | ---- | ---- |
| **Y=0** | 0    | 0    | 0    | 0    |
| **Y=1** | 0    | 3/8  | 3/8  | 0    |
| **Y=2** | 0    | 0    | 0    | 0    |
| **Y=3** | 1/8  | 0    | 0    | 1/8  |

综上,
$$
p(x,y)=\left\{\begin{array}{ll}{3/8} & {x=1,2 \quad y=1} \\ {1/8} & {x=0,3 \quad y=0}  \\ {0} & {其他}\end{array}\right.
$$

### 5

以 $M$ 表示针的重点, 以 $x$ 表示 $M$ 与最近的一条平行线的距离, 记它们的夹角为 $\phi$, 显然 $x$ 与 $\phi $ 可以确定针的相对距离, 且有
$$
0 \le x \le \frac{D}{2}\\
0 \le \phi \le \pi
$$
为了使得针与平行线相交, 有
$$
x\le \frac{L \sin \phi}{2}
$$
因为 $X$ 和 $\Phi$ 均为均匀分布, 且彼此独立, 故
$$
p=P(X\le \frac{l \sin \Phi}{2})=\frac{1}{\pi}\int_{0}^{\pi}{\frac{\frac{L \sin \phi}{2}}{\frac{D}{2}}}=\frac{2L}{\pi D}
$$
在试验次数足够多时, 频率趋近于概率, 故而在大量试验后, 可由针相交的频率 $r$ 估算 $\pi$
$$
\pi \approx \frac{2 L}{r D}
$$

### 6.

$$
f_{XY}(x,y)=f_X(x|y)f_Y(y)
$$

对于 $y$ 的密度函数, 其等于在每个 $y$ 值对应的水平线长度比上椭圆面积
$$
f_Y(y)=\frac{2 \sqrt{\frac{\left(a^{2} b^{2}-a^{2} y^{2}\right)}{b^{2}}}}{\pi a b}=\frac{2 \sqrt{b^{2}-y^{2}}}{\pi b^{2}}
$$
同理有
$$
f_{X}(x)=\frac{2 \sqrt{a^{2}-x^{2}}}{\pi a^{2}}
$$

### 7.

联合密度为
$$
\frac{\partial F(x,y)}{\partial x \partial y}=\alpha  \beta  e^{\alpha  (-x)-\beta  y}
$$
对于边际密度
$$
\begin{aligned} f_{X}(x)&=\int_{0}^{+\infty} f(x, y) d y\\&= \int_{0}^{+\infty} \alpha \beta e^{-\alpha x-\beta y} d y \\&=\alpha \beta e^{-\alpha x} \int_{0}^{+\infty} e^{-\beta y} d y \\&=\left.\alpha \beta e^{-\alpha x}\left(-\frac{e^{-\beta y}}{-\beta}\right)\right|_{0} ^{+\infty} \\&= \alpha \beta e^{-\alpha x} \frac{e^{-0}}{\beta} \\&= \alpha e^{-\alpha x} \end{aligned}
$$
由对称性
$$
f_Y(y)=\beta e^{-\beta y}
$$

### 8.

#### a.

##### 1

$$
\begin{aligned} P(X>Y)&=\iint_{x>y}{\frac{6}{7}(x+y)^{2}dxdy}\\&= \int_{0}^{1} \int_{y}^{1} \frac{6}{7}(x+y)^{2} d x d y \\&=\left.\int_{0}^{1}\left(\frac{2}{7}(x+y)^{3}\right)\right|_{y} ^{1} d y \\&= \int_{0}^{1}-2 y^{3}+\frac{6}{7} y^{2}+\frac{6}{7} y+\frac{2}{7} d y \\&=\left.\left(-\frac{y^{4}}{2}+\frac{2 y^{3}}{7}+\frac{3 y^{2}}{7}+\frac{2 y}{7}\right)\right|_{0} ^{1} \\&=\frac{1}{2} \end{aligned}
$$

##### 2.

$$
\begin{aligned} P(X+Y \leq 1)&= \int_{0}^{1} \int_{0}^{1-y} \frac{6}{7}(x+y)^{2} d x d y \\&=\left.\int_{0}^{1}\left(\frac{2}{7}(x+y)^{3}\right)\right|_{0} ^{1-y} d y \\&= \int_{0}^{1}-\frac{2}{7} y^{3}+\frac{2}{7} d y \\&=\left.\left(-\frac{1}{14} y^{4}+\frac{2}{7} y\right)\right|_{0} ^{1} \\&= \frac{3}{14}  \end{aligned}
$$

##### 3.

$$
\begin{aligned} P(X\leq \frac{1}{2}&=\int_{0}^{1} \int_{0}^{1 / 2} \frac{6}{7}(x+y)^{2} d x d y \\ &=\left.\int_{0}^{1}\left(\frac{2}{7}(x+y)^{3}\right)\right|_{0} ^{1 / 2} d y \\ &=\int_{0}^{1} \frac{3}{7} y^{2}+\frac{3}{14} y+\frac{1}{28} d y \\ &=\left.\left(\frac{1}{7} y^{3}+\frac{3}{28} y^{2}+\frac{1}{28} y\right)\right|_{0} ^{1} 
\\&=\frac{2}{7}\end{aligned}
$$

#### b

$$
\begin{aligned} f_{X}(x) &=\int_{0}^{1} \frac{6}{7}(x+y)^{2} d y \\ &=\left.\left(\frac{2}{7}(x+y)^{3}\right)\right|_{0} ^{1} \\ &=\frac{2}{7}(x+1)^{3}-\frac{2}{7} x^{3} \\ &=\frac{6}{7} x^{2}+\frac{6}{7} x+\frac{2}{7} \end{aligned}
$$

同理可得
$$
f_Y(y)=\frac{6}{7} y^{2}+\frac{6}{7} y+\frac{2}{7}
$$

#### c

$$
f(y | X=x)=\frac{f(x, y)}{f_{X}(x)}=\frac{\frac{6}{7}(x+y)^{2}}{\frac{6}{7} x^{2}+\frac{6}{7} x+\frac{2}{7}}=\frac{3(x+y)^{2}}{3 x^{2}+3 x+1}
$$

同理有
$$
f(x | Y=y)=\frac{f(x, y)}{f_{Y}(y)}=\frac{\frac{6}{7}(x+y)^{2}}{\frac{6}{7} y^{2}+\frac{6}{7} y+\frac{2}{7}}=\frac{3(x+y)^{2}}{3 y^{2}+3 y+1}
$$
