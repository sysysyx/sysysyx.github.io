---
dg-publish: true
info: 数学分析作业 12
share: true
---

> P328 2,3,4
> P338 2 3 6 7


![Pasted image 20231208150718.png](../../source/img/Pasted%20image%2020231208150718.png)
2. 证明: 
对 $[0,\pi]$ 上的任意连续函数 $f$ 首先将该函数做偶性延拓, 再计算其在三角多项式下的傅里叶系数, 由于
$$\int_{-\pi}^\pi f(x)\sin nx\text{ d}x=\int_{-\pi}^\pi f(x)\text{ d}x=0$$
对所有 $n$ 成立, 因此该函数的傅里叶级数只含余弦项, 从而可以用余弦多项式一致逼近.

3. 证明:
$$\lim_{n\rightarrow\infty}\frac {a_n}n=\lim_{n\rightarrow\infty}\frac{n\sigma_n-2(n-1)\sigma_{n-1}+(n-2)\sigma_{n-2}}{n}=\lim_{n\rightarrow\infty}(2\sigma-2\sigma)=0$$

![Pasted image 20231208150747.png](../../source/img/Pasted%20image%2020231208150747.png)
2. 证明: 由于 $f(x)$ 是偶函数, $b_n=0$, $a_0=\frac{2\alpha}{\pi}$
$$a_n=\frac1\pi\int_{-\pi}^\pi f(x)\cos nx\text dx=\frac{2\sin n\alpha}{n\pi}$$
所以该函数的 Parseval 等式是
$$\frac{4\alpha^2}{\pi^2}+\sum_{n=1}^\infty \frac{4\sin^2 n\alpha}{n^2\pi^2}=
\frac1\pi\int_{-\pi}^\pi f^2(x)=\frac{2\alpha}\pi$$
从而
$$\sum_{n=1}^\infty\frac{\sin^2 n\alpha}{n^2}=\frac{\pi\alpha}{2}-\alpha^2$$
由于
$$\sum_{n=1}^\infty\frac{\sin^2n\alpha+\cos^2n\alpha}{n^2}=\sum_{n=1}^\infty\frac{1}{n^2}=\frac{\pi^2}{6}$$
$$\sum_{n=1}^\infty\frac{\cos^2n\alpha}{n^2}=\frac{\pi^2}{6}-\frac{\pi\alpha}{2}+\alpha^2$$
3. 证明:
$$x^2=4\sum_{n=1}^\infty(-1)^{n-1}\frac{1-\cos nx}{n^2}=\frac{\pi^2}3+4\sum(-1)^n\frac{\cos nx}{n^2}$$
$$x^3=12\sum_{n=1}^\infty(-1)^{n-1}[\frac{x}{n^2}-\frac{\sin nx}{n^3}]=\frac{2\pi}{3}\sum(-1)^{n-1}\left(\frac{\sin nx}{n}-\frac{\sin nx}{n^3}\right)$$

$$x^4=48\sum_{n=1}^\infty(-1)^{n-1}[\frac {x^2}{2n^2}-\frac{1-\cos nx}{n^4}]$$

分别对 $x^3$, $x^4$ 利用 Parseval 等式, 化简得到

所以
$$\sum\frac{1}{n^6}=\frac{\pi^6}{945}$$
同理
$$\sum\frac1{n^8}=\frac{\pi^8}{9450}$$

![Pasted image 20231208150800.png](../../source/img/Pasted%20image%2020231208150800.png)

6.  证明:
$$\frac{1}{\pi}\int_{-\pi}^\pi f^2(x)\text{ d}x=a^2_0+\sum a_n^2+\sum b_n^2<\infty$$
$$\sum\frac{a_n}{n}<\sum(a_n^2+\frac1{n^2})<\infty$$
同理 $b_n$ 收敛

7. 证明:
$$\sum_{n=2}^\infty\frac{\sin nx}{\ln n}<\sum\sin nx<\infty$$
$$\lim_{n\rightarrow\infty}\frac{\sin nx}{\ln n}=0$$
从而该级数收敛

若它是某个函数的傅里叶级数, 有
$$\int_{-\pi}^\pi f(x)\sin nx\text dx=\frac1{\ln n}$$
根据 Parseval 等式,
$$\sum_{n=0}^\infty \frac{1}{\ln n^2}<+\infty$$
矛盾, 从而该级数不是某个函数的傅里叶级数.