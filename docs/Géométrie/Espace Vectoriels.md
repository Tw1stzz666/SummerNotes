# Espace vectoriels

## 1.Espace vectoriels

<div class="grid cards" markdown>

-   **Définition: Espace Vectoriel** 

    ---

    给定域 $\mathbb{K},+_\mathbb{K},\times_\mathbb{k},0_\mathbb{K},1_\mathbb{K}$ ,和集合$E$, 具有以下两种运算          

    \[
        向量加法: E \times E \to E , (u,v) \mapsto u+v
    \]        

    \[
        标量乘法: \mathbb{K} \times E \to E , (\lambda,u) \mapsto \lambda \cdot u
    \]

    **$E$ 为定义在域 $\mathbb{K}$ 上的向量空间**           

</div>

!!! note "Propriétés" 
    * $(E,\times)$是交换群(阿贝尔群)            
    * $\forall u \in E, \forall (\lambda,\mu) \in \mathbb{K}^2, (\lambda \times _ \mathbb{k} \mu) \cdot u=\lambda \cdot (\mu \cdot u)$, 即满足结合律
    * $\forall u \in E, 1_\mathbb{K} \cdot u=u$, 即有单位元
    * $\forall (u,v) \in E^2, \forall \lambda \in \mathbb{K}, \lambda \cdot (u+v)=\lambda \cdot u+\lambda \cdot v$, 即对向量加法的分配律
    * $\forall u \in E, \forall (\lambda ,\mu ) \in \mathbb{K}^2, (\lambda +_\mathbb{k} \mu)*u=\lambda \cdot u+\mu \cdot u$, 即对域加法的分配律

$E$ 中的元素被称为向量, $0_E \in (E,\times)$ 被称为零向量                    
$\mathbb{K}$中的元素被称为标量         

!!! note "Proposition"            

    === "Contenu"                    
        对于域 $\mathbb{K}$ , 整数 $n \ge 1$ , 集合 $\mathbb{K}^n={(x_1,...,x_n)|x_1 \in \mathbb{k},...,x_n \in \mathbb{k}}$ 具有两种运算:                 

        \[
            \forall (x_1,...,x_n) \in \mathbb{k}^2, \forall (y_1,...,y_n) \in \mathbb{k}^2, (x_1,...,x_n)+(y_1,...,y_n)=(x_1+y_1,...,x_n+y_n)
        \]            
    
        \[
            \forall (x_1,...,x_n) \in \mathbb{k}^2, \forall \lambda \in \mathbb{k}, \lambda \cdot (x_1,...,x_n)=(\lambda x_1,...,\lambda x_n)
        \]                 

        即满足向量加法和标量乘法              
        ** $\mathbb{k}^n$ 是在域 $\mathbb{K}$ 上的向量空间**        
             
    === "Démonstration"                      
        依次证明 $+$ 满足结合律, 交换律, 单位元, 逆元, 及 $(\mathbb{K}^n,+)$ 是阿贝尔群

??? example "Exemples"
    * 对于实数集, 可以看成是在实数域上的向量空间: $标量 \cdot 向量 = 2 \cdot 3 = 1 \cdot 6 = 6 = 向量$   
    更进一步说, 若 $\mathbb{K}$ 是 $\mathbb{L}$ 的子域, 则 $\mathbb{L}$ 是在 $\mathbb{K}$ 上的向量空间
    * 同样的, 对于多项式, 矩阵, 函数以及数列都可以构造这样的向量空间

<div class="grid cards" markdown>

-   **Définition: Sous-espace Vectoriel**

    ---

    若 $E$ 是 $\mathbb{K}$ 上的向量空间, 且 $F \subset E$ , 那么我们称 $F$ 是 $E$ 的一个向量子空间, 当且仅当以下条件成立:                 
    1. $\forall (u,v) \in F^2, u+v \in F$ , 即对向量加法封闭              
    2. $\forall u \in F, \forall \lambda \in \mathbb{K}, \lambda \cdot u \in F$ , 即对标量乘法封闭                        
    3. $F$ 中的运算满足向量空间的性质                      

</div>

!!! note "Proposition"
    === "Contenu"
        以上定义中若 $F$ 满足对向量加法封闭, 对标量乘法封闭且 $0_E \in F$ , 则 $F$ 中的运算满足向量空间的性质
    === "Démonstration"
        显然, 容易证得 $F$ 为阿贝尔群, 从而可以得出向量空间的五个性质成立

!!! note "Proposition(importante)"
    === "Contenu"
        以上定义中 $F$ 是 $E$ 的一个向量子空间, 当且仅当以下条件成立:                   
        1. $0_E \in F$                         
        2. $\forall (u,v) \in F^2, \forall \lambda \in \mathbb{K}, \lambda u+v \in F$          
    === "Démonstration"
        前一个性质的重新表述

??? example "Exemples"
    $E$ 是在 $\mathbb{K}$ 上的向量空间, $\{0_E\}$ 和 $E$ 本身是 $E$ 的向量子空间

!!! note "Proposition: Intersection des sous-espcaces vectoriels"
    === "Contenu"
        交集 $F$ 是 $E$ 的向量子空间                  

        \[                   
            F = \bigcap_{i \in I} F_i = \{u \in E | \forall i \in I, u \in F_i\}
        \]                      

        其中, $(F_i)$ 是 $E$ 的向量子空间
    === "Démonstration"
        $\forall i \in I, 0_E \in F_i$, 所以有 $0_E \in F$                          
        假设 $u,v \in F, \lambda \in \mathbb{K}, i \in I$, 有 $\forall i, \lambda u+v \in F_i$, 所以有 $\lambda u+v \in F$              
        由此得证            

## 2.Combinaisons linéaires

<div class="grid cards" markdown>

