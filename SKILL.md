---
name: english-song-interactive-worksheet
version: 2.2.0
author: hsinyuchi (Sylvia)
license: CC BY-NC-SA 4.0
description: >-
  打造專屬教師風格的「英語歌曲互動網頁版學習單」(Interactive English Song Worksheet Pro)。
  由 hsinyuchi (Sylvia) 針對臺灣高中職 A1~A2 英語課堂與 108 課綱學習歷程檔案優化設計。
  具備 10 題行內三選一聽力填空 (含辨音干擾項)、單字語音朗讀 (TTS)、高頻搭配詞與句型解析、
  1~5 星推薦滑桿、動態遊戲化回饋特效 (Confetti/氣球/震動/下雨)、
  A1~A2 友善鷹架句型引導 (Sentence Starters)、頁尾總結算按鈕與收錄完整反思之學習歷程成果認證卡。
  嚴格規範 YouTube 影片必須為英文字幕或無字幕（零中文字幕）、落實教育合理使用版權聲明，
  以及標準化 Cloudflare Pages (hsinyuchi-) 批次自動部署機制。
---

# 🎧 英語歌曲互動網頁版學習單製作技能 (English Song Worksheet Pro)

> 💡 **Designed & Crafted by**: **hsinyuchi (Sylvia)** | 臺灣高中職英語教育 AI 協作專案  
> 📜 **License**: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)（歡迎教育非商業用途引用、共備與改編，轉載請註明出處）

本 Skill 指導 Agent 遵循專業臺灣高中職英語教師的高效教學標準（特別兼顧普通高中與技術型高中 **CEFR A1 ~ A2 程度** 學習者），將西洋流行歌曲或音樂劇曲目，打造為兼具**「課綱學術鷹架」**與**「電玩級動態遊戲回饋」**的單一獨立 HTML5 互動學習單（支援手機、平板與電腦），並可一鍵部署至 Cloudflare Pages、GitHub Pages 或內嵌至 Google Sites。

---

## 🎯 核心規格與教學動線設計準則 (Pedagogical Standards & Flow)

### 1. 自然學習動線與「頁尾結算按鈕」規範
- 網頁流程必須嚴格遵循自然的課堂學習動線：
  1. **聽力挑戰**（10 題行內三選一，具即時對答案按鈕）
  2. **單字深究與發音**（5 大單字 + 搭配詞 + 🔊 朗讀）
  3. **句型文法解析**（大考核心句型 + 造句）
  4. **深度歌詞賞析**（雙語歌詞 + 意境導讀）
  5. **自我反思問答**（1~5 星推薦滑桿 + 句型開頭引導）
  6. **🔚 頁尾總結算按鈕**：
     - **「結算成績並領取成果認證卡」大按鈕必須位於網頁最底部 (Footer)**，讓學生在完整填寫反思問卷後才進行結算。
     - 點擊時若學生尚未填寫反思，系統會貼心提醒，確保產出之認證卡具備實質學習歷程價值。

### 2. 題數與計分規範
- 固定設計 **10 題** 關鍵聽力挖空，每題 10 分，滿分 **100 分**，直觀銜接平時課堂形成性評量。

### 3. 手機友善點擊互動與防遮擋標準 (Inline Popover & Anti-Overlap Standard)
- 摒除需要上下大幅滑動的單字庫拖曳模式。
- 點擊歌詞中的空格 `[ 1. ____ ]` 時，直接於空格下方彈出 **三選一 (Inline 3-Choice Popover)** 浮動按鈕，單手即可點擊作答。
- **高品質辨音干擾選項 (Phonological Distractors)**：每個挖空需配備 1 個正解 + 2 個發音相近、押韻、同字首字根或形似之干擾詞（例如：`submission` 配 `commission / permission`；`sail` 配 `sale / tail`），落實聽力辨音教學。
- 🛡️ **CSS 層疊上下文防遮擋規範（關鍵！）**：
  - 歌詞行與空格在作答展開時，必須設定高優先級層疊上下文，防止下一行空格或選項遮擋住上一行的選項按鈕：
    ```css
    .lyric-line.active-line { z-index: 500; position: relative; }
    .cloze-blank.has-popover { z-index: 1000 !important; }
    ```
  - 支援智慧翻轉（接近視窗底部時向上彈出 `.pop-up` 與指引小三角箭頭），確保上下相鄰挖空絕不互相覆蓋。

