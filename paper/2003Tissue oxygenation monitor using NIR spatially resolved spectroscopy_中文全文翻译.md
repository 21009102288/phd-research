# 使用近红外空间分辨光谱的组织氧合监测仪

> 原文：Susumu Suzuki, Sumio Takasaki, Takeo Ozaki, Yukio Kobayashi. *A Tissue Oxygenation Monitor using NIR Spatially Resolved Spectroscopy*. Hamamatsu Photonics K.K., SPIE Vol. 3597, 582–592, San Jose, January 1999.
>
> 说明：本地 PDF 文件名以“2003”开头，但原文首页明确标注会议时间为 1999 年 1 月，因此本文献按 1999 年著录。以下译文按原文结构完整翻译；公式符号依据 PDF 文本层与页面核对后整理。图、曲线和坐标仍以原 PDF 为准。

## 摘要

我们研制了一种新的临床组织氧合监测仪 NIRO-300。除监测血红蛋白浓度变化和细胞色素氧化酶氧化还原状态外，该仪器还可利用近红外空间分辨光谱（spatially resolved spectroscopy, SRS）测量组织氧合指数（tissue oxygenation index, TOI）。TOI 定义为氧合组织血红蛋白占组织总血红蛋白的比例。

SRS 在远离入射光点的位置测量光衰减随距离变化的斜率，并基于光子扩散理论计算 TOI。仪器采用 4 个激光二极管作为光源，照射皮肤的激光属于 IEC 825 规定的 1 类激光。探测端使用高增益、低噪声放大器，因此发射器—探测器间距可以达到约 5 cm。

为评价 NIRO-300 测得的 TOI，我们在含 Intralipid 和血液的仿体中，将其结果与血气分析仪测得的血氧饱和度（SO2）进行比较；同时还在人前臂上，将 NIRO-300 与基于时间分辨光谱（time-resolved spectroscopy, TRS）的 NIRS 仪器进行同步测量。两类实验中，TOI 均与血气分析仪或 TRS 仪器给出的结果高度相关，表明 TOI 有望用于临床测量。

**关键词：** 空间分辨光谱；组织氧合指数

## 1. 引言

自第一项发明以来，组织近红外光谱（NIRS）已有二十余年的发展历史，并已成为研究组织氧供、脑血流动力学等问题的成熟工具。基于修正 Beer–Lambert 法（MBL）、时间分辨光谱（TRS）、相位分辨光谱（PRS）和空间分辨光谱（SRS）等方法的多种 NIRS 仪器已经被开发出来。其中，MBL 和 SRS 均使用连续波（continuous wave, CW）光源；与另外两类方法相比，它们在成本和临床实用性方面更有优势。

我们此前已开发出采用 MBL 方法的 NIRO-500。它可测量氧合血红蛋白浓度变化 ΔO2Hb、脱氧血红蛋白浓度变化 ΔHHb、组织总血红蛋白浓度变化 ΔcHb（ΔcHb = ΔO2Hb + ΔHHb），以及细胞色素氧化酶氧化还原状态变化 ΔCtOx。NIRO-500 已在多家医院使用，主要用于心脏手术期间的脑氧合监测。

但是，NIRO-500 只能测量相对于任意起始点的浓度变化，因此其应用主要限于“变化本身即可作为诊断参数”的场景。临床一直希望在浓度变化之外，还能获得一种可在床旁测量的组织氧合绝对指标。近期已有一套 SRS 原型机实现了组织血红蛋白绝对饱和度测量，并显示出床旁应用的可行性。

在评估 SRS 原型机结果并继承 NIRO-500 技术的基础上，我们开发了新的临床组织氧合监测仪 NIRO-300。它利用 MBL 测量 ΔO2Hb、ΔHHb、ΔcHb 和 ΔCtOx，同时利用 SRS 测量组织氧合指数 TOI（O2Hb/cHb）。本文介绍仪器的技术特征、仿体实验结果，以及与 TRS 仪器进行的一项基础人体研究。

## 2. 测量理论

高散射介质中的光子传播可用扩散近似描述。对于半无限半空间几何，脉冲 δ 函数输入下的光子扩散方程解为：