-   **Définition: Combinaison linéaire d'un nombre fini de vecteurs**

    ---

    $E$ 是在 $\mathbb{K}$ 上的向量空间, 假设 $u_1, u_2,..., u_n \in E$                    
    向量的线性组合具有以下形式：                                

    \[
        \lambda_1 u_1 + ... + \lambda_n u_n
    \]

    其中, $\lambda_1 ,..., \lambda_n \in \mathbb{K}$, $\lambda_1,...,\lambda_n$被称为系数

</div>

<div class="grid cards" markdown>

-   **Définition: Famille à support fini**

    ---

    $Card(\{i \in I | \lambda_i \ne 0_\mathbb{K}\})<+ \infty$ , 即仅有有限个 $\lambda_i$ 为零

</div>

<div class="grid cards" markdown>

-   **Définition: Combinaison linéaire**

    ---

    称形如:                     

    \[                
        v = \sum_{i \in I} \lambda_i u_i
    \]              
    
    的向量为 $(u_i)_{i \in \mathbb{I}}$ 的线性组合, 其中 $(\lambda_i)_{i \in I} \in \mathbb{K} ^ I$ 为上一个定义中的 “Famille à support fini”                             

</div>

!!! note "Proposition"
    === "Contenu"
        $E$ 的非空子集 $A$ , $A$ 中的所有线性组合所构成的集合 $vect(A)$ , 是 $E$ 的一个子向量空间
    === "Démonstration"
        - $0_E = \sum_{i \in I} 0_\mathbb{K} \cdot u_i$ , 有 $0_E \in vect(A)$
        - 设 $u = \sum_{i \in I} \lambda_i u_i , v = \sum_{j \in J} \nu_j v_j$ , $\lambda \in \mathbb{K}$ , 有 $\lambda u + v = \sum_{i \in I} (\lambda \lambda_i) u_i + \sum_{j \in J} \nu_j v_j$ , 形如以上定义中的线性组合, 故有 $\lambda u + v \in vect(A)$                
        故命题得证

<div class="grid cards" markdown>

-   **Définition: Sous-espace engendré par un ensemble de vecteurs**

    ---

    设 $A \in E$ , 我们称                              
    
    \[                                        
        vect(A)=\{ \lambda_1 u_1 +...+ \lambda_n u_n \in | n \in \mathbb{N} , \lambda_1,...,\lambda_n \in \mathbb{K} , u_1,...,u_n \in A \}
    \]                  

    为由 $A$ 所生成的 $E$ 的子向量空间                              

</div>

??? example "Exemples"
    $\mathbb{K}_n[X]=vect(1,X,X^2,...,X^n)$ 是 $\mathbb{K}[X]$ 的子向量空间, 其中 $n \in \mathbb{N}$

!!! note "Proposition"
    === "Contenu"
        假设 $A \in E$ , 我们记: 

        \[
            \mathcal{C} = \{ F \in E | A \in F 且 F 是 E 的子向量空间 \}
        \]

        那么, $vect(A) = \bigcup_{F \in \mathcal{C}} F$
    === "Démonstration"
        $\subset$ :                      
        设 $v \in vect(A)$, 整数 $n \geq 1$, $\lambda_1,..\lambda_n \in \mathbb{K}, u_1,...,u_n \in A$, 使得 $v = \lambda_1 u_1+...+\lambda_n u_n$, 因为子向量空间 $F \in E$ 使得 $A \in F$, 所以有 $u_1,...,u_n \in F$, 又因为向量空间的性质(对于标量乘法和向量加法封闭), 可以得出$v = \lambda_1 u_1+...+\lambda_n u_n \in F$, 所以有 $v \in \bigcup_{f \in \mathcal{C}} F$, 故有 $vect(A) \in \bigcup_{F \in \mathcal{C}} F$              
        $\supset$ :                           
        由定理, $vect(A) \in \mathcal{C}$, 所以 $\forall u \in \bigcup_{F \in \mathcal{C}} F$, 有 $u \in vect(A)$ , 故有 $vect(A) \ni \bigcup_{F \in \mathcal{C}} F$                      
        故命题得证

!!! note "Proposition"
    === "Contenu"
        假设 $A \in E$ , $F$ 是 $E$ 的子向量空间, 那么 $A \in F$ , 当且仅当 $vect(A) \in F$ 
    === "Démonstration"
        $F$ 是一个子向量空间, 那么 $F$ 对于"线性组合"是封闭的, 可马上得知此命题成立
        故命题得证

## 3.Familles de vecteurs
> 我们将探讨对于一个向量 $u$ 是否可以写成 $u = \sum_{i \in I} \lambda_i u_i$ 的形式                     

<div class="grid cards" markdown>

-   **Définition: Famille génératrice et partie génératrice**

    ---

    * 设 $(u_i)_{i \in I} \in E^I$, 若 $E = vect((u_i)_{i \in I})$, 则称 $(u_i)_{i \in I}$ 为 "Famille génératrice" ("生成族")                         
    
    * 设 $A \in E$, 若 $A$ 中的向量可以构成一个 "Famille génératrice", 则称 $A$ 为 "Partie génératrice" ("生成集合")

</div>

??? example "Exemples"
    * $u_1=(1,0,0), u_2=(0,1,0), u_3=(0,0,1)$, 易知 $\mathbb{R}^3 = vect(u_1,u_2,u_3)$, 则 $(u_1,u_2,u_3)$ 是 $\mathbb{R}^3$ 的 "Famille génératrice"
    * 同样的 $(v_1=(-1,0,0),v_2=(-1,-1,0),v_3=(-1,-1,-1))$ 也是 $\mathbb{R}^3$ 的 "Famille génératrice", 而 $(w_1=(2,0,1),w_2=(-1,0,1))$ 则不是