### 4. YouTube 影片選用、播放相容性與字幕審查標準（極重要！）
- **全面檢測嵌入權限**：必須使用允許外部網頁 `iframe` 嵌入之影片（選定前需透過 YouTube oEmbed API 驗證 `status: 200`，絕不可使用 404 失效、私人未公開或被版權方禁止外嵌之 ID）。
- **字幕要求極致純淨（英文字幕或無字幕，絕對禁止中文字幕）**：
  - 首選官方純英文字幕 (Official Lyric Video)、官方無字幕音訊 (Official Audio) 或官方 MV。
  - **嚴格禁止任何帶有繁體或簡體中文字幕（中文翻譯）之影片**，避免學生直接抄答案、破壞英語聽力純度與教室沉浸感。
- **播放器防呆備援按鈕**：播放器右上角必備醒目的 `▶️ 若無法直接播放，點此開啟 YouTube 觀看` 備援跳轉連結。

### 5. 嚴謹版權聲明與教育合理使用規範 (Copyright & Fair Use Standard)
- **杜絕誇大宣傳語句**：嚴禁使用浮誇、自吹自擂或無意義的行銷文宣詞彙。
- **標準版權免責聲明結構**：
  - **總覽 Hub 旗艦橫幅**：必須明確標示非營利教學聲明與著作權歸屬：
    ```html
    <div class="max-w-3xl mx-auto mt-4 bg-white/10 backdrop-blur-md rounded-2xl p-4 border border-white/20 text-left text-xs text-purple-100 leading-relaxed space-y-2">
      <div class="flex items-center gap-2 font-bold text-white text-sm border-b border-white/20 pb-2">
        <span>⚖️ 版權聲明與合理使用原則 (Copyright & Educational Fair Use)</span>
      </div>
      <p>本教材由 <strong>hsinyuchi (Sylvia)</strong> 設計製作，<strong>僅供高中職英語課堂教學與學術研究非營利使用 (Educational Use Only)</strong>。</p>
      <p class="text-purple-200 text-xs">教材中所引用之流行音樂、官方音訊、歌詞文本與影音素材，<strong>所有著作權與智慧財產權均完整歸屬於原創作者、演唱歌手、所屬唱片公司及原發行出版商所有</strong>。</p>
      <div class="flex flex-wrap items-center justify-between pt-1 text-[11px] text-purple-300 border-t border-white/10">
        <span>📌 依據著作權法第 46 條及第 52 條學校教學合理使用範疇</span>
        <span>💡 程式與學習單架構採 CC BY-NC-SA 4.0 授權</span>
      </div>
    </div>
    ```
  - **單曲學習單頁尾**：作者標示旁必須附帶免責宣告：  
    `Designed with ❤️ by hsinyuchi (Sylvia) ｜ 本學習單僅供學術教學非商業使用，音樂與歌詞版權歸原出版唱片公司所有`

### 6. 單字庫朗讀發音按鈕 (Web Speech API TTS)
- 每個重點單字與常用搭配詞旁均內建 **「🔊 朗讀」** 按鈕，使用瀏覽器原生 Web Speech API (`en-US`) 免費即時發音，無須依賴外部付費音訊 API。

### 7. 遊戲化動態特效 (Gamified Visual Feedback)
- 引用 `canvas-confetti` 庫，根據結算成績觸發 4 級動態視覺特效：
  - **80 ~ 100 分**：魔杖星光 🧙‍♀️✨ + 雙側全彩 Confetti 彩帶噴發。
  - **60 ~ 79 分**：熱氣球升空飄浮動畫 🎈☁️。
  - **40 ~ 59 分**：畫面搖晃警告 (Screen Shake) 😬🧹。
  - **40 分以下**：全螢幕灰階降濾鏡 + 逼真雨滴落下動畫 🌧️。

### 8. 反思問卷之「英主中輔」與鷹架句型引導 (Scaffolded Reflection for A1-A2)
- **雙語友善原則**：題目以**「英文為主、繁中為輔」**呈現，並明文標註：`💡 Feel free to answer in English or Chinese! (歡迎用英文或中文作答，寫出真實想法最重要！)`，消除學生對英語寫作的焦慮。
- **提供句型開頭引導 (Sentence Starters) 與簡單雙語範例**：
  - 題目一：**Song Rating (1~5 星推薦滑桿)**，即時連動五星圖示與短評。
  - 題目二：**Why do you give this rating?** 附帶模板：`I like this song because...` / `The melody is...`，並提供簡易英中範例。
  - 題目三：**Which lyric line touched you the most? What did you learn?** 附帶模板：`My favorite line is "..." because...` / `From this song, I learned that...`。

