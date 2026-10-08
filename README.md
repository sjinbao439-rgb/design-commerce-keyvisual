# design-commerce-keyvisual

**AI-powered E-commerce Key Visual Design Skill**

从真实商品图片到专业电商主视觉，让 AI 理解商品、制定视觉策略并完成实际设计。

`design-commerce-keyvisual` 是一个面向电商视觉创作的 AI Skill。它能够根据商品实拍图、品牌素材、产品信息及设计参考图，生成或修改商品主图、营销海报、新品发布视觉与广告横幅。

不同于单纯的文生图提示词模板，本 Skill 将**商品身份保护、品类视觉策略、营销文案、参考图设计、图像生成和质量检查**整合为完整工作流程。

> **核心理念：Product First, Design Second.**
>
> 商品真实是基础，视觉设计为商品表达服务。

---

## ✨ Features

### 🎯 Product Identity Preservation

**保留真实商品特征，而不是重新想象一个商品。**

- 识别商品轮廓、颜色、比例与包装结构
- 保护 Logo、标签、接口、按钮和关键细节
- 区分不同 SKU、颜色、规格与套装组合
- 减少生成过程中出现的商品形变和错误配件
- 对高精度商品优先采用原始视角和保守编辑

### 🎨 Category-Aware Visual Design

**根据商品特点制定视觉策略，而不是套用固定模板。**

支持多种电商品类：

| Category | Visual Focus |
|---|---|
| Beauty & Skincare | 包装质感、光影、材质表现 |
| Food & Beverage | 食欲氛围、产品展示、场景体验 |
| Fashion & Accessories | 材质、形态、穿搭与陈列 |
| Consumer Electronics | 产品结构、科技质感、功能表达 |
| Home & Furniture | 空间关系、生活方式、材质细节 |
| Jewelry & Watches | 微观细节、反射、精致质感 |
| Baby & Pet Products | 柔和氛围、真实使用场景 |
| Sports & Outdoor | 使用环境、产品形态、运动氛围 |
| Tools & Hardware | 结构识别、功能场景、工业质感 |

品类只是辅助判断依据，具体设计以商品真实属性、使用场景和营销目标为准。

### 🖼️ Reference-Guided Generation

**使用设计参考图控制视觉方向，同时保留真实商品。**

支持分析参考图中的：

- 构图与主体布局
- 背景和配色
- 光照及阴影
- 字体气质与文字层级
- 空间关系和视觉节奏

参考图用于借鉴设计语言，不会将参考商品、品牌 Logo 或无关营销文案作为目标商品信息。

### ✍️ Marketing Copy Integration

**将商品卖点转化为清晰的视觉信息。**

- 提炼核心传播点
- 组织标题、副标题和卖点
- 控制文案密度与阅读层级
- 保留用户指定的价格、日期、型号及活动条件
- 避免编造产品功效、认证、销量和优惠信息

### 🔄 Generate, Review & Refine

**不仅生成图片，还检查图片是否符合要求。**

工作流程覆盖：

1. 商品与素材分析
2. 视觉策略选择
3. 文案与设计约束
4. 图像生成或编辑
5. 成图质量检查
6. 定向修改与交付

优先修正具体问题，避免在修改过程中破坏已确认的设计元素。

---

## 🚀 Quick Start

### Installation

下载本仓库，将 `design-commerce-keyvisual` 文件夹放入支持自定义 Skills 的 AI Agent 环境中。

确保目录中的 `SKILL.md` 和 `references/` 文件保持原有相对路径。

```text
your-skills-directory/
└── design-commerce-keyvisual/
    ├── SKILL.md
    ├── agents/
    ├── assets/
    └── references/
```

具体安装位置取决于所使用的 AI Agent 或 Skills 平台。

### Basic Usage

上传商品图片，然后输入：

```text
使用 $design-commerce-keyvisual

请根据上传的商品图片生成一张电商主视觉。

要求：
- 风格：高级简约
- 比例：1:1
- 商品作为视觉主体
- 柔和的商业摄影光线
- 背景简洁、有空间层次
- 保留商品原始外观、颜色、包装和标签
- 不添加未经确认的产品卖点
```

Skill 将根据商品信息选择视觉策略，并在具备图像生成能力的环境中执行成图与检查。

---

## 💡 Usage Examples

### 1. Product Hero Visual

