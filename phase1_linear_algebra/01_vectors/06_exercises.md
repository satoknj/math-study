# 6. 確認問題

## (a) 定義の確認

**Q1.** ベクトル空間の 8 公理のうち、(V7) と (V8) を書き下し、その違いを説明せよ。

**Q2.** 「線形独立」の定義を、論理記号（$\forall, \exists, \implies$）を使って書け。

**Q3.** ノルムの 3 公理を述べよ。$L^2$ ノルム以外にどのようなノルムがあるか 2 つ挙げよ。

## (b) 計算問題

**Q4.** $\mathbf{v} = (1, 2, -2)$ に対し、$\|\mathbf{v}\|_1$、$\|\mathbf{v}\|_2$、$\|\mathbf{v}\|_\infty$ をそれぞれ計算せよ。

**Q5.** $\mathbb{R}^3$ のベクトル $\mathbf{v}_1 = (1,0,1)$, $\mathbf{v}_2 = (0,1,1)$, $\mathbf{v}_3 = (1,1,2)$ は線形独立か。線形従属なら、$\mathbf{v}_3$ を $\mathbf{v}_1, \mathbf{v}_2$ の線形結合で表せ。

**Q6.** $\mathbf{v} = (3, 0, -4)$ を $L^2$ ノルムで正規化せよ。

## (c) 証明・応用問題

**Q7.** 多項式空間 $\mathbb{R}[x]$ がベクトル空間の公理を満たすことを示せ（V1〜V8 のうち、V7 と V8 を選んで具体的に証明せよ）。

**Q8.** $\{1, x, x^2\}$ が次数 2 以下の多項式空間 $P_2$ の基底であることを示せ。

**Q9.** コーシー・シュワルツの不等式 $|\langle \mathbf{v}, \mathbf{w}\rangle| \le \|\mathbf{v}\|_2 \|\mathbf{w}\|_2$ で **等号が成立する条件** は何か。証明を辿り直して答えよ。

**Q10.（応用）** 単語埋め込みで「類似度」を測るとき、$L^2$ 距離 $\|\mathbf{v}-\mathbf{w}\|_2$ ではなく **コサイン類似度** $\frac{\langle \mathbf{v}, \mathbf{w}\rangle}{\|\mathbf{v}\|_2 \|\mathbf{w}\|_2}$ が好まれる理由を、ノルムと方向の観点から説明せよ。

---

<details>
<summary>解答</summary>

**A1.** (V7) $(a+b)\mathbf{v} = a\mathbf{v} + b\mathbf{v}$ はスカラーの和に関する分配律。(V8) $a(\mathbf{u}+\mathbf{v}) = a\mathbf{u} + a\mathbf{v}$ はベクトルの和に関する分配律。「何を分配するか」が違う。両方なければ $K$ と $V$ の演算が整合しない。

**A2.** $\forall c_1, \dots, c_k \in K, \left( \sum_{i=1}^k c_i \mathbf{v}_i = \mathbf{0} \implies \forall i, c_i = 0 \right)$

**A3.** (N1) 非負性・非退化性、(N2) 斉次性、(N3) 三角不等式。$L^2$ 以外: $L^1$（マンハッタン）、$L^\infty$（最大値）、$L^p$（一般）など。

**A4.** $\|\mathbf{v}\|_1 = 1+2+2 = 5$、$\|\mathbf{v}\|_2 = \sqrt{1+4+4} = 3$、$\|\mathbf{v}\|_\infty = \max(1,2,2) = 2$。

**A5.** $\mathbf{v}_1 + \mathbf{v}_2 = (1,1,2) = \mathbf{v}_3$。よって $\mathbf{v}_3 = \mathbf{v}_1 + \mathbf{v}_2$ で線形従属。

**A6.** $\|\mathbf{v}\|_2 = \sqrt{9+0+16} = 5$。$\hat{\mathbf{v}} = (3/5, 0, -4/5)$。

**A7.** $p(x) = \sum a_i x^i$, $q(x) = \sum b_i x^i$ とおく。
- (V7): $(a+b)p(x) = (a+b)\sum a_i x^i = \sum (a+b)a_i x^i = \sum a a_i x^i + \sum b a_i x^i = ap(x) + bp(x)$。
- (V8): $a(p(x)+q(x)) = a \sum (a_i + b_i) x^i = \sum (a a_i + a b_i) x^i = ap(x) + aq(x)$。
体 $\mathbb{R}$ の分配律から従う。

**A8.** **張ること:** 任意の $p \in P_2$ は $p(x) = a_0 + a_1 x + a_2 x^2 = a_0 \cdot 1 + a_1 \cdot x + a_2 \cdot x^2$ と書ける。**線形独立性:** $c_0 \cdot 1 + c_1 \cdot x + c_2 \cdot x^2 = 0$（恒等的に 0）が成り立つとする。$x=0$ を代入して $c_0 = 0$。両辺微分して $x=0$ で $c_1 = 0$。さらに微分して $c_2 = 0$。よって全て 0。$\blacksquare$

**A9.** 証明では「2 次関数 $\|\mathbf{v}+t\mathbf{w}\|_2^2 \ge 0$ の判別式 $\le 0$」を使った。等号成立は判別式 $= 0$、すなわち **ある $t_0$ で $\mathbf{v} + t_0 \mathbf{w} = \mathbf{0}$**。つまり $\mathbf{v}$ と $\mathbf{w}$ が **平行**（一方が他方のスカラー倍、$\mathbf{w}=\mathbf{0}$ も含む）であるとき。

**A10.** $L^2$ 距離はベクトルの「ノルムの大きさ」にも影響される。一方コサイン類似度 $\frac{\langle \mathbf{v},\mathbf{w}\rangle}{\|\mathbf{v}\|\|\mathbf{w}\|}$ は **正規化** によりノルムをキャンセルし、「方向」のみを比較する。単語埋め込みでは「頻出語ほどノルムが大きくなる」傾向があり、頻度ではなく意味（方向）で類似度を測りたいときコサイン類似度の方が適切。形式的には $\hat{\mathbf{v}} = \mathbf{v}/\|\mathbf{v}\|$ として $\langle \hat{\mathbf{v}}, \hat{\mathbf{w}} \rangle$ を取っているのと同じ。

</details>

---

前: [[05_llm_category]] / 戻る: [[00_index]]
