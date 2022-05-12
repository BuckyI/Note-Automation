# ADRC 设计

[toc]

[本科教学：自抗扰控制的设计与仿真_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1YJ411w7Wr)
PID: 自校正原理，出现误差，进行调整.
ADRC: $\dot{y}=-ay+bu\to \dot{y}=f(y,d,t)+bu$
估计出 $\hat{f}$ , 令 $u=\frac{-\hat{f}(t)+u_0}{b}$, 则可以使 $\dot{y}=u_0$
在控制之前，使系统动态接近一个理想的积分器的动态.

如何估计 $f$?

1. $f=\dot{y}-bu$, 因此对 y 求导再滤波就可以. $\hat{f}=\frac{s}{\tau s+1}y-bu\approx \dot{y}-bu$ (DOB)
2. ESO 扩张状态观测器
    ![状态观测器](assets/ADRC%E8%AE%BE%E8%AE%A1/2022-03-29-16-37-25.png)
    ![一阶系统](assets/ADRC%E8%AE%BE%E8%AE%A1/2022-03-29-16-49-09.png)
