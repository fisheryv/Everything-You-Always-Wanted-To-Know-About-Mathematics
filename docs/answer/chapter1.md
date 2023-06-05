# 第一章 习题解答

## 章节思考题

### 1.1.1 思考题

*如果给你三个正数 $a, b,c$, 它们满足 $a^2+b^2=c^2$，是否一定存在直角边长为 $a、b$、斜边长为 $c$ 的直角三角形？如果存在，您要如何构建它？如果不是，为什么不是呢？*

**证明：** 要证明 $a, b, c$ 是否构成直角三角形，需要分2步。

1. 证明 $a, b, c$ 能构成三角形；
2. 证明这个三角形是直角三角形。

<p align="center"><b>证明 a, b, c 构成三角形</b></p>

我们首先证明第 1 步：$a, b, c$ 能构成三角形。

我们知道构成三角形的充分必要条件是：三角形任意两边长度之和大于第三边。根据题目给定条件，我们很容易得到
$$
\because a^2+b^2=c^2\\
\therefore a^2+b^2+2ab>c^2\\
\therefore (a+b)^2>c^2\\
\because a, b, c \gt 0 \\
\therefore a+b>c \tag{1}
$$
上面我们得到 $a + b \gt c$，我们还需要证明 $a+c \gt b$ 和 $b+c \gt a$。
$$
\because a^2+b^2=c^2 \quad (a, b, c \gt 0)\\
\therefore a^2 \lt c^2\\
\therefore a^2 \lt c^2 +2bc +b^2\\
\therefore a^2 \lt (c+b)^2\\
\therefore a \lt c+b\\
\therefore c+b \gt a\tag{2}
$$
同理可证 
$$
a+c \gt b \tag{3}
$$
根据上面个证明（1）（2）（3）的结论，我们可以得到 **$a, b, c$ 构成一个三角形**，即：
$$
\begin{rcases}
   a+b \gt c \\
   a+c \gt b \\
   b+c \gt a \\
\end{rcases} \implies \vartriangle ABC
$$

$$
\ast\ast\ast
$$

<p align="center"><b>证明该三角形是直角三角形</b></p>

接下来我们证明这个三角形是直角三角形。

假设长度为 $a, b, c$ 的三边构成的不是直角三角型，那么有 2 中情况：要么是锐角三角形，要么是钝角三角型。

假设构成的是锐角三角形，如下图所示，我们可以过 $A$ 点，做 $b$ 边的垂线，与 $BC$ 的延长线交于 $D$ 点。

![](C:\Users\Jarod\GitHub\Everything-You-Always-Wanted-To-Know-About-Mathematics\docs\_media\ans1.1.1_2.png)

设 $CD$ 的长度为 $c'$，$AD$ 的长度为 $d$，则根据毕达哥拉斯定理，我们可以得到
$$
d^2+b^2 = (c+c')^2 \tag{4}
$$
根据 $\vartriangle ACD$ 我们可知 $a+c' \gt d$，将其带入上面的公式（4）可得 
$$
\begin{aligned}
(a+c')^2 + b^2 &\gt (c+c')^2 \\ 
a^2+2ac'+\cancel{(c')^2}+b^2 &\gt c^2+2cc'+\cancel{(c')^2}\\
a^2+2ac'+b^2 &\gt c^2+2cc'\\
\because a^2+b^2&=c^2 \\
\therefore \cancel{a^2}+2ac'+\cancel{b^2} &\gt \cancel{c^2}+2cc'\\
\therefore 2ac' &\gt 2cc' \\
\therefore a &\gt c
\end{aligned}
$$
上面的结论与
$$
a^2+b^2=c^2  \quad (a, b, c \gt 0)\\
a^2 \lt c^2\\
a \lt c
$$
矛盾，所以假设不成立，**$a, b, c$ 不构成锐角三角形**。

