<p align="center">
  <img src="figure/zhongcai.png" width="420" alt="中央财经大学">
</p>

<h1 align="center">CUFE 课程论文 LaTeX 模板</h1>

<p align="center">
  <strong>中央财经大学（CUFE）课程论文 / 课程报告模板</strong>
  <br>
  XeLaTeX + Biber 编译 · GB/T 7714—2015 编号制引用
</p>

<p align="center">
  <img src="https://img.shields.io/badge/TeX-XeLaTeX-blue?logo=latex" alt="XeLaTeX">
  <img src="https://img.shields.io/badge/Biber-2.20-green?logo=biber" alt="Biber">
  <img src="https://img.shields.io/badge/Citation-GB%2FT%207714-orange" alt="GB/T 7714">
  <img src="https://img.shields.io/badge/License-MIT-lightgrey" alt="License">
</p>

---

## 特色

- 完整封面页 — 校徽、标题、学号、班级、任课教师等信息
- GB/T 7714—2015 参考文献格式（`biblatex-gb7714-2015`）
- 中文排版优化 — 宋体正文、黑体标题、楷体封面
- 章节自动编号（"一、"、"二、"）和 subsection 编号
- 图表全文连续编号，与章节无关
- 页眉自动显示论文标题
- 已配置定理、算法、代码等学术写作环境

## 快速开始

1. **克隆或下载** 本仓库

2. **填写个人信息** — 打开 `cuef_course_template.tex`，修改 `\newcommand` 部分：

```latex
\newcommand{\MYTITLE}{论文标题}
\newcommand{\MYID}{20xx310xxx}         % 学号
\newcommand{\MYNAME}{姓名}
\newcommand{\MYCLASS}{班级}
\newcommand{\MYADVISOR}{教师姓名}
\newcommand{\MYCOURSE}{课程名称}
\newcommand{\MYTERM}{20xx--20xx 第x学期}
\newcommand{\MYCOURSEID}{课程代码}
```

3. **编译**（需要 TeX 发行版 + `biblatex-gb7714-2015`）：

```bash
xelatex cuef_course_template.tex
biber cuef_course_template
xelatex cuef_course_template.tex
xelatex cuef_course_template.tex
```

> 或使用 `latexmk -xelatex cuef_course_template.tex` 一键编译。

## 环境要求

| 组件 | 说明 |
|------|------|
| TeX 发行版 | MiKTeX / TeX Live（推荐 MiKTeX 最新版） |
| 编译引擎 | XeLaTeX |
| 参考文献 | Biber + `biblatex-gb7714-2015` |
| 字体 | Times New Roman、SimSun、SimHei、KaiTi |

Windows 用户推荐安装 [MiKTeX](https://miktex.org/download)，包管理器会自动安装缺失宏包。

## 文件结构

```
cufe-course-paper-latex/
├── cuef_course_template.tex    # 模板主文件（填写个人信息后编译）
├── cuef_template.pdf           # 编译好的 PDF 预览
├── figure/
│   └── zhongcai.png            # 中央财经大学校徽
├── references/
│   └── bibs.bib                # 参考文献库（.bib 示例）
├── .gitignore                  # Git 忽略规则
└── README.md
```

## 模板结构

| 部分 | 说明 |
|------|------|
| 封面 | 校徽 + 标题 + 个人信息表（含评分栏） |
| 摘要 | 中文摘要 + 关键词 |
| 目录 | 自动生成 |
| 正文 | 四章结构（引言 / 文献综述 / 分析论证 / 结论） |
| 参考文献 | GB/T 7714 编号制，自动排序 |

## 自定义

- **修改引用格式** — 将 `style=gb7714-2015` 替换为其他标准（如 `gb7714-2015ay` 著者-年份制）
- **调整章节深度** — 修改 `\setcounter{tocdepth}{1}`（1 = 显示到 section）
- **添加附录** — 使用 `\begin{appendices} ... \end{appendices}` 环境

## 许可

本模板供中央财经大学师生自由使用、修改和分发。引用和参考文献示例来源于 ECB 治理相关学术文献，仅作格式示范。
