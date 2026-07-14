---
title: NIRS核心文献库
tags:
  - NIRS/文献库
  - NIRS/核心论文
  - fNIRS/综述
created: 2026-07-14
---

# NIRS核心文献库

本目录存放 [[脑血氧监测_NIRS_总览]] 与 [[fNIRS]] 调研相关的核心论文原文。每篇论文应逐步补充 DOI、研究问题、方法、核心结论、局限性和可回填到调研报告的位置。

## 已读取论文总表

| 序号 | 文献 | 类型 | 对应主题 | 报告回填位置 | 状态 |
|---|---|---|---|---|---|
| 1 | [[Jöbsis_1977_NIRS起点]] | 奠基论文 | 近红外无创氧合监测 | [[01_脑血氧监测系统详细调研报告#1.8 本地论文精读补充]] | 已读摘要/正文 |
| 2 | [[Delpy_1988_DPF光程测量]] | 方法论文 | DPF、飞行时间、光程 | [[01_脑血氧监测系统详细调研报告#1.8 本地论文精读补充]]、[[01_脑血氧监测系统详细调研报告#5.4 本地论文对验证体系的补充]] | 已读摘要/正文 |
| 3 | [[Patterson_1989_TD组织光学参数]] | 方法论文 | TD-NIRS、扩散近似、组织光学参数 | [[01_脑血氧监测系统详细调研报告#1.8 本地论文精读补充]]、[[01_脑血氧监测系统详细调研报告#5.4 本地论文对验证体系的补充]] | 已读摘要/结论 |
| 4 | [[Ferrari_Quaresima_2012_fNIRS历史综述]] | 综述 | fNIRS 历史、技术演进、应用场景 | [[01_脑血氧监测系统详细调研报告#7.2 本地论文对前沿判断的补充]] | 已读摘要/结论 |
| 5 | [[Scholkmann_2014_CW_fNIRS综述]] | 综述 | CW-fNIRS 仪器与方法学 | [[01_脑血氧监测系统详细调研报告#2.5 本地论文对架构分类的补充]]、[[01_脑血氧监测系统详细调研报告#7.2 本地论文对前沿判断的补充]] | 已读摘要/目录/关键段 |
| 6 | [[Matcher_1994_水吸收DPF估计]] | 方法论文 | 水吸收谱、DPF、CW 定量 | [[01_脑血氧监测系统详细调研报告#1.4 SRS]] | 已读摘要/结论/关键段 |
| 7 | [[Matcher_Cooper_1994_脱氧血红蛋白绝对定量]] | 方法论文 | Hb 绝对定量、水参考色团、二阶微分光谱 | [[01_脑血氧监测系统详细调研报告#1.4 SRS]] | 已读摘要/关键段 |
| 8 | [[Suzuki_2003_NIRO300_SRS_TOI]] | 系统论文 | SRS、TOI、NIRO-300、临床组织氧合监测 | [[01_脑血氧监测系统详细调研报告#1.4 SRS]]、[[01_脑血氧监测系统详细调研报告#5.4 本地论文对验证体系的补充]] | 已读摘要/公式/结论 |

## 论文精读卡片

### Jöbsis, 1977

- 文件：`Noninvasive, Infrared Monitoring of Cerebral and Myocardial Oxygen Sufficiency and Circulatory Parameters(科研通-ablesci.com).pdf`
- DOI：`10.1126/science.929199`
- 主题：证明 700–1300 nm 近红外窗口可用于活体组织穿透，并连续监测脑和心肌氧合相关变化。
- 核心贡献：提出近红外无创监测细胞氧合、血容量和血红蛋白氧合平衡的可行性。
- 可回填：[[NIRS基础原理]]、[[脑血氧监测_NIRS_总览]]、[[01_脑血氧监测系统详细调研报告#1.8 本地论文精读补充]]。
- 局限：早期实验系统与现代脑氧仪差距较大，细胞色素 aa3 的解释在后续研究中存在争议，应谨慎表述。

### Delpy et al., 1988

- 文件：`Estimation of optical pathlength through tissue from direct time of flight measurement(科研通-ablesci.com).pdf`
- DOI：`10.1088/0031-9155/33/12/008`
- 主题：通过皮秒光脉冲飞行时间估计组织光程。
- 核心贡献：说明组织中实际光程显著长于源探距，并给出大鼠头部光程约为头径 $5.3 \pm 0.3$ 倍的实验结果。
- 可回填：[[差分路径长度因子_DPF]]、[[修正比尔朗伯定律_MBLL]]、[[脑氧监测验证体系]]。
- 局限：动物头部与成人头部结构差异大；结果不能直接作为成人脑氧仪 DPF。

### Patterson, Chance & Wilson, 1989

- 文件：`Time resolved reflectance and transmittance for the noninvasive measurement of tissue optical properties(科研通-ablesci.com).pdf`
- DOI：`10.1364/AO.28.002331`
- 主题：时间分辨反射/透射信号用于估计组织吸收和散射系数。
- 核心贡献：基于扩散近似推导脉冲形状与 $\mu_a$、$\mu_s'$ 的关系，并用初步人体实验和蒙特卡洛仿真展示 TD 方法潜力。
- 可回填：[[时域_NIRS_TD]]、[[蒙特卡洛光传输]]、[[脑氧监测验证体系]]。
- 局限：均匀 slab 与半无限介质假设不能完全代表真实头部；早到达光子区域扩散近似可能不足。

### Ferrari & Quaresima, 2012

- 文件：`A brief review on the history of human functional near-infrared spectroscopy (fNIRS) development and fields of application.pdf`
- DOI：`10.1016/j.neuroimage.2012.03.049`
- 主题：人类 fNIRS 发展史与应用场景。
- 核心贡献：梳理 fNIRS 从单点测量到多通道脑功能成像、商业系统、无线系统和先进原型的发展脉络。
- 可回填：[[fNIRS历史]]、[[脑氧监测产品矩阵]]、[[01_脑血氧监测系统详细调研报告#7.2 本地论文对前沿判断的补充]]。
- 局限：历史综述不是算法或产品拆解，不能替代具体系统参数核验。

### Scholkmann et al., 2014

- 文件：`A review on continuous wave functional near-infrared spectroscopy and imaging instrumentation and methodology(科研通-ablesci.com).pdf`
- DOI：`10.1016/j.neuroimage.2013.05.004`
- 主题：CW-fNIRS 仪器与方法学综述。
- 核心贡献：系统总结商业 CW-fNIRS 仪器、光源、探测器、探头布局、MBLL、信号成分分离和数据分析方法。
- 可回填：[[连续波_NIRS_CW]]、[[fNIRS仪器架构]]、[[短距通道回归]]、[[01_脑血氧监测系统详细调研报告#2.5 本地论文对架构分类的补充]]。
- 局限：以 CW-fNIRS 成像为主，对临床脑氧仪厂商黑箱算法覆盖有限。

## 待补充字段模板

```markdown
## 论文标题

- 文件：
- DOI：
- PMID：
- 研究问题：
- 方法：
- 核心结论：
- 关键公式/模型：
- 实验对象/数据：
- 局限性：
- 可复现点：
- 可回填报告章节：
- 相关笔记：
```
