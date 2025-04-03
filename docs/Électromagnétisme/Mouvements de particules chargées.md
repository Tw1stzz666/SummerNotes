# Mouvements de particules chargées                         

在本章中, 我们关注的是电磁场中电荷的的运动

## 1.Particule chargée dans un champ électrique $\vec{E}$                                   

### 1.1 Valeur de la vitesse                         

tu

我们在先前的章节我们已经见过在两块金属板之间产生的匀强电场 $\vec{E}$ , 我们再次研究这样一个模型, 两个板分别为阳极 (anode) 和阴极 (cathode) , 板间距为 $d$
因此, 电场 𝐸⃗ 可表示为: $\vec{E} = E \vec{u_z}$ , 其方向由阳极指向阴极 (沿电势递减的方向) , 我们可以得出如下关系:          

\[
    \vec{E} = E \vec{u_z} 
\]

\[
    V_{\text{Anode}} - V_{\text{Cathode}} = U 
\]

\[
    U = - \int_{\text{Cathode}}^{\text{Anode}} \vec{E} \cdot \vec{dl} = Ed 
\]

\[
    E = \frac{U}{d}
\]

---

\[
    \vec{E} = - \vec{grad}(V)
\]

\[
    E \vec{u_z} = - \frac{dV}{dz} \vec{u_z}
\]

\[
    E = -\frac{dV}{dz}
\]

\[
    V(z) = - E_z + A
\]

\[
    U = V(0) - V(d) = Ed
\]

\[
    E = \frac{U}{d}
\]

以上使用了两种方法得出 $E$ 和 $U$ 之间的关系                  

我们考虑在极板间有一个初速度为零的电子                                     

\[
    \vec{F} = q \vec{E} = - e \vec{E}
\]

由动能定理:    

\[
    \Delta E_c = W
\]

\[
    E_c(\text{Anode}) - E_c(\text{Cathode}) = E_c(\text{Anode}) - 0 = W
\]

\[
    W = e E d = e U = E_c(\text{Anode}) = \frac{1}{2} m v_a^2
\]

\[
    v_a = \sqrt{\frac{2 e U}{m}}
\]

对于一个电子: $e = 1.6 \times 10^{-19} C, \quad m = 9 \times 10^{-31} kg$ , 极板间电压 $U = 220 V$

\[
    v_a = 8.8 \times 10^6 m \cdot s^{-1}
\]

!!! note "Note"

    - $E_c = e U$                                    
      其中 1 电子伏特 (eV) 等于 \(1.6 \times 10^{-19} J\), 因此 $E_c$ 的数值与 $U$ 相同                                    
      例如, 若 $U = 220V$ , 则 $E_c = 220eV$               
    - 当电子的速度 $v \geq 10^8 m \cdot s^{-1}$ 时, 它变为相对论性电子, 当 $U \geq 30 kV$ 时会发生这种情况  

### 1.2 Equation du mouvement                                       

tu

设粒子最初位于 $O$ 点, 初速度为 \( \vec{v_0} \) , 其运动位于 $(yOz)$ 平面内                      

在假设地球参考系为伽利略参考系的情况下, 应用牛顿第二定律：  

\[
    m \vec{a} = q \vec{E} = \frac{qU}{d} \vec{e_z}
\]

\[
    \begin{cases}
    m \ddot{x} = 0 \\
    m \ddot{y} = 0 \\
    m \ddot{z} = \frac{qU}{d}
    \end{cases}
    \Rightarrow
    \begin{cases}
    \dot{x} = A \\
    \dot{y} = B \\
    \dot{z} = \frac{qU}{md} + C
    \end{cases}
\]

由初始状态 $\vec{v}(0) = \vec{v_0} = v_0 \cos \alpha \vec{e_y} + v_0 \sin \alpha \vec{e_z}$ , 解得:      

\[
    \begin{cases}
    A = 0 \\
    B = v_0 \cos \alpha \\
    C = v_0 \sin \alpha
    \end{cases}
\]

代回速度表达式并在此积分:         

\[
    \begin{cases}
    x = D \\
    y = v_0 \cos \alpha t + F \\
    z = \frac{qU}{2md} t^2 + v_0 \sin \alpha t + G
    \end{cases}
\]

