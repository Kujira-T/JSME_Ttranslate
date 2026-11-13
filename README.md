# JSME_Translate (国际暖通风管与海工通风标准翻译 Skill)

> **JSME_Translate** 是一个面向**暖通空调风管制造、漏风量测试、海上石油天然气平台 HVAC 及钣金工程材料**等专业领域的国际工程规范与技术文档智能翻译 Skill。

专门优化支持的核心标准体系：
* **BESA DW/144**：英国建筑工程服务协会《金属风管制造与安装规范》（涵盖低压、中压、高压风管，插接法兰、加固与支吊架）
* **BESA DW/143**：英国《风管系统漏风量测试实用指南》（涵盖 Class A ~ Class D 压力等级与允许漏风率公式计算）
* **SMACNA**：美国钣金与空调承包商协会标准（《暖通空调风管施工标准：金属与柔性》、《风管漏风量测试手册》）
* **ISO 15138**：国际标准《石油和天然气工业 — 海上生产装置 — 采暖、通风与空调（HVAC）》（含危险区防爆通风、A-60/H-120 耐火风阀、抗爆阀、316L 防腐与正压保护）
* **ASTM 材料标准**：如 ASTM A653（镀锌板）、ASTM A240（不锈钢板）、ASTM A15 等钣金材料、镀层重量（G90/Z275）与力学性能标准

---

## 目录结构

```text
JSME_Ttranslate/
├── SKILL.md                          # 核心指令文件（包含 YAML frontmatter 及翻译准则）
├── references/                       # 核心术语对照库
│   ├── glossary.md                   # DW/144, DW/143, ISO 15138, ASTM 专用术语库
│   └── smacna_glossary.md            # SMACNA 暖通与钣金风管专用术语库
├── README.md                         # 项目说明与安装指引
└── .gitignore
```

---

## 核心特性

1. **规范条款效力严谨映射**：准确区分 `Shall / Must` (必须/应) 与 `Should` (宜/建议) 等强制与推荐条款。
2. **压力与漏风标准公式原生支持**：对 DW/143 各级漏风限值公式（如 $0.024 \cdot p^{0.65}$）及 SMACNA 漏风等级（CL 3, 6, 12 等）保持专业换算与格式渲染。
3. **海工与防爆特殊工况术语**：涵盖 ISO 15138 的海上危险区（Zone 1/2）、正压防爆、A-60/H-120 防火阀、抗爆阀（Blast damper）、盐雾除雾器等特种环境专有名词。
4. **单位双向对照**：英制参数（in. wg, gauge, psi, fpm, cfm）自动在译文中附带国际公制（Pa, mm, m/s）换算。
5. **段落级双语对照输出**：默认提供清晰的中英双语对照，方便工程审图、外资项目监理以及招投标答辩。

---

## 安装与配置方式

### 方式 1：全局安装（推荐，所有项目均可使用）

将本仓库克隆或复制到 Antigravity 全局配置目录中：

```powershell
# Windows 路径：
Copy-Item -Recurse -Force -Path ".\JSME_Ttranslate" -Destination "$HOME\.gemini\config\skills\"
```

### 方式 2：项目工作区级安装

放置在当前工程项目的根目录下：

```text
<你的工程项目根目录>/
└── .agents/
    └── skills/
        └── JSME_Ttranslate/
            ├── SKILL.md
            └── references/
```
