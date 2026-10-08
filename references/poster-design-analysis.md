# poster-design 来源分析

分析日期：2026-10-07。项目：[palxiao/poster-design](https://github.com/palxiao/poster-design)。检查版本：`129c1ad1b9d7345795d4df1583da23cbfb377f2e`（当时 main）。未运行项目，也未验证线上生成效果。

## 已读实现与链路

| 环节 | 文件证据 | 实现 |
| --- | --- | --- |
| 编辑与合成技术 | [README](https://github.com/palxiao/poster-design/blob/129c1ad1b9d7345795d4df1583da23cbfb377f2e/README.md) | Vue3/Pinia/TypeScript，原生 DOM 画布；声明前端 Html2canvas、后端 Puppeteer 与 sharp；素材/模板/PSD 辅助解析 |
| 画布与图层 | `src/store/design/canvas/page-default.ts`、`src/components/modules/widgets/wImage/wImageSetting.ts` | 画布尺寸/背景；图片 URL、坐标、宽高、旋转、透明度、裁剪与蒙版 |
| 模板应用 | `src/store/design/widget/actions/template.ts` | 约束组合到画布、重设部分 ID、解码文字、添加 widgets 并更新 |
| 抠图 | [useCutout.ts](https://github.com/palxiao/poster-design/blob/129c1ad1b9d7345795d4df1583da23cbfb377f2e/src/components/business/image-cutout/ImageCutout/helper/useCutout.ts) | rembg-web + ONNX/u2netp 浏览器推理、复用会话、输出 PNG Blob；还提供画笔修补工具 |
| AI 文案/配色/图片 | [ai.ts](https://github.com/palxiao/poster-design/blob/129c1ad1b9d7345795d4df1583da23cbfb377f2e/service/src/service/ai.ts) | 文案与配色调用兼容对话接口并解析；生图只传 model、prompt、size 到 images/generations，处理 URL/base64，保存并校验尺寸 |
| 插入排版 | [AiAssistant.vue](https://github.com/palxiao/poster-design/blob/129c1ad1b9d7345795d4df1583da23cbfb377f2e/src/components/business/ai-assistant/AiAssistant.vue) | 文案/生图/配色三入口；分别插为文字/图片组件，生成图等比居中；主色可作背景 |
| 作品再渲染 | [Draw.vue](https://github.com/palxiao/poster-design/blob/129c1ad1b9d7345795d4df1583da23cbfb377f2e/src/views/Draw.vue) | 读取 JSON，恢复 page/widgets 或 global/layers，加载背景、图片、SVG、字体，再发出完成信号 |
| 导出 | [screenshots.ts](https://github.com/palxiao/poster-design/blob/129c1ad1b9d7345795d4df1583da23cbfb377f2e/service/src/service/screenshots.ts)、[download-single.ts](https://github.com/palxiao/poster-design/blob/129c1ad1b9d7345795d4df1583da23cbfb377f2e/service/src/utils/download-single.ts) | 排队 Puppeteer，完成信号后截图；sharp 生成 JPEG 缩略图；尺寸/DPR限制、超时保护 |

可归纳为：上传或选素材 → 可选抠图 → 模板/图层排版 → 可选 AI 文案、图片、配色 → 保存数据 → 渲染合成 → 导出。

它是通用设计编辑器；上述已读生图路径没有产品参考图输入，也没有专门的电商品类推理或商品身份验收。不能据此声称会自动准确识别产品并一键完成电商设计。README 企业版展示不等于开源版已实现能力。未深入核验 PSD 解析与数据库种子模板内容。

## 本 skill 借鉴与扩展

- 借鉴商品、背景、文字、装饰分别控制的图层思路，转化为提示词约束与分项检查。
- 借鉴素材复用、尺寸适配、实际渲染后导出，采用跨品类构图策略并检查成图。
- 新增事实表、原图绑定、商品身份保护、品类适配、逐字文案、定向迭代；这些是 skill 的扩展，不归功于来源仓库。
- 日常使用内置图像工具，无需运行项目、配置其服务；来源尺寸映射仅是当时实现，不作当前 API 规范。

仅参考架构与方法，没有复制项目代码或分发模板/素材。项目许可证为 AGPL-3.0；另行复用代码或资产时检查其对应许可。
