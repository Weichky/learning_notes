《Python程序设计基础》读一下类与对象，其他的都无所谓。S
# 预备
### import
导入模块用法：`import '模块名' as '别名'`
导入对象用法：`from '模块名' import '对象名' as '别名'`
- *以\*为参数，导入并采用所有对象名*

### \_\_name\_\_属性
如果作为模块导入，`__name__`被自动设置成模块名；
如果直接运行，`__name__`被设置成`__main__`

### 常用内置对象
- `[list]`列表，元素可以为任何类型
- `{1:dict}`字典，结构为“键：值”
- `(tuple,)`元组
- `{set/frozenset}`集合

#### 变量
- `type()`用于查看变量类型
- python变量是值的引用
- 分数：标准库fractions中Fraction对象.`Fractions(分子,分母)，obj.numerator查看分子，obj.denominator查看分母`

#### 关系运算符
`in`用于测试一个对象是否为另一个对象的元素
`is`用于测试对象是否同一

#### 基本输入输出
`input()`
`print()`

# 正则表达式
# 模块
`jupyter notebook`启动jupyter notebook