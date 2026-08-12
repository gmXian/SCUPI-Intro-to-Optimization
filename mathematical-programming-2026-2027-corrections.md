# Mathematical Programming slides: fidelity and correction log

## Scope and reconstruction rule

- Source: `MP-Slides-Final(1)(1).pdf`, pages 1–80 only.
- Output: `mathematical-programming-2026-2027.tex`, exactly 80 pages after compilation.
- Source page $n$ maps to output page $n$.
- Except for the entries below, slide titles, prose, equations, examples, numerical values, item order, and figure captions are retained from the source.
- Reflowing text, changing line breaks, resizing equations, and adapting the 4:3 source to the repository's 16:9 SCU Beamer theme are formatting changes only.

## Intentional changes

| Source page | Source | Revised text or formula | Reason |
|---:|---|---|---|
| 1 and footer | Yue Ivan WU; Fall 2024; former instructor's email | Changxi Wang; 2026–2027 Academic Year; no unverified email | User-confirmed course identity |
| 3 | “My sincere gratitude to my graduate students”; “monitoring my possible mistakes” | Attributes the acknowledgment to the source lecture notes; “monitoring possible mistakes in the source deck” | Prevents falsely attributing the former instructor's students to the new instructor while retaining their names, photos, and contributions |
| 18 | Claims $x_iw_i=0$ means each line is assigned to exactly one product | States that $x_iw_i=0$ prevents simultaneous assignment to both products | Exact assignment additionally requires the page-19 constraint $x_i+w_i=1$ |
| 24 | Strict minima compare against every point in a set that includes $\bar{x}$; global definitions contain an irrelevant $\exists\varepsilon>0$ | Strict comparisons use $x\ne\bar{x}$; global definitions omit $\varepsilon$ | The source strict inequalities are impossible at $x=\bar{x}$; $\varepsilon$ does not occur in a global definition |
| 27 | `Post-otimal analysis` | `Post-optimal analysis` | Typographical error |
| 36 | $\sum_i x_i y_j$; $\lVert x\rVert=\sqrt{x^T y}$ | $\sum_i x_i y_i$; $\lVert x\rVert=\sqrt{x^T x}$ | Free-index and norm errors |
| 43 | Uses $n$ simultaneously for ambient dimension and the number of selected vectors; does not require the selected vectors to be distinct | Selected distinct vectors and coefficients are indexed by $k$ | Removes the index collision and prevents the same vector from being used twice to make every nonempty set appear dependent |
| 48 | `Dirac Function` | `Kronecker delta` | $\delta_{i,j}$ is the Kronecker delta, not the Dirac delta distribution |
| 51 | Lower-right block of $AB$ is $EG+FM$ | $EJ+FM$ | Block-multiplication error |
| 54 | `Elementary row operations does not ...` | `Elementary row operations do not ...` | Subject–verb agreement |
| 62 | Last diagonal entry of $U$ is $-11/13$ | $-11/3$ | Must agree with the elimination result on page 61 |
| 63 | Pivot matrix “differs from $I$ in at most one column” | Row-interchange matrix obtained by applying the same interchange to $I_m$ | The source statement is false for a row swap |
| 64 | Presents an unqualified $A=LU$-type conclusion while pivot matrices are used | $PA=LU$ and the corresponding two triangular solves | Correct factorization when row pivoting is present |
| 69 | Ray closure alone is stated as equivalent to being a convex cone | Closure under every nonnegative linear combination | Ray closure gives positive homogeneity but not addition/convexity |
| 71 | Hyperplane definition does not constrain its normal | Adds $c\ne0$ | A hyperplane requires a nonzero normal vector |
| 74 | `pair of point` | `pair of points` | Typographical error |
| 77 | `half planes`; implication displayed without prose | `half spaces`; “the converse does not hold in general” | Correct terminology in $\mathbb{R}^n$ and explicit rendering of the source implication symbols |
| 79 | Assumes the finite point generators are exactly the extreme points of every nonempty polyhedron | States finite point-and-ray generation without that restriction | A nonempty polyhedron can have no extreme points, e.g. a line or halfspace |

## Extracted image map

| Source page | Repository file |
|---:|---|
| 3 | `figures/mp-2026/p003-yang-yan.jpg` |
| 3 | `figures/mp-2026/p003-liao-sijia.jpg` |
| 3 | `figures/mp-2026/p003-yan-jiajun.jpg` |
| 5 | `figures/mp-2026/p005-optimization-manufacturing.jpg` |
| 6 | `figures/mp-2026/p006-optimization-transportation.jpg` |
| 68 | `figures/mp-2026/p068-hulls-example.jpg` |
| 70 | `figures/mp-2026/p070-affine-translate.jpg` |
| 71 | `figures/mp-2026/p071-hyperplane-halfspaces.jpg` |
| 72 | `figures/mp-2026/p072-convex-polytope.jpg` |
| 73 | `figures/mp-2026/p073-simplex-examples.jpg` |
| 74 | `figures/mp-2026/p074-extreme-points.jpg` |
| 78 | `figures/mp-2026/p078-unbounded-polyhedron.jpg` |
| 78 | `figures/mp-2026/p078-bounded-polytope.jpg` |
| 80 | `figures/mp-2026/p080-finite-basis-decomposition.jpg` |
