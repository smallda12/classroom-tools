# 📌 多 Agent 協作與權責規範檔 (AGENTS.md)

## 🤝 跨 Agent 協作核心原則 (Multi-Agent Collaboration Policy)

本專案 `G:\我的雲端硬碟\classroom-tools\` 是班級工具總專案，可能由多個 AI Agent（Claude Code、Codex、Antigravity/.gemini 等）共同協助開發。為避免互相覆蓋或干擾，所有 Agent 開工前請先讀這份檔案，收工前請回來更新第 3 節的進度清單。

> 📘 專案整體藍圖（工作模式、三個家、工作注意事項）請看同目錄的 `CLAUDE.md`，兩份檔案內容互補、不重複維護同一件事。

---

## 1. 權責邊界與資料夾分工 (Directory Scoping & Isolation)

| 範圍 | 說明與邊界 |
| :--- | :--- |
| 根目錄檔案（`CLAUDE.md` / `AGENTS.md` / `README.md` / `.gitignore`） | 專案共用設定，異動前先看第 3 節有沒有其他 Agent 剛好在改，避免同時寫入衝突 |
| `tools/<工具名>/` | 每個教學小工具各自獨立一個子資料夾。**負責該工具的 Agent 只在自己的 `tools/<工具名>/` 底下工作**，不修改其他工具的子資料夾 |
| 新增工具 | 開新工具前，先在第 3 節登記「工具名稱 + 負責 Agent + 狀態」，避免兩個 Agent 同時做同一個工具 |

---

## 2. 互不干擾與防呆規範 (Isolation & Anti-Collision Rules)

1. **獨立資料夾隔離**：只在自己負責的 `tools/<工具名>/` 內建立與修改檔案，不覆蓋其他 Agent 的產出。
2. **檔名與 commit 訊息要有意義**：commit message 寫清楚「做了什麼＋為什麼」，不要「更新」「修改」這種沒資訊的字。
3. **共用記憶檔同步**：
   - 開工時：讀 `AGENTS.md`（本檔案，尤其第 3 節）＋ `CLAUDE.md`，了解目前有哪些工具、誰在做什麼。
   - 收工時：把本次異動更新回第 3 節的進度清單，並正常 `git commit` + `git push`（是 Claude Code 的話，「收工」skill 會自動做 git 同步；其他 Agent 請自行 commit + push）。
4. **學生資料規範**：一律去識別化，只用座號＋班級代號，不存真名（見 `CLAUDE.md`）。
5. **`.claude/` 資料夾永遠不 commit**（Claude Code 專屬本地設定，可能含 token）。

---

## 3. 當前各 Agent 工作進度狀態 (Cross-Agent Status Checklist)

- [x] **初始化**（Claude Code，2026-07-24）：建立總專案骨架（`CLAUDE.md`／`.gitignore`／`README.md`）、GitHub 公開 repo（[smallda12/classroom-tools](https://github.com/smallda12/classroom-tools)）、Obsidian 工作筆記、收工/開工 skill 的專案內同步邏輯。尚未建立任何 `tools/` 子工具。

（之後每個新工具開工/收工時，在這裡加一行：工具名稱 + 負責 Agent + 目前狀態）
