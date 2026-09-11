---
name: english-song-interactive-worksheet
version: 2.1.0
author: hsinyuchi (Sylvia)
license: CC BY-NC-SA 4.0
description: >-
  打造專屬教師風格的「英語歌曲互動網頁版學習單」(Interactive English Song Worksheet Pro)。
  由 hsinyuchi (Sylvia) 針對臺灣高中職 A1~A2 英語課堂與 108 課綱學習歷程檔案優化設計。
  具備 10 題行內三選一聽力填空 (含辨音干擾項)、單字語音朗讀 (TTS)、高頻搭配詞與句型解析、
  1~5 星推薦滑桿、動態遊戲化回饋特效 (Confetti/氣球/震動/下雨)、
  A1~A2 友善鷹架句型引導 (Sentence Starters)、頁尾總結算按鈕與收錄完整反思之學習歷程成果認證卡。
---

# 🎧 英語歌曲互動網頁版學習單製作技能 (English Song Worksheet Pro)

> 💡 **Designed & Crafted by**: **hsinyuchi (Sylvia)** | 臺灣高中職英語教育 AI 協作專案  
> 📜 **License**: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)（歡迎教育非商業用途引用、共備與改編，轉載請註明出處）

本 Skill 指導 Agent 遵循專業臺灣高中職英語教師的高效教學標準（特別兼顧普通高中與技術型高中 **CEFR A1 ~ A2 程度** 學習者），將任意西洋流行歌曲或音樂劇曲目，打造為兼具**「課綱學術鷹架」**與**「電玩級動態遊戲回饋」**的單一獨立 HTML5 互動學習單（支援手機、平板與電腦），並可一鍵部署至 Cloudflare Pages、GitHub Pages 或內嵌至 Google Sites。

---

## 🎯 核心規格與教學動線設計準則 (Pedagogical Standards & Flow)

1. **自然學習動線與「頁尾結算按鈕」規範（重要！）**：
   - 網頁流程必須嚴格遵循自然的課堂學習動線：
     1. **聽力挑戰**（10 題行內三選一，具即時對答案按鈕）
     2. **單字深究與發音**（5 大單字 + 搭配詞 + 🔊 朗讀）
     3. **句型文法解析**（大考核心句型 + 造句）
     4. **深度歌詞賞析**（雙語歌詞 + 意境導讀）
     5. **自我反思問答**（1~5 星推薦滑桿 + 句型開頭引導）
     6. **🔚 頁尾總結算按鈕**：
        - **「結算成績並領取成果認證卡」大按鈕必須位於網頁最底部 (Footer)**，讓學生在完整填寫反思問卷後才進行結算。
        - 點擊時若學生尚未填寫反思，系統會貼心提醒，確保產出之認證卡具備實質學習歷程價值。
2. **題數與計分規範**：
   - 固定設計 **10 題** 關鍵聽力挖空，每題 10 分，滿分 **100 分**，直觀銜接平時課堂形成性評量。
3. **手機友善點擊互動 (Mobile-First Inline Popover)**：
   - 摒除需要上下大幅滑動的單字庫拖曳模式。
   - 點擊歌詞中的空格 `[ 1. ____ ]` 時，直接於空格下方彈出 **三選一 (Inline 3-Choice Popover)** 浮動按鈕，單手即可點擊作答。
   - **高品質辨音干擾選項 (Phonological Distractors)**：每個挖空需配備 1 個正解 + 2 個發音相近、押韻、同字首字根或形似之干擾詞（例如：`submission` 配 `commission / permission`；`sail` 配 `sale / tail`），落實聽力辨音教學。
4. **單字庫朗讀發音按鈕 (Web Speech API TTS)**：
   - 每個重點單字與常用搭配詞旁均內建 **「🔊 朗讀」** 按鈕，使用瀏覽器原生 Web Speech API (`en-US`) 免費即時發音，無須依賴外部付費音訊 API。
5. **遊戲化動態特效 (Gamified Visual Feedback)**：
   - 引用 `canvas-confetti` 庫，根據結算成績觸發 4 級動態視覺特效：
     - **80 ~ 100 分**：魔杖星光 🧙‍♀️✨ + 雙側全彩 Confetti 彩帶噴發。
     - **60 ~ 79 分**：熱氣球升空飄浮動畫 🎈☁️。
     - **40 ~ 59 分**：畫面搖晃警告 (Screen Shake) 😬🧹。
     - **40 分以下**：全螢幕灰階降濾鏡 + 逼真雨滴落下動畫 🌧️。