由初始状态 $x(0) = y(0) = z(0) = 0 = D = F = G$                        
可得:                  

\[
    \begin{cases}
    x = 0 \\
    y = v_0 \cos \alpha t \\
    z = \frac{qU}{2md} t^2 + v_0 \sin \alpha t 
    \end{cases}
\]

得出轨迹方程:                       

\[
    z = \frac{qU}{2md v_0^2 \cos^2 \alpha} y^2 + \tan \alpha y              
\]

当 $\alpha = \pm \frac{\pi}{2}$ , 则粒子沿 $z$ 轴做匀加速直线运动   

### 1.3 Application: Déviation d’un faisceau de particules

tu

在两块金属板之间, 电场 $\vec{E} = \frac{U}{d} \vec{e_z}$ , 而在其他区域, 电场 $\vec{E} = \vec{0}$                  
在这种情况下, 我们尝试计算粒子最终打在屏幕上的偏转量 $Z$ ：                          

利用 1.2 中得出的轨迹方程, 其中 $\alpha = 0$

\[
    z = \frac{qU}{2md v_0^2} y^2, \quad 0 \leq y \leq p
\]

\[
    \tan \beta = \frac{v_z (y=p)}{v_y (y=p)} = \frac{Z - z_S}{D}
\]

\[
    \begin{cases}
    v_y (y=p) = \dot{y} = v_0 \\       
    v_z (y=p) = \dot{z} = \frac{Uqp}{mdv_0}
    \end{cases}
\]

\[
    \frac{Z-z_S}{D} = \frac{Z - \frac{qUp^2}{2mdv_0^2}}{D} = \frac{v_z (y=p)}{v_y (y=p)} = \frac{\frac{qUp}{mdv_0}}{v_0}
\]

\[
    Z = \frac{qp}{mdv_0^2} (\frac{p}{2} + D) U
\]

!!! note "Note"

    - $Z$ 与 $U$ 成正比, 这正是示波器的工作原理         
    - 该装置还能充当粒子筛选器, 因为 $Z$ 与 \( \frac{q}{m} \) 成正比, 因此, 在 $Z$ 处放置一个狭缝, 只允许特定 \( \frac{q}{m} \) 比值的粒子通过   

## 2.Particule chargée dans un champ magnétique $\vec{B}$                             

### 2.1 Conservation de l’énergie cinétique                 

洛伦兹力的磁场部分不做功, 因此粒子的动能保持不变, 即速度大小 $v = \text{C}$ 恒定                    
但要注意, 速度的方向可能会改变, 即 \( \vec{v} ≠ \vec{C} \)   

### 2.2 Equation du mouvement

tu

设磁场方向为：$\vec{B} = B \vec{e_z}$ , 初始速度 $\vec{v_0}$ 位于 $(xOz)$ 平面内, 粒子最初位于 $O$ 点   

在假设地球参考系为伽利略参考系的情况下, 应用牛顿第二定律：         

\[
    m \vec{a} = q \vec{v} \wedge \vec{B}
\]

在空间的三个方向上展开, 可得到:      

\[
    m 
    \begin{pmatrix}
    \ddot{x} \\
    \ddot{y} \\
    \ddot{z}
    \end{pmatrix}
    =
    q 
    \begin{pmatrix}
    \dot{x} \\
    \dot{y} \\
    \dot{z}
    \end{pmatrix}
    \land
    \begin{pmatrix}
    0 \\
    0 \\
    B
    \end{pmatrix}
    \Rightarrow
    \begin{cases}       
    m \ddot{x} = q B \dot{y} \\           
    m \ddot{y} = -q B \dot{x} \\              
    m \ddot{z} = 0              
    \end{cases}
    \Rightarrow
    \begin{cases}       
    \ddot{x} = \frac{q B}{m} \dot{y} = \omega \dot{y}, \quad \omega = \frac{qB}{m} \\           
    \ddot{y} = - \frac{q B}{m} \dot{x} = - \omega \dot{x} \\              
    \ddot{z} = 0              
    \end{cases}
\]

\[
    \dot{x} = \omega y + cste = \omega y + v_0 \sin \alpha
\]

\[
    \dot{y} = -\omega x + cste = -\omega x           
\]

