Title: "随机事件和概率"
Date: 2016-05-15 20:44:00
Tags: probability
Category: mathematics
---

# 随机事件和事件的运算

## 随机实验
我们将随机现象的观察或观测称为随机实验,随机实验必须满足一下条件:
* 可重复性
* 可观察性
* 不确定性

## 样本空间

我们把一个随机实验的所有可能的结果称为这个随机实验的**样本空间**记为**S**.
每一个可能的取值称为**样本点**

1. $E_1$:抛一枚硬币，观察出现正面或者反面. 样本空间为:

    $S_1=\lbrace 正面, 反面 \rbrace$

2. $E_2$:掷一颗骰子, 观察出现的点数. 样本空间为:

    $S_2=\lbrace 1, 2, 3, 4, 5, 6\rbrace$

3. $E_3$:灯泡的寿命. 样本空间为:

    $S_3=\lbrace t | t \geq 0\rbrace$

从这3个例子可以发现$S_1$和$S_2$是离散的,$S_3$是连续的.
我们把随机实验的样本空间的子集称为**随机事件**,简称**事件**.
例如在上面例子$E_3$中, 假设寿命大于2000个小时的灯泡和合格产品，
那么所有满足这个条件的子集为一个事件，可以记为

$A=\lbrace t, t > 2000\rbrace = \lbrace 灯泡合格\rbrace$

只包含一个样本点的事件称为**基本事件**
样本空间S是自身的一个子集，在每次试验中它总是发生的，因此S也称为**必然事件**
同理空集$\varnothing$不可能发生，因此称为**不可能事件**

# 事件的关系和运算

## 事件的关系

同集合一样，事件直接也存在**等价**，**包含**等关系
1. 若 $A \subset B$, 则称时间B包含时间A, 如果A发生则B一定发生;
2. 若$A \subset B$ 且 $A \supset B$, 则A和B称相等,记着A = B;
3. 事件$A \cup B = \lbrace x | x \in A 或 x \in B\rbrace$称为A和B的和事件;
4. 事件$A \cap B = \lbrace x | x \in A 且 x \in B\rbrace$称为A和B的积事件;
5. 事件$A - B = \lbrace x | x \in A 且 x \notin B\rbrace$称为A和B的差事件;
6. 若 $A \cap B = \varnothing$, 则A和B称为互斥事件;
7. 若 $A \cup B = S$且$A \cap B = \varnothing$, 则称A和B互为逆事件;

## 事件的运算
既然事件是一个集合，那么事件满足所有集合的运算。事件的计算法则和集合相同



# 频率和概率

## 频率

**定义** 在相同条件下，进行n次试验，在这n次试验中，事件A发生的次数$n_A$
称为事件A发生的频数，比值$n_A/n$则称为事件A发生的**频率**记成$f_n(A)$

由定义，可以知频率有如下性质：
1.  $0 \leqslant f_n(A) \leqslant 1$;
2.  $f_n(S) = 1$;
3.  若$A_1, A_2, A_3,..., A_k$互为两两不相容事件,那么
    $f_n(A_1 \cup A_2 \cup A_3 \cup ...\cup A_k) = f_n(A_1) + f_n(A_2) + f_n(A_3) +...+ f_n(A_k)$

## 概率

**定义** 设E是**随机试验**, S是E的**样本空间**. 对于E的每一个事件A赋予一个实数,
记为P(A),称为事件A的**概率**,如果集合函数P()满足下列条件
1. **非负性**:对每一个事件A,有$P(A) \geqslant 0$;
2. **规范性**:对于必然事件S,有P(S) = 1
3. **可列可加性**: 设$A_1, A_2, ...$是两两不相容的事件，即对于
$A_i A_j = \varnothing i \neq j,i,j=1,2,...,$有:
    $P(A_1 \cup A_2 \cup A_3 \cup ...) = P(A_1)+P(A_2)+P(A_3) +...$

由定义可以知道，概率具有如下性质:
1. 不可能事件的概率:$P(\varnothing) = 0$
2. 有限可加. 若$A_1, A_2, A_3, ..., A_n$是两两不相容事件，那么有:
    $P(A_1 \cup A_2 \cup A_3 \cup ...\cup A_n) = P(A_1)+P(A_2)+P(A_3) +...+ P(A_n)$
3. 设A，B是两个事件，设有$A \subset B$,那么有:
    $P(B-A) = P(B) - P(A)$
    $P(B) \geqslant P(A)$
4. 逆事件的概率:$P(\bar{A}) = 1 - P(A)$
5. 加法公式:对任意两个事件有$P(A \cup A) = P(A) + P(B) - P(AB)$
