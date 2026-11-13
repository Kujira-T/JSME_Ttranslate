---
name: jsme-translate
description: >-
  专业工程技术规范与标准翻译工具（支持 JSME 日本机械学会标准、SMACNA 暖通风管标准、ASME、ISO、ASTM、GB 等工程规范）。
  当用户需要翻译机械工程、暖通空调、管道压力容器、焊接材料等技术文档，或进行专业工程中英/中日双语对照翻译与术语本地化时使用本技能。
---

# JSME & 工程技术标准翻译规范 (JSME_Translate)

本技能专为机械工程、暖通空调、压力容器及核电/工业设备领域的标准与技术文档翻译设计。执行翻译任务时，严格遵守以下准则。

---

## 一、核心翻译原则

1. **术语专业严谨，严禁生硬机翻**
   - 必须遵循国内外公认的工程术语规范（如 GB/T 通用术语、JSME 基準用語、ASME Boiler and Pressure Vessel Code 规范用语）。
   - 优先查阅 [references/glossary.md](./references/glossary.md) 与 [references/smacna_glossary.md](./references/smacna_glossary.md)。

2. **规范条款级别词汇的精确对等**
   - 工程标准中语气词具有法律与验收效力，必须严格区分：
     - **Shall / べし / なければならない** $\rightarrow$ **必须 / 应**（强制性条款）
     - **Should / 望ましい** $\rightarrow$ **宜 / 建议**（推荐性条款）
     - **May / 差し支えない** $\rightarrow$ **可以 / 得**（允许性条款）
     - **Shall not / てはならない** $\rightarrow$ **严禁 / 不得**（禁止性条款）

3. **专有名词与缩写规则**
   - 标准代号、型号、牌号必须保持原样（如 `JSME S NC1`, `SMACNA 006-2020`, `ASTM A36`, `SS400`, `SUS304`）。
   - 首次出现的行业公认缩写，使用 **中文译名 (英文/日文缩写)**，后续直接使用公认缩写。例如：
     - *TDC/TDF (Transverse Duct Connector / Flange)* $\rightarrow$ 机制法兰/共板法兰 (TDC/TDF)
     - *NDT (Non-Destructive Testing)* $\rightarrow$ 无损检测 (NDT)
     - *PWHT (Post-Weld Heat Treatment)* $\rightarrow$ 焊后热处理 (PWHT)

4. **工程量与单位处理**
   - 原文单位完整保留。美制/英制单位必须在括号内注明公制国际标准单位（SI）：
     - 例：`2 in. wg` $\rightarrow$ `2 in. wg (约 500 Pa)`
     - 例：`1/2 inch` $\rightarrow$ `1/2 英寸 (12.7 mm)`
     - 例：`50 psi` $\rightarrow$ `50 psi (约 0.345 MPa)`

---

## 二、默认输出格式（中英/中日双语对照）

为了方便工程人员校对与审核，默认采用**段落级双语对照**：

> **[原文]**
> The transverse joints shall be securely fastened to prevent air leakage exceeding the allowable class.
>
> **【译文】**
> 横向接头必须牢固紧固，以防止漏风量超过允许等级。

*注：若用户明确要求“仅输出中文”或“整理为报告”，则转为整篇结构化排版的纯中文技术报告格式。*

---

## 三、排版与结构完整性

1. **图表还原**：所有技术数据表必须完整转换为 Markdown 表格，表头逐项精准翻译，数值与容差原样保留。
2. **公式与符号**：涉及力学、热力学计算公式必须使用标准 LaTeX 排版（如应力 $\sigma = \frac{P \cdot D}{2t}$）。
3. **条文编号**：保持原文的章节编号（如 1.2.1, Table 2-1, Fig. 3-4），不可擅自合并或重排编号。