$$
R(\rho,t)=(4\pi Dct)^{-3/2}\exp(-\mu_a ct)\exp\left[-\frac{\rho^2+\mu_s'^{-2}}{4Dct}\right]
\tag{1}
$$

其中，$R$ 为反射光强；$\rho$ 和 $t$ 分别为距脉冲入射点的空间距离和时间；$\mu_a$ 与 $\mu_s'$ 分别为吸收系数和约化散射系数；$D=1/[3(\mu_a+\mu_s')]$ 为扩散系数；$c$ 为介质中的光速。

对于 CW 光，光强 $I(\rho)$ 是 $R(\rho,t)$ 对时间的积分。将光衰减 $A(\rho)$ 定义为 $I(\rho)$ 的负常用对数：

$$
A(\rho)=-\log_{10}\int R(\rho,t)\,dt
\tag{2}
$$

### 2.1 浓度变化的测量

根据 $A$ 的数学恒等关系，可得：

$$
\Delta A=L\,\Delta\mu_a
\tag{3}
$$

其中 $L$ 称为差分光程。式（3）给出了 MBL 方法的原理：在若干波长下测量光衰减变化 $\Delta A$，并已知 $L$ 时，可以计算吸收系数变化 $\Delta\mu_a$。随后利用 $\mu_a=\varepsilon C$ 的关系得到浓度变化 $\Delta C$，即 $\Delta C=(1/L)\varepsilon^{-1}\Delta A$，其中 $\varepsilon$ 表示被测组分的摩尔消光系数。

NIRO-300 采用 4 个波长测量 3 个组分，即 ΔO2Hb、ΔHHb 和 ΔCtOx，并用最小二乘法计算：

$$
\begin{bmatrix}
\Delta O_2Hb\\
\Delta HHb\\
\Delta CtOx
\end{bmatrix}
=\frac{1}{L}[\varepsilon]^{-1}
\begin{bmatrix}
\Delta A(\lambda_1)\\
\Delta A(\lambda_2)\\
\Delta A(\lambda_3)\\
\Delta A(\lambda_4)
\end{bmatrix}
\tag{4}
$$

其中被测组分为 O2Hb、HHb 和 CtOx，波长为 $\lambda_1$ 至 $\lambda_4$。典型波长为 775、810、850 和 905 nm；$[\varepsilon]$ 是各组分在各波长处的摩尔消光系数矩阵。

差分光程 $L$ 在解析上等于光速 $c$ 与平均飞行时间 $\bar T$ 的乘积：

$$
L=\frac{\partial A}{\partial\mu_a}=c\bar T,\qquad
\bar T=\frac{\int tR(\rho,t)dt}{\int R(\rho,t)dt}
\tag{5}
$$

因此，如果使用条纹相机等超高速光探测器测量 $R(\rho,t)$，便可根据时间分布求出 $\bar T$，并由 $L=c\bar T$ 得到差分光程。已有研究报告了人前额、手臂和腿等组织中 $L$ 的典型值。即使无法确定 $L$，仍可以测量以 $L\Delta C$ 表示的相对浓度变化，而非绝对 $\Delta C$。

### 2.2 TOI 的测量

对 $A(\rho)$ 关于 $\rho$ 求导，可得 SRS 的基本关系：

