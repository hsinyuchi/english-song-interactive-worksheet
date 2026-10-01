---
name: english-song-interactive-worksheet
version: 4.0.0
author: hsinyuchi (Sylvia)
license: CC BY-NC-SA 4.0
description: >-
  打造專屬教師風格的「英語歌曲互動網頁版學習單」(Interactive English Song Worksheet Pro)。
  由 hsinyuchi (Sylvia) 針對臺灣高中職英語課堂（CEFR A2~B1 核心，兼顧 A1~A2 基礎）與 108 課綱學習歷程檔案量身打造。
  具備【YouTube 官方影音 / 原創 MP3 音訊】雙模一體 16:9 劇院級播放器、大考 7000 單 Level 2~4 高品質形似辨音干擾選項、
  10 題行內三選一聽力填空 (含對答案按鈕)、全曲 100% 依序對齊轉錄稿（嚴禁截斷或刪減副歌/尾奏/短句）、
  縮寫單引號與選項字串管道符號安全規範（杜絕選對判錯 Bug）、單字 Web Speech API 真人發音、高頻搭配詞與大考核心文法深度解析、
  1~5 星推薦滑桿、Count on Me 黃金母版標準之雙語鷹架引導句 (Sentence Starters + 英中對照範例)、
  動態遊戲化回饋特效 (Confetti/氣球/震動/下雨)、純淨化成果小卡 (零教師名與官方誇大標籤)、
  100% 免疫 Google Sites 與 iframe 沙箱封鎖架構 (純前端對話框、秒級 html2canvas 渲染、長按/右鍵雙重存圖防護)、
  無編號與即時純前端搜尋過濾之總覽 Hub，以及跨平台 (Gemini / Claude Code / Codex / ChatGPT) 降敏相容規範。
---

# 🎧 英語歌曲互動網頁版學習單製作技能 (English Song Worksheet Pro) v4.0.0

> 💡 **Designed & Crafted by**: **hsinyuchi (Sylvia)** | 臺灣高中職英語教育 AI 協作專案  
> 📜 **License**: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)（歡迎教育非商業用途引用、共備與改編，轉載請註明出處）

本 Skill 指導 Agent 遵循專業臺灣高中職英語教師的高效教學標準，將西洋流行歌曲、音樂劇曲目，或教師透過 SUNO 等工具創作之**原創教學歌曲**，打造為兼具**「課綱學術鷹架」**與**「電玩級動態遊戲回饋」**的單一獨立 HTML5 互動學習單（支援手機、平板與電腦），並可一鍵部署至 Cloudflare Pages、GitHub Pages 或內嵌至 Google Sites。

---

## 🎯 核心規格與教學動線設計準則 (Pedagogical Standards & Flow)

### 1. 預設程度與目標對象：CEFR A2 ~ B1（普高與技高雙軌通用）
- **大考與課綱對齊**：預設難度精準鎖定臺灣普通型高中與技術型高中核心主力 **CEFR A2 ~ B1** 程度。
- **詞彙範圍**：目標單字錨定高中常用 **7000 單 Level 2 ~ Level 4**（以及技高核心詞彙），涵蓋大考高頻搭配詞（Collocations）。
- **高品質辨音干擾選項 (Phonological & Morphological Distractors)**：
  - 每個挖空配備 1 個正解 + 2 個干擾項。
  - 除音近詞外，全面升級融入**「形似字、同字根字首、音節重音、詞性變換」**（例如：`occupied / organized / occurred`；`authentic / artistic / automatic`），直接鍛鍊學測與統測克漏字、文意選填的敏銳度。
  - *彈性擴充*：若教師指定「基礎班/國三銜接」，可降階至 **A1~A2**；若為「大考衝刺班」，可進階至 **B1~B2**。

### 2. 雙音訊源架構 (Dual Audio Source: YouTube / 原生 MP3 播放器)
為確保全站視覺統一，**無論音樂來源為何，影音播放區一律採用標準 16:9 (`aspect-video rounded-2xl`) 劇院級播放視窗**：
- **模式 A：YouTube 影音模式**
  - 當提供 YouTube 網址時，於 16:9 視窗內嵌入標準純淨 YouTube 播放器（使用 `youtube-nocookie.com/embed/{id}?rel=0&enablejsapi=1`）。
  - 右上角必備醒目的 `▶️ 若無法直接播放，點此開啟 YouTube 觀看` 跳轉連結。
