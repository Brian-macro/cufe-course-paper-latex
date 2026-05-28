# 中央财经大学课程论文 LaTeX 模板

中央财经大学（CUFE）课程论文/报告 LaTeX 模板，基于 XeLaTeX + Biber 编译，采用 GB/T 7714-2015 编号制引用格式。

## 特色

- 完全符合 CUFE 课程论文格式要求
- 支持中文排版（ctex + xeCJK）
- GB/T 7714-2015 学术引用标准
- 封面页、目录、正文、参考文献完整结构

## 快速开始

1. 在 `cuef_course_template.tex` 开头的 `\newcommand` 部分填写个人信息（标题、学号、姓名、班级、课程等）
2. 使用 XeLaTeX + Biber 编译：

```bash
xelatex cuef_course_template.tex
biber cuef_course_template
xelatex cuef_course_template.tex
xelatex cuef_course_template.tex
```

## 依赖

- TeX 发行版（MiKTeX / TeX Live）
- 字体：Times New Roman、SimSun、SimHei、KaiTi
- biblatex-gb7714-2015 宏包

## 文件结构

```
├── cuef_course_template.tex   # 模板主文件
├── figure/
│   └── zhongcai.png           # 校徽
└── references/
    └── bibs.bib               # 参考文献库
```

## 许可

本模板供中央财经大学同学自由使用和修改。
