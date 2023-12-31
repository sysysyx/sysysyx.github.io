---
dg-publish: true
info: 概率论作业 13
share: true
---

![Pasted image 20231219190458.png](../../source/img/Pasted%20image%2020231219190458.png)
(a)
$$\begin{align}
F_n(+\infty)=F_n(1)=1\\ F_n(-\infty)=F_n(0)=0
\end{align}$$
density function:
$$f_n(x)=\frac{dF_n}{dx}=1-\cos(2n\pi x)>0$$
(b)
$$F(x):=x,\ |F_n(x)-F(x)|\leq|\frac{1}{2n\pi}|\rightarrow0\text{ as } n\rightarrow\infty$$
$$f(x):=1,\ \max |f(x)-f_n(x)|=1,\ |f(0)-f_n(0)|=1$$

![Pasted image 20231219201351.png](../../source/img/Pasted%20image%2020231219201351.png)

Let $X,Y$ (independent) with uniformly distinction on $[-a,a]$ and $[-b,b]$, we have 
$$\int_{-\infty}^\infty\phi_{X+Y}(t)dt=\int_{-\infty}^\infty \frac{\sin at\sin bt}{abt^2}dt=2\pi f_{X+Y}(0)=\frac{\pi\min\{a,b\}}{ab}$$
$$\int_{-\infty}^\infty \frac{\sin at\sin bt}{t^2}dt=\pi \min\{a,b\}$$

**补充：(cost)^2对应的分布函数**

$\cos t$ 的随机变量
$$\cos t=\frac{e^{it}+e^{-it}}{2}=\int_{-\infty}^\infty e^{itx}dF$$
$$X=\begin{cases}
1&\mathbb P=\frac12\\
-1&\mathbb P=\frac12
\end{cases}$$
$\cos^2 t$ 对应的随机变量
$$Y=X_1+X_2=\begin{cases}
2&\mathbb P=\frac14\\
0&\mathbb P=\frac12\\
-2&\mathbb P=\frac14
\end{cases}$$
$$F=\begin{cases}
0 & x<-2\\
\frac14 &-2\leq x<0\\
\frac34 &0\leq x<2\\
1 & x\geq 2
\end{cases}$$
