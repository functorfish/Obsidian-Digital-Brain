---
tags:
  - mathematics/theorem
  - mathematics/analysis
  - beauty
  - proof
aliases:
  - 欧拉恒等式
  - 最美的数学公式
  - God's Equation
creation-date: <% tp.file.creation_date() %>
---
# 欧拉恒等式：数学的璀璨明珠

> [!quote] 理查德·费曼 (Richard Feynman)
> "这是我们的宝石，是数学中最卓越的公式。"
> (This is our jewel, the most remarkable formula in mathematics.)

> [!abstract] 欧拉恒等式 (Euler's Identity)
> $$ e^{i\pi} + 1 = 0 $$

这个等式之所以被认为无与伦比，是因为它将数学中五个最核心的常数完美地融合在了一起：
- **$0$**：加法单位元。
- **$1$**：乘法单位元。
- **$\pi$**：[[圆周率π|圆周率]]，几何学的基石。
- **$e$**：[[自然常数e|自然常数]]，微积分的核心。
- **$i$**：[[虚数单位i|虚数单位]]，复数域的构建者。

它通过三种最基本的算术运算（加法、乘法、指数）将这些来自不同数学分支的常数联系起来，展现了数学深刻的内在和谐。

---

## 📜 证明之路：从欧拉公式到欧拉恒等式

欧拉恒等式本身是更通用的**欧拉公式 (Euler's Formula)** 的一个特例。因此，要理解它，我们必须先证明欧拉公式。

> [!tip] 核心桥梁：欧拉公式
> 对于任意实数 $x$，以下关系成立：
> $$ e^{ix} = \cos(x) + i\sin(x) $$

我们将使用[[泰勒级数]] (Taylor Series) 来证明欧拉公式，这是微积分中一个强大的工具，可以将函数表示为无穷项的和。

### 第一步：关键函数的泰勒级数展开

我们首先需要以下三个关键函数在 $x=0$ 处的泰勒级数（也称麦克劳林级数）：

1.  **指数函数 $e^z$**
    $$ e^z = \sum_{n=0}^{\infty} \frac{z^n}{n!} = 1 + z + \frac{z^2}{2!} + \frac{z^3}{3!} + \frac{z^4}{4!} + \dots $$

2.  **余弦函数 $\cos(x)$**
    $$ \cos(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \dots $$

3.  **正弦函数 $\sin(x)$**
    $$ \sin(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{(2n+1)!} = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \frac{x^7}{7!} + \dots $$

### 第二步：将 $e^z$ 中的 $z$ 替换为 $ix$

现在，我们将指数函数 $e^z$ 的级数展开式中的变量 $z$ 替换为 $ix$。

$$ e^{ix} = 1 + (ix) + \frac{(ix)^2}{2!} + \frac{(ix)^3}{3!} + \frac{(ix)^4}{4!} + \frac{(ix)^5}{5!} + \dots $$

接下来，我们利用虚数单位 $i$ 的幂次性质 ($i^2 = -1, i^3 = -i, i^4 = 1, \dots$) 来简化每一项：

$$ e^{ix} = 1 + ix - \frac{x^2}{2!} - i\frac{x^3}{3!} + \frac{x^4}{4!} + i\frac{x^5}{5!} - \dots $$

### 第三步：分离实部与虚部

现在，我们将上式中的项重新组合，分为不含 $i$ 的**实部**和含有 $i$ 的**虚部**。

> [!example]- 分离实部与虚部
> **实部 (Real Part):**
> $$ \left( 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots \right) $$
> **虚部 (Imaginary Part):**
> $$ i \left( x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots \right) $$

### 第四步：识别出 $\cos(x)$ 和 $\sin(x)$

仔细观察，我们发现：
- 分离出的**实部**，其级数形式与 $\cos(x)$ 的泰勒级数完全相同。
- 分离出的**虚部**中括号内的部分，其级数形式与 $\sin(x)$ 的泰勒级数完全相同。

因此，我们可以进行替换：
$$ e^{ix} = \cos(x) + i\sin(x) $$
至此，**欧拉公式证明完毕**。

---

## ✨ 终点：导出欧拉恒等式

有了欧拉公式这个强大的工具，导出欧拉恒等式就变得非常简单了。我们只需在欧拉公式中令 $x = \pi$。

1.  **代入 $x = \pi$**:
    $$ e^{i\pi} = \cos(\pi) + i\sin(\pi) $$

2.  **计算三角函数值**:
    我们知道 $\cos(\pi) = -1$ 且 $\sin(\pi) = 0$。

3.  **代入计算结果**:
    $$ e^{i\pi} = -1 + i(0) $$
    $$ e^{i\pi} = -1 $$

4.  **移项得到最终形式**:
    将 $-1$ 移到等式左边，我们就得到了这个辉煌的恒等式。

> [!success] 欧拉恒等式
> $$ e^{i\pi} + 1 = 0 $$

---

## 📚 严谨参考来源

1.  **The Feynman Lectures on Physics, Vol. I, Chapter 22: Algebra**
    - 理查德·费曼在他的讲义中对欧拉公式有非常直观和深刻的解释。
    - [Feynman Lectures Website](https://www.feynmanlectures.caltech.edu/I_22.html)

2.  **Wolfram MathWorld, "Euler Formula"**
    - 一个全面且严谨的数学资源网站，提供了公式的多种证明和应用。
    - [MathWorld Article](https://mathworld.wolfram.com/EulerFormula.html)

3.  **《普林斯顿微积分读本》(Calculus: A Rigorous First Course) by Adrian Banner**
    - 这类优秀的微积分教材详细讲解了泰勒级数及其在证明欧拉公式中的应用。
