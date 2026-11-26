# 北航大科学装置研究院硕士开题 LaTeX 模板

为北京航空航天大学大科学装置研究院硕士研究生准备的开题报告和文献综述模板。两份文档独立编译，共用封面信息与参考文献库，支持学术硕士和专业硕士。模板依据研究院提供给 2025 级硕士生的 Word 样式和 2026 年 10 月修订细则整理。提交格式请以本届学院通知为准。

**[下载完整 ZIP](buaa-master-proposal-latex.zip)** · [开题报告 PDF](examples/master-proposal.pdf) · [文献综述 PDF](examples/master-review.pdf)

ZIP 内含完整 LaTeX 源码、填写说明和两份已编译的 PDF。也可以直接克隆本仓库，在根目录编译。

## 填写和编译

1. 修改 [metadata.tex](metadata.tex)，填写题目、姓名、学号、专业和导师等信息。学硕使用 `\MasterProfessionalfalse`，专硕改为 `\MasterProfessionaltrue`。
2. 开题报告的摘要和正文在 [proposal/](proposal/)，文献综述的摘要和正文在 [review/](review/)。实际引用的文献填入 [references.bib](references.bib)，正文用 `\cite{条目键}` 引用。
3. 使用 TeX Live 或 MacTeX，在源码目录分别编译两份文档。`latexmk` 会自动运行 BibTeX 并更新目录、图表清单和交叉引用。

   ```sh
   latexmk -xelatex master-proposal.tex
   latexmk -xelatex master-review.tex
   ```

编译会生成 `master-proposal.pdf` 和 `master-review.pdf`。本地未安装宋体、黑体、华文行楷或 Times New Roman 时，模板会使用 TeX Live 自带的替代字体。研究叙述、图表和参考文献条目均为写作示例，提交前请替换为自己的内容。

## 排版与材料要求

| 项目 | 开题报告 | 文献综述 |
| --- | --- | --- |
| 内容 | 选题依据、研究目标与研究内容、拟采用的研究方案、可行性分析、预期目标与成果、论文进度安排 | 绪论、各研究分支的现状与趋势、结论 |
| 字数 | 不少于 10,000 字 | 不少于 5,000 字 |
| 分页 | 中英文摘要和正文章首从奇数页开始 | 中英文摘要从奇数页开始，正文各章另页开始 |
| 示例 | 技术路线图、公式和论文进度三线表，可选主要符号表和缩略语说明 | 研究现状归纳图、对比三线表及文献引用 |

学院细则要求学硕阅读文献至少 50 篇，其中精读外文至少 30 篇。工程硕士至少阅读相关文献 50 篇。两份文档均采用 A4、正文四边 25 mm，前置部分以罗马数字编号，正文从阿拉伯数字 1 起。图表分别连续编号，参考文献采用顺序编码和上标引用。

## 来源

本项目为个人整理版，封面和文档结构依据大科学装置研究院的开题报告及硕士文献综述 Word 模板。通用排版细节可参照北航研究生院发布的学位论文规范。参考文献样式基于 Zeping Lee 的 GB/T 7714 BibTeX 样式改编，许可条款保留在 `.bst` 文件头。校徽来自学院 Word 模板。[研究生院规范](https://graduate.buaa.edu.cn/info/1275/10411.htm) · [学院 2025 级开题指导](https://piqs.buaa.edu.cn/info/1039/2769.htm) · [GB/T 7714 样式](https://github.com/zepinglee/gbt7714-bibtex-style)
