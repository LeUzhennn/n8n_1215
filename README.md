# n8n_1215

n8n 工作流程自動化專案，使用 OpenSpec 進行規格驅動開發。

## 專案概述

本專案旨在創建 n8n 工作流程自動化解決方案，並使用 OpenSpec 管理開發流程。專案包含 n8n 簡單程式碼範例、工作流程模板，以及完整的開發環境配置。

## 技術棧

- **Node.js**: v24.12.0
- **npm**: v11.6.2
- **n8n**: v1.123.5 - 工作流程自動化平台
- **OpenSpec**: v0.16.0 - 規格驅動開發工具
- **Git**: 版本控制

## 快速開始

### 前置需求

- Node.js v20.19.0 或更高版本
- npm v11.x 或更高版本
- Git

### 安裝步驟

1. **克隆專案**
   ```bash
   git clone https://github.com/LeUzhennn/n8n_1215.git
   cd n8n_1215
   ```

2. **安裝 OpenSpec**（如果尚未安裝）
   ```bash
   npm install -g @fission-ai/openspec@latest
   ```

3. **安裝 n8n**（如果尚未安裝）
   ```bash
   npm install -g n8n
   ```

4. **啟動 n8n**
   ```bash
   n8n start
   ```
   
   訪問 http://localhost:5678 開始使用 n8n

## 專案結構

```
n8n_1215/
├── .agent/                    # Antigravity 工作流程配置
│   └── workflows/
│       ├── openspec-apply.md
│       ├── openspec-archive.md
│       └── openspec-proposal.md
├── .devcontainer/             # DevContainer 配置
├── openspec/                  # OpenSpec 規格和變更
│   ├── changes/
│   │   └── 01-generate-n8n-simple-code/
│   │       ├── proposal.md
│   │       ├── tasks.md
│   │       └── specs/
│   ├── project.md
│   └── AGENTS.md
├── conversation_summary.md    # 開發過程記錄
├── test2.json                 # n8n 工作流程範例
├── .gitignore
├── AGENTS.md
└── README.md
```

## OpenSpec 變更管理

本專案使用 OpenSpec 進行變更管理，所有變更提案都使用自動數字前綴（01-, 02-, 03-...）。

### 當前變更

#### 01-generate-n8n-simple-code
創建 n8n 簡單程式碼範例，涵蓋：
- 資料處理
- API 整合
- 條件邏輯
- 資料格式化
- 錯誤處理

### 查看變更

```bash
# 列出所有變更
openspec list

# 查看特定變更
openspec show 01-generate-n8n-simple-code

# 驗證變更
openspec validate 01-generate-n8n-simple-code
```

## n8n 工作流程

### 範例工作流程

專案包含範例工作流程 `test2.json`，這是一個簡單的 Webhook 測試工作流程。

**匯入工作流程**：
1. 啟動 n8n
2. 在 n8n UI 中點擊 "Import from File"
3. 選擇 `test2.json`
4. 啟動工作流程

## 開發指南

### 創建新的 OpenSpec 變更

1. **創建變更提案**
   ```bash
   # 使用 Antigravity 或其他 AI 助手
   # 說明：「創建一個 OpenSpec 變更提案來 [描述功能]」
   ```

2. **驗證提案**
   ```bash
   openspec validate <change-id> --strict
   ```

3. **實施變更**
   ```bash
   # 按照 tasks.md 中的任務清單執行
   ```

4. **封存變更**
   ```bash
   openspec archive <change-id> --yes
   ```

### 命名規範

- **變更命名**: `NN-descriptive-name`（例如：`01-add-authentication`）
- **使用兩位數字前綴**（01, 02, ..., 10, 11）
- **描述性名稱使用 kebab-case**
- **動詞開頭**（add, fix, update, remove 等）

## n8n MCP 整合

本專案支援 n8n MCP（Model Context Protocol）整合。

### 安裝 MCP 社群節點

1. 啟動 n8n
2. 進入 Settings → Community Nodes
3. 安裝 `n8n-nodes-mcp`
4. 重啟 n8n

詳細說明請參考 [n8n MCP 安裝指南](https://docs.n8n.io/)

## 環境變數

建議配置以下環境變數以優化 n8n 性能：

```bash
# SQLite 連接池
DB_SQLITE_POOL_SIZE=5

# 啟用 Task Runners
N8N_RUNNERS_ENABLED=true

# 環境變數存取控制
N8N_BLOCK_ENV_ACCESS_IN_NODE=false

# Git Node 安全設定
N8N_GIT_NODE_DISABLE_BARE_REPOS=true
```

## 文檔

- [對話記錄整理](conversation_summary.md) - 完整的開發過程記錄
- [OpenSpec 官方文檔](https://github.com/fission-ai/openspec)
- [n8n 官方文檔](https://docs.n8n.io/)

## 貢獻

1. Fork 本專案
2. 創建功能分支 (`git checkout -b feature/amazing-feature`)
3. 提交變更 (`git commit -m 'Add some amazing feature'`)
4. 推送到分支 (`git push origin feature/amazing-feature`)
5. 開啟 Pull Request

## 授權

本專案採用 MIT 授權 - 詳見 LICENSE 檔案

## 聯絡方式

- GitHub: [@LeUzhennn](https://github.com/LeUzhennn)
- 專案連結: [https://github.com/LeUzhennn/n8n_1215](https://github.com/LeUzhennn/n8n_1215)

## 致謝

- [n8n](https://n8n.io/) - 強大的工作流程自動化平台
- [OpenSpec](https://github.com/fission-ai/openspec) - 規格驅動開發工具
- [Antigravity](https://deepmind.google/technologies/gemini/) - AI 編碼助手

---

**專案狀態**: 🚀 開發中

最後更新: 2025-12-15
