# 集合

## 标准集

* **自然数**
  $$
  \N = \set{1,2,3,4,5,\dots}
  $$
  注意： $0 \notin \N$

* 对于任意 $n \in \N$ ，集合 $[n]$ （“**中括号** $n$ ”）定义为：
  $$
  [n] = \set{x \in \N\ \:|\: 1 \le x \le n} = \set{1,2,3,\dots,n}
  $$

* **整数**
  $$
  \Z = \set{\dots,-3,-2,-1,0,1,2,3,\dots}
  $$

* **有理数**
  $$
  \Q = \Set{x \in \R \:|\: \exists a,b \in \Z. b \ne 0 \:\text{且}\: \frac{a}{b}=x}
  $$

* **实数**用 $\R$ 表示。任何一个实数要么是**有理数**要么是**无理数**。

* **空集**是没有元素的集合。写作 $\emptyset$ 或 $\set{\:}$

## 集合构建符号

* 如果 $U$ 是一个集合，$P(x)$ 是对任意给定 $x$ 成立或不成立的某种**属性**，那么我们总是可以通过如下方式定义一个新集合：
  $$
  S = \set{x \in U \:|\: \text{具有}P(x)}
  $$

* 此为集合构建符号。必须包含**全集** $U$ 和**属性** $P(x)$。

## 元素和子集

* “$x$ 是集合 $S$ 的元素”，可以写做
  $$
  x \in S
  $$
  “$x$ 不是集合 $S$ 的元素”，可以写做
  $$
  x \notin S
  $$

* “$S$ 是 $T$ 的子集”，可以写做
  $$
  S \sube T
  $$
  这是由条件语句“$S$ 的每个元素也是 $T$ 的元素”定义的。可以表示为
  $$
  \forall x \in U \sdot x \in S \implies x \in T
  $$
  即，对于全集（假设$S,T \sube U$）中的每个元素 $x$，只要 $x \in S$，我们就知道 $x\in T$。

* 要证明一个集合是另一个集合的子集，比如 $S \sube T$，我们需要这样做
  $$
  \text{设} x \in S \text{是任意且固定的}\\
  \dots \text{此处是证明过程（略）}\dots\\
  \text{所以}x \in T\\
  \text{因此}S \sube T
  $$

* “$S$ 是 $T$ 的真子集”，可以写做
  $$
  S \subset T
  $$
  这意味着 $S \sube T$ 且 $S \ne T$。

* 空集是任意集合的子集，即 $\forall S,\emptyset \sube S$ 。

* 任意集合都是其本身的子集，即 $\forall S, S \sube S$ 。

## 幂集

* 设 $S$ 是一个集合，$S$ 的幂集记作 $\mathcal{P}(S)$，其定义如下：
  $$
  \mathcal{P}(S) = \set{A \:|\: A \sube S}
  $$
  即，$\mathcal{P}(S)$ 是 $S$ 所有子集的集合。

* 对于任意集合 $S$，空集 $\emptyset \in \mathcal{P}(S)$ 且  $S\in \mathcal{P}(S)$ 。

## 集合相等

* “集合 $S$ 和集合 $T$ 相等”，我们写作 $S=T$，定义为
  $$
  S = T \enspace\text{当且仅当} \enspace S \sube T \:\text{且}\: T \sube S\\
  S=T \iff S \sube T \:\text{且}\: T \sube S
  $$

* 要**证明**两个集合相等，比如 $S=T$，我们需要这么做：
  $$
  \text{首先，我们证明}S \sube T\\
  \text{设} x \in S \text{是任意且固定的}\\
  \dots \text{此处是证明过程（略）}\dots\\
  \text{所以}x \in T\\
  \text{因此}S \sube T\\
  \\
  \text{接着，我们证明}T \sube S\\
  \text{设} y \in T \text{是任意且固定的}\\
  \dots \text{此处是证明过程（略）}\dots\\
  \text{所以}y \in S\\
  \text{因此}T \sube S\\
  \\
  \text{因此}S = T\\
  $$
  这被称为双重遏制论证.

## 集合操作

设 $S,T,U$ 是三个集合，且 $S \sube U, T \sube U$。

* 两个集合的**并集**定义为
  $$
  S \cup T = \set{x \in U \:|\: x \in S \:\text{或}\: x \in T}
  $$
  即至少属于两个集合 $S$ 和 $T$ 之一的所有元素的集合。

* 两个集合的**交集**定义为
  $$
  S \cap T = \set{x \in U \:|\: x \in S \:\text{且}\: x \in T}
  $$
  即同时属于两个集合 $S$ 和 $T$ 的所有元素的集合。

* 两个集合的**差集**定义为
  $$
  S - T = \set{x \in U \:|\: x \in S \:\text{且}\: x \notin T}
  $$
  即所有属于 $S$ 但不属于 $T$ 的元素的集合。

* 集合的**补集**定义为
  $$
  \bar{S} = \set{x\in U \:|\: x \notin S}=U-S
  $$
  即全集中所有不属于 $S$ 的元素的集合。

* 两个集合的**笛卡尔积**定义为
  $$
  S \times T = \set{(x,y) \:|\: x \in S \:\text{且}\: y \in T}
  $$
  即所有有序对的集合，其中第一个坐标是 $S$ 的元素，第二个坐标是 $T$ 的元素。

## 索引集操作

假设 $I$ 是一个索引集，$U$ 是全集，我们已经定义了（对于每个 $i \in I$）一些集合 $A_i \sube U$。

* 所有 $A_i$ 集的**索引并集**定义为
  $$
  \bigcup_{i \in I}A_i = \set{x \in U \:|\: \exists k \in I. x \in A_k}
  $$
  即全集中所有元素 $x$ 的集合，使得 $x$ 是并集中至少一个索引集合的元素。

* 所有 $A_i$ 集的**索引交集**定义为
  $$
  \bigcap_{i \in I}A_i = \set{x \in U \:|\: \forall i \in I.x \in A_i}
  $$
  即全集中所有元素 $x$ 的集合，使得 $x$ 是交集中所有索引集合的元素。

## 分割

* 设 $S$ 是一个集合，$S$ 的分割是成对不相交且并集为 $S$ 的集合的集合。也就是说，分割由索引集 $I$ 和满足以下条件的非空集 $S_i$（为每个 $i \in I$ 定义）构成：
  $$
  \forall i \in I.S_i \ne \emptyset\\
  \forall i \in I.S_i \subset S\\
  \forall i,j \in I. i \ne j \implies S_i \cap S_j = \emptyset\\
  \bigcup_{i \in I} S_i= S
  $$
  

