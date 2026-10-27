---
name: sylvia-song
aliases: [english-song-interactive-worksheet, hsinyuchi-english-song]
version: 4.1.0
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

# 🎧 英語歌曲互動網頁版學習單製作技能 (English Song Worksheet Pro) v4.1.0

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

### 8. 🌐 自動化 Cloudflare 部署與 Portal / Hub 聯動規範 (Cloudflare & Portal Auto-Publishing SOP)
每當英語歌曲互動學習單產出完成後，AI 必須自動執行以下發布檢測流程：
1. **Cloudflare 憑證智慧嗅探**：
   - 執行 wrangler whoami。若本機未登入 Cloudflare 或無有效憑證，**自動優雅降級**（免報錯打擾教師），僅產出本地獨立 HTML、歌詞文字稿與 site.zip 部署壓縮包供手動上傳。
2. **具備 Cloudflare 憑證時的全自動三級發布管線**：
   - **一級：單曲獨立部署**：將該歌曲部署至專屬 Pages 站點 hsinyuchi-[song-slug]，**一律強制指定 --branch=main --commit-dirty=true**（指令：
px wrangler pages deploy <dir> --project-name=hsinyuchi-[slug] --branch=main --commit-dirty=true），確保線上頂級網域即時更新。
   - **二級：總覽 Hub 同步發布**：將新歌曲卡片與單機檔同步複製至  1_線上播放總覽Hub，依英文字母 A-Z 順序插入，自動更新總曲目數量徽章，並重新部署至 hsinyuchi-songs-hub（網址：https://hsinyuchi-songs-hub.pages.dev）。
   - **三級：個人入口網 (Portal) 聯動發布**：同步檢查個人總入口 Portal 網站（hsinyuchi-portal，位於  0_Portal），更新曲目數量標籤（如 28+ 曲目），並一併自動部署至 https://hsinyuchi-portal.pages.dev。

---


## ⚠️ 常見地雷、教訓與零降級防坑守則 (Anti-Patterns & Critical Pitfalls)

以下總結 Sylvia 與 AI 在實戰迭代過程中遭遇的關鍵痛點與踩坑紀錄，所有後續開發**嚴格禁止重蹈覆轍**：

