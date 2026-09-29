# 盘后复盘

`laogu-close`

盘后复盘 skill：在每个交易日收盘后（15:00 后；盘中执行则复盘上一个交易日）生成中文复盘报告。

## 一键安装

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-close`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-close.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-close/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-close/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-close/`（项目级用 `.trae/skills/laogu-close/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
## 文件结构

- `SKILL.md` — 主流程（平台中立，定时能力由宿主平台提供）
- `references/sources.md` — 数据源：行情接口、板块/涨停复盘搜索路径、资金数据来源

## 输出结构

- 今日指数：上证/深成指/创业板涨跌、成交额、涨跌家数、涨停/跌停数
- 板块：领涨/领跌板块
- 异动股：涨停股一句话原因
- 资金：北向成交总额及占比（净流入 2024 年 5 月后不再披露，不写该数字）
- 明日展望：次日日历事件（不做涨跌预测）

## 定时建议

- A股交易日 16:00–18:00 推送（收盘后复盘）
- 可与 `laogu-morning`（每日早报）配合使用：早报看今日看点，复盘看今日发生了什么

---
## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。
