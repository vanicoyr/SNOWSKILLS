# ❄️ Snowball Skills（雪球技能）

基于 [BNB Chain MCP](https://docs.bnbchain.org/showcase/mcp/skills/) 的 AI 技能，让 Agent 能够通过 SnowballSkill 合约在 BSC 上**创建自进化代币**、用 **BNB** 直接**买入/卖出**指定代币。

---

## 依赖

本技能依赖 **BNB Chain MCP**。使用前请先完成：

- **连接 BNB Chain MCP**：运行 `npx @bnb-chain/mcp@latest`
- **安装 BNB Chain 官方技能**（可选）：`npx skills add bnb-chain/bnbchain-skills`

详细说明见：[BNB Chain Skills 文档](https://docs.bnbchain.org/showcase/mcp/skills/)

---

## 安装

### Cursor / Claude

在当前项目中安装（仅当前项目可用）：

```bash
npx skills add snowball-builder/snowball-skills
全局安装（所有项目可用）：Bashnpx skills add snowball-builder/snowball-skills -g
OpenClaw本技能已上架 ClawHub。先安装 ClawHub CLI，再安装本技能：Bashnpm i -g clawhub
clawhub install snowball-skills
安装后新开一次 OpenClaw 会话，技能才会被加载。使用方式与下方「如何使用」相同：在对话中说「雪球技能」即可触发。
OpenClaw 需已配置 BNB Chain MCP，且环境中已设置 PRIVATE_KEY 才能发送链上交易。
如何使用触发方式在对话中说「雪球技能」即可触发本技能。
前置条件已安装并连接 BNB Chain MCP在 MCP 的 env 中已配置 PRIVATE_KEY，否则无法发送链上交易支持的操作操作说明创建进化代币默认 3% 税点。
按「名称：… 符号：…」格式说明，可选「官网：…」「简介：…」并附图片；
Agent 将生成元数据并关联母币回购逻辑买入直接使用 BNB 按指定金额买入目标代币卖出（按数量）指定代币地址与卖出的 Token 数量，
换回 BNB卖出（按比例）指定代币地址与比例（如 50%、100%），实现自动化滚雪球止盈
