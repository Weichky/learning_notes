## 热力学第一定律

### 基本概念
- 热力学第零定律`与确定状态的第三系统达成热平衡的两个系统必定互为热平衡.`

系统
- 敞开
- 封闭
- 隔离

系统的性质
- 强度性质`与物质的量无关`
- 广延性质`与物质的量成正比`

状态函数
- 状态函数的改变量只与始终态有关，与途径无关.
- 状态函数的微小变化是全微分

热力学平衡态
- 热平衡
- 机械平衡
- 化学平衡
- 相平衡

热和功
热
- 吸正放负
功
- 体积功`因体积变化而做的功,符号W`
- 非体积功`符号W'`
- 得正做负

热和功与过程有关，微小变化应当写成$\delta Q$和$\delta W$,而不是$\rm dQ$和$\rm dW$

#### 体积功计算
$\delta W=-p_e{\rm d}V$
等温膨胀也要考虑途径，取决于外界压强

**可逆过程特点**
- 系统始终无限接近于平衡，处于准静态过程
- 过程无限缓慢
- $p_e=p_i\pm dp$ 推动力和阻力只差一个无限小
- 可逆过程系统做功最大，环境对系统做功最小

$$W=\int^{V_2}_{V_{1}}(p_i-{\rm d}p){\rm d}V=-nRT\ln\frac{V_2}{V_1}=-nRT\ln\frac{p_1}{p_2},\quad 其中p_i高次无穷小忽略$$

### 热力学能（内能）
系统内各种能量的总和，不包括系统整体的动能和势能.
Q和W都是过程相关量.

$$\Delta U=Q+W$$$${\rm d}U=\delta Q+\delta W$$
#### 等容热$Q_V$
$$\Delta U=Q_V$$
#### 等压热$Q_P$
$$H=U+pV$$
H称为焓，是一种状态函数，具有广度性质，属于能量单位.
$$Q_p=H_2-H_1=\Delta H$$
H是系统的状态性质，任意过程都有$$\Delta H=\Delta U+\Delta(pV)$$

#### 任意过程$\Delta H$的求算
- 理想气体变温过程$$pV=nRT,\quad\Delta H=\Delta U+nR\Delta T$$
- 相变过程（恒温恒压）若始态为凝聚相，终态为气相，则$$\Delta(pV)\approx pV_2=nRT,\quad\Delta H=\Delta U+nRT$$
- 化学反应过程（恒温恒压）$$\Delta(pV)=\Delta n(g)RT,\quad\Delta H=\Delta U+\Delta n(g)RT$$

#### 热容
定义
- **系统**每升高1K所吸收的热量.
平均热容：$C=\frac{Q}{T_2-T_1}\quad$ 真热容：$C=\frac{\delta Q}{{\rm d}T}$
由于Q不是状态函数，所以C也不是状态函数
$$C=\frac{\partial H}{\partial T}$$
$Q_V$和$Q_p$与途径无关，所以$C_V$、$C_p$都是系统的状态性质，且为广度性质.
一般$Q_p>Q_V$.

>Q：状态性质、状态函数的区别？<br>A：<a href="https://www.bilibili.com/read/cv29131177">物理化学中，状态性质、状态变量与状态函数的含义是不是一回事? 什么是状态方程?</a>

若指定系统中物质的量为1mol，则其热容表示为$C_{V,m}、C_{p,m}$，两者均为强度性质.
$$\begin{aligned}&\because{\rm d}H={\rm d}U+{\rm d}(pV)={\rm d}U+{\rm d}(nRT)\\&\therefore C_p{\rm d}T=C_V{\rm d}T+nR{\rm d}T\end{aligned}$$
从下式可以看出,$$C_p-C_V=[(\frac{\partial U}{\partial V})_T+p](\frac{\partial V}{\partial T})_p$$
$C_p>C_V$的本质是系统对外界做功$p(\partial V/\partial T)_p$，以及由于体积变化而引起分子间势能$(\partial U/\partial V)_T(\partial V/\partial T)_p$增加.
一般来说，对固体和液体主要是前一因素为主，对于气体而言主要是后者.

- 对熔融金属，有经验公式$$C_{p,m}-C_{V,m}=0.87R$$
- 对于纯固体，由于一般过程中体积变化很小，$C_{p,m}\approx C_{V,m}$
- 理想气体的热容与温度无关，有$$C_p-C_V=nR\quad或\quad C_{p,m}-C_{V,m}=R$$对于单原子分子理想气体$C_{V,m}=1.5R$，双原子分子理想气体$C_{V,m}=2.5R$
- 实际物质的热容均与温度有关且符合下列经验式：$$C_{p,m}=a+bT+c^\prime T^{-2}(或cT^2)$$式中$a、b、c、c^\prime$皆为经验常数，高温下一般取$c^\prime T^{-2}$

由$C_V=(\frac{\partial U}{\partial T})_V$得$\delta Q_V={\rm d}U=C_V{\rm d}T$，同理得：$$\begin{aligned}&Q_V=\Delta V=\int_{T_1}^{T_2}C_V{\rm d}T\quad或\\&Q_p=\Delta H=\int_{T_1}^{T2}C_p{\rm d}T\end{aligned}$$
将$C_{p,m}$公式代入积分.
**关系是始终存在的**
一般情况下，压力对焓的影响不大，视为等压算焓变.
若有相变，需要分段积分，并要加上相变潜热，如：$$\begin{aligned}H(g,T{\rm K})-H(s,0{\rm K})=&\int_0^{T_{trs}}C_p({\rm I}){\rm d}T+\Delta_{trs}H+\int_{T_{trs}}^{T_{fus}}C_p({\rm II}){\rm d}T+\Delta_{fus}H\\&+\int_{T_{fus}}^{T_b}C_p({\rm I}){\rm d}T+\Delta_{vap}H+\int_{T_b}^TC_p({g}){\rm d}T\\其中\Delta_{trs}H、\Delta_{fus}H、\Delta_{vap}H&分别为晶型转变焓、融化焓和蒸发焓.\end{aligned}$$
#### 热力学第一定律对理想气体的应用
- 焦耳实验：$水浴Q=0,真空膨胀\Delta U=Q+W=0$<br>得出U和H都只是温度的函数 __理想气体情况下__
- 绝热状态`等熵过程`$$T_1V_1^{\gamma-1}=T_2V_2^{\gamma-1},\quad其中\frac{C_{p,m}}{C_{V,m}}=\gamma,\ TV^{\gamma-1}=常数，\quad还有pV^\gamma，p^{1-\gamma}T^\gamma$$
## 热力学第二定律
自发过程`不需要环境做功而能自动进行的过程`
自发过程的共同特征：不可逆性.
自发过程的限度：平衡状态.

克劳修斯的表述指出热传递的不可逆性，开尔文的表述指出了热功转换的不可逆性.这两者表述是等价的.
#### 卡诺定理
$$\eta\overset{def}{=}\frac{-W}{Q_1}=\frac{Q_1+Q_2}{Q_1}$$
可逆热机效率与高温热源T1及低温热源T2有关$$\eta\leq\eta_r=\frac{T_1-T_2}{T_1}$$
热温商$$\frac{Q_1}{T_1}+\frac{Q_2}{T_2}\leq0\quad其中Q/T称为热温商$$
熵定义$$\boxed{\begin{aligned}&{\rm d}S\overset{def}{=}\frac{\delta Q_r}{T}\\或\quad&\Delta S=\int_A^B\frac{\delta Q_r}{T}\end{aligned}}$$有**克劳修斯不等式**$$\oint\frac{\delta Q_{ir}}{T}\leq0\quad(当相等时为可逆过程)$$
