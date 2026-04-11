# 数学学習ロードマップ

## 目標

- LLM（大規模言語モデル）の数学的理解
- 圏論の理解

## 学習の流れ

```
LLM の理解
├── 線形代数（ベクトル・行列・固有値）
├── 微積分（勾配・連鎖律・最適化）
└── 確率・統計（分布・最尤推定・情報理論）

圏論の理解
├── 集合論（写像・関係）
├── 抽象代数（モノイド・群）
└── 圏論本体（圏・関手・自然変換・モナド）
```

具体（LLMの数学）から抽象（圏論）へ順に進む。

---

## Phase 1 — 線形代数

| # | タイトル | ファイル | 状態 |
|---|---|---|---|
| 1 | ベクトル | `phase1_linear_algebra/01_vectors.md` | [x] |
| 2 | 行列と線形写像 | `phase1_linear_algebra/02_matrices.md` | [ ] |
| 3 | 連立方程式とガウス消去法 | `phase1_linear_algebra/03_gaussian_elimination.md` | [ ] |
| 4 | 内積とノルム | `phase1_linear_algebra/04_inner_product.md` | [ ] |
| 5 | 固有値・固有ベクトル | `phase1_linear_algebra/05_eigenvalues.md` | [ ] |
| 6 | 行列の対角化・SVD | `phase1_linear_algebra/06_diagonalization_svd.md` | [ ] |
| 7 | 勾配と線形変換（LLMへの橋渡し） | `phase1_linear_algebra/07_gradient_linear_transform.md` | [ ] |
| 8 | まとめと演習 | `phase1_linear_algebra/08_review.md` | [ ] |

## Phase 2 — 微積分

| # | タイトル | ファイル | 状態 |
|---|---|---|---|
| 1 | 関数・極限・連続性 | `phase2_calculus/01_functions_limits.md` | [ ] |
| 2 | 微分（1変数） | `phase2_calculus/02_differentiation.md` | [ ] |
| 3 | 多変数関数と偏微分 | `phase2_calculus/03_partial_derivatives.md` | [ ] |
| 4 | 勾配・ヤコビアン・ヘッシアン | `phase2_calculus/04_gradient_jacobian_hessian.md` | [ ] |
| 5 | 連鎖律とバックプロパゲーション | `phase2_calculus/05_chain_rule_backprop.md` | [ ] |
| 6 | 最適化（勾配降下法） | `phase2_calculus/06_optimization.md` | [ ] |

## Phase 3 — 確率・情報理論

| # | タイトル | ファイル | 状態 |
|---|---|---|---|
| 1 | 確率の基礎 | `phase3_probability/01_probability_basics.md` | [ ] |
| 2 | 確率変数と分布 | `phase3_probability/02_distributions.md` | [ ] |
| 3 | 期待値・分散・共分散 | `phase3_probability/03_expectation_variance.md` | [ ] |
| 4 | 最尤推定・ベイズ推定 | `phase3_probability/04_mle_bayes.md` | [ ] |
| 5 | 情報量・エントロピー | `phase3_probability/05_entropy.md` | [ ] |
| 6 | KLダイバージェンスとクロスエントロピー損失 | `phase3_probability/06_kl_crossentropy.md` | [ ] |

## Phase 4 — 集合論・抽象代数

| # | タイトル | ファイル | 状態 |
|---|---|---|---|
| 1 | 集合・写像・関係 | `phase4_algebra/01_sets_maps.md` | [ ] |
| 2 | 群の基礎 | `phase4_algebra/02_groups.md` | [ ] |
| 3 | モノイドと半群 | `phase4_algebra/03_monoids.md` | [ ] |
| 4 | 環と体 | `phase4_algebra/04_rings_fields.md` | [ ] |
| 5 | まとめと圏論への橋渡し | `phase4_algebra/05_bridge_to_category.md` | [ ] |

## Phase 5 — 圏論

| # | タイトル | ファイル | 状態 |
|---|---|---|---|
| 1 | 圏とは何か | `phase5_category_theory/01_categories.md` | [ ] |
| 2 | 関手（Functor） | `phase5_category_theory/02_functors.md` | [ ] |
| 3 | 自然変換 | `phase5_category_theory/03_natural_transformations.md` | [ ] |
| 4 | 普遍性・極限・余極限 | `phase5_category_theory/04_limits_colimits.md` | [ ] |
| 5 | 随伴関手 | `phase5_category_theory/05_adjunctions.md` | [ ] |
| 6 | モナド | `phase5_category_theory/06_monads.md` | [ ] |
| 7 | 豊穣圏・高次圏への入口 | `phase5_category_theory/07_enriched_higher.md` | [ ] |
| 8 | まとめと応用 | `phase5_category_theory/08_review.md` | [ ] |
