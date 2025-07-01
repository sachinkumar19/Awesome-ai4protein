# Awesome AI4Protein [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> 精选的人工智能在蛋白质研究领域应用的资源列表

这个仓库整理了AI在蛋白质研究中的最新进展，包括论文、工具、数据集、预训练模型等资源。

## 目录

- [基础知识](#基础知识)
- [数据集](#数据集)
- [预训练模型](#预训练模型)
- [蛋白质结构预测](#蛋白质结构预测)
- [蛋白质功能预测](#蛋白质功能预测)
- [蛋白质序列分析](#蛋白质序列分析)
- [蛋白质设计](#蛋白质设计)
- [药物发现](#药物发现)
- [分子动力学模拟](#分子动力学模拟)
- [工具和软件](#工具和软件)
- [会议和期刊](#会议和期刊)
- [课程和教程](#课程和教程)
- [博客和资源](#博客和资源)
- [贡献](#贡献)

## 基础知识

### 综述论文
- **Computational Protein Science in the Era of Large Language Models (LLMs)** - [[2501.10282] Computational Protein Science in the Era of Large Language Models (LLMs)](https://arxiv.org/abs/2501.10282)
- **Biological structure and function emerge from scaling unsupervised learning to 250 million protein sequences** - [PNAS 2021](https://www.pnas.org/doi/10.1073/pnas.2016239118)

### AI4Protein主要任务分类

#### 1. 蛋白质结构预测 (Protein Structure Prediction)
**任务描述**: 从氨基酸序列预测蛋白质的三维结构

- **主要方法**: AlphaFold2/3, ESMFold, ColabFold, RoseTTAFold
- **评价指标**:
  - **GDT-TS (Global Distance Test - Total Score)**: 评估全局结构相似性，使用1Å、2Å、4Å、8Å截断距离
  - **GDT-HA (Global Distance Test - High Accuracy)**: 高精度评估，使用0.5Å、1Å、2Å、4Å截断距离
  - **RMSD (Root Mean Square Deviation)**: 均方根偏差，越小越好
  - **TM-score**: 模板建模评分，>0.5表示相似拓扑结构
  - **lDDT (Local Distance Difference Test)**: 局部距离差异测试，评估局部结构质量

#### 2. 蛋白质功能预测 (Protein Function Prediction)
**任务描述**: 预测蛋白质的生物学功能，包括GO注释、酶分类等
- **主要方法**: DeepGO, GOLabeler, NetGO, ESM-based方法
- **评价指标**:
  - **CAFA评估**: Critical Assessment of Functional Annotation
  - **Precision/Recall/F1-score**: 分类性能指标
  - **AUPR (Area Under Precision-Recall curve)**: PR曲线下面积
  - **Semantic similarity**: GO术语语义相似性
  - **Matthews Correlation Coefficient (MCC)**: 马修斯相关系数

#### 3. 蛋白质序列分析 (Protein Sequence Analysis)
**任务描述**: 包括二级结构预测、接触预测、保守性分析等
- **评价指标**:
  - **Q3/Q8 accuracy**: 三态/八态二级结构预测准确率
  - **Contact prediction accuracy**: 接触预测准确率 (Top-L/5, Top-L/2, Top-L)
  - **INF (Interaction Network Fidelity)**: 相互作用网络保真度

#### 4. 蛋白质设计 (Protein Design)
**任务描述**: 设计具有特定功能的新蛋白质序列
- **主要方法**: ProteinMPNN, RFDiffusion, ESMFold, AlphaFold3
- **评价指标**:
  - **Designability**: 可设计性评估
  - **Structural feasibility**: 结构可行性
  - **Functional validation**: 功能验证指标
  - **Novelty and diversity**: 新颖性和多样性

#### 5. 蛋白质相互作用预测 (Protein-Protein Interaction)
**任务描述**: 预测蛋白质间的相互作用界面和亲和力
- **评价指标**:
  - **Interface RMSD**: 相互作用界面RMSD
  - **DockQ Score**: 对接质量综合评分
  - **CAPRI评估**: Critical Assessment of PRotein Interactions

#### 6. 蛋白质-配体结合预测 (Protein-Ligand Binding)
**任务描述**: 预测小分子与蛋白质的结合模式和亲和力
- **评价指标**:
  - **Binding affinity prediction**: 结合亲和力预测准确性
  - **Pose prediction accuracy**: 结合构象预测准确性
  - **RMSD of ligand pose**: 配体构象RMSD

### 入门资料

## 数据集

### 蛋白质结构数据库
- **[PDB (Protein Data Bank)](https://www.rcsb.org/)** - 最权威的蛋白质3D结构数据库
- **[AlphaFold DB](https://alphafold.ebi.ac.uk/)** - DeepMind的AlphaFold预测结构数据库
- **[CATH](https://www.cathdb.info/)** - 蛋白质结构分类数据库

### 蛋白质序列数据库
- **[UniProt](https://www.uniprot.org/)** - 蛋白质序列和功能信息数据库
- **[Pfam](http://pfam.xfam.org/)** - 蛋白质家族数据库
- **[InterPro](https://www.ebi.ac.uk/interpro/)** - 蛋白质功能分析数据库

### 专用数据集

- **[ProteinNet](https://github.com/aqlaboratory/proteinnet)** - 标准化的蛋白质结构预测数据集
- **[TAPE](https://github.com/songlab-cal/tape)** - 蛋白质评估任务数据集

## 预训练模型

### 蛋白质语言模型
- **[ESM (Evolutionary Scale Modeling)](https://github.com/facebookresearch/esm)** - Meta的蛋白质语言模型
- **[ProtBERT](https://huggingface.co/Rostlab/prot_bert)** - 基于BERT的蛋白质模型
- **[ProtTrans](https://github.com/agemagician/ProtTrans)** - 蛋白质序列的Transformer模型
- **[ProteinLM](https://github.com/BytedProtein/ByProt)** - 字节跳动的蛋白质语言模型

### 结构预测模型
- **[AlphaFold2](https://github.com/deepmind/alphafold)** - DeepMind的蛋白质结构预测模型
- **[ColabFold](https://github.com/deepmind/alphafold)** - AlphaFold的快速实现版本
- **[ChimeraX AlphaFold](https://www.rbvi.ucsf.edu/chimerax/features.html#alphafold)** - 结构可视化工具

## 蛋白质结构预测

### 最新论文
- **AlphaFold: a solution to a 50-year-old grand challenge in biology** - Nature 2021
- **Highly accurate protein structure prediction with AlphaFold** - Nature 2021
- **ColabFold: making protein folding accessible to all** - Nature Methods 2022
- **Improved protein structure prediction using potentials from deep learning** - Nature 2020
- **ProSST: Protein Language Model for Protein Sequencing and Structure-based Tasks** - [NeurIPS 2024](https://neurips.cc/virtual/2024/poster/94722)

### 工具和方法
- **[AlphaFold2](https://github.com/deepmind/alphafold)** - 最先进的结构预测方法
- **[ColabFold](https://colab.research.google.com/github/deepmind/alphafold/blob/main/notebooks/AlphaFold.ipynb)** - 在线AlphaFold服务
- **[ChimeraX](https://www.cgl.ucsf.edu/chimerax/)** - 蛋白质结构可视化
- **[PyMOL](https://pymol.org/2/)** - 分子可视化软件

## 蛋白质功能预测

### 方法和工具
- **[DeepGO](https://github.com/bio-ontology-research-group/deepgo)** - 基于深度学习的GO功能预测
- **[GOLabeler](https://github.com/jianlin-cheng/GOLabeler)** - 蛋白质功能标注工具
- **[NetGO](https://github.com/davidchyou/NetGO)** - 网络增强的GO预测

### 相关论文
- **Deep learning for protein function prediction** - Current Opinion in Structural Biology 2019
- **GOLabeler: improving sequence-based large-scale protein function prediction** - Bioinformatics 2020
- **Language models enable zero-shot prediction of the effects of mutations on protein function** - [NeurIPS 2021](https://proceedings.neurips.cc/paper/2021/hash/f51338d736f95dd42427296047067694-Abstract.html)
- **Predicting a Protein's Stability under a Million Mutations** - [NeurIPS 2023](https://proceedings.neurips.cc/paper_files/paper/2023/hash/84b4b5cbb0388e48d143fa1c0acb2e4b-Abstract-Conference.html)
- **Zero-shot prediction of mutation effects with multimodal deep representation learning guides protein engineering** - [Cell Research 2024](https://www.nature.com/articles/s41422-024-00986-w)
- **DDMut: predicting effects of mutations on protein stability using deep learning** - [Nucleic Acids Research 2023](https://academic.oup.com/nar/article/51/W1/W122/7160066)
- **ESM-Effect: Predicting Mutation Effects with Evolution-Scale Models** - [ICLR 2025](https://openreview.net/forum?id=ESM-Effect)
- **DDMut-PPI: predicting effects of mutations on protein–protein interactions using graph-based deep learning** - [Nucleic Acids Research 2024](https://academic.oup.com/nar/article/52/W1/W122/7571080)

## 蛋白质序列分析

### 进化分析
- **[MSA Transformer](https://github.com/facebookresearch/esm)** - 多序列比对的Transformer模型
- **[EVcouplings](https://github.com/debbiemarkslab/EVcouplings)** - 进化耦合分析
- **MSA Transformer** - [ICML 2021](https://proceedings.mlr.press/v139/rao21a.html)

### 序列设计
- **[ProteinGAN](https://github.com/Biomatter-Designs/ProteinGAN)** - 基于GAN的蛋白质设计
- **[SeqDesign](https://github.com/programmablebio/seqdesign)** - 序列设计工具

## 蛋白质设计

### 设计方法
- **[RFDiffusion](https://github.com/RosettaCommons/RFDiffusion)** - 基于扩散模型的蛋白质设计
- **[ProteinMPNN](https://github.com/dauparas/ProteinMPNN)** - 基于消息传递的蛋白质设计
- **[ESMFold](https://github.com/facebookresearch/esm)** - Meta的蛋白质折叠和设计

### 最新研究
- **Robust deep learning-based protein sequence design using ProteinMPNN** - Science 2022
- **De novo protein design by deep network hallucination** - Nature 2021
- **Self-play reinforcement learning guides protein engineering** - [Nature Machine Intelligence 2023](https://www.nature.com/articles/s42256-023-00691-9)
- **ProteinZero: Self-Improving Protein Generation via Online Reinforcement Learning** - [arXiv 2025](https://arxiv.org/abs/2501.08437)
- **A general temperature-guided language model to design proteins of enhanced stability and activity** - [Science Advances 2024](https://www.science.org/doi/10.1126/sciadv.adn6447)

## 药物发现

### 分子对接
- **[AutoDock](http://autodock.scripps.edu/)** - 分子对接软件
- **[Smina](https://sourceforge.net/projects/smina/)** - 快速分子对接
- **[DeepChem](https://github.com/deepchem/deepchem)** - 深度学习药物发现框架

### 药物设计
- **[RDKit](https://github.com/rdkit/rdkit)** - 化学信息学工具包
- **[OpenEye](https://www.eyesopen.com/)** - 药物设计软件套件

## 分子动力学模拟

### 模拟软件
- **[GROMACS](http://www.gromacs.org/)** - 分子动力学模拟包
- **[AMBER](https://ambermd.org/)** - 生物分子模拟软件
- **[NAMD](https://www.ks.uiuc.edu/Research/namd/)** - 可扩展分子动力学

### AI增强模拟
- **[DeePMD-kit](https://github.com/deepmodeling/deepmd-kit)** - 深度学习分子动力学
- **[TorchMD](https://github.com/torchmd/torchmd)** - PyTorch分子动力学

## 工具和软件

### 开发框架
- **[BioPython](https://biopython.org/)** - Python生物信息学工具包
- **[MDAnalysis](https://www.mdanalysis.org/)** - 分子动力学分析
- **[ProDy](http://prody.csb.pitt.edu/)** - 蛋白质动力学分析

### 可视化工具
- **[ChimeraX](https://www.cgl.ucsf.edu/chimerax/)** - 分子可视化
- **[VMD](https://www.ks.uiuc.edu/Research/vmd/)** - 分子可视化和分析
- **[3Dmol.js](https://3dmol.csb.pitt.edu/)** - 基于Web的分子可视化

## 会议和期刊

### 顶级会议
- **[RECOMB](http://recomb.org/)** - 计算分子生物学研究
- **[ISMB](https://www.iscb.org/ismb2024)** - 智能系统分子生物学
- **[NeurIPS](https://neurips.cc/)** - 神经信息处理系统
- **[ICML](https://icml.cc/)** - 国际机器学习会议

### 重要期刊
- **Nature** - 自然科学综合期刊
- **Science** - 科学综合期刊
- **Cell** - 细胞生物学期刊
- **Nature Methods** - 自然方法学期刊
- **Bioinformatics** - 生物信息学期刊
- **PNAS** - 美国国家科学院院刊

## 课程和教程

### 在线课程
- **[Stanford CS229 Machine Learning](http://cs229.stanford.edu/)** - 机器学习基础
- **[MIT Computational Biology](https://ocw.mit.edu/courses/biology/)** - 计算生物学
- **[Coursera Bioinformatics](https://www.coursera.org/specializations/bioinformatics)** - 生物信息学专业课程

### 教程资源
- **[EMBL-EBI Training](https://www.ebi.ac.uk/training/)** - 欧洲生物信息学培训
- **[Rosalind](http://rosalind.info/)** - 生物信息学编程练习

## 博客和资源

### 技术博客
- **[DeepMind Blog](https://deepmind.com/blog)** - DeepMind技术博客
- **[Papers with Code](https://paperswithcode.com/area/biology)** - 生物学相关论文和代码

### 社区资源
- **[r/bioinformatics](https://www.reddit.com/r/bioinformatics/)** - Reddit生物信息学社区
- **[Biostars](https://www.biostars.org/)** - 生物信息学问答社区

## 贡献

欢迎对这个列表做出贡献！

### 贡献方式

1. Fork 这个仓库
2. 创建你的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交你的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

## 许可证

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情。

## 致谢

感谢所有为蛋白质研究和人工智能领域做出贡献的研究者和开发者们。

---

⭐ 如果这个列表对您有帮助，请给我们一个 star！

📧 有问题或建议？请创建一个 [issue](../../issues)。
