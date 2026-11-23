# The polygonal Pólya–Szegő inequality for the first Dirichlet eigenvalue

[阅读论文 / Read the paper (PDF)](./polygonal_polya_szego.pdf) · [LaTeX 源码 / Source](./polygonal_polya_szego.tex)

英文手稿，2026 年 11 月 22 日，27 页，含两幅示意图。

## 主要结果

在面积相等、边数至多为 $N$ 的简单平面多边形中，哪一种使第一 Dirichlet 特征值最小？手稿的定理 1.1 给出的极小形状是正 $N$ 边形，对每个整数 $N\geq 3$ 均成立，包括非凸多边形在内。边数在合并相邻共线边后计算。

记 $\lambda_1(P)$ 为多边形 $P$ 的第一 Dirichlet 特征值，$|P|$ 为其面积，$R_N$ 为正 $N$ 边形。定理的尺度不变形式为

$$
|P|\,\lambda_1(P) \geq |R_N|\,\lambda_1(R_N).
$$

等号成立当且仅当 $P$ 与 $R_N$ 相似。固定面积后，极小形状在全等意义下唯一。

## 阅读指引

- **第 2 节**处理凸多边形。将多边形分成带混合边界条件的子区域后，问题归结为等腰三角形谱函数的支撑线估计。
- **第 3–4 节**用凸顶点的数目限制可能优于正多边形的竞争者，再处理只有一个内角大于 $\pi$ 的多边形所需的紧性。
- **第 5–8 节**比较第一特征函数的超水平集。驻定非凸多边形的边界条件要求某个超水平集不连通，而圆盘上的定量估计在同一高度给出连通性。第 8 节汇总论证并处理等号。附录 A–C 给出扇形与圆盘上用到的估计。

同一不等式另有一篇采用凸包分割的 14 页手稿。[阅读分割证明](https://github.com/ChengZhuoCZ/polygonal-faber-krahn-partition-proof)

## English summary

The manuscript presents a unified analytic argument for all $N\geq 3$. It first treats convex polygons by a mixed-eigenvalue comparison, then uses compactness for polygons with a single reflex vertex and the topology of ground-state superlevel sets to exclude nonconvex minimizers.

## 本地编译 / Build

在仓库根目录使用带有 pdfLaTeX 和 latexmk 的 TeX Live 环境运行

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error polygonal_polya_szego.tex
```

两幅图由 TikZ 绘制，参考文献收录在同一份源码中。latexmk 会重复运行 pdfLaTeX，直至目录和交叉引用稳定。
