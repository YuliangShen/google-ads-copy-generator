# Google Ads 广告文案 AI 批量生成器

> 输入产品信息，AI 批量生成符合字符限制的广告标题和描述，一键导出 CSV 导入 Google Ads Editor。

## 背景

负责公司 Google Ads 投放时，每次新建广告系列都要手写十几条标题和描述，还要逐条数字符数。这个工具让 AI 批量生成文案，自动校验字符限制，导出标准 CSV 直接导入 Google Ads Editor，跳过手动录入。

## 功能

- 输入产品名称、核心卖点、目标受众，一次生成最多 5 组文案
- 实时字符计数，自动标红超限内容（标题 ≤30字符，描述 ≤90字符）
- Google 广告预览，所见即所得
- 导出标准 CSV，兼容 Google Ads Editor 批量导入格式
- 内置 JSON 调试面板，可查看 AI 返回的原始结构化数据

## 使用方式

双击 `google_ads_generator.html` 用浏览器打开，无需安装任何环境。填入千问 API Key，输入产品信息，点击生成。

## 导入 Google Ads 流程

```
AI 生成文案 → 下载 CSV → Google Ads Editor → 文件 → 导入 CSV → 检查预览 → 上传发布
```

## 技术要点

- Prompt 要求 AI 只返回 JSON，不含任何多余文字
- 前端用 `JSON.parse()` 解析结构化数据，再转为 CSV 输出
- 完整链路：Prompt 设计 → 结构化 JSON 输出 → 表格数据 → 文件下载

## 技术栈

HTML · JavaScript · 千问 API（兼容 OpenAI 格式）· 结构化 JSON 输出