- **模式 B：原創 MP3 / 本機音訊模式（Suno、錄音或自備音檔）**
  - 當提供 MP3 檔案或原創音樂時，16:9 視窗自動渲染為 **劇院級原生音訊播放器**：
    1. 中央配置醒目的 **YouTube 風格大型播放/暫停按鈕 (▶️/⏸️)**，點擊畫面中央即刻播放。
    2. 播放時中央同步啟動 **動態聲波頻譜動畫 (Equalizer Waveform)**。
    3. 底部配置現代化半透明控制列：播放切換、**`⏪ -5s / +5s ⏩` 快退快進（聽力精聽必備）**、時間進度條（Scrubber 與 `00:00 / 03:33` 時間標籤）、**`0.8x 慢速 / 1.0x 原速 / 1.2x 挑戰` 三段聽力變速膠囊**。
    4. 音訊來源支援多重備援：本機 `audio.mp3`、Hub 同步檔 `audio_{slug}.mp3`，以及 Cloudflare 全球 CDN 直連串流。
    5. 右上角配置 `▶️ 點此下載或於新視窗播放原曲 MP3` 備援按鈕。

### 3. 全曲完整轉錄稿 100% 依序對齊鐵律 (Absolute Red Line: 100% Unabridged Lyrics)
- 🎙️ **嚴禁截斷或腰斬歌詞**：學生聽力作答是眼睛盯著網頁歌詞、耳朵跟隨旋律。一旦歌詞中途腰斬或省略，學生會瞬間失去定位！
- 包含：前奏 Intro ➜ 主歌 Verse 1 ➜ 導歌 Pre-Chorus 1 ➜ 副歌 Chorus 1 ➜ 主歌 Verse 2 ➜ 導歌 Pre-Chorus 2 ➜ 副歌 Chorus 2 ➜ 橋段 Bridge ➜ 副歌 Chorus 3 ➜ 尾奏 Outro。
- 從 0:00 唱到最後一秒收尾，逐行依序排列，每一句均附標準繁體中文意譯。
- 🛡️ **括號防衝突安全規範**：僅 10 個挖空單字允許使用半形中括號 `[word]`。其餘角色標籤或合唱標籤一律使用圓括號 `(Chorus)` 或全形括號 `【合唱】`。

### 4. 手機友善點擊互動與防遮擋標準 (Inline Popover & Anti-Overlap Standard)
- 點擊歌詞中的空格 `[ 1. ____ ]` 時，直接於空格下方彈出 **三選一 (Inline 3-Choice Popover)** 浮動按鈕，單手即可點擊作答。
- 🛡️ **CSS 層疊上下文防遮擋規範**：
  ```css
  .lyric-line.active-line { z-index: 500 !important; }
  .cloze-blank.has-popover { z-index: 1000 !important; }
  ```
- 支援智慧翻轉（接近視窗底部時向上彈出 `.pop-up`），確保上下相鄰挖空絕不互相覆蓋。
- 🛡️ **選項字串管道符號安全規範 (Apostrophe Safety)**：
  - 選項存入 DOM 時改用管道符號 `|` 分隔（如 `data-options="${optsList.join('|')}"`），嚴禁反斜線轉義 `\'`。
  - 比對答案一律採去首尾空白比對 `userAns.trim() === correct.trim()`，杜絕英文縮寫單引號（如 `don't`, `you're`）判定失效 Bug。

### 5. 跨平台相容性與降敏規範 (Cross-Platform: Claude Code / Codex / ChatGPT / Gemini)
- **版權防禦解敏 (Copyright Sensitivity De-escalation)**：
  - 將全曲歌詞與音訊明確宣告為**「英語教學形成性評量轉錄稿 (Educational Listening Transcript & Cloze Worksheet)」**，符合臺灣著作權法第 46 條及國際合理使用 (Fair Use) 原則。
  - 避免使用「抓取全曲完整歌詞」等可能觸發外部 LLM 版權封鎖的敏感字眼，將任務聚焦於「聽力測驗題庫編寫與排版」。
  - 若遇冷門曲目或模型記憶庫受限，AI 應友善引導教師「直接貼上歌詞或音訊轉錄稿」，由 AI 自動進行挖空與版型建構。
