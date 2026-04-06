🍱 SmartBento: A Modular Food Ordering Orchestrator
💡 開發動機 | Project Vision
在快節奏的辦公環境中，點餐不應成為行政負擔。SmartBento 旨在重新定義「辦公室點餐體驗」，透過 Streamlit 的反應式介面與 Google Sheets API 的透明化後端，實現從「發起揪團」到「數據彙整」的全自動化流程。
SmartBento redefines office group-buy experiences by leveraging Streamlit's reactive UI and Google Sheets API as a transparent backend, automating the entire workflow from "group creation" to "data aggregation."

🏗️ 系統架構設計 | System Architecture
本專案嚴格遵循 關注點分離 (SoC) 與 模組化設計，確保程式碼具備高擴展性與測試性：
Strictly adheres to Separation of Concerns (SoC) and Modular Design for scalability:

Plaintext
smart-bento/
├── app.py                # 系統核心：動態路由與應用入口 (Core Routing)
├── modules/              # 表現層：UI 組件與互動模組 (Presentation Layer)
│   └── order_system.py   # 卡片式選單與 Session State 狀態管理
├── utils/                # 邏輯層：資料訪問與商務邏輯 (Data Access Layer)
│   └── sheets_api.py     # Google Sheets API 封裝與 Cache 優化
└── styles/               # 視覺層：樣式規範與主題定義 (Theme & Styles)
    └── theme.py          # 統一 UI 顏色常數與 CSS 注入
🔥 技術亮點 | Engineering Highlights
1. 🎨 現代化組件式 UI (Component-based UI)
中文：全面棄用傳統表格，改用「卡片式佈局」，優化行動端的操作流暢度。

English: Abandoned traditional tables in favor of a "Card Layout," optimizing mobile responsiveness.

2. 🧠 智慧數據快取 (Smart Data Caching)
中文：針對 Google Sheets API 實作 @st.cache_data，顯著降低請求延遲並規避 API Quota 限制。

English: Implemented @st.cache_data for Google Sheets API to reduce latency and stay within API Quotas.

3. 🛡️ 安全開發規範 (Security-First)
中文：透過 .env 進行環境變數管理，並在 .gitignore 中嚴格屏蔽金鑰檔。

English: Managed via .env with strict .gitignore rules to prevent credential leakage.

🛠️ 開發藍圖 | Roadmap
[x] 基礎模組化架構開發 (Core Modular Setup)

[ ] Google Sheets 關聯式 Schema 實作 (RDBMS-like Sheets Schema)

[ ] 智能歷史訂單重複功能 (Smart Order Persistence)

[ ] 管理員自動化統計面板 (One-click Admin Summary)

🚀 快速啟動 | Getting Started
1. 環境克隆 (Clone & Setup)
Bash
git clone https://github.com/JERRY-CHANG-TW/food-ordering-system.git
cd food-ordering-system
2. 安裝依賴 (Install Dependencies)
Bash
pip install -r requirements.txt
3. 啟動應用 (Run App)
Bash
streamlit run app.py
📄 授權協議 | License
本專案採用 MIT License。
Licensed under the MIT License.
