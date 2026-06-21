# 國立臺南大學資訊工程學系 - 多代理人影音生成專案

本專案為多媒體系統課程之 Final 自主學習作業。本團隊透過 OpenClaw 架構規劃，設計並實作了一套包含 5 個專屬 Agent（企劃、編劇、分鏡、審查、統整）的受控式工作流（Controlled Workflow），並據此剪輯產出一支 60 秒的南大資工形象宣傳短片。

##  團隊成員
* 學號：S11259007
* 姓名：呂守勳

##  實作路徑與環境聲明
* **實作框架**：OpenClaw Agent 宣告式架構。
* **付費聲明**：本專案嚴格遵循課程之「零付費政策」，採用 Mock/Stub Agent 路線。所有 Agent 的身份定義（Persona）與交接紀錄（Handoff JSON）皆以人工 Dry-run 模擬生成，確保流程完全可受控、可追蹤。
* **影音剪輯工具**：Movavi Video Editor 26 剪輯平台。

##  專案目錄結構
```text
Final_Project_Repo/ 
├── README.md                  # 本說明文件
├── report/ 
│   └── Final_Report.pdf # 自主學習成果報告書
├── agents/                    # 5個 Agent 的身分設定與提示詞 (Prompt)
│   ├── 01_planner_agent.md 
│   ├── 02_script_agent.md 
│   ├── 03_visual_agent.md 
│   ├── 04_reviewer_agent.md 
│   └── 05_finalizer_agent.md 
├── handoff/                   # 各 Agent 之間的結構化 JSON 交接紀錄
│   ├── 01_planner_output.json 
│   ├── 02_script_output.json 
│   ├── 03_visual_output.json 
│   ├── 04_reviewer_feedback.json 
│   └── 05_finalizer_output.json 
├── traces/ 
│   └── execution_trace.md     # 系統運行追蹤紀錄與流程證明
├── baseline/ 
│   └── single_agent_baseline.md # 單一 Prompt 的對照組腳本
└── outputs/ 
    ├── final_video.mp4        # 最終 60 秒短影片主體 
    ├── subtitles.srt          # 影片之標準時間軸字幕檔 
    └── asset_sources.md       # 影像與音樂素材來源宣告 