**单品英雄视觉**

适用于品牌主视觉、商品宣传图及新品发布。

```text
使用 $design-commerce-keyvisual

以这张商品实拍图为基础，制作一张高级电商主视觉。

设计方向：
- 极简商业摄影风格
- 产品居中，突出主体轮廓
- 使用自然、柔和的光影
- 通过背景层次提升产品质感
- 画面干净，避免过多装饰

保持商品真实结构和包装细节。
```

### 2. Reference-Based Design

**参考图驱动设计**

适用于已有参考海报、品牌风格图或竞品视觉的场景。

```text
使用 $design-commerce-keyvisual

图片1：真实商品图片
图片2：视觉风格参考图

请参考图片2的构图、配色、光影和版式，
为图片1中的商品制作新的电商主视觉。

要求：
- 商品外观严格参考图片1
- 风格和构图参考图片2
- 不复制参考图中的商品与品牌
- 使用当前商品的真实信息
- 保持专业商业设计质感
```

### 3. Promotional Poster

**促销营销海报**

适用于节日活动、店铺促销和专题营销。

```text
使用 $design-commerce-keyvisual

根据上传的商品图片制作促销海报。

活动标题：秋季好物节
优惠信息：满299减40
活动时间：10月1日—10月7日

设计要求：
- 暖色系商业视觉
- 商品作为第一视觉焦点
- 活动标题清晰突出
- 优惠信息醒目但不过度拥挤
- 保留商品原始包装和标签
- 不添加其他未经确认的优惠条件
```

### 4. Product Scene Design

**商品使用场景图**

适用于生活方式营销、品牌内容和商品展示。

```text
使用 $design-commerce-keyvisual

将上传的商品放入自然、真实的使用场景。

要求：
- 场景符合商品实际用途
- 商品结构和颜色保持一致
- 光影方向与环境统一
- 商品与桌面、背景有合理接触关系
- 重点突出商品本身
- 不添加未经证实的产品功能
```

### 5. Iterative Editing

**已有视觉定向修改**

适用于设计优化和多轮修改。

```text
使用 $design-commerce-keyvisual

修改当前海报：

1. 保持商品外观不变
2. 将背景调整为浅米色
3. 增强自然光影
4. 优化标题与商品的间距
5. 保留所有已确认的文字内容

只修改上述部分，不改变其他设计元素。
```

---

## 🧠 How It Works

Skill 通过六个阶段，将原始商品素材转化为实际设计输出。

```text
Product Images / Brand Assets / References
                    │
                    ▼
          01. Product Analysis
             商品事实分析
                    │
                    ▼
          02. Visual Strategy
             视觉策略制定
                    │
                    ▼
          03. Content & Constraints
             文案及约束确认
                    │
                    ▼
          04. Image Generation
             图像生成与编辑
                    │
                    ▼
          05. Quality Review
             商品与设计检查
                    │
                    ▼
          06. Refine & Deliver
             定向修正与交付
```

### Stage 1 — Product Analysis

分析商品图片、产品资料、品牌素材与参考图，建立商品事实信息。

区分真实商品信息、可观察特征和设计假设，避免将视觉参考误认为产品事实。

### Stage 2 — Visual Strategy

依据商品形态、材质、使用场景和传播目标，确定：

- 核心传播点
- 主体构图
- 背景与道具
- 光影与配色
- 文案区域和信息层级

### Stage 3 — Content & Constraints

锁定商品身份特征、必须保留的文案，以及不允许改变或新增的内容。

### Stage 4 — Image Generation

组织商品参考图、设计要求和生成约束，调用当前环境提供的图像生成或编辑工具。

默认目标是完成实际图像，而不仅是输出提示词。

### Stage 5 — Quality Review

检查最终结果：

| Check | Criteria |
|---|---|
| Product Identity | 颜色、形态、结构、标签与原图一致 |
| Copy Accuracy | 文案、数字、单位和活动条件准确 |
| Composition | 商品突出，标题易读，布局合理 |
| Visual Realism | 材质、光照、阴影和尺度合理 |
| Output | 实际比例、格式及尺寸符合要求 |

### Stage 6 — Refine & Deliver

根据检查结果进行局部修正。

若商品身份、关键文案或输出规格仍存在问题，应明确说明限制，不将未通过检查的设计称为可直接投放的正式稿。

---

## 📁 Project Structure

