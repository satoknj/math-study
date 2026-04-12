# 1. ベクトル空間

## 1.1 素朴な見方から抽象的な定義へ

ベクトルとは「大きさと向きを持つ量」、あるいは「数を並べたもの」。

$$
\mathbf{v} = (v_1, v_2, \dots, v_n) \in \mathbb{R}^n
$$

加法とスカラー倍を成分ごとに定める：

$$
\mathbf{v} + \mathbf{w} = (v_1+w_1, \dots, v_n+w_n), \quad c\mathbf{v} = (cv_1, \dots, cv_n)
$$

これは具体的で扱いやすいが、「数のリストでないものはベクトルではない」と思い込む罠がある。実際には、関数も多項式も行列も「ベクトル」になりうる。本質は **構造** にある。

## 1.2 ベクトル空間の公理的定義

**定義（ベクトル空間）。** 体 $K$（典型的には $\mathbb{R}$ または $\mathbb{C}$）上の **ベクトル空間** とは、集合 $V$ と二つの演算

- 加法 $+ : V \times V \to V$
- スカラー倍 $\cdot : K \times V \to V$

の組 $(V, +, \cdot)$ であって、任意の $\mathbf{u}, \mathbf{v}, \mathbf{w} \in V$ と $a, b \in K$ に対して以下の **8 公理** を満たすものをいう：

| # | 公理 | 内容 |
|---|---|---|
| (V1) | 加法結合律 | $(\mathbf{u}+\mathbf{v})+\mathbf{w} = \mathbf{u}+(\mathbf{v}+\mathbf{w})$ |
| (V2) | 加法交換律 | $\mathbf{u}+\mathbf{v} = \mathbf{v}+\mathbf{u}$ |
| (V3) | 零元の存在 | $\exists \mathbf{0} \in V$ s.t. $\mathbf{v}+\mathbf{0}=\mathbf{v}$ |
| (V4) | 加法逆元の存在 | $\forall \mathbf{v}, \exists (-\mathbf{v})$ s.t. $\mathbf{v}+(-\mathbf{v})=\mathbf{0}$ |
| (V5) | スカラー倍の結合律 | $a(b\mathbf{v}) = (ab)\mathbf{v}$ |
| (V6) | 単位元 | $1 \cdot \mathbf{v} = \mathbf{v}$ |
| (V7) | スカラーに関する分配律 | $(a+b)\mathbf{v} = a\mathbf{v} + b\mathbf{v}$ |
| (V8) | ベクトルに関する分配律 | $a(\mathbf{u}+\mathbf{v}) = a\mathbf{u} + a\mathbf{v}$ |

**ポイント。** 「成分」も「矢印」も定義に登場しない。加法とスカラー倍が「うまく振る舞う」集合は何でもベクトル空間。

(V1)〜(V4) は「$V$ が加法に関して **可換群** をなす」と言っているだけ（後の Phase 4 で群論として再登場）。(V5)〜(V8) は「スカラー倍が加法と整合している」という条件。

## 1.3 ベクトル空間の例（数のリストでない例に注目）

| 例 | $V$ の元 | 加法 | スカラー倍 |
|---|---|---|---|
| $\mathbb{R}^n$ | $(v_1,\dots,v_n)$ | 成分ごと | 成分ごと |
| 多項式空間 $\mathbb{R}[x]$ | $p(x) = a_0 + a_1 x + \cdots$ | 係数ごと | 係数ごと |
| 連続関数空間 $C([0,1])$ | $f : [0,1] \to \mathbb{R}$ 連続 | $(f+g)(x) = f(x)+g(x)$ | $(cf)(x) = c f(x)$ |
| $m \times n$ 実行列 $M_{m,n}(\mathbb{R})$ | 行列 $A$ | 成分ごと | 成分ごと |
| 零空間 $\{\mathbf{0}\}$ | 零元のみ | 自明 | 自明 |

**注意:** 多項式や関数は「無限次元」のベクトル空間になる（[[02_basis_and_dimension]]）。LLM では有限次元ベクトル空間 $\mathbb{R}^d$（$d=768, 4096, \dots$）が中心だが、関数空間の視点はカーネル法・関数解析・連続時間モデルで再登場する。

## 1.4 公理から導かれる初等的事実（証明付き）

**命題.** 任意のベクトル $\mathbf{v} \in V$ に対し、$0 \cdot \mathbf{v} = \mathbf{0}$。

**証明.** スカラーの分配律 (V7) より $0 \cdot \mathbf{v} = (0+0) \cdot \mathbf{v} = 0\cdot\mathbf{v} + 0\cdot\mathbf{v}$。両辺に $-(0\cdot\mathbf{v})$ を加えれば $\mathbf{0} = 0\cdot\mathbf{v}$。$\blacksquare$

**命題.** $(-1) \cdot \mathbf{v} = -\mathbf{v}$（加法逆元）。

**証明.** $\mathbf{v} + (-1)\mathbf{v} = 1\cdot\mathbf{v} + (-1)\mathbf{v} = (1 + (-1))\mathbf{v} = 0\cdot\mathbf{v} = \mathbf{0}$。よって $(-1)\mathbf{v}$ は $\mathbf{v}$ の加法逆元。逆元の一意性から $(-1)\mathbf{v} = -\mathbf{v}$。$\blacksquare$

このように、「成分計算」を一切使わずに公理だけで性質が導ける。これが抽象化の力。

---

次: [[02_basis_and_dimension]] — 線形結合・独立・基底・次元
