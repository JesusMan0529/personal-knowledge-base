#Markdown
#### 基本语法结构

- **命令**：以反斜杠 `\` 开头，如 `\alpha`、`\sum`
- **参数**：用花括号 `{}` 包围，如 `\frac{a}{b}`
- **下标**：使用 `_`，如 `x_1`
- **上标**：使用 `^`，如 `x^2`
- **分组**：用花括号将多个字符组合，如 `x_{i+1}`

#### 常用 LaTeX 命令

>\alpha, \beta, \gamma   % 希腊字母
   \sum, \prod, \int            % 求和、乘积、积分
   \frac{分子}{分母}             % 分数
   \sqrt{表达式}                  % 平方根
   \sqrt[n]{表达式}              % n次根
   \to                                  % →

#### 行内公式

行内公式使用单个美元符号 `$` 包围，公式会嵌入到文本中。

文本中的变量 $x = 5$ 和函数 $f(x) = x^2 + 2x + 1$。

#### 块级公式

块级公式使用双美元符号 `$$` 包围，公式会独立成行并居中显示。

$$E = mc^2$$

$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$

#### 多行公式

使用 `align` 环境创建多行对齐公式。

> `&` 为对齐符号，使 `&` **后**的对象**竖直对齐**。
   `\\` 为换行符号。

$$
	\begin{align}
		&f(x) = ax^2 + bx + c \\
    &f'(x) = 2ax + b \\
    &f''(x) = 2a
	\end{align}
$$
#### 基本运算符号

- 加减乘除：`+`, `-`, `\times`, `\div` → $+$, $-$, $\times$, $\div$
- 分数：`\frac{a}{b}` → $\frac{a}{b}$
- 根号：`\sqrt{x}`, `\sqrt[n]{x}` → $\sqrt{x}$, $\sqrt[n]{x}$
- 指数：`x^2`, `e^{i\pi}` → $x^2$, $e^{i\pi}$
#### 比较符号

- 等于：`=`, `\neq`, `\equiv` → $=$, $\neq$, $\equiv$
- 大小：`<`, `>`, `\leq`, `\geq` → $<$, $>$, $\leq$, $\geq$
- 约等于：`\approx`, `\sim` → $\approx$, $\sim$

#### 集合符号

- 属于：`\in`, `\notin` → $\in$, $\notin$
- 包含：`\subset`, `\supset` → $\subset$, $\supset$
- 交并：`\cap`, `\cup` → $\cap$, $\cup$
- 空集：`\emptyset` → $\emptyset$
#### 希腊字母

| 小写    | 大写  | LaTeX      | 小写    | 大写  | LaTeX    |
| ----- | --- | ---------- | ----- | --- | -------- |
| **α** | Α   | `\alpha`   | ν     | Ν   | `\nu`    |
| **β** | Β   | `\beta`    | ο     | Ο   | `o`      |
| **γ** | Γ   | `\gamma`   | **π** | Π   | `\pi`    |
| **δ** | Δ   | `\delta`   | ρ     | Ρ   | `\rho`   |
| ε     | Ε   | `\epsilon` | σ     | Σ   | `\sigma` |
| **θ** | Θ   | `\theta`   | τ     | Τ   | `\tau`   |
| **λ** | Λ   | `\lambda`  | φ     | Φ   | `\phi`   |
| **μ** | Μ   | `\mu`      | ω     | Ω   | `\omega` |

#### 特殊函数和符号

- 三角函数：`\sin`, `\cos`, `\tan` → $\sin$, $\cos$, $\tan$
- 对数：`\log`, `\ln` → $\log$, $\ln$
- 极限：`\lim_{x \to 0}` → $\lim_{x \to 0}$
- 求和：`\sum_{i=1}^{n}` → $\sum_{i=1}^{n}$
- 积分：`\int_{a}^{b}` → $\int_{a}^{b}$
- 无穷：`\infty` → $\infty$

#### 矩阵表示

使用 `matrix` 环境。

$$
    \begin{pmatrix}
    a & b \\
    c & d
    \end{pmatrix}
$$

**不同括号类型的矩阵**

- `pmatrix`：圆括号 $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$
- `bmatrix`：方括号 $\begin{bmatrix} a & b \\ c & d \end{bmatrix}$
- `vmatrix`：行列式 $\begin{vmatrix} a & b \\ c & d \end{vmatrix}$