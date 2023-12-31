---
dg-publish: true
info: 概率论作业 11
share: true
---

> 概率论作业 11

![Pasted image 20231205091132.png](../../source/img/Pasted%20image%2020231205091132.png)

since $\mathbb E[X_n]=0,\mathbb E[X_n^2]=\frac{n}{\log n},\mathbb E[X_mX_n]=\mathbb E[X_m]\mathbb E[X_n]=0$
we have $\mathbb E[(\sum_2^nX_i)^2]=\mathbb E[\sum_2^nX_i^2]=\sum_2^n\frac{i}{\log i}\leq \frac{n^2}{\log n}$ 
hence $\forall \varepsilon>0,\mathbb P[|n^{-1}\sum X|>\varepsilon]=\mathbb P[n^{-2}(\sum X)^2>\varepsilon^2]\leq\frac{\mathbb E[\sum X_i^2]}{n^2\varepsilon^2}=\frac{1}{\varepsilon^2\log n}\rightarrow0\text{ as }n\rightarrow\infty$
****

![Pasted image 20231205091218.png](../../source/img/Pasted%20image%2020231205091218.png)
proof:
$I_{m}(i):=\mathcal I{\{X_m \text { is in the ith interval}\}}$, $\mathbb E[I_{m}(i)]=p_i$, hence $\frac{Z_m(i)}{m}=\frac{\sum_1^m I_n(i)}{m}\stackrel{\text{a.s.}}\longrightarrow p_i$
$$m^{-1}\log R_m=\sum_{i=1}^n\frac{Z_m(i)}{m}\log p_i\stackrel{\text{a.s.}}\longrightarrow m^{-1}\log R_m=\sum_{i=1}^np_i\log p_i=-h$$
****
![Pasted image 20231205091239.png](../../source/img/Pasted%20image%2020231205091239.png)
proof:
Forall $m\in[0,1]$, let $m_i$ be the ith demical place of $m$
$$\mathbb P[X_n<m]=\sum_{i-1}^n 10^{-i}m_i{\longrightarrow}m=\mathbb P[Y<m]\text{ as }n\rightarrow\infty$$
i.e $X_n\stackrel{D}{\rightarrow}Y$, by Skorokhod theorem, there exist some $Y$, s.t. $X_n\stackrel{\text{a.s.}}{\longrightarrow}Y$

****
![Pasted image 20231205091255.png](../../source/img/Pasted%20image%2020231205091255.png)
Define $Y_n:=X_nI_{\{|X|\leq n\}}$, therefore $\mathbb P(X_n\neq Y_n \text{ for infinite many values of }n)=0$

$$\exists A>>0, \sum_{n=1}^\infty\mathbb P(|\sum_{i=1}^nY_i|>\varepsilon)\leq\frac{A}{\varepsilon^2}\sum_{i=1}^\infty\frac1 {i^2}\mathbb E(Y_i^2)\leq2[\mathbb E(X_i)+1]<2$$
hence
$$\frac1{n}\sum_{i=1}^n Y_i\stackrel{\text{a.s.}} \longrightarrow0, \text{ as }n\rightarrow\infty$$
****
**补充题 1**: 设 $\{X_k\}$ i.i.r, $X_k$ 均为非负, 若 $\mathbb E[X_1]=\infty$ 试证明
$$\frac1n\sum_{k=1}^nX_k\stackrel{\text{a.s.}}{\longrightarrow}\infty$$
证明: 
$$\sum_n\mathbb P(X_n>n)\geq\mathbb E(X_1)-1=\infty$$
由第二 Borel–Cantelli 引理, 我们有
$$\mathbb{P}(存在无穷多个n, 使得X_n>n)=1$$
$\{b_1,b_2,\cdots\}=\{b:X_b>b\}$,
$$\limsup_{n\rightarrow\infty}\frac{\sum_1^nX_i}{n}=\infty$$
由于 $X_n$ 非负, $\frac1n\sum_{k=1}^nX_k$ 有极限, 极限是正无穷.

****
**补充题 2**: 记
$$I_n=\int_{[0,1]^n}\frac{n}{\sum_{k=1}^n\frac1{x_n}}\text{ d}x_1\text{ d}x_2\cdots\text{ d}x_n$$
试证: $\lim_{n\rightarrow\infty}I_n$ 存在 
证明: 
令 $X_i$ i.i.r 是 $[0,1]$ 上的平均分布, $Y_n=\frac{n}{\sum_{k=1}^n\frac1{X_k}}$, 则 $I_n=\mathbb E(Y_n)$, 对 $Y_n$ 有
$$\forall \varepsilon>0, \mathbb P(Y_n\leq\varepsilon)\geq(1-\frac\varepsilon n)^n=e^{-\varepsilon}\rightarrow1\text{ as }n\rightarrow\infty,\varepsilon\rightarrow0$$
从而$Y_n\stackrel{P}\longrightarrow0$,$\lim_{n\rightarrow\infty}I_n=0$