假设 $a, b, c$ 构成的是钝角三角形，如下图所示，我们可以过 $A$ 点，做 $b$ 边的垂线，与 $BC$ 交于 $D$ 点。

![](C:\Users\Jarod\GitHub\Everything-You-Always-Wanted-To-Know-About-Mathematics\docs\_media\ans1.1.1.png)

设 $CD$ 的长度为 $c_1$，$BD$ 的长度为 $c_2$，$AD$ 的长度为 $d$，则根据毕达哥拉斯定理，我们可以得到
$$
c_1+c_2=c\\
d^2+b^2=c_2^2=(c-c_1)^2 \tag{5}
$$
根据 $\vartriangle ACD$ 我们可知 $d+c_1 \gt a \implies d \gt a-c_1$，将其带入上面的公式（5）可得
$$
\begin{aligned}
(a-c_1)^2 +b^2 &\lt (c-c_1)^2\\
a^2 - 2ac_1 +\cancel{c_1^2} + b^2 &\lt c^2-2cc_1 +\cancel{c_1^2}\\
a^2 - 2ac_1 + b^2 &\lt c^2-2cc_1 \\
\because a^2+b^2&=c^2 \\
\therefore \cancel{a^2}-2ac_1 + \cancel{b^2}&\lt \cancel{c^2}-2cc_1\\
\therefore -2ac_1 &\lt -2cc_1 \\
\therefore a &\gt c
\end{aligned}
$$
上面结论与 $a \lt c$ 矛盾，所以假设不成立，**$a, b, c$ 不构成钝角三角形**。

综上，边长满足 $a^2+b^2=c^2$ 的三角形只能是直角三角形。$\blacksquare$

以上证明相当于证明了毕达哥拉斯定理的逆定理，结合毕达哥拉斯定理，我们可以得出 **边长满足 $a^2+b^2=c^2$ 是直角三角形的充分必要条件**。 
$$
a^2+b^2=c^2 \iff Rt\vartriangle
$$

### 1.1.3 思考题

*试着自己回答以下问题。 如果你的答案是“是”，试着找一个例子，如果你的答案是“否”，试着解释为什么不可能出现期望的情况。*

1. *是否存无理数 $a$ 和 $b$，其乘积 $a \cdot b$ 为有理数？*

   **答**：存在。例如 $a=\sqrt{2}, b=\sqrt{8}=2\sqrt{2}, a \cdot b = \sqrt{2} \times \sqrt{8} = \sqrt{16} = 4$。

2. *是否存在无理数 $a$ 和 $b$，其和 $a + b$ 为有理数？*

   **答**：存在。例如 $a=0.1010010001\dots$ ，每个1前0的个数依次增大，虽然这个数写法很有规律，但是无限不循环小数。$b = 0.8989989998\dots$，这样 $a+b = 0.\dot{9} = 1$。

3. *是否存在无理数 $a$ 和 $b$，其乘方 $a ^ b$ 为有理数？*

   **证明**：已知 $\sqrt{2}$ 是无理数，设 $x = \sqrt{2}^{\sqrt{2}}$，则有如下两种可能：

   * 如果 $x$ 为有理数，那么我们令 $a=\sqrt{2}, b=\sqrt{2}$，那么 $a^b = \sqrt{2}^{\sqrt{2}} = x $ 是个有理数；

   * 如果 $x$ 为无理数 ，那么我们令 $a=x=\sqrt{2}^{\sqrt{2}}, b=\sqrt{2}$，那么 
     $$
     a^b = \Big(\sqrt{2}^{\sqrt{2}}\Big)^{\sqrt{2}}=\sqrt{2}^{\sqrt{2} \cdot \sqrt{2}} = \sqrt{2}^2=2
     $$
     2是个有理数。 

   上述两种情况，我们都可以找到无理数 $a$ 和 $b$ 使得 $a^b$ 是有理数。 因此，必然存在这样一对数字。$\blacksquare$

## 练习题