# 第一章 集合与映射
## 集合 
#### 常用集合  
| 全体正整数         | 全体整数 | 全体有理数 | 全体实数 |
| ------------- | ---- | ----- | ---- |
| N<sub>+</sub> | Z    | Q     | R    |
#### 集合运算  
- 求差：`两个集合S和T的差是由属于S但不属于T的元素组成的集合，记作S\T`  
- 对偶律`（De Morgan公式）`:<br>$$(A\cup B)^C=A^C\cap B^C$$$$(A\cap B)^C=A^C\cup B^C$$
#### 有限集与不限集  
- 无限集
	- 可列集
	- 不可列集

## 映射与函数
#### 映射
设X，Y是两个给定的集合，若按照某种规则f，使得对集合X中的每一个元素x，都可以找到集合Y中唯一确定的元素y唯一与之对应，则称这个对应规则f是集合X到集合Y的一个**映射**，记为<br>$$f:X\rightarrow Y$$$$x\mapsto y=f(x)$$
y称为x的**像**，x称为**逆像** *(也叫原像)*，集合X称为**定义域**，记为D<sub>f</sub>=X .像y的全体称为**值域**，记为R<sub>f</sub>.`注：集合Y与值域不完全重合。`
- f的逆像也具有唯一性，则为**单射**
- R<sub>f</sub>=Y则为**满射**
- 既是单射，又是满射，则为**双射** `一一对应`
- 现有映射$$g:X\rightarrow U_f,x\mapsto u=g(x)和$$$$f:U_2\rightarrow Y,u\mapsto y=f(u)$$如果$$R_g\subset U_2=D_f$$则有$$f\circ g:X\rightarrow Y$$$$x\mapsto y=f(g(x))$$称为复合映射。
- 两个函数不仅函数关系相同，而且定义域也相同时，他们表示的是相同的函数。
#### 平均值
`调和平均数`$$n/(\frac{1}{a_1}+\frac{1}{a_2}+...+\frac{1}{a_n})$$
`平均值不等式`$$\frac{a_1+a_2+...+a_n}{n}\geq \sqrt{a_1+a_2+...+a_n}\geq n/(\frac{1}{a_1}+\frac{1}{a_2}+...+\frac{1}{a_n})$$
# 数列极限  
## 实数系的连续性  
#### 实数系  
有理数集合Q的元素可以用$$\frac{q}{p}(p\in N^+,q\in Z)$$表示.
整数集Z具有**离散型**，有理数集Q具有**稠密性**，实数集R具有**连续性**。
#### 上确界与下确界
`上确界`$$\forall m\geq f(x),m\in U;\beta=\min U,\beta=\sup U$$
`下确界`$$\forall n\leq f(x),n\in U;\alpha = \max U,\alpha =\inf U$$
## 数列极限  
- 唯一性
- 有界性
- 保序性
- 夹逼性`若`$$x_n\leq y_n\leq z_n,n\geq N_0;\lim\limits_{n\rightarrow\infty}x_n=\lim\limits_{n\rightarrow\infty}y_n=\lim\limits_{n\rightarrow\infty}z_n=a$$`则`$$\lim\limits_{n\rightarrow\infty}z_n=a$$

- 收敛数列的极限必唯一
- 收敛数列必有界

### stolz 定理  
`若`$$\{y_n\}是严格单调增加的正无穷大量，且\lim\limits_{n\rightarrow\infty}\frac{x_n-x_{n-1}}{y_n-y_{n-1}}=a(a可以是有限量或无穷量)$$
`则`$$\lim\limits_{n\rightarrow\infty}\frac{x_n}{y_n}=a$$
## 收敛准则
- 单调有界数列必收敛
