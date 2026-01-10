# Awesome AI4Protein [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![Protein Structure](https://img.shields.io/badge/Protein%20Structure-Prediction-blue.svg) ![AI Tools](https://img.shields.io/badge/AI%20Tools-Resources-green.svg)

精选的人工智能在蛋白质研究领域应用的资源列表

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

**任务描述**: 从氨基酸序列预测蛋白质的三维结构。

- **主要方法**: 
  - AlphaFold2/3
  - ESMFold
  - ColabFold
  - RoseTTAFold

- **评价指标**:
  - **GDT-TS (Global Distance Test - Total Score)**: 衡量预测结构与真实结构的相似性。
  - **RMSD (Root Mean Square Deviation)**: 评估预测和真实结构之间的平均差异。

#### 2. 蛋白质功能预测 (Protein Function Prediction)

**任务描述**: 根据蛋白质序列推测其生物学功能。

- **主要方法**:
  - DeepGO
  - ProtBERT
  - TAPE

- **评价指标**:
  - **准确率 (Accuracy)**: 正确预测的功能占总预测的比例。
  - **F1 Score**: 综合考虑准确率和召回率的指标。

#### 3. 蛋白质序列分析 (Protein Sequence Analysis)

**任务描述**: 分析蛋白质序列的特征和模式。

- **主要方法**:
  - BLAST
  - Clustal Omega
  - MUSCLE

- **评价指标**:
  - **比对得分 (Alignment Score)**: 序列比对的质量评分。

#### 4. 蛋白质设计 (Protein Design)

**任务描述**: 设计新的蛋白质以满足特定功能。

- **主要方法**:
  - Rosetta
  - EvoDesign

- **评价指标**:
  - **功能实现率 (Functionality Rate)**: 设计蛋白质实现预期功能的比例。

#### 5. 药物发现 (Drug Discovery)

**任务描述**: 利用AI技术加速新药的发现过程。

- **主要方法**:
  - Virtual Screening
  - QSAR Modeling

- **评价指标**:
  - **命中率 (Hit Rate)**: 有效药物的发现比例。

#### 6. 分子动力学模拟 (Molecular Dynamics Simulation)

**任务描述**: 模拟蛋白质在不同环境中的动态行为。

- **主要方法**:
  - GROMACS
  - NAMD

- **评价指标**:
  - **均方位移 (Mean Squared Displacement)**: 描述粒子运动的平均距离。

## 数据集

- **Protein Data Bank (PDB)**: 提供蛋白质三维结构的数据库。 [访问链接](https://www.rcsb.org)
- **UniProt**: 包含丰富的蛋白质序列和功能信息。 [访问链接](https://www.uniprot.org)
- **AlphaFold DB**: 提供AlphaFold预测的蛋白质结构。 [访问链接](https://alphafold.ebi.ac.uk)

## 预训练模型

- **AlphaFold**: 提供准确的蛋白质结构预测。 [访问链接](https://github.com/deepmind/alphafold)
- **ESM**: 提供高效的蛋白质序列表示。 [访问链接](https://github.com/facebookresearch/esm)

## 蛋白质结构预测

- **AlphaFold**: 该工具通过深度学习模型预测蛋白质的三维结构。它在CASP比赛中表现优异。
- **RoseTTAFold**: 另一个流行的蛋白质结构预测工具，能够处理大规模数据集。

## 蛋白质功能预测

- **DeepGO**: 利用深度学习方法进行蛋白质功能的预测，适用于大规模数据。
- **TAPE**: 提供多种模型以适应不同的功能预测任务。

## 蛋白质序列分析

- **BLAST**: 经典的序列比对工具，用于寻找相似序列。
- **MUSCLE**: 用于多序列比对，适合分析蛋白质家族。

## 蛋白质设计

- **Rosetta**: 一个强大的蛋白质设计平台，广泛用于科学研究。
- **EvoDesign**: 结合进化信息进行蛋白质设计。

## 药物发现

- **Virtual Screening**: 通过计算机辅助筛选潜在药物分子。
- **QSAR Modeling**: 量化结构与活性之间的关系。

## 分子动力学模拟

- **GROMACS**: 高效的分子动力学模拟软件，适用于生物分子。
- **NAMD**: 适合大规模系统的分子动力学模拟工具。

## 工具和软件

- **PyMOL**: 用于可视化蛋白质结构的工具。 [访问链接](https://pymol.org)
- **Chimera**: 提供高级可视化和分析功能。 [访问链接](https://www.cgl.ucsf.edu/chimera)

## 会议和期刊

- **Nature Methods**: 发表生物技术和计算生物学领域的研究。
- **Bioinformatics**: 专注于生物信息学的期刊，涵盖AI在蛋白质研究中的应用。

## 课程和教程

- **Coursera: Bioinformatics Specialization**: 提供生物信息学的全面学习资源。 [访问链接](https://www.coursera.org/specializations/bioinformatics)
- **edX: Data Science for Genomics**: 结合数据科学与基因组学的课程。 [访问链接](https://www.edx.org/professional-certificate/data-science-for-genomics)

## 博客和资源

- **Towards Data Science**: 讨论AI和生物信息学的博客。 [访问链接](https://towardsdatascience.com)
- **Nature Reviews Molecular Cell Biology**: 发表最新的生物学研究和评论。

## 贡献

欢迎任何形式的贡献。请查看[贡献指南](https://github.com/sachinkumar19/Awesome-ai4protein/releases)了解更多信息。

如需获取最新版本，请访问[发布页面](https://github.com/sachinkumar19/Awesome-ai4protein/releases)。