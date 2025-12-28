# NCKU-CSIE-OfficeBot
bot對話機器人，解答【國立成功大學資訊工程學系大學部】學生相關問題

---

## Quick Start
- Before Start: <kbd>clone</kbd> repository到本地
- OpenWebUI
  1. 到 https://www.docker.com/ 下載安裝Docker Desktop
  2. Docker Compose
   請在terminal執行 <kbd>docker compose up -d</kbd> 創建新的Docker Container
   待執行成功，請在本地瀏覽器輸入網址 http://localhost:3000/ ，即可啓動OpenWebUI

- Ollama（LLM）
  - 課堂提供API
    - api url：https://api-gateway.netdb.csie.ncku.edu.tw/
    - api key: ***
  1. 點擊使用者頭像 --> <kbd>Admin Panel</kbd> --> <kbd>Settings</kbd> --> <kbd>Connections</kbd>
  2. 找到Ollama欄位，把api url和api key填上去即可使用LLM
---

## 創建專屬 Model
### 基礎設定
- 點擊使用者頭像 --> <kbd> Workspace </kbd> --> <kbd> Model</kbd>界面 --> <kbd> + New Model</kbd>
- 選擇base model：

### 進階設定
- System Prompts
  - 將<kbd>system_prompts.txt</kbd>的文字copy and paste到<kbd>system prompts</kbd>欄位
- RAG
  - 在<kbd>Knowledge</kbd>欄位點擊<kbd> Upload Files</kbd>
  - 把<kbd>documents</kbd>所有的檔案執行上傳
- Tools
  - 在<kbd>Tools</kbd>界面選擇<kbd> New Tool </kbd> --> 把Email Tools的文字copy & paste到裏面 --> 按儲存。
  - 檔名設爲 Email Tools


