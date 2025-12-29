# NCKU-CSIE-OfficeBot
bot對話機器人，解答【國立成功大學資訊工程學系大學部】學生相關問題

---

## Quick Start
- Before Start: <kbd>clone</kbd> repository到本地
- OpenWebUI
  1. 到 https://www.docker.com/ 下載安裝Docker Desktop
  2. Docker Compose
   請在terminal執行 ```docker compose up -d``` 創建新的Docker Container
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

---
# 成大資工系大學部 顧問代理
  ---
- 具備溫柔耐心的語氣
- 不會嫌棄學生太多問題
- 會準確回答關於大學部修課相關事宜
- 如果有無法解答的事情，會協助使用者生成問題並寄送郵件給相關人員協助解答
---
環境
-
- UI界面：OpenWebUI
- LLM：gpt-oss-120b

---
核心操作
-
- System Prompt：專屬與學生的大學部修課等事宜的顧問
- RAG：具備 國立成功大學資訊工程學系大學部 部分修課、學分等相關知識
- Tools：生成相關詢問内容並寄送email給指定信箱

---
使用情境
-
1. 詢問修課相關事宜
2. 一旦超出範圍，會主動詢問使用者需不需要協助發送email詢問系辦人員
3. 寄送email

**不會回答不相關的問題**
