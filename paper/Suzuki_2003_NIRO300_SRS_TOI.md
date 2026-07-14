---
title: Suzuki 2003 NIRO300 SRS TOI
tags:
  - NIRS/SRS
  - NIRS/TOI
  - Hamamatsu/NIRO
  - paper/read
year: 2003
---

# Suzuki 2003 NIRO300 SRS TOI

## 文献信息

- 文献：Suzuki, S., Takasaki, S., Ozaki, T., & Kobayashi, Y. (2003). *A tissue oxygenation monitor using NIR spatially resolved spectroscopy*.
- 本地文件：`paper/2003Tissue oxygenation monitor using NIR spatially resolved spectroscopy.pdf`
- 关联：[[空间分辨光谱_SRS]]、[[Hamamatsu_NIRO]]、[[脑血氧监测_NIRS_总览]]

## 研究问题

如何基于 CW 光源和空间分辨光谱，在临床床旁系统中输出组织氧合指数 TOI，而不只输出 HbO/HbR 相对变化。

## 核心结论

- SRS 通过远离光源处的光衰减空间斜率 $\partial A(\rho,\lambda)/\partial \rho$ 估计吸收相关量。
- 在约化散射系数波长依赖可参数化的前提下，可求得相对吸收系数并进一步估计 $k HbO$、$k HbR$。
- TOI 使用比值 $HbO/(HbO+HbR)$，公共比例因子 $k$ 抵消，因此可在不知道绝对散射尺度时输出组织氧合指数。
- NIRO-300 使用多波长、约 5 cm 源探距、三段探测器监测斜率线性，并用仿体血气和 TRS 对照验证。

## 对课题的启发

- CW-SRS 是低成本临床脑氧原型最现实的路线之一。
- 探头设计必须保证远距离高灵敏度、局部斜率线性和光安全。
- TOI 是准绝对指标，不等于完整 HbO/HbR 绝对浓度。

## 可回填位置

- [[01_脑血氧监测系统详细调研报告#1.4 SRS]]
- [[01_脑血氧监测系统详细调研报告#2.5 本地论文对架构分类的补充]]
- [[01_脑血氧监测系统详细调研报告#5.4 本地论文对验证体系的补充]]