### 1. 🚨 Cloudflare Pages Production 分支陷阱（頂級網域未更新 Bug）
- **痛點情境**：本地 Git 若處於 master 分支，直接執行 
px wrangler pages deploy 會預設發布為 master 預覽分支 (Preview)。而 Cloudflare Pages 的生產頂級網域 (https://<project-name>.pages.dev/) 僅綁定 main 生產分支，導致線上畫面完全沒變，讓使用者誤以為部署失敗！
- **黃金指令**：
  `ash
  # 部署時必須明確指定 --branch=main 與 --commit-dirty=true
  npx wrangler pages deploy <部署目錄> --project-name=<專案名稱> --branch=main --commit-dirty=true
  `
- **建立專案防呆**：
  `ash
  # 建立新 Pages 專案時一律指定 --production-branch=main 並加上 --force 避免被根目錄 wrangler.jsonc 劫持為 Workers
  npx wrangler pages project create <專案名稱> --production-branch=main --force
  `

### 2. 🏛️ SongsHub 黃金母版 100% 規格鎖定（嚴禁自行發明新模組與版面失控）
- **嚴禁模組擴張 (Zero Scope Creep)**：全站所有曲目均屬於同一個 SongsHub 體系，外觀動線與區塊規格必須 100% 一致。**絕對禁止擅自新增未經要求的自創模組**（如「聽力連音弱讀指南」、「發音比較表」或巨型額外解說）。
- **文法句型解析嚴格維持 2 張標準卡片**：
  - 即使教師指定更換文法焦點（如：關係子句限定/非限定用法），也只能將內容填入現有的 2 張標準卡片（每張卡片包含：句型公式與核心考點、🎵 歌詞原句、💡 升學實用造句）。
  - **嚴禁膨脹為教科書式長篇章節**，維持精準易讀的微學習卡片結構。
- **歌詞對齊一律靠左 (	ext-left)**：
  - 歌詞容器一律靠左對齊，**嚴禁出現部分置中、部分靠左的混亂排版**。
- **三選一挖空互動標準鎖定**：
  - 挖空處必須為虛線底線膠囊容器 .cloze-blank，點擊呼叫 	oggleInlinePopover(id, event)。
  - 彈出選單必須為橫向排列的 .inline-popover，含三顆選項按鈕與三角形指針，並支援接近畫面底部時向上翻轉 (.pop-up)。
  - **嚴禁擅改為原生下拉選單 (<select>)、靜態按鈕列或居中對話框**。

### 3. 🎙️ Behind the Song（聽懂這首歌）對話語氣鐵律（嚴禁論文式說教與教師視角）
- **受眾對象**：直面**臺灣高中職學生**（青年學子）。
- **人稱與語調**：必須使用**第二人稱「你」**或親切溫暖的「同學們」，語調具同理心、有溫度、像知心朋友或大姊姊與學生促膝談心。
- **嚴格禁止第三人稱教育學術/行政說教腔調**：
  - ❌ **錯誤範例（寫給評審/老師看的）**：「本曲旨在引導學生發掘自我價值，提醒每位年輕學子不必迎合世俗標準，卸下成長過程中的外表焦慮。」
  - ✅ **正確範例（直接跟學生說話）**：「當你站在鏡子前，是不是也曾挑剔自己的不完美？這首歌想溫柔地告訴你：做最真實的你就已經足夠，你的獨特與善良，就是全世界最閃耀的光芒！」

### 4. 🎓 Grand Submission 結算大卡片與認證卡 Modal 完整性
- 頁尾必須保留紫粉漸層 3D 大卡片容器（含 SVG 幾何浮水印、🎓 學習任務總結算 ｜ 108課綱學習歷程數位佐證 膠囊徽章、雙行鼓勵說明與脈衝按鈕）。
- 點擊後喚起純前端自製 Modal（嚴禁 window.alert / window.confirm），認證卡無教師名與官方誇大標籤，支援手機長按存圖與 html2canvas 匯出 PNG。


---

## 🏛️ 英歌總部自動雙向歸檔規範 (Headquarters Auto-Filing)

每當完成新歌曲或更新歌曲學習單時，除當前工作區外，**必須自動同步鏡像歸檔至英歌總部**：
- **總部絕對路徑**：`H:\我的雲端硬碟\# Sylvia's Workspace\[置頂] Sylvia's 英歌總部\`
- **標準歸檔動作**：
  1. 在 `02_各曲獨立完整包/` 建立/更新歌曲專屬目錄（如 `26_曲名/`），置入單機 HTML、site.zip、歌詞 txt、字幕 lrc（若為 MP3 模式，一併收納 audio.mp3）。
  2. 同步複製單機 HTML 與必要音檔至 `01_線上播放總覽Hub/`，並按英文字母首字母 (A-Z) 排序更新 Hub 首頁卡片清單與總數徽章。
  3. 自動更新總部的 `README_歌曲線上學習單總覽.md`（追加曲目表格、線上網址與最新曲目總數）。

---

## 🔒 跨 Agent 執行防漂移鐵律 (Cross-Agent Anti-Drift Protocol)

> **⚡ 適用環境：Google Antigravity、OpenAI Codex CLI、Claude Code、Cursor 等全平台 Agent**

任何 AI Agent 在執行本技能時，**嚴禁依賴各平台大模型的默認輸出習慣自由發揮**，必須 100% 嚴格落實以下防漂移守則：

1. **零自作主張 (Zero Creative Deviation)**：
   - 嚴格沿用本規範定義之排版結構、區塊順序、欄位標籤與樣式。
   - **嚴禁私自「改寫/簡化」架構**（例如擅自將特定 Flex/Grid 佈局改寫為文字列表、將精確卡片改為空泛條列、或將樣式簡化）。
   - **嚴禁自創未經授權的新區塊**（例如擅自新增額外理論講義、發音表或未要求的長篇大論）。
2. **骨架代碼與格式優先 (Template Boilerplate Priority)**：
   - 若本規範提供具體代碼片段（HTML、CSS、JS、Markdown 骨架、卡片容器），必須作為不可變更之「填空基底 (Immutable Slots)」。
   - Agent 的任務僅是將內容精準填入對應的 Slots 容器中，**禁止改動外層容器 class 名稱、DOM 結構與事件綁定機制**。
3. **成品規格不降級 (No Spec Downgrade)**：
   - 嚴禁因 Token 長度限制或內容龐大，而將「圖文並茂互動網頁/雙軌講義」偷工減料降級為「純文字草稿」或「簡短大綱」。
   - 遇長文本時必須完整輸出全課內容或完整分段寫入目標檔案，**絕不省略後半段**。
4. **雙軌/多模態完整性 (Dual-Track Completeness)**：
   - 凡涉及「學生練習版」與「教師紅字解答版」之技能，必須兩套完整產出，答案與詳解必須扎實完整，嚴禁留白。
   - 凡涉及固定卡片數量（如 2 張文法卡片、5 大單字卡片、10 題挖空等），**嚴格維持指定數量，不多不少**。
5. **角色語氣與受眾鎖定 (Persona & Audience Alignment)**：
   - 嚴格維持臺灣高中職英語科專業教師立場，第二人稱「你」或「同學們」具同理心之對話語調，**嚴格杜絕第三人稱論文式說教腔**。

### 🏛️ 歌曲學習單不可變更之核心元件 HTML 骨架 (Immutable Component Boilerplate)

#### (1) 行內三選一挖空按鈕骨架（嚴禁改為 select 下拉選單）：
```html
<span class="cloze-wrapper relative inline-block mx-1 my-0.5">
  <span id="blank-q1" class="cloze-blank border-b-2 border-dashed border-indigo-400 text-indigo-700 font-bold px-2 py-0.5 cursor-pointer hover:bg-indigo-50 rounded transition-all duration-200 select-none" onclick="toggleInlinePopover('q1', event)">______</span>
  <div id="popover-q1" class="inline-popover hidden absolute left-1/2 -translate-x-1/2 bottom-full mb-2 z-50 bg-white shadow-xl rounded-xl p-1.5 border border-indigo-100 flex gap-1.5 items-center whitespace-nowrap">
    <button type="button" class="px-2.5 py-1 text-xs font-semibold rounded-lg bg-slate-100 hover:bg-indigo-600 hover:text-white transition-colors" onclick="selectAnswer('q1', '選項A', '正確答案')">選項A</button>
    <button type="button" class="px-2.5 py-1 text-xs font-semibold rounded-lg bg-slate-100 hover:bg-indigo-600 hover:text-white transition-colors" onclick="selectAnswer('q1', '選項B', '正確答案')">選項B</button>
    <button type="button" class="px-2.5 py-1 text-xs font-semibold rounded-lg bg-slate-100 hover:bg-indigo-600 hover:text-white transition-colors" onclick="selectAnswer('q1', '選項C', '正確答案')">選項C</button>
  </div>
</span>
```

#### (2) 大考核心句型解析骨架（嚴格 2 張卡片並列 Grid）：
```html
<section id="grammar-section" class="max-w-4xl mx-auto my-12 px-4">
  <h2 class="text-2xl font-black text-slate-800 mb-6 flex items-center gap-2"><span>🎯</span> 大考核心句型解析</h2>
  <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
    <!-- Card 1 -->
    <div class="bg-white border-2 border-indigo-100 rounded-2xl p-6 shadow-sm hover:shadow-md transition">
      <div class="inline-block px-3 py-1 bg-indigo-50 text-indigo-700 text-xs font-bold rounded-full mb-3">Pattern 01 ｜ 文法焦點名稱</div>
      <div class="text-sm font-bold text-slate-800 bg-slate-50 p-3 rounded-xl mb-4 font-mono border-l-4 border-indigo-500">公式：S + V ...</div>
      <div class="text-xs text-slate-600 mb-2 leading-relaxed"><strong class="text-indigo-600">🎵 歌詞原句：</strong>"Lyrics sentence here"</div>
      <div class="text-xs text-slate-600 leading-relaxed"><strong class="text-emerald-600">💡 升學造句：</strong>Practical sentence for CEEC exams.</div>
    </div>
    <!-- Card 2 -->
    <div class="bg-white border-2 border-indigo-100 rounded-2xl p-6 shadow-sm hover:shadow-md transition">
      <div class="inline-block px-3 py-1 bg-indigo-50 text-indigo-700 text-xs font-bold rounded-full mb-3">Pattern 02 ｜ 文法焦點名稱</div>
      <div class="text-sm font-bold text-slate-800 bg-slate-50 p-3 rounded-xl mb-4 font-mono border-l-4 border-indigo-500">公式：S + V ...</div>
      <div class="text-xs text-slate-600 mb-2 leading-relaxed"><strong class="text-indigo-600">🎵 歌詞原句：</strong>"Lyrics sentence here"</div>
      <div class="text-xs text-slate-600 leading-relaxed"><strong class="text-emerald-600">💡 升學造句：</strong>Practical sentence for CEEC exams.</div>
    </div>
  </div>
</section>
```

#### (3) 頁尾 Grand Submission 結算大卡片骨架（置中漸層 3D 卡片）：
```html
<section id="submission-section" class="max-w-2xl mx-auto my-12 px-4">
  <div class="bg-gradient-to-r from-purple-600 via-indigo-600 to-pink-500 rounded-3xl p-8 text-white text-center shadow-2xl relative overflow-hidden">
    <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-white/20 backdrop-blur-sm text-xs font-semibold mb-4">
      <span>🎓</span> 學習任務總結算 ｜ 108課綱學習歷程數位佐證
    </div>
    <h3 class="text-2xl font-black mb-2 tracking-wide">恭喜完成全曲聽力與反思任務！</h3>
    <p class="text-white/80 text-xs mb-6 max-w-md mx-auto">點擊下方按鈕結算成績，生成專屬學習歷程數位認證卡，可一鍵儲存為成果圖檔佐證。</p>
    <button id="grand-submit-btn" type="button" onclick="handleGrandSubmission()" class="px-8 py-3.5 bg-white text-indigo-700 font-extrabold rounded-2xl shadow-lg hover:shadow-xl hover:scale-105 active:scale-95 transition-all text-sm tracking-wider inline-flex items-center gap-2">
      <span>🏆</span> 結算成績並領取認證卡
    </button>
  </div>
</section>
```

#### (4) 純淨化認證卡 Modal 骨架（零教師名與官方生硬標籤）：
```html
<div id="cert-modal" class="hidden fixed inset-0 z-50 bg-black/60 backdrop-blur-sm flex items-center justify-center p-4">
  <div class="bg-white rounded-3xl max-w-lg w-full p-6 shadow-2xl relative max-h-[90vh] overflow-y-auto">
    <button type="button" onclick="closeCertModal()" class="absolute top-4 right-4 text-slate-400 hover:text-slate-600 text-lg font-bold">&times;</button>
    <div id="cert-card-render" class="p-6 bg-gradient-to-br from-indigo-500 via-purple-600 to-pink-500 rounded-2xl text-white shadow-inner">
      <!-- Certificate Content: 100% Student Achievement -->
    </div>
    <div class="mt-4 flex gap-3">
      <button type="button" onclick="exportCertAsPNG()" class="flex-1 py-2.5 bg-indigo-600 text-white font-bold rounded-xl text-xs hover:bg-indigo-700 transition">📸 下載證書圖片 (PNG)</button>
      <button type="button" onclick="closeCertModal()" class="px-4 py-2.5 bg-slate-100 text-slate-600 font-bold rounded-xl text-xs hover:bg-slate-200 transition">關閉</button>
    </div>
  </div>
</div>
```