\[
    \ddot{x} = -\omega^2 x              
\]

下面介绍两种求解方法：  

#### 2.2.1 Méthode « classique »

对等式 $\ddot{x} = \omega \dot{y}$ 再次微分:         

\[
    \ddot{v_x} = \omega \dot{v_y} = − \omega^2 v_x
\]

可知, $v_x$ 是简谐振动：

\[
    v_x = A \cos(\omega t) + B \sin(\omega t)
\]

由初始条件 $v_x(0) = v_0 \sin(\alpha) = A, \quad \dot{v_x}(0) = \omega v_y(0) = 0 = B$        
可得：

\[
    \begin{cases}
    v_x = v_0 \sin(\alpha) \cos(\omega t) \\
    v_y = -v_0 \sin(\alpha) \sin(\omega t)
    \end{cases}
\]

#### 2.2.2 Méthode des complexes

定义复变量：

\[
    Z = v_x + jv_y = \dot{x} + j \dot{y}
\]

对 $Z$ 微分: 

\[
    \dot{Z} = \ddot{x} + j \ddot{y} = \omega \dot{y} - j \omega \dot{x} = - j w \left( \dot{x} + j \dot{y} \right) = -j w Z
\]

可得出:  

\[
    \dot{Z} + j w Z = 0
\]

解一阶微分方程:                   

\[
    Z = A e^{-j w t}
\]

由初始状态 $Z(0) = v_x (0) + j v_y (0) = v_0 \sin (\alpha)$ , 可得:                          

\[
    A = v_0 \sin (\alpha)
\]

代回原式:               

\[
    Z = v_0 \sin (\alpha) \, e^{-j w t} = v_0 \sin (\alpha) \left( \cos (w t) - j \sin (w t) \right)
\]

得出:                           

\[
    \begin{cases}
    v_x = v_0 \sin(\alpha) \cos(\omega t) \\
    v_y = -v_0 \sin(\alpha) \sin(\omega t)
    \end{cases}
\]



#### 2.2.3 Equation paramétrique

我们尝试求出电荷轨迹的参数方程                                     

对速度表达式积分并根据初始条件 \( x(0) = y(0) = z(0) = 0 \), 解出：

\[
    \begin{cases}
    x = \frac{v_0 \sin(\alpha)}{\omega} \sin(\omega t) \\
    y = \frac{v_0 \sin(\alpha)}{\omega} (\cos(\omega t) - 1) \\
    z = v_0 \cos(\alpha) t
    \end{cases}
\]

我们注意到 $x,y$ 之间有如下关系：

\[
    x^2 + (y + R)^2 = R^2
\]

其中：

\[
    R = \frac{v_0 \sin(\alpha)}{|\omega|} = \frac{v_0 m \sin(\alpha)}{|q|B}
\]

电荷的轨迹在 $(Oxy)$ 平面上形成一个以 \( C(0, R) \) 为中心, 半径为 \( R \) 的圆, 而在 z 方向粒子则做匀速直线运动, 因此整体轨迹为螺旋线   

螺旋线的螺距为：

\[
    h = v_0 \cos(\alpha) T = \frac{2\pi v_0 \cos(\alpha)}{|\omega|}
\]

其中螺距表示相邻两圈螺旋的间距 

!!! note "Note"
    粒子同时进行绕点 $C$ 的匀速圆周运动以及沿 \( O_z \) 方向的匀速直线运动, 因此可以得出结论, 磁场会使带电粒子的轨迹沿磁场方向螺旋运动 

## 3.Cas particulier de la trajectoire circulaire

当 $\alpha = \frac{\pi}{2}$ 时, 粒子仅在 $(𝑂𝑥𝑦)$ 平面内运动, 其轨迹为匀速圆周运动, 半径为 $R = \frac{v_0}{|\omega|} = \frac{v_0 m}{|q|B}$

下面给出一些应用的例子

!!! example "Exemple"

    - 气泡室：已知磁场 \( B \), 测量轨迹半径 \( R \) 可推导粒子的动量 \( p = mv_0 \) 或电荷 \( q \)   
    - 质谱仪：电离原子后, 利用磁场分离不同同位素, 因为其质量不同     
    - 非线性粒子加速器, 如回旋加速器  

