# Espaces vectoriels de dimension finie

> 本章中, $\mathbb{K}$ 均定义为一个域

## 1.Théorie de la dimension

<div class="grid cards" markdown>

-   **Définition: Matrice représentative d’un vecteur dans une base** 

    ---

    设 \( E \) 是一个 \( \mathbb{K} \)-向量空间, 且整数 \( n \geq 1 \) , 假设 \( E \) 存在一组基

    \[
        \mathcal{B} = (e_1, \dots, e_n)
    \]  

    对于任意 \( u \in E \), 设 \( x_1, \dots, x_n \in \mathbb{K} \) 是 \( u \) 在基 \( B \) 下的坐标, 则列矩阵  

    \[
    \text{mat}_B(u) =  
    \begin{pmatrix}  
    x_1 \\  
    \vdots \\  
    x_n  
    \end{pmatrix}  
    \in M_{n,1}(\mathbb{K})  
    \]  

    称为 \( u \) 在基 \( B \) 下的表示矩阵   

    换句话说, \( u \) 可以表示为: $u = x_1 e_1 + \dots + x_n e_n$

</div>

??? example "Exemple"
    ### 示例 1  
    设 \( E \) 是一个 \( K \) 上的向量空间。假设 \( B = (e_1, e_2, e_3) \) 和 \( B' = (f_1, f_2, f_3) \) 是 \( E \) 的两个基，并且向量 \( u \in E \) 满足：  
    \[
    u = 2e_1 - 4e_3
    \]
    \[
    u = f_1 + \frac{1}{2} f_2
    \]
    那么 \( u \) 在基 \( B \) 下的矩阵表示为：  
    \[
    \text{mat}_B(u) =
    \begin{pmatrix}
    2 \\
    0 \\
    -4
    \end{pmatrix}
    \]
    而 \( u \) 在基 \( B' \) 下的矩阵表示为：  
    \[
    \text{mat}_{B'}(u) =
    \begin{pmatrix}
    1 \\
    \frac{1}{2} \\
    0
    \end{pmatrix}
    \]

    ---

    ### 示例 2  
    在 \( \mathbb{R}^4 \) 的标准基 \( C \) 下，向量  
    \[
    v = (1, -4, 3, 1)
    \]
    的矩阵表示为：  
    \[
    \text{mat}_C(v) =
    \begin{pmatrix}
    1 \\
    -4 \\
    3 \\
    1
    \end{pmatrix}
    \]

    ---

    ### 示例 3  
    设 \( E \) 是一个 \( K \) 上的向量空间，配备基 \( B = (e_1, e_2, e_3, e_4) \)。若向量 \( u \in E \) 满足：  
    \[
    \text{mat}_B(u) =
    \begin{pmatrix}
    1 \\
    -1 \\
    2 \\
    0
    \end{pmatrix}
    \]
    则 \( u \) 在基 \( B \) 下展开为：  
    \[
    u = e_1 - e_2 + 2e_3
    \]



!!! note "Proposition"            

    === "Contenu"                      
        **命题 17.1.1**  

        设 \( E \) 是一个 \( K \)-向量空间，且 \( n \geq 1 \) 为一整数。假设 \( E \) 存在一组基  
        \[ B = (e_1, \dots, e_n). \]  
        设 \( m \geq 1 \) 为一整数，且 \( u_1, \dots, u_m \in E \)。则：  

        1. 族 \( (u_1, \dots, u_m) \) 线性无关当且仅当族 \( (\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \) 线性无关。  
        2. 族 \( (u_1, \dots, u_m) \) 生成 \( E \) 当且仅当族 \( (\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \) 生成 \( M_{n,1}(K) \)。  
        3. 对任意 \( k \in \mathbb{N} \)，对于所有不同的指标 \( i_1, \dots, i_k \in \{1, \dots, m\} \)，子族 \( (u_{i_1}, \dots, u_{i_k}) \) 是 \( \text{vect}(u_1, \dots, u_m) \) 的一组基当且仅当族 \( (\text{mat}_B(u_{i_1}), \dots, \text{mat}_B(u_{i_k})) \) 是 \( \text{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \) 的一组基。  

    === "Démonstration"                      
        1. 设 \( m \geq 1 \)，且 \( u_1, \dots, u_m \in E \)。由于 \( 0_E = 0 \cdot e_1 + \dots + 0 \cdot e_n \)，可知  
        \[
        \text{mat}_B(0_E) = 0_{n,1}.
        \]  
        通过以下等价关系可得结论：  
        
        \[
        \text{族 } (u_1, \dots, u_m) \text{ 线性无关}
        \]  
        \[
        \iff \forall (\lambda_1, \dots, \lambda_m) \in K^m, \lambda_1 u_1 + \dots + \lambda_m u_m = 0_E \Rightarrow \lambda_1 = \dots = \lambda_m = 0
        \]  
        \[
        \overset{\text{习题 17.1.1 (4) }}{\iff} \forall (\lambda_1, \dots, \lambda_m) \in K^m, \text{mat}_B(\lambda_1 u_1 + \dots + \lambda_m u_m) = \text{mat}_B(0_E) \Rightarrow \lambda_1 = \dots = \lambda_m = 0
        \]  
        \[
        \iff \forall (\lambda_1, \dots, \lambda_m) \in K^m, \text{mat}_B(\lambda_1 u_1 + \dots + \lambda_m u_m) = 0_{n,1} \Rightarrow \lambda_1 = \dots = \lambda_m = 0
        \]  
        \[
        \overset{\text{习题 17.1.1 (3) }}{\iff} \forall (\lambda_1, \dots, \lambda_m) \in K^m, \lambda_1 \text{mat}_B(u_1) + \dots + \lambda_m \text{mat}_B(u_m) = 0_{n,1} \Rightarrow \lambda_1 = \dots = \lambda_m = 0
        \]  
        \[
        \iff \text{族 } (\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \text{ 线性无关}.
        \]  

        2. 设 \( u_1, \dots, u_m \in E \)，我们采用双向推理：  

        **\( \Rightarrow \) 方向：** 假设族 \( (u_1, \dots, u_m) \) 是一组生成集。对于任意  
        \[
        X =
        \begin{pmatrix}
        x_1 \\ \vdots \\ x_n
        \end{pmatrix}
        \in M_{n,1}(K),
        \]  
        我们证明 \( X \in \text{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \)。设  
        \[
        u = x_1 e_1 + \dots + x_n e_n. \quad \quad (17.1)
        \]  
        由于假设 \( \text{vect}(u_1, \dots, u_m) = E \)，存在 \( \lambda_1, \dots, \lambda_m \in K \) 使得  
        \[
        u = \lambda_1 u_1 + \dots + \lambda_m u_m. \quad \quad (17.2)
        \]  
        由 (17.1) 可知 \( X = \text{mat}_B(u) \)，由 (17.2) 及习题 17.1.1 (3) 可得  
        \[
        \text{mat}_B(u) = \lambda_1 \text{mat}_B(u_1) + \dots + \lambda_m \text{mat}_B(u_m),
        \]  
        因此  
        \[
        X \in \text{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)).
        \]  
        由此可得，族 \( (\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \) 生成。  

        **\( \Leftarrow \) 方向：** 假设族 \( (\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \) 是一组生成集，则对于任意 \( u \in E \)，由假设  
        \[
        \text{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) = M_{n,1}(K),
        \]  
        存在 \( \lambda_1, \dots, \lambda_m \in K \) 使得  
        \[
        \text{mat}_B(u) = \lambda_1 \text{mat}_B(u_1) + \dots + \lambda_m \text{mat}_B(u_m).
        \]  
        由习题 17.1.1 (3) 可得  
        \[
        \text{mat}_B(u) = \text{mat}_B(\lambda_1 u_1 + \dots + \lambda_m u_m),
        \]  
        再由习题 17.1.1 (4) 可得  
        \[
        u = \lambda_1 u_1 + \dots + \lambda_m u_m.
        \]  
        这意味着 \( u \in \text{vect}(u_1, \dots, u_m) \)，即族 \( (u_1, \dots, u_m) \) 也是生成集。  

        3. 设 \( u_1, \dots, u_m \in E \)，且 \( k \in \mathbb{N} \)。设 \( i_1, \dots, i_k \in \{1, \dots, m\} \) 为互不相同的指标。  

        由 (1) 可知，族 \( (u_{i_1}, \dots, u_{i_k}) \) 线性无关当且仅当族 \( (\text{mat}_B(u_{i_1}), \dots, \text{mat}_B(u_{i_k})) \) 线性无关。  

        通过类似 (2) 的推理，可得族 \( (u_{i_1}, \dots, u_{i_k}) \) 生成 \( \text{vect}(u_1, \dots, u_m) \) 当且仅当族 \( (\text{mat}_B(u_{i_1}), \dots, \text{mat}_B(u_{i_k})) \) 生成 \( \text{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \)。  

        综上所述，结论成立。     





### 命题 17.1.2  
设 \( n \geq 1 \) 为整数。则在 \( M_{n,1}(K) \) 中，任何包含 \( n+1 \) 个向量的族都是线性相关的。  

#### 证明  
我们使用数学归纳法对 \( n \) 进行证明。  

**基例（初始情况）**：设 \( (u, v) \) 是 \( M_{1,1}(K) \) 中的两个向量，我们区分两种情况：  
- **情况 1**：若 \( u = 0 \)，则有线性关系：
  \[
  1 \cdot u + 0 \cdot v = 0_{1,1}
  \]
  这表明 \( (u, v) \) 是线性相关的。  
- **情况 2**：若 \( u \neq 0 \)，则 \( u \) 仅有的系数 \( x \in K \) 是非零的，设 \( v \) 的唯一系数为 \( y \in K \)，则
  \[
  \frac{y}{x} \cdot u + (-1) \cdot v = 0_{1,1}
  \]
  这表明 \( (u, v) \) 仍然是线性相关的。  

**归纳假设**：假设对于某个 \( n \geq 1 \)，\( M_{n,1}(K) \) 中的任何 \( n+1 \) 个向量的族都是线性相关的。  

**归纳步骤**：我们需要证明 \( M_{n+1,1}(K) \) 中的任何 \( n+2 \) 个向量的族也是线性相关的。  

设 \( u_1, \dots, u_{n+2} \) 是 \( M_{n+1,1}(K) \) 中的向量：
\[
u_1 =
\begin{pmatrix}
x_{1,1} \\
x_{2,1} \\
\vdots \\
x_{n+1,1}
\end{pmatrix}, \quad
\dots, \quad
u_{n+2} =
\begin{pmatrix}
x_{1,n+2} \\
x_{2,n+2} \\
\vdots \\
x_{n+1,n+2}
\end{pmatrix}
\]
我们再次区分两种情况：  

- **情况 1**：所有向量的最后一个分量均为 0，即：
  \[
  u_1 =
  \begin{pmatrix}
  x_{1,1} \\
  x_{2,1} \\
  \vdots \\
  x_{n,1} \\
  0
  \end{pmatrix}, \quad
  \dots, \quad
  u_{n+2} =
  \begin{pmatrix}
  x_{1,n+2} \\
  x_{2,n+2} \\
  \vdots \\
  x_{n,n+2} \\
  0
  \end{pmatrix}
  \]
  忽略最后一个分量后，我们得到 \( M_{n,1}(K) \) 中的 \( n+2 \) 个向量：
  \[
  v_1 =
  \begin{pmatrix}
  x_{1,1} \\
  x_{2,1} \\
  \vdots \\
  x_{n,1}
  \end{pmatrix}, \quad
  \dots, \quad
  v_{n+2} =
  \begin{pmatrix}
  x_{1,n+2} \\
  x_{2,n+2} \\
  \vdots \\
  x_{n,n+2}
  \end{pmatrix}
  \]
  根据归纳假设，\( (v_1, \dots, v_{n+2}) \) 是线性相关的，即存在 \( \lambda_1, \dots, \lambda_{n+2} \in K \)，使得：
  \[
  \lambda_1 v_1 + \dots + \lambda_{n+2} v_{n+2} = 0_{n,1}
  \]
  这意味着：
  \[
  \lambda_1 u_1 + \dots + \lambda_{n+2} u_{n+2} = 0_{n+1,1}
  \]
  由此可知，\( (u_1, \dots, u_{n+2}) \) 是线性相关的。  

- **情况 2**：至少有一个向量的最后一个分量非零。我们假设 \( u_{n+2} \) 满足 \( x_{n+1,n+2} \neq 0 \)，其它情况类似处理。对所有 \( i = 1, \dots, n+1 \)，定义：
  \[
  w_i = u_i - \frac{x_{n+1,i}}{x_{n+1,n+2}} u_{n+2}
  \]
  构造的向量 \( w_1, \dots, w_{n+1} \) 的最后一个分量都是 0，因此它们在 \( M_{n,1}(K) \) 中定义了向量 \( v_1, \dots, v_{n+1} \)。根据归纳假设，这些向量是线性相关的，即存在非全为零的 \( \lambda_1, \dots, \lambda_{n+1} \) 使得：
  \[
  \lambda_1 v_1 + \dots + \lambda_{n+1} v_{n+1} = 0_{n,1}
  \]
  由此可得：
  \[
  \sum_{i=1}^{n+1} \lambda_i w_i = 0_{n+1,1}
  \]
  代入 \( w_i \) 的表达式：
  \[
  \sum_{i=1}^{n+1} \lambda_i \left( u_i - \frac{x_{n+1,i}}{x_{n+1,n+2}} u_{n+2} \right) = 0_{n+1,1}
  \]
  展开后：
  \[
  \sum_{i=1}^{n+1} \lambda_i u_i - \left( \sum_{i=1}^{n+1} \lambda_i \frac{x_{n+1,i}}{x_{n+1,n+2}} \right) u_{n+2} = 0_{n+1,1}
  \]
  记
  \[
  \lambda_{n+2} = - \sum_{i=1}^{n+1} \lambda_i \frac{x_{n+1,i}}{x_{n+1,n+2}}
  \]
  由于 \( \lambda_1, \dots, \lambda_{n+1} \) 不全为零，因此 \( (\lambda_1, \dots, \lambda_{n+2}) \) 也不全为零，这表明 \( (u_1, \dots, u_{n+2}) \) 是线性相关的。  

由此归纳证明完成。

---

### 命题 17.1.3  
设 \( E \) 是一个 \( K \) 上的向量空间，且 \( n, m \geq 1 \) 为整数。设  
\[
e_1, \dots, e_n, f_1, \dots, f_m \in E
\]
如果 \( (e_1, \dots, e_n) \) 和 \( (f_1, \dots, f_m) \) 都是 \( E \) 的基，则有 \( n = m \)。

**证明**：  
假设 \( n \neq m \)，且 \( m > n \)。在基 \( B = (e_1, \dots, e_n) \) 下，\( (f_1, \dots, f_{n+1}) \) 的矩阵表示：
\[
\text{mat}_B(f_1), \dots, \text{mat}_B(f_{n+1})
\]
根据命题 17.1.2，这些向量是线性相关的，从而 \( (f_1, \dots, f_m) \) 也是线性相关的，矛盾。因此 \( n = m \)。




**命题 17.1.2**  
设 \( n \geq 1 \) 为整数，则任意 \( n+1 \) 个属于 \( M_{n,1}(K) \) 的向量构成的族都是线性相关的。  

**证明**  
我们对 \( n \) 进行数学归纳法证明。  

**初始情况**：  
设 \( (u, v) \) 是 \( M_{1,1}(K) \) 中的两个向量，我们分以下两种情况讨论：  
- 如果 \( u = 0 \)，则有线性关系：
  \[
  1 \cdot u + 0 \cdot v = 0_{1,1}
  \]
  说明 \( (u, v) \) 线性相关。  
- 如果 \( u \neq 0 \)，设 \( u \) 唯一的系数为 \( x \neq 0 \)，设 \( v \) 的唯一系数为 \( y \)，则有：
  \[
  \frac{y}{x} \cdot u + (-1) \cdot v = 0_{1,1}
  \]
  说明 \( (u, v) \) 线性相关。  

**归纳假设**：  
设 \( n \geq 1 \)，假设 \( M_{n,1}(K) \) 中任意 \( n+1 \) 个向量构成的族都是线性相关的，我们需要证明对于 \( M_{n+1,1}(K) \)，任意 \( n+2 \) 个向量构成的族也是线性相关的。  

设 \( u_1, \dots, u_{n+2} \in M_{n+1,1}(K) \)，其中：
\[
u_i =
\begin{pmatrix}
x_{1,i} \\
x_{2,i} \\
\vdots \\
x_{n+1,i}
\end{pmatrix}
\]
其中 \( x_{j,i} \in K \)。我们分两种情况讨论：  

1. **情况 1**：所有向量的最后一个分量均为零，即：
   \[
   u_i =
   \begin{pmatrix}
   x_{1,i} \\
   x_{2,i} \\
   \vdots \\
   x_{n,i} \\
   0
   \end{pmatrix}, \quad i = 1, \dots, n+2.
   \]
   去掉最后一个分量后，得到 \( n+2 \) 个 \( M_{n,1}(K) \) 中的向量：
   \[
   v_i =
   \begin{pmatrix}
   x_{1,i} \\
   x_{2,i} \\
   \vdots \\
   x_{n,i}
   \end{pmatrix}, \quad i = 1, \dots, n+2.
   \]
   由归纳假设，\( (v_1, \dots, v_{n+2}) \) 是线性相关的，即存在不全为零的 \( \lambda_1, \dots, \lambda_{n+2} \in K \) 使得：
   \[
   \lambda_1 v_1 + \dots + \lambda_{n+2} v_{n+2} = 0_{n,1}.
   \]
   在 \( M_{n+1,1}(K) \) 中，我们有：
   \[
   \lambda_1 u_1 + \dots + \lambda_{n+2} u_{n+2} =
   \begin{pmatrix}
   0 \\
   0 \\
   \vdots \\
   0 \\
   0
   \end{pmatrix} = 0_{n+1,1}.
   \]
   这表明 \( (u_1, \dots, u_{n+2}) \) 是线性相关的。  

2. **情况 2**：至少有一个向量的最后一个分量不为零。假设 \( u_{n+2} \) 满足 \( x_{n+1, n+2} \neq 0 \)（其他情况类似）。对所有 \( i \in \{1, \dots, n+1\} \)，定义：
   \[
   w_i = u_i - \frac{x_{n+1,i}}{x_{n+1,n+2}} u_{n+2}.
   \]
   由定义，\( w_1, \dots, w_{n+1} \) 的最后一个分量均为零。去掉最后一个分量后，得到 \( n+1 \) 个 \( M_{n,1}(K) \) 中的向量 \( v_1, \dots, v_{n+1} \)，由归纳假设，它们是线性相关的，即存在不全为零的 \( \lambda_1, \dots, \lambda_{n+1} \in K \) 使得：
   \[
   \lambda_1 v_1 + \dots + \lambda_{n+1} v_{n+1} = 0_{n,1}.
   \]
   注意到：
   \[
   \sum_{i=1}^{n+1} \lambda_i w_i = 0_{n+1,1}
   \]
   即：
   \[
   \sum_{i=1}^{n+1} \lambda_i \left( u_i - \frac{x_{n+1,i}}{x_{n+1,n+2}} u_{n+2} \right) = 0_{n+1,1}.
   \]
   展开后得：
   \[
   \sum_{i=1}^{n+1} \lambda_i u_i - \left( \sum_{i=1}^{n+1} \lambda_i \frac{x_{n+1,i}}{x_{n+1,n+2}} \right) u_{n+2} = 0_{n+1,1}.
   \]
   由于 \( \lambda_1, \dots, \lambda_{n+1} \) 不是全零，因此：
   \[
   \lambda_1, \dots, \lambda_{n+1}, - \sum_{i=1}^{n+1} \lambda_i \frac{x_{n+1,i}}{x_{n+1,n+2}}
   \]
   不是全零，因此 \( (u_1, \dots, u_{n+2}) \) 线性相关。  

**命题 17.1.3**  
设 \( E \) 是一个 \( K \)-向量空间，设 \( n \geq 1 \) 和 \( m \geq 1 \) 为两个整数。设：
\[
e_1, \dots, e_n, f_1, \dots, f_m \in E.
\]
如果 \( (e_1, \dots, e_n) \) 和 \( (f_1, \dots, f_m) \) 均是 \( E \) 的基，则 \( n = m \)。  

**证明**  
反证法。假设 \( n \neq m \)，不失一般性，设 \( m > n \)。考虑向量 \( (f_1, \dots, f_{n+1}) \) 在基 \( B = (e_1, \dots, e_n) \) 下的坐标：
\[
\operatorname{mat}_B(f_1), \dots, \operatorname{mat}_B(f_{n+1}).
\]
由命题 17.1.2，\( M_{n,1}(K) \) 中的 \( n+1 \) 个向量线性相关，因此 \( (f_1, \dots, f_{n+1}) \) 线性相关，与基的定义矛盾。因此 \( n = m \)。  

**注记**  
因此，在一个具有基大小为 \( n \geq 1 \) 的 \( K \)-向量空间中，所有基的大小均为 \( n \)。此外，唯一大小为零的族是空集 \( \emptyset \)，它是零空间 \( \{0_E\} \) 的基。由于任何包含 \( 0_E \) 的族都是线性相关的，因此空集是 \( \{0_E\} \) 的唯一基。




### **定义 17.1.2：维数**  
设 \( E \) 是一个 \( K \)-向量空间。  

— 如果 \( E \) 存在大小为 \( n \) 的基，其中 \( n \) 为某个自然数 \( n \in \mathbb{N} \)，则称 \( E \) 为**有限维** \( K \)-向量空间，整数 \( n \) 称为 \( E \) 的**维数**，记作 \( \dim_K(E) \) 或 \( \dim(E) \)。  
— 如果 \( E \) 没有任何有限大小的基，则称 \( E \) 为**无限维** \( K \)-向量空间，记作 \( \dim_K(E) = \infty \) 或 \( \dim(E) = \infty \)。  

### **示例**  
— 对于所有 \( n \geq 1 \)，\( K^n \) 的**标准基**包含 \( n \) 个向量，因此：  
  \[
  \dim(K^n) = n.
  \]  
  同样地，  
— 对于所有整数 \( n \geq 1 \) 和 \( m \geq 1 \)，有：  
  \[
  \dim(M_{n,m}(K)) = nm.
  \]  
— 多项式环 \( K[X] \) 是无限维的，因此：  
  \[
  \dim(K[X]) = \infty.
  \]  
— 对于所有 \( n \in \mathbb{N} \)，记  
  \[
  K_n[X] = \{P \in K[X] \mid \deg P \leq n\},
  \]  
  则其维数为：  
  \[
  \dim(K_n[X]) = n + 1.
  \]  

---

### **定理 17.1.1（提取基）**  
设 \( E \) 是一个 \( K \)-向量空间。设 \( A \subset E \) 和 \( B \subset E \) 为两个子集，满足：  
- \( A \) 是**有限**且**线性无关**的；  
- \( B \) 是**有限**且**生成整个空间** \( E \) 的。  

则存在 \( C \subset B \)，使得 \( A \cup C \) 形成 \( E \) 的一个**基**。  

---

### **证明**  
我们分两种情况讨论：  

1. **情况 1**：如果 \( A \) 是一个生成集，则取 \( C = \emptyset \)，此时 \( A \cup C = A \) 本身已是 \( E \) 的一个基，结论成立。  

2. **情况 2**：如果 \( A \) 不是生成集，则 \( B \not\subset \text{vect}(A) \)（即 \( B \) 中至少有一个向量不在 \( A \) 生成的子空间中）。根据**命题 15.2.3**（第 15 章第 14 页），我们有等价关系：
   \[
   B \subset \text{vect}(A) \quad \Longleftrightarrow \quad \text{vect}(B) \subset \text{vect}(A).
   \]
   由于 \( B \) 生成整个 \( E \)，即 \( \text{vect}(B) = E \)，所以：
   \[
   B \subset \text{vect}(A) \quad \Longleftrightarrow \quad E \subset \text{vect}(A).
   \]
   因此，\( \text{vect}(A) \neq E \) 意味着 \( B \not\subset \text{vect}(A) \)。  
   这说明存在 \( u \in B \) 使得 \( u \notin \text{vect}(A) \)。  

   由于：
   - \( A \) 是**线性无关**的；  
   - \( u \notin \text{vect}(A) \)，  

   根据性质（17.5），可以得到：
   \[
   A \cup \{u\} \text{ 是线性无关的}。
   \]
   这意味着集合  
   \[
   \Omega = \{ C \subset B \mid A \cup C \text{ 是线性无关的} \}
   \]
   **非空**，因为 \( \{u\} \in \Omega \)。  

   现在，我们选择一个**最大**的集合 \( C \in \Omega \)（即 \( C \) 的**元素个数最大**）。  
   
   **为了证明结论，我们需验证 \( A \cup C \) 是生成集**。  

   我们采用**反证法**：假设 \( A \cup C \) 不是生成集，则存在 \( v \in B \) 使得：
   \[
   v \notin \text{vect}(A \cup C).
   \]
   由前述推理，可得：
   \[
   A \cup C \cup \{v\} \text{ 是线性无关的}。
   \]
   但这意味着 \( C \cup \{v\} \) 仍属于 \( \Omega \)，即：
   \[
   C \cup \{v\} \in \Omega.
   \]
   这与 \( C \) 是 \( \Omega \) 中**最大**的集合相矛盾！  

   因此，我们得出结论：\( A \cup C \) 必须是**生成集**，即形成 \( E \) 的一个**基**。  

---

### **注记**  
在特殊情况下，如果 \( A = \emptyset \)，则定理 17.1.1 通常表述为：  
> **从任何生成族中，都可以提取一个基。**  

此外，**有限维 \( K \)-向量空间的定义**可以表述为：  
> 一个有限维 \( K \)-向量空间是存在**某个有限生成且线性无关**的向量族的 \( K \)-向量空间。  

要证明一个向量空间是**有限维的**，定理 17.1.1 告诉我们：  
> **只要存在一个有限生成集，即可证明该向量空间是有限维的。**  

---

### **该定理的重要性**  
这个定理在很多数学领域都有重要应用，例如：  
- 证明所有有限维向量空间的基大小相等；  
- 研究线性代数中的秩-零空间定理；  
- 在抽象代数和泛函分析中，用于构造适当的基。





### **定理 17.1.2（不完整基）**  
设 \( E \) 是一个有限维 \( K \)-向量空间，维数 \( n \geq 1 \)。对任意 \( k \in \mathbb{N} \)，  
\( E \) 中的任意线性无关向量组 \( (e_1, \dots, e_k) \) 都可以补充成一个基：  
存在 \( e_{k+1}, \dots, e_n \in E \) 使得 \( (e_1, \dots, e_k, e_{k+1}, \dots, e_n) \) 是 \( E \) 的一个基。  

#### **证明**  
由于 \( E \) 是有限维的，其维数为 \( n \)，因此存在向量 \( f_1, \dots, f_n \in E \) 使得 \( (f_1, \dots, f_n) \) 是一个生成集。  
根据**定理 17.1.1（提取基）**，存在不重复的索引 \( i_{k+1}, \dots, i_n \in \{1, \dots, n\} \)，使得  
\[
(e_1, \dots, e_k, f_{i_{k+1}}, \dots, f_{i_n})
\]  
是 \( E \) 的一个基。  

---

### **命题 17.1.4**  
设 \( E \) 是一个有限维 \( K \)-向量空间，设 \( F \subset E \) 是一个子空间，则：  
1. \( \dim(F) \leq \dim(E) \)。  
2. 若且仅若 \( \dim(F) = \dim(E) \)，则 \( F = E \)。  

#### **证明**  
1. 设 \( B \) 是 \( F \) 的一个基，则 \( B \) 的大小等于 \( \dim(F) \)。由于 \( B \) 是 \( E \) 中的一个线性无关集，根据**不完整基定理 17.1.2**，我们可以向 \( B \) 添加一些向量，使其成为 \( E \) 的一个基。这样得到的基大小至少为 \( \dim(F) \)，因此有  
   \[
   \dim(E) \geq \dim(F).
   \]  

2. 方向“\( \Rightarrow \)”显然成立。我们用**反证法**证明“\( \Leftarrow \)”：  
   假设 \( F \) **严格包含于** \( E \)，即 \( F \neq E \)。设 \( B \) 是 \( F \) 的一个基，则有  
   \[
   \text{vect}(B) = F.
   \]  
   由于 \( F \neq E \)，\( B \) 不是 \( E \) 的一个生成集。根据**不完整基定理**，我们必须向 \( B \) 至少添加一个向量才能构成 \( E \) 的一个基。因此，\( E \) 的基大小至少为 \( \dim(F) + 1 \)，即  
   \[
   \dim(E) > \dim(F).
   \]  
   这与假设 \( \dim(F) = \dim(E) \) 矛盾，因此只能有 \( F = E \)。  

---

### **命题 17.1.5**  
设 \( E \) 是一个有限维 \( K \)-向量空间，维数 \( n \geq 1 \)。设 \( e_1, \dots, e_n \in E \) 是一些向量，则：  
1. 如果 \( (e_1, \dots, e_n) \) 是线性无关的，则它是 \( E \) 的一个基。  
2. 如果 \( (e_1, \dots, e_n) \) 是生成集，则它是 \( E \) 的一个基。  

#### **证明**  
1. 假设 \( (e_1, \dots, e_n) \) 线性无关。  
   注意到 \( (e_1, \dots, e_n) \) 是子空间 \( \text{vect}(e_1, \dots, e_n) \) 的一个生成集，因此它是该子空间的基，从而有  
   \[
   \dim(\text{vect}(e_1, \dots, e_n)) = n.
   \]  
   由于 \( \text{vect}(e_1, \dots, e_n) \subseteq E \) 且它的维数等于 \( \dim(E) \)，根据**命题 17.1.4**，可得  
   \[
   \text{vect}(e_1, \dots, e_n) = E.
   \]  
   也就是说，\( (e_1, \dots, e_n) \) 是 \( E \) 的一个生成集。因此，它是 \( E \) 的一个基。  

2. 假设 \( (e_1, \dots, e_n) \) 是生成集。  
   根据**定理 17.1.1（提取基）**，我们可以从其中选出一个子集 \( I \subset \{1, \dots, n\} \)，使得 \( (e_i)_{i \in I} \) 形成 \( E \) 的一个基。  
   如果 \( I \neq \{1, \dots, n\} \)，那么 \( E \) 存在一个基，其大小严格小于 \( \dim(E) \)，这显然是**矛盾的**。  
   因此，必须有 \( I = \{1, \dots, n\} \)，即 \( (e_1, \dots, e_n) \) 本身就是 \( E \) 的一个基。  

---

### **示例**  
复数域 \( \mathbb{C} \) 既是一个**实数向量空间**，也是一个**复数向量空间**，但其维数不同：  
\[
\dim_{\mathbb{R}}(\mathbb{C}) = 2, \quad \dim_{\mathbb{C}}(\mathbb{C}) = 1.
\]  
在这种情况下，我们必须明确指定标量域（即基础数域）才能确定维数。














## 2.Rangs et calcul matriciel



### **矩阵的列族在整个讨论中起着重要作用**  

对于矩阵  
\[
A =
\begin{pmatrix}  
1 & 1 & 2 & 0 \\  
2 & 0 & 1 & 0 \\  
4 & 1 & 0 & 0  
\end{pmatrix}  
\in M_{3,4}(K)
\]  
我们规定，写作  
\[
A =
\begin{pmatrix}  
C_1 & C_2 & C_3 & C_4  
\end{pmatrix}
\]  
表示我们称 \(C_1, C_2, C_3, C_4 \in M_{4,1}(K)\) 为矩阵 \(A\) 的列矩阵，其中：
\[
C_1 =
\begin{pmatrix}  
1 \\ 2 \\ 4  
\end{pmatrix},  
C_2 =
\begin{pmatrix}  
1 \\ 0 \\ 1  
\end{pmatrix},  
C_3 =
\begin{pmatrix}  
2 \\ 1 \\ 0  
\end{pmatrix},  
C_4 =
\begin{pmatrix}  
0 \\ 0 \\ 0  
\end{pmatrix}.
\]
对于任意大小的矩阵，我们使用类似的记号。

---

### **命题 17.2.1（矩阵运算的性质）**  
设 \( n \geq 1, m \geq 1, p \geq 1 \) 是三个正整数。  

1. 对于任意矩阵 \( M \in M_{n,m}(K) \)，若记作  
   \[
   M =
   \begin{pmatrix}  
   C_1 & \cdots & C_m  
   \end{pmatrix}
   \]
   并定义标准基向量  
   \[
   e_1 =
   \begin{pmatrix}  
   1 \\ 0 \\ \vdots \\ 0  
   \end{pmatrix},  
   \ldots,  
   e_m =
   \begin{pmatrix}  
   0 \\ \vdots \\ 0 \\ 1  
   \end{pmatrix}
   \]
   其中 \((e_1, \dots, e_m)\) 是 \( M_{m,1}(K) \) 的标准基，则对于任意索引 \( j \in \{1, \dots, m\} \)，有：
   \[
   M e_j = C_j.
   \]

2. 对于任意矩阵 \( M \in M_{n,m}(K) \)，若记作  
   \[
   M =
   \begin{pmatrix}  
   C_1 & \cdots & C_m  
   \end{pmatrix},
   \]  
   那么对于任意标量 \( x_1, \dots, x_m \in K \)，在 \( M_{m,1}(K) \) 中：
   \[
   M
   \begin{pmatrix}  
   x_1 \\ x_2 \\ \vdots \\ x_m  
   \end{pmatrix}
   =
   \begin{pmatrix}  
   C_1 & \cdots & C_m  
   \end{pmatrix}
   \begin{pmatrix}  
   x_1 \\ x_2 \\ \vdots \\ x_m  
   \end{pmatrix}
   = x_1 C_1 + \cdots + x_m C_m.
   \]

3. 对于任意矩阵 \( A \in M_{n,m}(K) \)，\( B \in M_{m,p}(K) \)，若记作  
   \[
   B =
   \begin{pmatrix}  
   C_1 & \cdots & C_m  
   \end{pmatrix},
   \]
   则在 \( M_{n,p}(K) \) 中：
   \[
   AB = A
   \begin{pmatrix}  
   C_1 & \cdots & C_m  
   \end{pmatrix}
   =
   \begin{pmatrix}  
   AC_1 & \cdots & AC_m  
   \end{pmatrix}.
   \]
**证明**：这些性质直接来自矩阵加法和乘法的定义。  

> **注意**：此处的记号并非标准记号，建议在使用之前先说明其意义。

---

### **例子**  

\[
\begin{pmatrix}  
1 & 0 & 1 \\  
2 & 1 & 3  
\end{pmatrix}
\begin{pmatrix}  
1 \\ 0 \\ 0  
\end{pmatrix}
=
\begin{pmatrix}  
1 \\ 2  
\end{pmatrix},  
\]
\[
\begin{pmatrix}  
1 & 0 & 1 \\  
2 & 1 & 3  
\end{pmatrix}
\begin{pmatrix}  
0 \\ 1 \\ 0  
\end{pmatrix}
=
\begin{pmatrix}  
0 \\ 1  
\end{pmatrix},  
\]
\[
\begin{pmatrix}  
1 & 0 & 1 \\  
2 & 1 & 3  
\end{pmatrix}
\begin{pmatrix}  
0 \\ 0 \\ 1  
\end{pmatrix}
=
\begin{pmatrix}  
1 \\ 3  
\end{pmatrix}.
\]

---

### **矩阵向量乘法的例子**  

\[
\begin{pmatrix}  
2 & -1 \\  
4 & 0 \\  
1 & 1  
\end{pmatrix}
\begin{pmatrix}  
-3 \\ 2  
\end{pmatrix}
= -3
\begin{pmatrix}  
2 \\ 4 \\ 1  
\end{pmatrix}
+ 2
\begin{pmatrix}  
-1 \\ 0 \\ 1  
\end{pmatrix}
=
\begin{pmatrix}  
-8 \\ -12 \\ -1  
\end{pmatrix}.
\]

---

### **矩阵乘法的例子**  

\[
\begin{pmatrix}  
1 & 0 \\  
0 & 2 \\  
1 & 1 \\  
0 & 2  
\end{pmatrix}
\begin{pmatrix}  
1 & 0 & 4 & 0 \\  
-1 & 2 & -8 & 0  
\end{pmatrix}
=
\begin{pmatrix}  
1 & 0 & 4 & 0 \\  
-2 & 4 & -16 & 0 \\  
0 & 2 & -4 & 0 \\  
-2 & 4 & -16 & 0  
\end{pmatrix}.
\]

---

### **定义 17.2.1：一个向量族的秩**  
设 \( E \) 是一个 \( K \)-向量空间，\( F \) 是 \( E \) 中的一个向量族。那么由 \( F \) 中向量生成的子空间的维数被称为 \( F \) 的秩，记作：
\[
\text{rg}(F) = \dim(\text{vect}(F)).
\]

---

### **定义 17.2.2：矩阵的秩**  
设 \( n \geq 1 \), \( m \geq 1 \) 是两个正整数。对于任意矩阵  
\[
A =
\begin{pmatrix}  
C_1 & \cdots & C_m  
\end{pmatrix}
\in M_{n,m}(K),
\]
矩阵 \( A \) 的秩被定义为列向量族 \( (C_1, \dots, C_m) \) 在 \( M_{n,1}(K) \) 中的秩，记作：
\[
\text{rg}(A) = \dim(\text{vect}(C_1, \dots, C_m)).
\]



**定义 17.2.3：一组向量的表示矩阵**  

设 \( E \) 是一个维数为 \( n \geq 1 \) 的 \( K \)-向量空间，\( B \) 是 \( E \) 的一个基。设 \( m \geq 1 \) 为整数，令  
\[ F = (u_1, \dots, u_m) \]  
是一组 \( E \) 中的 \( m \) 个向量。矩阵 \( \text{mat}_B(F) \in M_{n,m}(K) \) 定义如下：  

\[
\text{mat}_B(F) =
\begin{pmatrix}
\text{mat}_B(u_1) & \cdots & \text{mat}_B(u_m)
\end{pmatrix}
\]

称其为**\( F \) 在基 \( B \) 下的表示矩阵**，也可记作 \( \text{mat}_B(u_1, \dots, u_m) \)。  

换句话说，对于每个 \( j \in \{1, \dots, m\} \)，矩阵 \( \text{mat}_B(F) \) 的第 \( j \) 列包含向量 \( u_j \) 在基 \( B \) 下的坐标。  

---

**命题 17.2.2（对基的选择无关性）**  

设 \( E \) 是一个维数为 \( n \geq 1 \) 的 \( K \)-向量空间，\( B \) 是 \( E \) 的一个基，\( F \) 是 \( E \) 中的一个有限向量组，则有：  
\[
\operatorname{rg}(F) = \operatorname{rg}(\text{mat}_B(F))
\]  

**证明**：  
设  
\[
B = (e_1, \dots, e_n), \quad F = (u_1, \dots, u_m)
\]  
其中 \( m \geq 1 \)，且 \( e_1, \dots, e_n \in E \)，\( u_1, \dots, u_m \in E \)。设 \( k = \operatorname{rg}(F) \)，即：  
\[
\operatorname{rg}(F) = \dim(\operatorname{vect}(u_1, \dots, u_m)),
\]
\[
\operatorname{rg}(\text{mat}_B(F)) = \dim(\operatorname{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m))).
\]  
由**定理 17.1.1（基的提取）**，可以选择一个整数 \( k \) 及 \( k \) 个互不相同的索引 \( i_1, \dots, i_k \in \{1, \dots, m\} \)，使得向量组  
\[
(u_{i_1}, \dots, u_{i_k})
\]  
构成 \( \operatorname{vect}(u_1, \dots, u_m) \) 的一组基。  

根据**命题 17.1.1**（第 3 页），向量组  
\[
(\text{mat}_B(u_{i_1}), \dots, \text{mat}_B(u_{i_k}))
\]  
构成 \( \operatorname{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m)) \) 的一组基。因此，  
\[
\dim(\operatorname{vect}(\text{mat}_B(u_1), \dots, \text{mat}_B(u_m))) = k.
\]  
最终得出：  
\[
\operatorname{rg}(\text{mat}_B(F)) = k = \operatorname{rg}(F).
\]  

---

**注释**  

习题 17.1.1（第 2 页）和命题 17.1.1（第 3 页）的一种理解方式如下：在维数 \( n \geq 1 \) 的 \( K \)-向量空间中进行推理和计算，本质上等同于在 \( M_{n,1}(K) \) 中进行推理和计算。  

类似地，命题 17.2.2 说明：计算一个维数为 \( n \geq 1 \) 的 \( K \)-向量空间中 \( m \geq 1 \) 个向量的秩，本质上等同于计算一个 \( M_{n,m}(K) \) 矩阵的秩。





**命题 17.2.3（基变换公式）**  

设 \( E \) 是一个维数为 \( n \geq 1 \) 的 \( K \)-向量空间，且 \( B \) 和 \( B' \) 是 \( E \) 的两个基。  
1. 对于任意向量 \( u \in E \)，有：  
\[
\text{mat}_{B'}(B) \, \text{mat}_B(u) = \text{mat}_{B'}(u)
\]
2. 对于任意有限向量组 \( F = (u_1, \dots, u_m) \)，有：  
\[
\text{mat}_{B'}(B) \, \text{mat}_B(F) = \text{mat}_{B'}(F)
\]

**证明**  

1. 设 \( u \in E \)，令 \( B = (e_1, \dots, e_n) \)，\( B' = (e_1', \dots, e_n') \)，  
\[
\text{mat}_{B'}(B) = \begin{pmatrix} a_{1,1} & \dots & a_{1,n} \\ \vdots & \ddots & \vdots \\ a_{n,1} & \dots & a_{n,n} \end{pmatrix}, \quad
\text{mat}_B(u) = \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix}, \quad
\text{mat}_{B'}(u) = \begin{pmatrix} x_1' \\ \vdots \\ x_n' \end{pmatrix} \in M_{n,1}(K)
\]
根据 \( \text{mat}_{B'}(B) \)、\( \text{mat}_B(u) \)、\( \text{mat}_{B'}(u) \) 的定义，  
有  
\[
u = x_1 e_1 + \dots + x_n e_n \tag{17.7}
\]  
和  
\[
u = x_1' e_1' + \dots + x_n' e_n' \tag{17.8}
\]  
对于每个 \( i \in \{1, \dots, n\} \)，有：  
\[
e_i = a_{i,1} e_1' + \dots + a_{i,n} e_n' \tag{17.9}
\]  
从 (17.7) 开始，使用 (17.9) 可以写成：  
\[
u = x_1 (a_{1,1} e_1' + \dots + a_{n,1} e_n') + \dots + x_n (a_{1,n} e_1' + \dots + a_{n,n} e_n')
\]  
得到  
\[
u = (x_1 a_{1,1} + \dots + x_n a_{1,n}) e_1' + \dots + (x_1 a_{n,1} + \dots + x_n a_{n,n}) e_n' \tag{17.10}
\]  
由向量在基中的唯一表示性，(17.8) 和 (17.10) 说明：  
对于所有 \( i \in \{1, \dots, n\} \)，  
\[
x_1 a_{i,1} + \dots + x_n a_{i,n} = x_i'
\]  
即，矩阵乘积 \( \text{mat}_{B'}(B) \, \text{mat}_B(u) \) 等于 \( \text{mat}_{B'}(u) \)。

2. 这个结果是第一个结论以及命题 17.2.1（第 11 页）的直接结果。

---

**命题 17.2.4**  

设 \( E \) 是一个维数为 \( n \geq 1 \) 的 \( K \)-向量空间，且 \( B \) 和 \( B' \) 是 \( E \) 的两个基，则矩阵 \( \text{mat}_{B'}(B) \in M_n(K) \) 是可逆的，且其逆矩阵是 \( \text{mat}_B(B') \)。

**证明**：  
根据命题 17.2.3，第 2 点，  
\[
\text{mat}_B(B') \, \text{mat}_{B'}(B) = \text{mat}_B(B)
\]  
令 \( B = (e_1, \dots, e_n) \)，则有：  
\[
e_1 = 1 \cdot e_1 + 0 \cdot e_2 + \dots + 0 \cdot e_n, \quad \dots, \quad e_n = 0 \cdot e_1 + \dots + 0 \cdot e_{n-1} + 1 \cdot e_n
\]  
因此，  
\[
\text{mat}_B(e_1) = \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix}, \dots, \text{mat}_B(e_n) = \begin{pmatrix} 0 \\ \vdots \\ 0 \\ 1 \end{pmatrix}
\]  
即，\( \text{mat}_B(B) \)，即 \( \text{mat}_B(e_1, \dots, e_n) \)，是单位矩阵 \( I_n \in M_n(K) \)。同样，可以证明  
\[
\text{mat}_{B'}(B) \, \text{mat}_B(B') = \text{mat}_{B'}(B') = I_n
\]  
因此，矩阵 \( \text{mat}_{B'}(B) \in M_n(K) \) 是可逆的，且其逆矩阵是 \( \text{mat}_B(B') \)。

---

**命题 17.2.5**  

设 \( n \geq 1 \) 是一个整数，\( m \geq 1 \) 是另一个整数，\( F = (u_1, \dots, u_m) \) 是 \( K^n \) 中的一组 \( m \) 个向量。则 \( F \) 是线性无关的当且仅当 \( \operatorname{rg}(F) = m \)。

**证明**：  
我们通过双向推理来证明：  
\( \Rightarrow \) 假设 \( (u_1, \dots, u_m) \) 是线性无关的。因为 \( (u_1, \dots, u_m) \) 是 \( \operatorname{vect}(u_1, \dots, u_m) \) 的一组生成元，所以它是 \( \operatorname{vect}(u_1, \dots, u_m) \) 的一组基，因此  
\[
\dim(\operatorname{vect}(u_1, \dots, u_m)) = m
\]  
而且 \( \operatorname{rg}(F) = \dim(\operatorname{vect}(u_1, \dots, u_m)) \)，因此 \( \operatorname{rg}(F) = m \)。

\( \Leftarrow \) 假设 \( \operatorname{rg}(F) = m \)，即  
\[
\dim(\operatorname{vect}(u_1, \dots, u_m)) = m
\]  
因为 \( (u_1, \dots, u_m) \) 是 \( \operatorname{vect}(u_1, \dots, u_m) \) 的一组生成元，所以根据命题 17.1.5（第 8 页），我们得出 \( (u_1, \dots, u_m) \) 是 \( \operatorname{vect}(u_1, \dots, u_m) \) 的一组基。因此，\( (u_1, \dots, u_m) \) 是线性无关的。

---

**命题 17.2.6**  

设 \( n \geq 1 \) 是一个整数，\( m \geq 1 \) 是另一个整数，\( F = (u_1, \dots, u_m) \) 是 \( K^n \) 中的一组 \( m \) 个向量。则 \( F \) 是生成元当且仅当 \( \operatorname{rg}(F) = n \)。

**证明**：  
通过双向推理来证明：  
\( \Rightarrow \) 假设 \( (u_1, \dots, u_m) \) 是生成元。则  
\[
\operatorname{vect}(u_1, \dots, u_m) = K^n
\]  
因此  
\[
\dim(\operatorname{vect}(u_1, \dots, u_m)) = n
\]  
而且 \( \operatorname{rg}(F) = \dim(\operatorname{vect}(u_1, \dots, u_m)) \)，因此 \( \operatorname{rg}(F) = n \)。

\( \Leftarrow \) 假设 \( \operatorname{rg}(F) = n \)，即  
\[
\dim(\operatorname{vect}(u_1, \dots, u_m)) = n
\]  
因为 \( \operatorname{vect}(u_1, \dots, u_m) \) 是 \( K^n \) 的子空间，而 \( \dim(K^n) = n \)，所以根据命题 17.1.4（第 8 页），我们得出  
\[
\operatorname{vect}(u_1, \dots, u_m) = K^n
\]  
因此，\( (u_1, \dots, u_m) \) 是生成元。  

---

**注释**  
通过组合前两个命题，我们得出，对于任何整数 \( n \geq 1 \)，对于 \( K^n \) 中的任意 \( n \) 个向量的有限组 \( F = (u_1, \dots, u_n) \)，如果 \( F \) 是 \( K^n \) 的基，当且仅当 \( \operatorname{rg}(F) = n \)。此时，\( K^n \) 可以替换为任何维数为 \( n \geq 1 \) 的 \( K \)-向量空间。


**命题 17.2.7**。设 \( n \geq 1 \) 为整数，定义

\[
M = 
\begin{pmatrix}
C_1 & \cdots & C_n
\end{pmatrix} \in M_n(K)
\]
为一个方阵。以下条件是等价的：

1. \( M \) 可逆；
2. \( M \) 的列 \( C_1, \dots, C_n \) 构成 \( M_{n,1}(K) \) 的一组基；
3. \( \text{rg}(M) = n \)。

**证明：**

**1 ⇒ 2**：假设 \( M \) 是可逆的。设 \( M^{-1} = 
\begin{pmatrix}
D_1 & \cdots & D_n
\end{pmatrix}
\)。令 \( e_1, \dots, e_n \) 为 \( M_{n,1}(K) \) 的标准基，其中

\[
e_1 = \begin{pmatrix} 1 \\ 0 \\ \vdots \\ 0 \end{pmatrix}, \quad e_n = \begin{pmatrix} 0 \\ \vdots \\ 0 \\ 1 \end{pmatrix}。
\]

由 \( MM^{-1} = I_n \)，可以写成：

\[
M \begin{pmatrix} D_1 & \cdots & D_n \end{pmatrix} = \begin{pmatrix} e_1 & \cdots & e_n \end{pmatrix}。
\]

进一步根据 **命题 17.2.1 第 3 条**，有：

\[
MD_1 = e_1, \dots, MD_n = e_n \quad \text{(公式 17.11)}。
\]

另一方面，根据 **命题 17.2.1 第 2 条**，对任意 \( i \in \{1, \dots, n\} \)，有

\[
MD_i \in \text{vect}(C_1, \dots, C_n) \quad \text{(公式 17.12)}。
\]

由 \( MD_1 = e_1, \dots, MD_n = e_n \) 和 \( MD_i \in \text{vect}(C_1, \dots, C_n) \)，可以推得

\[
e_1, \dots, e_n \in \text{vect}(C_1, \dots, C_n)，
\]

因此 \( \text{vect}(e_1, \dots, e_n) \subset \text{vect}(C_1, \dots, C_n) \)。由于 \( \text{vect}(e_1, \dots, e_n) = M_{n,1}(K) \)，可以得出 \( (C_1, \dots, C_n) \) 是 \( M_{n,1}(K) \) 的一组生成元。由于 \( \dim(M_{n,1}(K)) = n \)，根据 **命题 17.1.5 第 2 条**，可以得出 \( (C_1, \dots, C_n) \) 是 \( M_{n,1}(K) \) 的一组基。

**2 ⇒ 3**：如果 \( C_1, \dots, C_n \) 是 \( M_{n,1}(K) \) 的一组基，则 \( \text{rg}(M) = \dim(\text{vect}(C_1, \dots, C_n)) = \dim(M_{n,1}(K)) = n \)。

**3 ⇒ 1**：假设 \( \text{rg}(M) = n \)。即 \( \dim(\text{vect}(C_1, \dots, C_n)) = n \)。由于 \( (C_1, \dots, C_n) \) 是 \( \text{vect}(C_1, \dots, C_n) \) 的一组生成元，因此根据 **命题 17.1.4 第 2 条**，可以得出 \( \text{vect}(C_1, \dots, C_n) = M_{n,1}(K) \)。特别地，\( (C_1, \dots, C_n) \) 是 \( M_{n,1}(K) \) 的一组基。

如果记 \( C = (C_1, \dots, C_n) \) 为 \( M_{n,1}(K) \) 的标准基，则

\[
M = \begin{pmatrix} C_1 & \dots & C_n \end{pmatrix} = \text{mat}_C(C_1, \dots, C_n) = \text{mat}_C(B)。
\]

根据 **命题 17.2.4**，可以得出 \( M \) 是可逆的，且其逆矩阵为 \( \text{mat}_B(C) \)。

**备注：**

在特殊情况下，对于 \( 2 \times 2 \) 矩阵

\[
A = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \in M_2(K),
\]

其行列式定义为 \( \det(A) = ad - bc \)，并且有以下准则：

- \( A \) 可逆当且仅当 \( \det(A) \neq 0 \)。

**例子：**

以下矩阵不是可逆的：

\[
\begin{pmatrix} 1 & 5 \\ 10 & 50 \end{pmatrix}, \quad
\begin{pmatrix} -1 & 5 \\ -1 & 6 \\ 5 & 6 \end{pmatrix}, \quad
\begin{pmatrix} 6 & -6 \\ -2 & 2 \end{pmatrix}, \quad
\begin{pmatrix} 0 & 2 \\ 0 & 2 \end{pmatrix}, \quad
\begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}.
\]

以下矩阵是可逆的：

\[
\begin{pmatrix} 1 & 5 \\ 10 & 49 \end{pmatrix}, \quad
\begin{pmatrix} -1 & 5 \\ -1 & 6 \\ 5 & 12 \end{pmatrix}, \quad
\begin{pmatrix} 6 & 6 \\ -2 & 2 \end{pmatrix}, \quad
\begin{pmatrix} 1 & 2 \\ 0 & 2 \end{pmatrix}, \quad
\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}.
\]

**例子：**

对于任何 \( \theta \in \mathbb{R} \)，定义矩阵

\[
R_\theta = \begin{pmatrix} \cos(\theta) & -\sin(\theta) \\ \sin(\theta) & \cos(\theta) \end{pmatrix} \in M_2(\mathbb{R}),
\]

它是可逆的，因为

\[
\det(R_\theta) = \cos^2(\theta) + \sin^2(\theta) = 1 \neq 0。
\]

接下来的三个结果在接下来的证明中会用到。虽然它们不必须立即了解，但它们是有用的。需要注意的是，对于任意整数 \( n \geq 1 \)，\( GL_n(K) \subset M_n(K) \) 表示可逆矩阵的集合。




**命题 17.2.8**。设 \( E \) 是一个有限维 \( K \)-向量空间，维数为 \( n \geq 1 \)，并且 \( M \in GL_n(K) \)。对于任意 \( E \) 的基 \( B \)，存在一个唯一的基 \( B' \) 使得 \( M = \text{mat}_{B'}(B) \)。

**证明**：

后续只使用存在性，但通过以下分析-综合的推理可以得到唯一性。设 \( B = (e_1, \dots, e_n) \) 是 \( E \) 的基。

**分析**：假设存在 \( B' = (f_1, \dots, f_n) \) 使得 \( M = \text{mat}_{B'}(B) \)。那么 \( M^{-1} = \text{mat}_B(B') \)。对于任意 \( j \in \{1, \dots, n\} \)， \( M^{-1} \) 的第 \( j \) 列给出了 \( f_j \) 在基 \( B \) 中的坐标，即

\[
f_j = \sum_{i=1}^n M^{-1}_{i,j} e_i \quad (17.13)。
\]

如果 \( B' \) 存在，(17.13) 显示了 \( B' \) 完全由 \( M \) 和 \( B \) 决定，这也就证明了唯一性。

**综合**：根据 (17.13) 设定 \( f_1, \dots, f_n \)。根据定义，

\[
M^{-1} = \begin{pmatrix} \text{mat}_B(f_1) & \cdots & \text{mat}_B(f_n) \end{pmatrix} \quad (17.14)。
\]

根据 **命题 17.2.7**，由于 \( M^{-1} \) 是可逆的，\( M^{-1} \) 的列 \( \text{mat}_B(f_1), \dots, \text{mat}_B(f_n) \) 形成 \( M_{n,1}(K) \) 的一组基。根据 **命题 17.1.1**，可以得出 \( B' = (f_1, \dots, f_n) \) 是 \( E \) 的一组基。根据 (17.14)，有 \( M^{-1} = \text{mat}_B(B') \)。因此，存在性得以证明。

**命题 17.2.9**。设 \( E \) 是一个有限维 \( K \)-向量空间，维数为 \( n \geq 1 \)，并且 \( B \) 是 \( E \) 的基。设 \( F \) 是 \( E \) 中的一个有限向量集。对于任意可逆矩阵 \( M \in GL_n(K) \)，存在一个基 \( B' \)，使得

\[
M \, \text{mat}_B(F) = \text{mat}_{B'}(F)。
\]

**证明**：根据 **命题 17.2.8**，设 \( B' \) 为 \( E \) 的基，使得 \( M = \text{mat}_{B'}(B) \)。则

\[
M \, \text{mat}_B(F) = \text{mat}_B(B) \, \text{mat}_B(F) = \text{mat}_{B'}(F)。
\]

**命题 17.2.10**。设 \( n \geq 1 \) 为整数，且 \( M \in GL_n(K) \)，\( N \in M_n(K) \)。则有 \( \text{rg}(MN) = \text{rg}(N) \)。

**证明**：设 \( C_1, \dots, C_n \in M_{n,1}(K) \) 为 \( N \) 的列向量。如果 \( C \) 是 \( M_{n,1}(K) \) 的标准基，则

\[
N = \begin{pmatrix} C_1 & \cdots & C_n \end{pmatrix} = \text{mat}_C(C_1, \dots, C_n)。
\]

根据 **命题 17.2.9**，选择 \( M_{n,1}(K) \) 的一组基 \( B \)，使得 \( M = \text{mat}_B(C) \)。则

\[
MN = \text{mat}_B(C) \, \text{mat}_C(C_1, \dots, C_n) = \text{mat}_B(C_1, \dots, C_n)。
\]

根据 **命题 17.2.2**，得出

\[
\text{rg}(MN) = \text{rg}(\text{mat}_B(C_1, \dots, C_n)) = \text{rg}(C_1, \dots, C_n) = \text{rg}(\text{mat}_C(C_1, \dots, C_n)) = \text{rg}(N)。
\]















## 3.Calcul matriciel et applications

### 3.1 Matrices échelonnées, matrices échelonnées réduites

### 3.2 Famille libre, famille génératrice, base

### 3.3 Changement de bases

### 3.4 Relation de dépendance linéaire

### 3.5 Passage d’un système d’équations à une famille génératrice

### 3.6 Passage d’une famille génératrice à un système d’équations

## 4.Sommes et supplémentaire

