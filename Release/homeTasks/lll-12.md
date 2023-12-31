---
dg-publish: true
info: 概率论作业 12
share: true
---

> 概率论作业 12

![Pasted image 20231205182633.png](../../source/img/Pasted%20image%2020231205182633.png)

$$M_{X^2}=\mathbb E(e^{sX^2})=\int_Re^{sx^2}\frac1{\sqrt{2\pi}}e^{-\frac12(x-\mu)^2}\text { d}x=\frac1{\sqrt{1-2s}}\exp\left(\frac{\mu^2s}{1-2s}\right)$$
$$M_Y=\prod X=\frac{1}{(1-2s)^{n/2}}\exp\left(\frac{s\theta}{1-2s}\right)$$
$$\phi_Y(t)=\frac{1}{(1-2it)^{n/2}}\exp\left(\frac{it\theta}{1-2it}\right)$$

****
![Pasted image 20231205182701.png](../../source/img/Pasted%20image%2020231205182701.png)
$U:=R\cos\Theta$ $V:=R\sin\Theta$ $\Theta$ is independent to $X,Y$
$Z=X\cos\Theta+Y\sin\Theta\sim N(0+0,\sin^\Theta+\cos^2\Theta)=N(0,1)$
****
![Pasted image 20231205182716.png](../../source/img/Pasted%20image%2020231205182716.png)
$$\begin{align}
\mathbb E(e^{itx})&=\lambda\int e^{itx-\lambda x}\text{ d}x\\
&=\lambda\int e^{-\lambda x}\cos tx\text { d} x+i\lambda\int e^{-\lambda x}\sin tx\text{ d}x\\
&=\lambda e^{-\lambda x}(\cos tx-\frac t\lambda\sin tx)(-\lambda-\frac{t^2}{\lambda})^{-1}|_0^\infty\\&+i\lambda e^{-\lambda}(\sin tx+\frac t\lambda\cos tx)(-\lambda-\frac{t^2}{\lambda})^{-1}|_0^\infty\\
&=\frac{\lambda}{\lambda^2-t^2}(\lambda+it)=\frac{\lambda}{\lambda-it}
\end{align}$$
****
![Pasted image 20231205182729.png](../../source/img/Pasted%20image%2020231205182729.png)
(a)
$$\small\mathbb E(e^{itX})=\frac12\int_\mathbb Re^{itx-|x|}\text{ d}x=\frac12\int_{\mathbb R^+}2e^{-x}\cos tx\text { d}x=\left.(\cos tx-t\sin tx)(t^2-1)^{-1}e^{-x}\right|_0^\infty=\frac2{t^2-1}$$
(b)
$$\begin{align}
\mathbb E(e^{itX})&=\int_{\mathbb R^+}xe^{-x}\cos tx\text { d}x\\&=(\frac{xt\sin tx-x\cos tx}{t^2+1}+\frac{2t}{(t^2+1)^2}\sin t+\frac{t^2-1}{(t^2+1)^2}\cos t)e^{-x}|_0^\infty\\&
=\frac{t^2-1}{(t^2+1)^2}
\end{align}$$
另解: 先对 t 积分去掉 x , 再计算后对 t 求导

****
![Pasted image 20231205182740.png](../../source/img/Pasted%20image%2020231205182740.png)
$X=Y=Z=0$ 显然符合题意

设 X 的矩母函数为 $M(t)$, 则
$$M(t)=\int_0^1M(ut)du\Rightarrow tM'+M=M^2\Rightarrow M=\frac{\lambda}{\lambda+t}$$
从而是指数分布