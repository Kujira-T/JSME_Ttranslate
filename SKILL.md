---
name: jsme-translate
description: >-
  国际暖通与通风风管技术规范翻译工具（支持 DW/144、DW/143、SMACNA、ISO 15138 海上油气暖通、ASTM 板材标准等）。
  当用户需要翻译通风管道施工、风管漏风量测试、海上平台 HVAC、钣金制造与材料检验等技术规范、工程规格书，
  或要求进行专业技术中英双语对照翻译与术语本地化时使用本技能。
---

# 国际风管与暖通工程标准翻译规范 (JSME_Translate)

本技能专为**通风空调风管制造、漏风量测试、海上石油天然气平台 HVAC 以及钣金工程材料**等专业标准设计，重点支持：
* **BESA DW/144**（金属风管制造与安装规范：低压、中压、高压风管系统）
* **BESA DW/143**（风管系统漏风量测试实用指南）
* **SMACNA**（美国暖通空调与钣金承包商协会：金属与柔性风管施工标准、漏风测试手册）
* **ISO 15138**（石油与天然气工业 — 海上生产装置 — 采暖、通风与空调 HVAC）
* **ASTM 材料标准**（镀锌钢板 ASTM A653、不锈钢板 ASTM A240、ASTM A15 等材料与涂层标准）

---

## 一、核心翻译准则

### 1. 规范条款语气词的法律与验收效力对等
工程与国际规范中语气词具有强制验收效力，必须严格翻译：
* **Shall / Must** $\rightarrow$ **必须 / 应**（强制性、法定合格判定项）
* **Should / Recommended** $\rightarrow$ **宜 / 建议**（推荐性、良好工程实践）
* **May / Permitted** $\rightarrow$ **可以 / 得**（允许采用的备选方案）
* **Shall not / Prohibited** $\rightarrow$ **严禁 / 不得**（绝对禁止项）

### 2. 标准体系与专有名词精准映射
* **英国 BESA 标准体系 (DW/144, DW/143)**：
  * 压力分级：`Class A` (低压 500 Pa), `Class B` (中压 1000 Pa), `Class C` (高压 2000 Pa), `Class D` (超高压 2500 Pa)。
  * 接头与加固：`Slide-on Flange` (滑入式法兰/机制插接法兰), `Mez / Doby Flange` (梅兹/多比型角码法兰), `Stiffener` (加劲件/加固肋), `Turning Vane` (导流叶片), `Spigot` (插管短接/套接管)。
  * 漏风测试：`Permissible Leakage Rate` (允许漏风率), `Static Gauge Pressure` (静压表压), `Test Section` (测试管段)。
* **美标 SMACNA 体系**：
  * 板厚号数 `Gauge (ga.)`、静压等级（`in. wg`）、咬口形式（`TDC/TDF 共板/机制法兰`, `Pittsburgh Lock 匹兹堡咬口`, `Slip & Drive S码/C码插条`）、漏风等级（`CL 3, 6, 12, 24`）。
* **海上平台 HVAC 体系 (ISO 15138)**：
  * 防爆与安全：`Hazardous Area` (危险区域/防爆分区), `Pressurization` (正压保护/加压), `Blast Damper` (抗爆阀/防冲击波阀), `A-60 / H-120 Fire Damper` (A-60 / H-120 级耐火/气密防火阀), `Fire and Gas (F&G) System` (火气探测系统)。
  * 海洋腐蚀与材料：`316L Stainless Steel`, `Droplet Separator / Mist Eliminator` (汽水分离器/除雾百叶), `Heavy-duty Industrial Damper` (重型工业风阀)。
* **材料标准 (ASTM)**：
  * 材质牌号与镀层重量（如 `G90 / Z275` 镀锌层重量、屈服强度 `Yield Strength`、延伸率 `Elongation`）原样保留并附带中文释义。

### 3. 工程单位与公式智能处理
* **双单位对照**：英制单位（in. wg, psi, gauge, cfm, ft/min）在译文中完整保留，并在括号内附上公制 SI 单位换算值：
  * 例：`4 in. wg` $\rightarrow$ `4 in. wg (约 1000 Pa)`
  * 例：`20 ga.` $\rightarrow$ `20 ga. (公称厚度约 0.9 mm)`
  * 例：`1500 fpm` $\rightarrow$ `1500 fpm (约 7.6 m/s)`
* **计算公式还原**：漏风量公式、阻力计算采用标准 $\LaTeX$ 渲染，如 DW/143 漏风限值计算：
  $$0.024 \times p^{0.65} \quad (\text{Class A}), \quad 0.009 \times p^{0.65} \quad (\text{Class B})$$

---

## 二、默认输出格式（中英双语逐段对照）

为便于工程图纸核对、监理审核与规格书技术答辩，默认采用**段落级双语对照**：

> **[Original / 原文]**
> Air duct systems shall be tested for air leakage in accordance with the procedures described in DW/143. For Class C ductwork, the maximum permissible air leakage rate shall not exceed $0.003 \times p^{0.65}\text{ litres/second/m}^2$.
>
> **【Translation / 译文】**
> 风管系统必须按照 DW/143 规定的程序进行漏风量测试。对于 C 级 (Class C) 风管，最大允许漏风率严禁超过 $0.003 \times p^{0.65}\text{ L/(s}\cdot\text{m}^2\text{)}$。

*(若用户明确提出“只要中文”或“整理为工程报告”，则输出纯中文技术报告格式)*

---

## 三、术语库快速参考

翻译时优先遵循：
* [DW/144、DW/143、ISO 15138 与材料术语表](./references/glossary.md)
* [SMACNA 风管与钣金专用术语表](./references/smacna_glossary.md)
