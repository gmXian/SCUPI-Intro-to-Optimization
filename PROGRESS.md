# 工作进度状态

> 记录日期：2026-08-29
> 当前阶段：**前 80 页大纲同步修改已完成**；81-160 页相关工作暂时搁置

## 一、涉及文件

| 文件 | 说明 |
| --- | --- |
| `mathematical-programming-2026-2027-1-80.tex` | 主文件（前 80 页，已按大纲更新，现共 85 页） |
| `mathematical-programming-2026-2027-81-160.tex` | 第 81–160 页（另一人提供） |
| `figures-81-160.zip` | 第 81–160 页图片（已解压） |
| `figures/mp-2026/` | 第 1–80 页图片 |
| `figures/Figure/`、`figures/Formula/` | 解压后得到的第 81–160 页图片 |
| `figures/Mathematical_Programming.png` | 教材封面图（Jeter《Mathematical Programming》） |
| `figures/convex_optimization_textbook.png` | 旧教材封面图（Boyd，现已不被引用，文件保留） |
| `mathematical-programming-2026-2027-1-160.tex` | 合并文件（**未完成，已搁置**） |

编译工具链：`latexmk` + `xelatex`（配置文件 `.latexmkrc`，辅助目录 `tmp/build`）。

## 二、前 80 页的大纲同步修改（已完成）

> 依据 Fall 2026 syllabus，对 `mathematical-programming-2026-2027-1-80.tex` 修改。总页数 80 → 85。

### 2.1 关于课程（About the Course）

- 删除 `Credit hours: 48`。
- 新增课程编号 `MATH 1101`、教师信息（办公室 N403 / 邮箱 / Office Hours）。
- 新增上课时间地点（Tue 19:20–21:55, SCUPI S204）与习题课（每周一次 45 分钟）。
- 成绩构成改为大纲五项（列表形式，一行一项）：Attendance 10% / Quiz 10% / Homework 15% / Mid-term 30% / Final 35%。

### 2.2 教材页（Textbook，单开一页）

- 教材改为 Jeter：`Jeter M. Mathematical Programming: An Introduction to Optimization. CRC Press, 1986.`
- 左栏为封面图 `figures/Mathematical_Programming.png`，右栏为 Title / Author / Publisher / Preview 链接 / Reference。
- Reference 列为 Boyd & Vandenberghe《Convex Optimization》。
- 旧教材 Boyd 封面图 `convex_optimization_textbook.png` 现已不被引用，文件保留未删。

### 2.3 新增页面

- `Course Objectives`（6 条课程目标）。
- `Learning Outcomes`（7 条学习成果）。
- `Material Covered (Weeks 1–9)` 与 `Material Covered (Weeks 10–18)`（教学进度表，`tabularx` + `booktabs`）。

### 2.4 助教页（Acknowledgments → Teaching Assistants）

- 更新为 Yifan Lyu 吕一凡、Guanmeng Xian 贤冠萌（含邮箱），办公室 N407、Office Hours、QQ 群 1108310197。

### 2.5 字体

- 在 `\beamer@scu@fontextend` 中补 `\setCJKsansfont{PingFang SC}`，使中文助教姓名正常显示（否则 Latin Modern Sans 缺中文字形）。

### 2.6 页面顺序（最终）

```
About the Course → Textbook → Course Objectives → Learning Outcomes
→ Material Covered (1–9) → Material Covered (10–18)
→ Teaching Assistants → Introduction（正文）
```

## 三、81-160 页相关（已搁置）

### 3.1 已完成的工作

1. 编译了 81-160 页，定位到若干 LaTeX 错误（见 3.2）。
2. 解压 `figures-81-160.zip` 到 `figures/` 目录。
3. 初步生成合并文件 `mathematical-programming-2026-2027-1-160.tex`（未最终完成，已搁置）。

### 3.2 编译发现的问题

> 编译本身能出 PDF（81 页），但存在下列错误。为方便日后继续，记录如下。

#### 3.2.1 真实 LaTeX 错误（致命，需修复）

| # | 页 | 原 tex 行 | 问题 | 修复方式 |
| --- | --- | --- | --- | --- |
| 1 | 88 | 143 | `\\ [\mathbf{x}^*]_i`：`\\` 后紧跟 `[` 被当作可选长度参数 | 改为 `\\ {[\mathbf{x}^*]_i}` |
| 2 | 95 | 266、271 | `\begin{cases}...\end{cases}` 未处于数学模式 | 用 `\[ ... \]` 包裹 |
| 3 | 96 | 285 | `\begin{array}{rcl}...\end{array}` 未处于数学模式 | 用 `\[ ... \]` 包裹 |
| 4 | 103 | 387 | `\\ [c_B^T...]`：同 #1 的 `\\ [` 问题 | 改为 `\\ {[c_B^T...]}` |
| 5 | 155 | 1315 | `\begin{array}{ccc}` 声明 3 列，实际 4 列 | 改为 `{cccc}` |
| 6 | 159 | 1388 | `\begin{array}{rcl}...\end{array}` 未处于数学模式 | 用 `\[ ... \]` 包裹 |

#### 3.2.2 占位符问题（等待替换为图片）

- 原文用 `\textit{[此处为...示意图]}` 占位，其中 **7 处**被错误放在 `\[ ... \]` 数学模式内，已移到文本模式。
- 占位符中文在 Latin Modern 字体中缺失，产生大量 `Missing character` 警告（不影响编译，但文字不显示）。
- 仍有 **2 处**占位符文本含数学字符，在文本模式下报 `Missing $` 错误（未修复）：
  - 第 93 页：`z_o`（下划线）
  - 第 136 页：`x^*=[0,0,1,2,0]^T`（插入符）

#### 3.2.3 帧标题 Unicode 问题

- 第 106、132 页帧标题用字面 `F̂`（F + 组合抑扬符 U+0302）。
- 第 119 页帧标题用字面 `σ`（U+03C3）。
- 这些字形在 Latin Modern 字体中缺失；应改为 `$\hat{F}$`、`$\sigma$`。

### 3.3 合并文件状态（`mathematical-programming-2026-2027-1-160.tex`）

已完成的合并处理：

- 采用前 80 页的前言，并补入 `\usepackage{arydshln}`（81-160 内容用到 `\hdashline`）。
- 移除 81-160 部分重复的前言、`\setcounter{framenumber}{80}`、`(Part 2)` 副标题。
- 在「Linear Programming Problem」小节下新增 `\subsection{The Simplex Method}`（第 81 页前）和 `\subsection{Duality}`（第 152 页前）。
- 修复了 3.2.1 节全部 6 处错误，以及 3.2.3 节帧标题 Unicode。

未完成 / 已知残留：

- 3.2.2 节所述 2 处占位符数学字符报错（第 93、136 页）。
- 占位符仍未替换为 `figures/` 中的实际图片（图片→占位符的对应关系尚未确认）。

## 四、下一步

- 前 80 页大纲同步已完成；如需微调（如 Material Covered 排版、教材引用格式）可继续。
- 81-160 页相关工作暂时搁置，重启时先处理 3.2.2 的占位符残留，再继续合并。
