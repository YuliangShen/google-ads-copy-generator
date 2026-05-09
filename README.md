## 📢 项目二：Google Ads 文案批量生成器

输入产品信息，AI 批量生成符合 Google Ads 字符限制的广告标题和描述，
一键导出 CSV 直接导入 Google Ads Editor。

### 功能

- 输入产品名称、卖点、目标受众，一次生成最多 5 组广告文案
- 实时字符计数，自动标红超限内容（标题 ≤30字符，描述 ≤90字符）
- Google 广告预览，所见即所得
- 导出标准 CSV，兼容 Google Ads Editor 批量导入格式
- 内置 JSON 调试面板，可查看 AI 返回的原始结构化数据

### 使用方式

双击 `google_ads_generator.html` 用浏览器打开，无需安装任何环境。

填入千问 API Key，输入产品信息，点击生成即可。

### 导入 Google Ads 流程
AI 生成文案 → 下载 CSV → 打开 Google Ads Editor
→ 文件 → 导入 CSV → 检查预览 → 上传发布
### 技术要点

- 提示词要求 AI 只返回 JSON 格式，不含任何多余文字
- 前端用 `JSON.parse()` 解析结构化数据，再转为 CSV 输出
- 展示了"结构化输出"的完整链路：Prompt → JSON → 表格数据
