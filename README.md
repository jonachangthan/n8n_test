## 📊 Workflow 功能說明
這個 workflow 是一個 AI 內容分析器，使用 Groq 的 AI 模型來自動分析文字內容並提取關鍵資訊。

## 🔄 工作流程
1️⃣ Manual Trigger（手動觸發）
你點擊按鈕來啟動整個流程
不需要外部 API 呼叫或 webhook
2️⃣ Workflow Configuration（工作流程設定）
集中管理所有設定參數：
maxSummaryLength: 摘要最大長度（500 字元）
emailRecipient: 郵件收件人（選用）
content: 你要分析的文字內容（可以隨時修改）
3️⃣ AI Content Analyzer（AI 內容分析器）
這是核心節點，使用 AI 來分析文字，執行以下任務：

📝 生成簡潔摘要（最多 500 字元）
🏷️ 提取關鍵主題
😊😐😞 識別情感（正面/中性/負面）
💡 提取關鍵洞察
連接的 AI 組件：

Groq Chat Model: 使用 llama-3.3-70b-versatile 模型進行分析
Structured Output Parser: 確保輸出格式化為標準 JSON
Gmail Tool: 可選功能，如果你在文字中要求，AI 可以發送分析結果到指定郵箱
## 📤 輸出結果
執行完成後，你會得到結構化的 JSON 結果：

{
  "summary": "內容摘要...",
  "topics": ["主題1", "主題2", "主題3"],
  "sentiment": "positive",
  "keyInsights": ["洞察1", "洞察2"]
}
## 💡 使用場景
這個 workflow 適合用於：

📰 新聞文章分析
📧 郵件內容摘要
📱 社群媒體貼文分析
📄 文件快速理解
🎯 客戶反饋情感分析
## ✏️ 如何使用
點擊 Workflow Configuration 節點
修改 content 欄位為你想分析的文字
點擊 Test workflow 按鈕
查看 AI Content Analyzer 節點的輸出結果
完全在 n8n 介面內操作，不需要寫程式或外部工具！