- 🚫 **嚴格禁止道德說教與警語標籤**：
  - **絕對嚴禁在網頁前端、成果小卡或程式碼中主動輸出「涉及性暗示」、「兒少不宜警告」或對教師指指點點的道德審查警語**。
  - 教材選用與教學情境之判斷權 100% 歸屬於教師本人，AI 應專注於呈現乾淨專業的教材本體。

### 6. 自然學習動線與「Count on Me 黃金母版」標準
網頁架構、模組順序與 DOM ID 必須 100% 完全對齊《Count on Me》黃金母版規範：
1. **Header 導覽與右上角鎖定計時器** (`#live-timer`)
2. **16:9 劇院級播放視窗** (YouTube 模式或 MP3 原生播放器模式)
3. **聽力測驗區 (`#quiz-area`) 與黏性進度條** (`#progress-bar`, `#progress-text`)
   - 底部配置 `✅ 即時對答案 (Check Answers)` 與 `⬇️ 繼續往下學習與填寫反思` 雙按鈕。
4. **單字深究區 (Vocabulary Study)**：5 大重點單字片語，內建 🔊 Web Speech API 原生真人發音與高頻搭配詞。
5. **大考核心句型解析 (Target Sentence Patterns)**：2 大高頻句型公式、歌詞示範與升學實用造句。
6. **聽懂這首歌：青年共鳴與背後寓意**：面向高中職學生的對話式賞析短文 ＋ 歌曲檔案卡。
7. **學生自我反思問答區 (`#reflection-section`)**：
   - Q1: 1~5 星動態推薦滑桿 (`#rating-slider`, `#rating-badge`)。
   - Q2 & Q3: 獨立雙語鷹架方塊 (Sentence Starters ＋ 英中對照範例)，引導學生寫出扎實學習歷程心得。
8. **頁尾 Grand Submit 結算區塊**：大卡片包裝之結算按鈕，內建「漏填反思貼心防呆守門員 (Reflection Guard)」。
9. **學習歷程認證卡 Modal 與 PNG 匯出**：生成純淨化雙語認證卡（100% 屬於學生個人成就，無教師名與官方生硬標籤），支援 `html2canvas` 一鍵匯出 PNG。
10. **頁尾非營利教育版權宣告**。

### 7. 🛡️ Google Sites 與 iframe 沙箱 100% 相容鐵律
- 🚫 **零原生彈跳視窗（Zero Native Dialogs）**：絕對嚴禁使用 `window.alert()` 與 `window.confirm()`！一律使用純前端自製容器 `#custom-dialog-modal`。
- ⚡ **html2canvas 效能與防跨域超時規範**：配置 `imageTimeout: 1200`、`useCORS: true`、`allowTaint: true`、`logging: false`，保證 1～2 秒內秒級完成卡片繪製。
- 📱 **Google Sites / 行動裝置雙重保險存圖機制**：生成 PNG 後，同步呈現在 `#cert-image-preview-wrapper` 供手機長按存圖或電腦右鍵另存。

---

## 🏛️ 英歌總部自動雙向歸檔規範 (Headquarters Auto-Filing)

每當完成新歌曲或更新歌曲學習單時，除當前工作區外，**必須自動同步鏡像歸檔至英歌總部**：
- **總部絕對路徑**：`H:\我的雲端硬碟\# Sylvia's Workspace\[置頂] Sylvia's 英歌總部\`
- **標準歸檔動作**：
  1. 在 `02_各曲獨立完整包/` 建立/更新歌曲專屬目錄（如 `26_曲名/`），置入單機 HTML、site.zip、歌詞 txt、字幕 lrc（若為 MP3 模式，一併收納 audio.mp3）。
  2. 同步複製單機 HTML 與必要音檔至 `01_線上播放總覽Hub/`，並按英文字母首字母 (A-Z) 排序更新 Hub 首頁卡片清單與總數徽章。
  3. 自動更新總部的 `README_歌曲線上學習單總覽.md`（追加曲目表格、線上網址與最新曲目總數）。
