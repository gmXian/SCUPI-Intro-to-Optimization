# Corrections for source PDF pages 161–240

The TeX file reproduces the source slide order, titles, prose, formulas, examples, and figure captions. The following changes are intentional. Page numbers refer to the source PDF.

| Source page | Source content | Revised content | Reason |
|---:|---|---|---|
| 165 | The reformulated nonnegative-variable list still contains `x_3 >= 0` after the unrestricted variable `x_3` has been replaced by `x_4-x_5`. | The list contains `x_1`, `-x_2`, `x_4`, `x_5`, `x_6`, and `x_7`. | `x_3` is no longer an independent variable in the reformulated problem; requiring it to be nonnegative would also contradict its original unrestricted status. |
| 172 | The concavity inequality is printed as `f(alpha x + (1-alpha)y) >= f(x) + (1-alpha)f(y)`. | Restored `alpha f(x)` on the right-hand side. | The coefficient is required by the definition of concavity and by the convex-combination weights. |
| 181 | “Any quadratic from can be expressed as” | “Any quadratic form can be expressed as” | Typographical error. |
| 184 | The proof of Proposition 4 says “Due to positive definite property” although the proposition concerns positive semidefinite quadratic forms. | “Due to the positive semidefinite property” | The proof uses only the non-strict inequality `(x-y)^T B (x-y) >= 0`. |
| 185 | The proof concludes that the scalar `f(alpha x + (1-alpha)y)` belongs to the level set. | The convex combination `alpha x + (1-alpha)y` belongs to the level set. | A level set is a set of domain points, not function values. |
| 193 | “Critical point: `nabla f(x-bar)=0`, local max/minimum” can be read as saying every critical point is a local extremum. | States the necessary condition in the correct direction: an interior differentiable local maximum or minimum has zero gradient and is therefore a critical point. | A critical point need not be a local maximum or minimum; it can, for example, be a saddle point. |
| 196 | The Sylvester-criterion bullet refers generally to “principal minors” while displaying the nested upper-left determinants. | “Leading principal minors” | Positive definiteness is characterized by positivity of all leading principal minors, not all arbitrary principal minors. |
| 210 | The two-sided directional derivative at an unconstrained differentiable local maximum is written as being at most zero for every direction. | Uses `D_v f(x*)=0`. | Applying the inequality to both `v` and `-v`, or using the two-sided derivative directly, forces equality and yields the stated zero-gradient condition. |
| 214 | The Taylor expansion omits `t` from the first-order term. | Restored `t [nabla f(x*)]^T v`. | Taylor expansion of `f(x*+t v)` requires the factor `t`; the subsequent limit argument also depends on it. |
| 218 | The equality-constraint slide states `b in R^{n x 1}` although `g(x)` has `m` components, and places the twice-differentiability statement on the partial derivatives of `g_i`. | Uses `b in R^{m x 1}` and states that `f` and each `g_i` are twice continuously differentiable. | Dimensional consistency and the standard smoothness assumptions for the Lagrange multiplier theorem. |
| 228 | Stationarity conditions contain an incorrect beta index and omit partial-derivative symbols/arguments. | Uses derivatives with respect to `beta_{k+1},...,beta_n`, `lambda`, and `x`, with all arguments shown. | Notational correction; the original expressions are not well-formed derivatives. |
| 233 | The complementary-slackness line labels `[b-g(x*)]^T lambda*` as a derivative with respect to `x`. | Labels it as `[partial L / partial lambda]^T lambda*`. | Since `partial L / partial lambda = b-g(x)`, the original denominator is incorrect. |
| 234 | The displayed objective contains `+4x_2^3`, but the derivative, KKT system, solution, and stated optimum all omit that term. | Removed `+4x_2^3`; the objective is `-x_1^2-3x_2^2+4x_1+6x_2`. | This is the unique version consistent with every subsequent calculation and the stated value `f(2,1)=7`. |
| 240 | The acknowledgments slide contains a portrait of the former instructor. | The portrait is omitted; the closing text is retained. | The 2026–2027 course instructor is Changxi Wang, so retaining another instructor’s portrait would be factually misleading. |

## Course metadata

- Instructor: Changxi Wang
- Academic year: 2026–2027
- Source footer names and email addresses are not reproduced; the SCUPI Beamer template supplies the updated course footer.
