## Markdown
### 表格
- 表格前后留空，才能形成表格
- `:---`左对齐
- `---:`右对齐
- `:---:` 居中

### 数学表达式

#### 希腊字母表

|             |     lower     |   upper    |       notes       |
| :---------: | :-----------: | :--------: | :---------------: |
|   \alpha    |   $\alpha$    |            |                   |
|    \beta    |    $\beta$    |            |                   |
|   \gamma    |   $\gamma$    |  $\Gamma$  |                   |
|   \delta    |   $\delta$    |  $\Delta$  |                   |
|  \epsilon   |  $\epsilon$   |            |        不常用        |
| \varepsilon | $\varepsilon$ |            |        常用         |
|    \zeta    |    $\zeta$    |            |                   |
|    \eta     |    $\eta$     |            |                   |
|   \theta    |   $\theta$    |  $\Theta$  |      有var版本       |
|   \kappa    |   $\kappa$    |            |                   |
|   \lambda   |   $\lambda$   | $\Lambda$  |                   |
|     \mu     |     $\mu$     |            |                   |
|     \nu     |     $\nu$     |            |        尖底         |
|     \xi     |     $\xi$     |   $\Xi$    |                   |
|     \pi     |     $\pi$     |   $\Pi$    |                   |
|    \rho     |    $\rho$     |            |                   |
|   \sigma    |   $\sigma$    |  $\Sigma$  | var版本：$\varsigma$ |
|    \tau     |    $\tau$     |            |                   |
|  \upsilon   |  $\upsilon$   | $\Upsilon$ |      圆底，用于速度      |
|    \phi     |    $\phi$     |   $\Phi$   |                   |
|   \varphi   |   $\varphi$   |            |                   |
|    \chi     |    $\chi$     |            |                   |
|    \psi     |    $\psi$     |   $\Psi$   |                   |
|   \omega    |   $\omega$    |  $\Omega$  |                   |

#### 箭头符号
><a href=https://blog.csdn.net/Sugar_wolf/article/details/130085570>markdown箭头汇总</a>| 

|          语法           |         符号         |         例子          |
| :-------------------: | :----------------: | :-----------------: |
|    方向+arrow，大写为双线     |    \\Rightarrow    |    $\Rightarrow$    |
|      相反方向对+arrow      |    \Updownarrow    |   $\Updownarrow$    |
|        long加长         |                    |                     |
|          n否定          |   \\nRightarrow    |   $\nRightarrow$    |
| circlearrow+方向`无大写用法` | \\circlearrowright | $\circlearrowright$ |
|  ne,nw,se,sw`无大写用法`   |     \\nearrow      |     $\nearrow$      |

#### 公式格式
- `$ $`行内公式
- `$$ $$`公式块

- `\\`换行
- `&`表示上下对齐
- 空格
	- `\qquad`两宽
	- `\quad`一宽
	- `\ `1/3宽
	- `\;`
	- `\,`
	- `\!`紧贴，缩进1/6宽

- 取消斜体`\rm`
- 向量印数体$\mathbf{a}$`\mathbf{}`
- 方框`\boxed{}`$$\begin{aligned}\boxed{x^2+y^2=z^2}\end{aligned}$$

- `\begin{}`与`\end{}`
	- {aligned}`最基本的对齐环境`
	- 环境（大括号）`{cases}`参考示例：<br>`$$y=\begin{cases}-x,\quad x\leq0\\x,\quad x\geq0\end{cases}$$`$$y=\begin{cases}-x,\quad x\leq0\\x,\quad x\geq0\end{cases}$$
	- 矩阵$$\begin{bmatrix}1&2&3\\4&567&8.91\\7&8&9\end{bmatrix}$$
		- `matrix`无括号
		- 要加小括号需要使用`\left`和`\right`
		- `bmatrix`中括号
		- `Bmatirx`大括号
		- `vmatrix`竖线
		- `Vmatrix`双竖线
- 定界符`\left`和`\right`中间用括号包括

- 省略号
	- `\cdots` `\vdots``\ddots`分别横竖斜.$$\begin{bmatrix}a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\vdots&\vdots&\ddots&\vdots\\a_{n1}&a_{n2}&\cdots&a_{nn}\end{bmatrix}$$

#### 基本计算符号
- 上角`^`，下角标`_`
- 分数`\frac{}{}`
- 开方`sqrt[]{}`
- 加减`\pm`
- 点乘`\cdot`
- 乘`\times`
- 除`\div`
#### 积分计算符号
- 积分`\int^{b}_{a}{f(x)}{\rm d}x`$$\int^{b}_{a}{f(x)}{\rm d}x$$
- 二重积分`\iint`参考积分
- 无穷`\infty`
- 极限`\lim_{}{}`$$\lim_{n\to +\infty}{\frac{x_{n+1}}{x_n}}=1$$
- `\prime`一阶导数`要加 ^`
- `\oint`曲线积分
- `\nabla`梯度
- `\partial`偏导

#### 其他计算符号
- 累加`\sum_{}^{}{}`$$\sum^{n}_{i=1}{a_i}$$
- 累乘`\prod`用法和累加类似

#### 小标
- `\dot`加点
- `\ddot`加双点
- `\hat`加帽
- `\widehat`加宽帽
- `\tilde`波浪号
- `\vec`向量
- `\bar`平均
- `\overbrace`与`\underbrace`$$\overbrace{a+ \underbrace{b+c}_{1.0}+d}^{2.0}$$
- `\bot`垂直
- `\angle`角
- `\circ`圆，与次方连用表示度
- `\odot`$\odot$
- `\otimes`$\otimes$
- `\triangle`$\triangle$

#### 不等式
- `\ll`远小于
- `\gg`远大于
- `\leq`小于等于
- `geq`大于等于
- `\approx`约等于
- `neq`不等于

#### 集合与关系
- `\varnothong`空集
- `\in`属于
- `\notin`不属于
- `\subset`子集于
- `\supset`父集于
- `\cup`并集
- `\cap`交集

#### 命题
- `\because`
- `\therefore`
- `\forall`任意
- `\exist`存在

### 插入
插入图片
`![alt](path "title")`
![afterClass](images/afterClass.jpg)
## HTML
### 基本知识
- 标签通常成对出现
#### 基本结构
`<!DOCTYPE html>`声明为HTML5文档
`<html>`html根元素
`<head>`包含了文档的元(meta)数据，如`<meta charset="utf-8>"`定义网页编码格式为utf-8
`<title>`描述文档标题
`<body>`可视页面部分
#### 段落
- `<h>`标题，有1-6可选
- `<p>`段落
- `<hr>`分割线
- `<!--something--> `注释
- `<br>`换行

#### \<img>
`<img src="url" alt="some text" width="nub" height="unb" >`
- `obsidian中可能无法显示`
<img src="./images/afterClass.jpg" alt="after class">

#### <\a>
`<a href="url">something<\a>`
<a href="https://www.bing.com">微软必应</a>

#### \<iframe>
`<iframe src="path" width="nub" height="nub">something</iframe>`