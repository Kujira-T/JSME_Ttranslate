# JSME_Translate

> **JSME_Translate** 是一个面向机械工程、暖通空调、管道压力容器及核电工业等专业领域的技术文档与国际规范智能翻译 Skill。

专门优化支持：
* **JSME**（日本机械学会标准：如 S NC1 发电用核能设备规格、配管减薄与裂纹评估）
* **SMACNA**（美国钣金与空调承包商协会标准：如 006-2020 风管施工标准、016-2012 漏风测试）
* **ASME**（美国机械工程师协会 BPVC 系列标准）
* **ISO / ASTM / GB** 等工业标准

---

## 目录结构

```text
JSME_Ttranslate/
├── SKILL.md                          # 核心指令文件（包含 YAML frontmatter 及翻译准则）
├── references/                       # 专业技术词汇表与术语规范
│   ├── glossary.md                   # JSME / 机械工程 / 压力容器 / 无损检测中日英术语库
│   └── smacna_glossary.md            # SMACNA 暖通与钣金风管专用术语库
├── README.md                         # 项目说明与安装指引
└── .gitignore
```

---

## 安装与配置方式

### 方式 1：全局安装（推荐，所有项目均可使用）

将本仓库克隆或复制到 Antigravity 全局配置目录中：

```powershell
# Windows 路径：
Copy-Item -Recurse -Path ".\JSME_Ttranslate" -Destination "$HOME\.gemini\config\skills\JSME_Ttranslate"
```

### 方式 2：项目工作区级安装

放置在当前项目的根目录下：

```text
<你的工程项目根目录>/
└── .agents/
    └── skills/
        └── JSME_Ttranslate/
            ├── SKILL.md
            └── references/
```

---

## 核心特性

1. **严格的标准语态区分**：准确映射 `Shall` (必须/应) 与 `Should` (宜/建议) 等规范条款效力。
2. **多语言与缩写保留**：支持中、英、日专业术语三向对照，保留标准编号、材质牌号及公认缩写。
3. **单位智能换算**：美制单位（in. wg, psi, gauge, ft）自动附带 SI 公制单位换算。
4. **图表与公式原生还原**：技术表格完整转换为 Markdown，力学公式采用标准 LaTeX 排版。
5. **默认段落双语对照**：便于工程监理、审图专家及设计人员逐句校对核验。
