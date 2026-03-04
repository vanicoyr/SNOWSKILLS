# ❄️ SNOWSKILL (雪球技能) - 

> **项目说明**：基于 BNB Chain MCP 的自进化 AI 技能，支持 Agent 在 BSC 上一键创建 3% 税点代币并使用 BNB 进行自动化交易。

---

## 1. README.md (项目主文档)

# Snowball Skills

基于 [BNB Chain MCP](https://docs.bnbchain.org/showcase/mcp/skills/) 的 AI 技能，让 Agent 能够通过 SnowballSkill 合约在 BSC 上**创建代币**、用 **BNB** **买入/卖出**指定代币。

### 🚀 核心逻辑
- **自进化机制**：子币进化产生，通过交易税收回购母币，实现价值增长。
- **3% 固定税点**：所有通过本技能创建的代币默认设置 **3% 税点**。
- **BNB 本位**：直接使用原生 BNB 交易，无需中间代币，提高效率。

### 依赖
- **连接 BNB Chain MCP**：`npx @bnb-chain/mcp@latest`
- **安装官方技能**：`npx skills add bnb-chain/bnbchain-skills`

### 安装方式
- **Cursor / Claude**: `npx skills add snowball-builder/snowball-skills`
- **OpenClaw**: `clawhub install snowball-skills`

### 支持的操作
- **创建代币**：格式「名称：… 符号：…」。默认 3% 税点，Agent 自动关联母币。
- **买入**：使用 BNB 按指定数量买入。示例：「雪球技能 用 0.1 BNB 买入 0x...」
- **卖出**：支持按数量或比例（如 50%、100%）。示例：「雪球技能 卖出 100% 的 0x...」

---

## 2. package.json (项目配置)

```json
{
  "name": "snowball-skills",
  "version": "1.0.0",
  "description": "AI-powered self-evolving token creation and BNB trading skill for BSC",
  "main": "index.js",
  "keywords": ["BNBChain", "MCP", "Snowball", "AI-Agent"],
  "dependencies": {
    "ethers": "^6.10.0",
    "axios": "^1.6.0"
  }
}