6. **反思問卷之「英主中輔」與鷹架句型引導 (Scaffolded Reflection for A1-A2)**：
   - **雙語友善原則**：題目以**「英文為主、繁中為輔」**呈現，並明文標註：`💡 Feel free to answer in English or Chinese! (歡迎用英文或中文作答，寫出真實想法最重要！)`，消除學生對英語寫作的焦慮。
   - **提供句型開頭引導 (Sentence Starters) 與簡單雙語範例**：
     - 題目一：**Song Rating (1~5 星推薦滑桿)**，即時連動五星圖示與短評。
     - 題目二：**Why do you give this rating?** 附帶模板：`I like this song because...` / `The melody is...`，並提供簡易英中範例。
     - 題目三：**Which lyric line touched you the most? What did you learn?** 附帶模板：`My favorite line is "..." because...` / `From this song, I learned that...`。
7. **108 課綱專屬：學習歷程數位成果認證卡 (Certificate of Achievement)**：
   - 免去手動指導老師簽名欄位。
   - **收錄完整學生反思問答（絕不截斷！）**：完整呈現推薦星等、理由與歌詞心得，作為大學端或校內多元表現審查的實質證據。
   - **智慧教師激勵短評適合 A1~A2 學生理解**：嚴格禁止艱深詞彙，採親切基礎英文，並**一律附上繁體中文註解**：
     - 100 分: *"Amazing job! You heard every word correctly! You are a super listener!"*（太棒了！你每個字都聽對了，你是超級聽力大師！）
     - 80~90 分: *"Great job! Your English listening is wonderful! Keep it up!"*（做得好！你的英文聽力很棒，繼續保持！）
     - 60~70 分: *"Good work! You can catch the beat! Practice more and you will be even better!"*（很棒！你抓到歌曲節奏了，多練習會更進步！）
     - < 60 分: *"Keep trying! Just like a good friend, English will always be here for you! Try again!"*（別放棄！就像好朋友一樣，英文永遠陪伴你，再試一次吧！）
   - 包含學生班級、座號、姓名、作答日期、即時累計耗時、得分、星級評分與反思文字。
   - 使用 `html2canvas` 匯出為高解析度 PNG 圖檔。

---

## 📋 製作標準流程 (SOP 四大階段)

### Step 1: 歌曲資訊與課堂切入點確認
1. **確認曲目與 YouTube 連結**：確認歌曲名稱、歌手/曲目背景、官方 YouTube 影片網址（使用 `youtube-nocookie.com` 嵌入以最大化相容性）。
2. **鎖定 10 大關鍵挖空詞彙與辨音干擾項**：精選 10 個核心單字/片語挖空，每題配置 2 個具辨音價值的近音/押韻干擾項。
3. **挑選 5 個精講單字與 1~2 個高中核心句型**：單字落在 7000 單 Level 2~4；句型符合大考高頻文法。

---

### Step 2: 教學內容精細設計 (Pedagogical Content)
1. **單字深究區 (Vocabulary Study with Audio)**：單字 (含 🔊 發音按鈕)、詞性、中釋、搭配詞 (Collocations)、A1 例句（附發音與中譯）。
2. **核心句型解析 (Target Sentence Structures)**：句型公式化解析、真實歌詞示範、升學/生活實用造句。
3. **深度意境賞析與雙語歌詞 (Song Appreciation & Lyrics)**：200 字左右文化與情意導讀、全曲完整中英對照歌詞。
4. **反思問卷 (Student Reflection with Sentence Starters)**：英主中輔提示語、允許中英自由作答、1~5 星推薦滑桿與句型開頭引導。

---

### Step 3: 高質感 HTML5 互動網頁開發 (單檔純前端)

技術堆疊：`HTML5` + `Tailwind CSS (CDN)` + `Vanilla JavaScript` + `html2canvas (CDN)` + `canvas-confetti (CDN)`。

#### 網頁必備核心模組：
1. **Header 導覽與計時器**：歌曲標題、主題副標、自動跳動作答計時器（`00:00`）。
2. **YouTube 播放視窗 (含防版權跳轉備援按鈕)**：右上角必備 `▶️ 若無法直接播放，點此開啟 YouTube 觀看`。
3. **10 題歌詞挖空與行內三選一 Popover**：點擊空格彈出 3 個按鈕，單手操作，支援進度條。聽力區提供「即時對答案」按鈕。
4. **單字語音與句型賞析區塊**。
5. **反思問卷區塊**：1~5 星滑桿 + 句型開頭鷹架。
6. **頁尾 Grand Submit 區塊**：大卡片包裝之結算按鈕，觸發 Confetti / 氣球 / 震動 / 灰階下雨。
7. **學習歷程認證卡 Modal 與 PNG 匯出**：生成包含完整反思問答之雙語認證卡，一鍵匯出圖檔。

---

### Step 4: 交付成果與部署指南

1. 將產出的單一完整 HTML 程式碼儲存為 `index.html`（或歌曲中文名）。
2. 自動建立打包檔 `site.zip`。
3. 建立本機免上傳測試器（`server.ps1` 與 `.bat`）以利本機即時預覽 YouTube。
4. 提示使用者拖曳至 Cloudflare Pages 或內嵌至 Google Sites。
