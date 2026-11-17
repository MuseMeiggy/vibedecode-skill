# VIBEDECODE

**把想法说清楚，让开发更顺畅。**

作者：**MuseMeiggy**

VIBEDECODE 帮助你在编程交流中识别准确术语，把口语化描述整理成可以直接执行的需求，并解释开发回复中影响判断的概念。

## 能做什么

- **说清需求**：保留原意，把“鼠标放上去弹出一行说明”表达成“为按钮添加文字提示（Tooltip）”。
- **看懂回复**：结合当前任务解释开发术语，帮助判断下一步该怎么做。
- **边做边提示**：继续完成开发任务，同时自然补充最相关的 1–3 个术语。
- **提供来源**：引用术语服务实际返回的词条链接，不编造地址。

## 安装

把这个仓库交给你的 Agent，并告诉它：

> 请安装本仓库中的 `skills/vibedecode` 技能。

也可以把 `skills/vibedecode` 整个文件夹复制到本地技能目录。安装后使用 `$vibedecode` 调用，展示名称为 **VIBEDECODE**。

## 使用示例

```text
使用 $vibedecode，把这句话改成更准确的开发需求：
这个按钮鼠标放上去变个色，点下去也要有一下反馈。
```

```text
Agent 说这里需要做状态管理。
结合当前页面用大白话解释，并告诉我接下来该问什么。
```

## 运行要求

需要 Node.js 20 或更高版本与联网能力，无需账号或 API Key。

术语查询仍由 **VibeHub**（`https://vibe-hub.org`）提供。本项目名称、技能调用名和作者署名独立于术语服务名称。

```bash
node skills/vibedecode/scripts/vibedecode.mjs resolve --query "Tooltip" --compact
```

如需连接其他兼容的术语服务，可使用 `--site-url` 或环境变量 `VIBEDECODE_SITE_URL`；旧变量 `VIBEHUB_SITE_URL` 仍兼容。

## 隐私

查询前会移除常见密钥、网址、邮箱、本地路径和代码块。只查询脱敏后的短术语，不发送整段需求、项目源代码或客户资料。Agent 已看到的上下文仍遵循其所在平台的隐私设置。

## 许可

MIT License · Copyright (c) 2026 MuseMeiggy