### 9. 108 課綱專屬：學習歷程數位成果認證卡 (Certificate of Achievement)
- 免去手動指導老師簽名欄位。
- **收錄完整學生反思問答（絕不截斷！）**：完整呈現推薦星等、理由與歌詞心得，作為大學端或校內多元表現審查的實質證據。
- **智慧教師激勵短評適合 A1~A2 學生理解**：採親切基礎英文，並**一律附上繁體中文註解**（100 分、80~90 分、60~70 分、< 60 分）。
- 包含學生班級、座號、姓名、作答日期、即時累計耗時、得分、星級評分與反思文字。
- 使用 `html2canvas` 匯出為高解析度 PNG 圖檔。

---

## 📋 製作標準流程 (SOP 四大階段)

### Step 1: 歌曲資訊、課堂切入點與影片審查
1. **確認曲目與 YouTube 官方影片**：
   - 必須挑選**「純英文字幕」或「官方無字幕」**版本，嚴禁任何中文字幕。
   - 使用 `youtube-nocookie.com/embed/{id}?rel=0&enablejsapi=1` 嵌入以最大化相容性。
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
3. **10 題歌詞挖空與行內三選一 Popover**：
   - 點擊空格彈出 3 個按鈕，單手操作，支援進度條。聽力區提供「即時對答案」按鈕。
   - 套用防遮擋 CSS：`.lyric-line.active-line`（`z-index: 500`）與 `.cloze-blank.has-popover`（`z-index: 1000 !important`）。
4. **單字語音與句型賞析區塊**。
5. **反思問卷區塊**：1~5 星滑桿 + 句型開頭鷹架。
6. **頁尾 Grand Submit 區塊**：大卡片包裝之結算按鈕，觸發 Confetti / 氣球 / 震動 / 灰階下雨。
7. **學習歷程認證卡 Modal 與 PNG 匯出**：生成包含完整反思問答之雙語認證卡，一鍵匯出圖檔。
8. **頁尾教育版權聲明**：載明非商業教學用途與版權歸屬。

---

### Step 4: 交付成果與部署指南

1. **單檔與離線包產出**：
   - 產出單一完整 HTML（如 `Taylor_Swift_Shake_It_Off_網頁學習單.html`）。
   - 自動打包對應之 `_site.zip` 離線與部署壓縮檔。
2. **總覽 Hub 入口升級**：
   - 總覽 Hub 頂部具備完整版權聲明。
   - 每首卡片皆提供三大行動按鈕：
     - `🚀 線上互動版`：直連專屬 Cloudflare Pages 網址。
     - `💻 單機版`：本機離線瀏覽。
     - `📦 Zip`：下載部署包。
3. **Cloudflare Pages 全域命名與部署規範**：
   - **專案前綴統一規範**：`hsinyuchi-[song-slug]`（例如 `hsinyuchi-count-on-me`），總覽 Hub 為 `hsinyuchi-songs-hub`。
   - **正式網址結構**：
     - 單曲：`https://hsinyuchi-[song-slug].pages.dev`
     - 總覽 Hub：`https://hsinyuchi-songs-hub.pages.dev`
   - **自動化部署腳本防呆設計**：
     - Windows 批次檔必須宣告 `chcp 65001 >nul`，確保繁體中文路徑與訊息不亂碼。
     - 呼叫原生 `python`（自動偵測本機 Python 路徑，杜絕語法錯誤閃退）。
     - 批次檔結尾必須加入 `pause >nul`，確保執行結果保持顯示，絕不閃退。

---

## 🛡️ 研習現場自動防呆與環境相容機制 (Workshop Foolproof & Pre-Flight Check)

為了確保在研習工作坊、教師社群共備現場，**每一位老師（無論使用 Windows / Mac / 公用電腦）都能 100% 成功編譯與運行**，AI Agent 必須遵循以下防呆標準作業程序：

### 1. 自動環境前置檢測 (Automated Pre-Flight Check)
在執行任何產出任務前，AI 必須主動檢查執行環境。若缺少必要套件，**必須主動提供「一鍵複製貼上」的安裝指令**：
```bash
# 研習學員必備核心工具包（一鍵全裝指令）：
pip install requests beautifulsoup4
```

### 2. 零門檻優雅降級模式 (Graceful Fallback)
若學員受限於學校電腦權限無法安裝 Python 套件時，AI 必須自動啟動**「免安裝純前端降級模式」**：
- 語音播放：自動採用瀏覽器原生免安裝的 **Web Speech API (TTS)**。
- 簡報與學習單運作：維持 **100% 純原生 Vanilla HTML5/CSS3/JS**，免開伺服器、免配資料庫，點開瀏覽器即刻教學！
