# NLP实验2 LaTeX报告

主文件为 `NLP_exp2_report.tex`，配套截图位于 `figures/`。请保持整个文件夹结构一起使用。

## 编译

使用 XeLaTeX。TeXstudio 中打开主文件后，选择“选项 → 设置TeXstudio → 构建 → 默认编译器 → XeLaTeX”。文件首行也已指定 XeLaTeX。

建议连续编译两次，以更新图片、表格和参考文献的交叉引用：

```text
xelatex -interaction=nonstopmode -halt-on-error NLP_exp2_report.tex
xelatex -interaction=nonstopmode -halt-on-error NLP_exp2_report.tex
```

报告采用 `ctexart` 文档类，使用 Windows 的宋体（SimSun）、黑体（SimHei）及 Times New Roman 字体。需要电脑上安装这三种字体。常规宏包包括 graphicx、booktabs、tabularx、caption、subcaption、fvextra、newtxmath、tocloft、hyperref 等。无需启用 shell-escape，也不使用 listings 或 minted。

## 排版格式

开头仅有实验标题及自动目录，正文从下一页开始，不显示姓名、学号或课程信息。大标题为黑体三号加粗；一级标题为黑体四号加粗；二级标题为黑体四号；三级标题为宋体四号；正文为宋体小四。正文中的英文和数字为 Times New Roman，数学公式使用 Times 风格的 newtxmath。段前段后为0，行距使用 `\linespread{1.25}`，首行缩进两个汉字。图题、表题及表内文字沿用五号。截图内部文字保留原样。

图表页的图表间距已设为固定值，页面剩余空间留在页底，避免图表之间出现过大的空白。

全部10个正文表格及表题居中，所有单元格内容居中，表头统一加粗。可换行的宽列同时采用垂直居中。

## 文件与截图

- `NLP_exp2_report.tex`：完整、可编辑的LaTeX源码。
- `NLP_exp2_report.pdf`：编译后的报告。
- `figures/`：用户提供的18张PNG截图，按实验步骤命名。截图内容、尺寸和像素保持原样。
- `figures_manifest.json`：原文件名、对应内容、图片尺寸和SHA-256校验值。

18张截图均已插入正文，部分相关截图组成同一个图。正文保留教师规定的10部分结构，数值表格按运行结果整理；CBOW仅写为样本构造，负采样及层次Softmax仅写为原理分析。

少数原截图中，Jupyter的长代码行或表头已在截图时被窗口截断。报告保留原截图，同时以可编辑表格完整列出关键数值。
