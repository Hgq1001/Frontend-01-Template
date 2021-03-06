# 总结

\### 按语法分类

\- ##### 非形式语言

\- 中文，英文

\- ##### 形式语言（乔姆斯基谱系）

\- 0型 无限制语法

\- 1型 上下文相关文法

\- 2型 上下文无关文法

\- 3型 正则文法

\> 0-型文法（无限制文法或短语结构文法）包括所有的文法。该类型的文法能够产生所有可被图灵机识别的语言。可被图灵机识别的语言是指能够使图灵机停机的字串，这类语言又被称为递归可枚举语言。注意递归可枚举语言与递归语言的区别，后者是前者的一个真子集，是能够被一个总停机的图灵机判定的语言。

\>

\> 1-型文法（上下文相关文法）生成上下文相关语言。这种文法的产生式规则取如 αAβ -> αγβ 一样的形式。这里的A 是非终结符号，而 α, β 和 γ 是包含非终结符号与终结符号的字串；α, β 可以是空串，但 γ 必须不能是空串；这种文法也可以包含规则 S->ε ，但此时文法的任何产生式规则都不能在右侧包含 S 。这种文法规定的语言可以被线性有界非确定图灵机接受。

\>

\> 2-型文法生成上下文无关语言。这种文法的产生式规则取如 A -> γ 一样的形式。这里的A 是非终结符号，γ 是包含非终结符号与终结符号的字串。这种文法规定的语言可以被非确定下推自动机接受。上下文无关语言为大多数程序设计语言的语法提供了理论基础。

\>

\> 3-型文法（正规文法）生成正规语言。这种文法要求产生式的左侧只能包含一个非终结符号，产生式的右侧只能是空串、一个终结符号或者一个非终结符号后随一个终结符号；如果所有产生式的右侧都不含初始符号 S ，规则 S -> ε 也允许出现。这种文法规定的语言可以被有限状态自动机接受，也可以通过正则表达式来获得。正规语言通常用来定义检索模式或者程序设计语言中的词法结构。

\### 产生式（BNF）**********

\- 用尖括号括起来的名称来表示语法结构名

\- 语法结构分成基础结构和需要用

\- 基础结构称终结符

\- 复合结构称非终结符

\- 引号和中间的字符标识终结符

\- *标识重复多次

\- | 标识或

\- +表示至少一次

\> 四则运算

\>

\> <Number> ::= "0" | "1" | "2" | ..... | "9"

\>

\> <DecimalNumber> ::= "0" | (("1" | "2" | ..... | "9") <Number>* )

\>

\> <PrimaryExpression> ::= <DecimalNumber> |

\> "(" <LogicalExpression> ")"

\>

\> <MultiplicativeExpression> ::= <PrimaryExpression> |

\> <MultiplicativeExpression> "*" <PrimaryExpression>|

\> <MultiplicativeExpression> "/" <PrimaryExpression>

\>

\> <AdditiveExpression> ::= <MultiplicativeExpression> |

\> <AdditiveExpression> "+" <MultiplicativeExpression>|

\> <AdditiveExpression> "-" <MultiplicativeExpression>

\>

\> <LogicalExpression> ::= <AdditiveExpression> |

\> <LogicalExpression> "||" <AdditiveExpression> |

\> <LogicalExpression> "&&" <AdditiveExpression>

小作业：用正则表示四则运算

\```

/^((0|[1-9][0-9]*)([-+*/](0|[1-9][0-9]*))*[-+*/]?)*(((?<K>\()((0|[1-9][0-9]*)+([+*/-](0|[1-9][0-9]*))*)+[-+*/]?)+((?<-K>\))([-+*/](0|[1-9][0-9]*)[-+*/]?)*)+)*((0|[1-9][0-9]*)([-+*/](0|[1-9][0-9]*))*)*$/

\```

\### 通过产生式理解形式语言

\- 0型 无限制文法

\- ? ::= ?

\- 1型 上下文相关文法

\- ?<A>? ::= ?<B>?

\- 2型 上下文无关文法

\- <A> ::= ?

\- 3型 正则文法

\- <A>::=<A>?

\- <A>::=?<A> （不允许）

\### 动态与静态

\- 动态

\- 在用户的设备/在线服务器上

\- 产品实际运行时

\- Runtime

\- 静态

\- 在程序员的设备上

\- 产品开发时

\- Compiletime

\### 一般命令式编程语言

\- Atom（原子：变量）

\- Identifier

\- Liteal

\- Expression（表达式）

\- Atom

\- Operator

\- Punctuator

\- Statement（声明）

\- Expression

\- Keyword

\- Punctuator

\- Structure（结构化）

\- Function

\- Class

\- Process

\- Namespace

\- Program（程序）

\- Program

\- Module（模块、组件）

\- Package

\- Library
