# 3. ノルム（長さの一般化）

ノルムとは「ベクトルに長さを与える関数」。長さの本質を抽象化すると次の 3 公理になる。

## 3.1 ノルムの公理

**定義.** ベクトル空間 $V$ 上の関数 $\|\cdot\| : V \to \mathbb{R}_{\ge 0}$ が **ノルム** であるとは、任意の $\mathbf{v}, \mathbf{w} \in V$, $c \in K$ に対し：

| # | 公理 | 内容 |
|---|---|---|
| (N1) | 非負性・非退化性 | $\|\mathbf{v}\| \ge 0$、かつ $\|\mathbf{v}\| = 0 \iff \mathbf{v} = \mathbf{0}$ |
| (N2) | 斉次性 | $\|c\mathbf{v}\| = \|c\| \cdot \|\mathbf{v}\|$ |
| (N3) | 三角不等式 | $\|\mathbf{v} + \mathbf{w}\| \le \|\mathbf{v}\| + \|\mathbf{w}\|$ |

## 3.2 主要なノルム（$L^p$ ノルム）

$\mathbb{R}^n$ 上で最もよく使われるのは **$L^p$ ノルム**（$p \ge 1$）：

$$
\|\mathbf{v}\|_p = \left( \sum_{i=1}^n |v_i|^p \right)^{1/p}
$$

| 名称 | 定義 | 用途 |
|---|---|---|
| $L^1$（マンハッタン） | $\sum_i |v_i|$ | スパース正則化（Lasso） |
| $L^2$（ユークリッド） | $\sqrt{\sum_i v_i^2}$ | 標準的な「長さ」、最小二乗法 |
| $L^\infty$（最大値） | $\max_i |v_i|$ | 最悪値評価、リプシッツ連続性 |

**例.** $\mathbf{v} = (3, -4)$ のとき、$\|\mathbf{v}\|_1 = 7$、$\|\mathbf{v}\|_2 = 5$、$\|\mathbf{v}\|_\infty = 4$。同じベクトルでもノルムによって「長さ」は違う。

## 3.3 三角不等式の証明（$L^2$ の場合）

$L^2$ ノルムは内積 $\langle \mathbf{v}, \mathbf{w} \rangle = \sum v_i w_i$ から $\|\mathbf{v}\|_2 = \sqrt{\langle \mathbf{v}, \mathbf{v}\rangle}$ で定まる。

**補題（コーシー・シュワルツの不等式）.** $|\langle \mathbf{v}, \mathbf{w}\rangle| \le \|\mathbf{v}\|_2 \|\mathbf{w}\|_2$。

**証明スケッチ.** 任意の $t \in \mathbb{R}$ に対し $\|\mathbf{v} + t\mathbf{w}\|_2^2 \ge 0$。展開すると

$$
\|\mathbf{v}\|_2^2 + 2t\langle \mathbf{v},\mathbf{w}\rangle + t^2 \|\mathbf{w}\|_2^2 \ge 0
$$

これは $t$ の 2 次式で常に非負。したがって判別式 $\le 0$ より

$$
4 \langle \mathbf{v}, \mathbf{w}\rangle^2 - 4 \|\mathbf{v}\|_2^2 \|\mathbf{w}\|_2^2 \le 0
$$

整理して両辺の平方根を取れば $|\langle \mathbf{v}, \mathbf{w}\rangle| \le \|\mathbf{v}\|_2 \|\mathbf{w}\|_2$。$\blacksquare$

**三角不等式の証明.**

$$
\|\mathbf{v}+\mathbf{w}\|_2^2 = \|\mathbf{v}\|_2^2 + 2\langle\mathbf{v},\mathbf{w}\rangle + \|\mathbf{w}\|_2^2
\le \|\mathbf{v}\|_2^2 + 2\|\mathbf{v}\|_2\|\mathbf{w}\|_2 + \|\mathbf{w}\|_2^2 = (\|\mathbf{v}\|_2 + \|\mathbf{w}\|_2)^2
$$

両辺の平方根を取れば $\|\mathbf{v}+\mathbf{w}\|_2 \le \|\mathbf{v}\|_2 + \|\mathbf{w}\|_2$。$\blacksquare$

## 3.4 単位ベクトルと正規化

$\|\mathbf{v}\| = 1$ のベクトルを **単位ベクトル** という。任意の $\mathbf{v} \neq \mathbf{0}$ に対し

$$
\hat{\mathbf{v}} = \frac{\mathbf{v}}{\|\mathbf{v}\|}
$$

は単位ベクトル（**正規化**）。これは「向き」だけを抽出する操作と解釈できる。

---

前: [[02_basis_and_dimension]] / 次: [[04_pitfalls]]