```text
design-commerce-keyvisual/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── icon.svg
└── references/
    ├── category-strategies.md
    ├── generation-recipes.md
    └── poster-design-analysis.md
```

| File | Description |
|---|---|
| `SKILL.md` | Skill 核心指令与完整工作流程 |
| `agents/openai.yaml` | Agent 展示信息及默认配置 |
| `assets/icon.svg` | Skill 图标 |
| `references/category-strategies.md` | 跨品类视觉策略与商品分析 |
| `references/generation-recipes.md` | 图像生成、参考图绑定与迭代方法 |
| `references/poster-design-analysis.md` | 设计方法与参考项目分析 |

### Reference Files

**category-strategies.md**

用于分析不同商品的材质、形态、购买动机及视觉表达方向。

**generation-recipes.md**

用于组织图像生成要求、锁定商品身份、绑定输入素材，以及执行定向修正。

**poster-design-analysis.md**

记录相关设计项目的分析与方法参考。日常图像生成不需要运行该参考项目。

---

## 📐 Design Principles

### 1. Product First

商品身份高于视觉风格。

不为追求画面效果擅自改变商品的颜色、结构、包装及配件。

### 2. Facts Before Claims

所有营销卖点必须有事实依据。

不自动编造功效、价格、折扣、认证、销量或技术参数。

### 3. Design for Context

根据用途选择设计方式。

品牌营销主视觉、平台白底商品图和促销海报属于不同设计任务，不应混用规则。

### 4. Reference the Style, Not the Product

参考图用于学习视觉表达，不用于替换真实商品身份。

### 5. Review the Actual Output

质量检查以实际成图为依据，而非仅检查提示词是否完整。

### 6. Make Targeted Changes

对已有设计优先进行针对性修正，避免无关元素发生变化。

---

## 📦 Outputs

根据用户任务及运行环境的工具能力，Skill 可以交付：

- 电商主视觉图片
- 商品营销海报
- 新品发布视觉
- 促销活动海报
- 商品使用场景图
- 品牌营销横幅
- 图像修改结果
- 视觉设计方案
- 图像生成提示词

**默认以实际成图为目标。** 当用户明确只需要设计方案或提示词时，按照指定范围交付。

### Output Limitations

实际输出格式、像素尺寸、透明背景及编辑能力由当前图像工具决定。

扁平图像不等于具有可编辑图层的 PSD、Figma 或其他源文件。

---

## ⚠️ Limitations

### Product Fidelity

生成式图像编辑无法保证像素级一致。商品标签、精细结构、Logo 和包装文字可能出现偏差。

对商品身份高度敏感的任务，应优先保留原始商品视角，并对结果进行人工复核。

### Text Accuracy

AI 生成图像中的文字可能存在拼写、数字、单位或排版错误。

包含价格、优惠条件、法律声明和产品参数的正式营销素材，应在发布前核对。

### Platform Requirements

不同电商平台对主图尺寸、背景、文字和商品展示方式有不同要求。

涉及具体平台规范时，应使用其最新官方要求。

### Tool Availability

Skill 本身不包含独立的图像生成模型或外部 API 服务。

实际成图需要运行环境具备兼容的图像生成或编辑工具。工具不可用时，应明确说明无法完成成图。

---

## 🔍 Inspiration & References

本项目的设计方法参考了以下开源项目：

[poster-design](https://github.com/palxiao/poster-design)

相关分析记录在：

`references/poster-design-analysis.md`

本 Skill 聚焦于 AI Agent 场景下的电商视觉生成工作流程，不需要部署或运行上述参考项目。

如复用参考项目的代码或素材，应遵守其相应的开源许可证要求。

---

## 🤝 Contributing

欢迎通过 Issue 或 Pull Request 提出改进建议。

可贡献的方向包括：

- 新增商品品类视觉策略
- 优化图像生成提示词
- 改进商品身份保护规则
- 扩展参考图设计方法
- 完善文案与质量检查标准
- 增加经过验证的真实使用案例

提交更改时，请尽量提供明确的适用场景、预期行为和可复现示例。

---

## 📄 License

本 Skill 尚未指定独立发布许可证。

如需公开分发或允许第三方复用，请由项目维护者明确添加相应许可证文件。

---

**design-commerce-keyvisual**

*Real Products. Better Visuals. Smarter Commerce Design.*