$$
\frac{\partial A}{\partial\rho}
=\frac{1}{\ln 10}\left[\sqrt{3\mu_a\mu_s'}+\frac{2}{\rho}\right]
\tag{6}
$$

SRS 在多个波长下测量 $\partial A/\partial\rho$，再由式（6）计算相对吸收信息。一阶近似下，在近红外波段可将 $\mu_s'(\lambda)$ 看作常数 $k$，从而得到相对吸收系数 $k\mu_a(\lambda)$，并进一步得到相对浓度 $kO_2Hb$ 和 $kHHb$。因为 TOI 是 O2Hb 与 O2Hb + HHb 的比值，公共比例因子 $k$ 会相消。

实际上，$\mu_s'(\lambda)$ 会随波长略微下降，可表示为：

$$
\mu_s'(\lambda)=k(1-h\lambda)
$$

其中 $h$ 是 $\mu_s'$ 随波长变化的归一化斜率。作者认为该参数在不同组织类型和不同受试者之间相对稳定，将其加入计算可以提高准确度。因此：

$$
k\mu_a(\lambda)=
\frac{1}{3(1-h\lambda)}
\left[\ln 10\frac{\partial A(\lambda)}{\partial\rho}-\frac{2}{\rho}\right]^2
\tag{7}
$$

仪器使用 3 个波长和 $h=6.3\times10^{-4}\ \mathrm{nm}^{-1}$ 来测量 $kO_2Hb$ 与 $kHHb$，并通过最小二乘法求解：

$$
\begin{bmatrix}
kO_2Hb\\
kHHb
\end{bmatrix}
=[\varepsilon]^{-1}
\begin{bmatrix}
k\mu_a(\lambda_1)\\
k\mu_a(\lambda_2)\\
k\mu_a(\lambda_3)
\end{bmatrix}
\tag{8}
$$


最终：

$$
TOI=\frac{O_2Hb}{O_2Hb+HHb}
=\frac{kO_2Hb}{kO_2Hb+kHHb}
$$

## 3. 仪器设计

仪器的关键部件是探头（图 1）。其设计遵循以下原则。

### （a）高灵敏度

为了相对于表层区域获取更多脑组织信息、提高脑监测可靠性，应尽可能增大发射器—探测器间距。因此探测器灵敏度被设计为：即使发射端采用下述低功率照射，在大多数情况下仍可实现约 5 cm 的间距。

### （b）安全的激光照射

考虑到新生儿、长期监测以及激光意外照射眼睛等场景，照射功率被限制在 IEC 825 定义的 1 类激光范围内。

### （c）准确测量 $\partial A/\partial\rho$

1. 斜率测量区域较小，仅约 8 mm × 8 mm，并且与发射器相距约 5 cm，因此较少受到头部几何形状或表面不均匀性的影响。
2. 理论上两个传感器即可测量 $\partial A/\partial\rho$，但 $A$ 随 $\rho$ 线性变化是 SRS 成立的前提，因此仪器采用 3 个传感器持续监测线性度。
3. 为了在不扭曲空间分布的情况下将皮肤表面的光传送到传感器，探测器入射窗采用光纤面板（fiber optic plate, FOP）。

**图 1：探头示意图。** 三个探测段的总跨度约 8 mm，单个传感器宽度约 2 mm；发射器到探测阵列距离 $d$ 约 5 cm。

整机框图见图 2，由探头、测量单元（measurement unit, MU）和显示单元（display unit, DU）组成。探头线缆长约 2 m，并连接至 MU。一个 DU 可连接两个 MU，从而在两个位置同时测量。

仪器采用脉冲激光二极管作为光源，典型波长为 775、810、850 和 905 nm。各波长依次通过由光纤束构成的发射器照射皮肤。每个激光脉冲宽度约 100 ns，每个波长的重复频率约 2 kHz；照射到皮肤的总平均功率约 1 mW，属于 1 类激光。

如图 1 所示，探测器使用三段 PIN 光电二极管。TOI 所需的空间斜率由三个光电二极管共同测得；O2Hb 等浓度变化所需的 $\Delta A$ 则由中间光电二极管测量。各光电二极管产生的光电流经高增益、低噪声放大器放大。放大器的均方根噪声折算为探测器入射光子数，约为每个激光脉冲 1000 个光子。

每个激光脉冲对应的放大器输出进入 A/D 转换器，再传输至 CPU；CPU 按预设时间窗口执行信号累加与平均。CPU 还监测并控制每个激光二极管的输出功率：测量开始前，它会针对被测对象自动设定最优激光功率；测量过程中，若探测光量超出或低于探测范围，也会自动调节功率，使探测光量回到有效范围。计算还会校正激光输出功率漂移所造成的数据漂移。

最终，ΔO2Hb、ΔHHb、ΔcHb、ΔCtOx 和 TOI 实时显示在屏幕上，并同时提供数字与模拟输出。

**图 2：仪器框图。** 光源驱动与激光二极管通过发射光纤向组织送光；三段 PIN 光电二极管、放大器、A/D 和 CPU 构成探测与计算链路；结果传到显示单元并输出数据。

## 4. 仪器评价实验

### 4.1 仿体测量

#### 4.1.1 TOI

为验证 SRS 得到的 TOI 的准确性，作者使用含人全血、Intralipid 和水（0.96% Dulbecco PBS）的仿体，同时用 NIRO-300 和血气分析仪（NOVA Biomedical STAT Profile 2）测量。图 3 给出了实验装置和所用仿体 P1–P6。

仿体容器置于恒温水槽中，温度维持在 37 ℃。通过加入酵母消耗氧气，并通过 O2 鼓泡提高氧合水平。NIRO-300 探头套入薄壁乳胶护套以防水，然后放入仿体中连续监测 TOI；实验人员定期抽取少量仿体液体，用血气分析仪测量 SO2。

P1–P6 由三种 Intralipid 浓度（0.5%、1.0%、1.5%）与两种血液条件组合而成，用于覆盖不同散射和吸收条件。

**图 3：仿体实验装置与 P1–P6 的组成。** 仿体位于黑色遮光容器和恒温水槽中，NIRO-300 连续测量 TOI，同时定期取样做血气分析。

图 4 给出了 P5 仿体中 TOI 和 SO2 随时间变化的典型结果。加入酵母前，氧合水平接近 100%；加入酵母后，由于酵母耗氧，氧合水平逐渐降至一定程度；开始 O2 鼓泡后，氧合水平恢复到初始水平。图中 TOI 与 SO2 的变化高度一致。

图 5 汇总了 P1–P6 全部仿体中 TOI 与 SO2 的相关性。在不同仿体条件下，两者均表现出很高的一致性；图中代表性回归结果包括 $y=0.96x+4.23, R^2=0.99$ 和 $y=0.97x+0.96, R^2=0.99$。这些结果表明，至少在均匀介质中，NIRO-300 能给出准确的 TOI；这也是此类仪器进入真实组织测量前必须满足的基本条件。

#### 4.1.2 浓度变化

在仿体实验中，ΔO2Hb 与 ΔHHb 出现大幅变化；理想情况下，ΔcHb 和 ΔCtOx 不应变化。因此，观察 ΔcHb 和 ΔCtOx 是否保持稳定，可以评价算法有效性，尤其可以评估血红蛋白信号串扰到细胞色素通道的程度。

图 6 给出了与图 4 同一次实验中的 ΔO2Hb、ΔHHb、ΔcHb 和放大 10 倍显示的 ΔCtOx。尽管 ΔO2Hb 与 ΔHHb 变化很大，ΔcHb 与 ΔCtOx 仍相对稳定。实际观测到，ΔcHb 和 ΔCtOx 的变化幅度分别约为 ΔO2Hb（或 −ΔHHb）变化幅度的 5% 和 1%。作者据此认为，数据失真和通道串扰处于与既有仿真结果相符的合理范围内。

### 4.2 人体前臂测量

为验证人体组织中 TOI 的有效性，作者用 NIRO-300 与一套 TRS 仪器进行同步测量。TRS 仪器使用 780 nm 和 830 nm 脉冲激光二极管，产生脉宽 50 ps、重复频率 5 MHz 的光脉冲。组织透射光由时间相关光子计数（time-correlated photon counting, TCPC）系统探测，以获得到达光的时间分布。

测得的时间分布用式（1）的理论曲线拟合，得到两个波长下的绝对 $\mu_a$ 与 $\mu_s'$，随后计算 O2Hb、HHb 及 SO2（等价的氧合比值指标）。

图 7 给出了实验装置。NIRO-300 与 TRS 探头彼此相邻地固定在前臂上，上臂放置血压袖带。袖带分别充压至 200 mmHg 和 90 mmHg，用于观察动脉阻断和静脉阻断时 NIRO-300 的 TOI 与 TRS 的 SO2。

**图 7：人体组织同步测量装置。** 两套探头相邻放置在前臂，上臂袖带用于实施动脉或静脉阻断。

图 8 显示：

- 动脉阻断（200 mmHg）期间，TOI 约从 55% 降至 15%；解除袖带后立即反弹，最高约 70%，随后在数分钟内回到基线。
- 静脉阻断（90 mmHg）期间，TOI 下降约 10%；解除后反弹较小，并在约 1 min 内恢复到初始值。
- 两类实验中，TRS 与 NIRO-300 的动态结果均表现出良好一致性。

TRS 的主要优势是能够在不依赖 $\mu_s'$ 假设的情况下测量绝对浓度，因此其 SO2 也无需预设 $\mu_s'$。相比之下，NIRO-300 的 TOI 计算采用了式（7）中的散射谱假设。尽管如此，本实验中 TOI 与 TRS-SO2 高度吻合，因此作者认为用于 TOI 计算的散射假设在该测量条件下是合理的。

## 5. 结论

作者开发了新的临床组织氧合监测仪 NIRO-300。它通过 MBL 测量 ΔO2Hb、ΔHHb、ΔcHb 和 ΔCtOx，通过 SRS 测量 TOI。

在多个仿体中，NIRO-300 与血气分析仪对照后给出了准确的 TOI；血红蛋白信号向细胞色素通道的串扰也处于作者认为合理的范围内。人体前臂上，NIRO-300 与 TRS 仪器同步测量得到的两组氧合指标高度相关，支持 TOI 在人体组织测量中的可用性。

不过，多层组织结构对 NIRS 测量的影响仍是共同难题。作者指出，进一步研究多层结构影响，有望继续提高测量准确性。

## 参考文献

1. Jöbsis FF. “Non-invasive infrared monitoring of cerebral and myocardial oxygen sufficiency and circulatory parameters.” *Science*, 198, 1264–1267, 1977.
2. Cope M, Delpy DT. “A system for long-term measurement of cerebral blood and tissue oxygenation in newborn infants by near-infrared transillumination.” *Medical & Biological Engineering & Computing*, 26, 289–294, 1988.
3. Miwa M, Ueda Y, Chance B. “Development of time resolved spectroscopy system for quantitative non-invasive tissue measurement.” *Proceedings of SPIE*, 2389, 142–149, 1995.
4. Duncan A, Whitlock TL, Cope M, Delpy DT. “A multiwavelength, wideband, intensity modulated optical spectrometer for near infrared spectroscopy and imaging.” *Proceedings of SPIE*, 1888, 248–257.
5. Matcher SJ, Kirkpatrick P, Nahid K, Cope M, Delpy DT. “Absolute quantification methods in tissue near infrared spectroscopy.” *Proceedings of SPIE*, 2389, 486–495, 1993.
6. du Plessis AJ, Newburger J, Jonas RA, et al. “Cerebral oxygenation supply and utilization during infant cardiac surgery.” *Annals of Neurology*, 37, 488–497, 1995.
7. Nollert G, Möhnle P, Tassani-Prell P, et al. “Postoperative neuropsychological dysfunction and cerebral oxygenation during cardiac surgery.” *Thoracic and Cardiovascular Surgeon*, 43, 260–264, 1995.
8. Patterson MS, Chance B, Wilson BC. “Time resolved reflectance and transmittance for the noninvasive measurement of tissue optical properties.” *Applied Optics*, 28, 2331–2336, 1989.
9. Delpy DT, Cope M, van der Zee P, et al. “Estimation of optical pathlength through tissue from direct time of flight measurement.” *Physics in Medicine and Biology*, 33(12), 1433–1442, 1988.
10. van der Zee P, Cope M, Arridge S, et al. “Experimentally measured optical pathlength for the adult head, calf and forearm and the head of newborn infants as a function of interoptode spacing.” *Advances in Experimental Medicine and Biology*, 316, 143–153, 1992.
11. Matcher SJ, Cope M, Delpy DT. “In vivo measurements of the wavelength dependence of tissue scattering coefficients between 760 and 900 nm measured with time resolved spectroscopy.” *Applied Optics*, 36, 386–396, 1997.
12. Matcher SJ, Elwell CE, Cooper CE, Cope M, Delpy DT. “Performance comparison of several published tissue near-infrared spectroscopy algorithms.” *Analytical Biochemistry*, 227, 54–68, 1995.

## 译者核对说明

- 原 PDF 的部分公式和图中字符存在 OCR 错位；本译文根据上下文恢复了 SRS、MBL、TOI、$\mu_a$、$\mu_s'$、$\partial A/\partial\rho$ 等符号。
- 图 5 的六个回归子图在文本层中提取不完整，因此仅列出 PDF 中可清楚核验的代表性回归式；不据此虚构其余参数。
- 原文人体实验仅描述前臂袖带阻断，没有报告受试者数量、年龄、重复次数和统计区间；这些信息不能从当前 PDF 补出。
