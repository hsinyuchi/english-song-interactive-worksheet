---
name: english-song-interactive-worksheet
version: 2.9.0
author: hsinyuchi (Sylvia)
license: CC BY-NC-SA 4.0
description: >-
  打造專屬教師風格的「英語歌曲互動網頁版學習單」(Interactive English Song Worksheet Pro)。
  由 hsinyuchi (Sylvia) 針對臺灣高中職 A1~A2 英語課堂與 108 課綱學習歷程檔案優化設計。
  具備 10 題行內三選一聽力填空 (含辨音干擾項)、音訊轉錄稿 100% 依序對齊與全曲完整中英歌詞無缺漏、單字語音朗讀 (TTS)、高頻搭配詞與句型解析、
  1~5 星推薦滑桿、動態遊戲化回饋特效 (Confetti/氣球/震動/下雨)、
  Count on Me 黃金母版標準之雙語鷹架句型引導 (Sentence Starters + 英中對照範例)、
  自然教學動線（歌曲賞析置於反思前提供情意輸入）、純淨化親切成果小卡（絕無教師名與官方誇大機構標籤）、
  無編號與具備純前端即時搜尋過濾且按首字母 (A-Z) 排列之總覽 Hub，以及標準化 Cloudflare Pages 批次自動部署機制。
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
  4. **聽懂這首歌：青春共鳴與背後寓意**（歌手檔案與超狂戰績 + 面向學生的對話式賞析）
  5. **深度雙語歌詞賞析**（雙語歌詞 + 意境導讀）
  6. **學生自我反思與推薦問答**（Count on Me 黃金標準：Sentence Starters ＋ 英中對照範例）
  7. **🔚 頁尾總結算按鈕**：
     - **「結算成績並領取成果認證卡」大按鈕必須位於網頁最底部 (Footer)**，讓學生在完整填寫反思問卷後才進行結算。
     - 點擊時若學生尚未填寫反思，系統會貼心彈出確認視窗，提醒學生填寫以確保認證卡具備實質學習歷程價值。

### 2. 題數、計分規範與「全曲完整歌詞與轉錄稿依序對齊」原則 (Full Lyrics & Transcript Integrity)
- **滿分 100 分之 10 題挖空**：固定設計剛好 **10 題** 關鍵聽力挖空，每題 10 分，滿分 **100 分**，直觀銜接平時課堂形成性評量。
- 🎙️ **音訊轉錄稿 100% 依序對齊（絕不可缺行、跳行或順序錯亂）**：
  - 學生在課堂進行聽力挑戰時，是**緊盯著網頁歌詞跟著音訊秒數與旋律同步對照**。如果歌詞中途遺漏了短句、重複呼喊或合唱過渡段（例如：`Speechless!`、`'Cause I`、`Let the storm in`、`So come on and try` 等），學生會**瞬間失去定位、抓不到唱到哪裡**，造成極度嚴重的挫折感與課堂混亂！
  - **嚴格規範**：歌詞清單必須**完整依照音訊影片的真實時間軸 (Audio Transcript / Timeline)，逐句逐行依序列出**，絕不可主觀刪減短句、不可整併跳行、亦不可套用非當前播放版本的歌詞。
- 📜 **全曲完整歌詞無缺漏保證 (Full Unabridged Lyrics)**：
  - 網頁必須完整收錄全曲所有段落（主歌 Verses、副歌 Chorus、過渡 Pre-Chorus、橋段 Bridge、尾奏 Outro 及合唱/對唱段落）。
  - **嚴禁只保留 10 句挖空題目而刪去其餘歌詞**！其餘未挖空的歌詞行需完整呈現雙語英中對照，讓學生能一邊聆聽音樂一邊跟讀理解全貌。
- 🛡️ **括號防衝突語法安全守則 (Bracket Syntax Safety)**：
  - 只有**真正要被挖空的 10 個英文單字**才允許使用半形中括號標註（如：`[peculiar]`）。
  - 歌詞中的**角色名稱、合唱註記、說話者標籤**（如 Galinda、Elphaba、Students、Both），**嚴禁使用中括號 `[Galinda]`**，一律改用圓括號 `(Galinda)` 或全形括號 `【格琳達】`！
  - *原因*：前端渲染核心採用 `html.replace(/\[(.*?)\]/g, ...)`，若角色標籤使用中括號，會被誤判為第 11、12 個額外填空，導致題數失真與計分異常。

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

### 4. YouTube 影片選用：動態畫面首選、播放相容性與字幕審查標準（極重要！）
- 🎬 **第一優先挑選「有動態演出/電影畫面」之影片 (Dynamic Moving Visuals Priority)**：
  - 首選官方電影片段 (Official Movie Clip)、官方劇情 MV (Official Music Video)、或具備生動動畫/豐富分鏡之動態歌詞版 (Official Animated Lyric Video)。
  - **嚴格禁止使用從頭到尾只有一張靜態專輯封面、靜止圖片之音訊影片 (Static Album Art)**！高中職學生高度重視視覺臨場感，靜止畫面容易導致注意力渙散與沉悶。
- **全面檢測嵌入權限**：必須使用允許外部網頁 `iframe` 嵌入之影片（選定前需透過 YouTube oEmbed API 驗證 `status: 200`，絕不可使用 404 失效、私人未公開或被版權方禁止外嵌之 ID）。
- **字幕要求極致純淨（英文字幕或無字幕，絕對禁止中文字幕）**：
  - 首選官方純英文字幕、官方無字幕音訊或官方原版 MV。
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

### 6. 歌曲深度賞析之「青年共鳴」與「歌手戰績」寫作準則 (Youth-Oriented Song Appreciation & Storytelling)
- **核心定位（重要思維轉變！）**：
  - **讀者對象是學生（高中職生）**：賞析是寫給學生看、引領學生共感的，**嚴格禁止使用「本單元旨在引導學生...」、「適合高中職課堂破冰...」等教師備課端、教案式的上對下說教口吻**。
  - **語言與口吻**：親切熱血、真誠對話、共感同理（以「你」、「我們」稱呼）。例如：「在求學路上，你有沒有過這種感覺？」、「當你戴上耳機，這首歌想告訴我們的是...」。
  - 💡 **動線黃金法則（賞析置於反思前）**：歌曲深度賞析必須嚴格安排在「學生自我反思」之前！遵循認知學習動線（Input ➜ Internalization ➜ Output），先提供文化與情意主題輸入，學生在寫反思問答時才能深刻結合個人經驗，避免心得流於空洞。
- **內容必備兩大板塊**：
  1. **【歌手檔案與超狂戰績卡】(Artist Profile & Accolades)**：
     - 標明歌手/樂團全名、在當代流行音樂史上的代表地位。
     - 列舉最具震撼力的大獎榮譽（如：葛萊美獎、奧斯卡最佳原創歌曲、告示牌 Hot 100 冠軍週數、RIAA 鑽石唱片認證、YouTube 破數十億串流等），激發學生對西洋流行文化的好奇心與眼界。
  2. **【青春共感與背後寓意短文】(Youth Resonance & Story Behind the Song)**：
     - **創作背景**：介紹這首歌是在什麼真實故事或情境下誕生的（如飛機上的靈感錄音、電影中向摯友告別的承諾、重拾童年動漫熱愛的純真）。
     - **深層寓意與青春課題**：深刻扣合高中職學生切身面對的心靈課題（面對升學與考試焦慮時的心理重開機、遭遇同儕排擠或網路酸民時的自信建立、自我認同與生涯迷惘、化解人際偏見的包容力、劃清健康情感界線，以及真誠友誼的陪伴力量）。

### 7. 學生自我反思之「Count on Me 旗艦黃金規範」(Scaffolded Reflection with Bilingual Starters)
- **設計哲學**：全面貫徹《Count on Me》所樹立之教學標竿，消除高中職（A1~A2）學生的英語寫作焦慮，讓每位學生都能充滿成就感地寫出有深度的學習歷程心得。
- **標準三問結構**：
  1. **Q1: Song Rating（1~5 星動態推薦滑桿）**：
     - 欄位 ID：`id="rating-slider"`，連動 `id="rating-badge"`。
     - 拖曳即時觸發 `updateRatingDisplay(this.value)`，提供生動情境文字反饋：
       - `5 星`：⭐⭐⭐⭐⭐ (5/5) 絕世神曲！不聽後悔
       - `4 星`：⭐⭐⭐⭐☆ (4/5) 旋律超棒，非常值得推薦
       - `3 星`：⭐⭐⭐☆☆ (3/5) 節奏輕快，感覺還不錯
       - `2 星`：⭐⭐☆☆☆ (2/5) 普普通通，不是我的菜
       - `1 星`：⭐☆☆☆☆ (1/5) 不太有共鳴
  2. **Q2: Why do you give this rating?（推薦理由與聽覺感受）**：
     - 欄位 ID：`id="student-reason"`。
     - **必備獨立雙語鷹架方塊 (Scaffolding Box)**：
       ```html
       <div class="bg-amber-50/70 border border-amber-200 rounded-xl p-3 mb-2 text-xs text-slate-600">
         <span class="font-bold text-amber-800">💡 Sentence Starter (你可以這樣開頭)：</span>
         <div class="mt-1.5 space-y-1 font-mono text-[11px]">
           <p>• <strong>I like this song because...</strong> (我喜歡這首歌，因為...)</p>
           <p>• <strong>The melody is... and it makes me feel...</strong> (旋律很...，讓我覺得...)</p>
           <p class="text-slate-500 pt-0.5">📝 Example: <span class="text-slate-700 italic">"I like this song because the melody is warm and sweet."</span> (我喜歡這首歌，因為旋律很溫暖甜蜜。)</p>
         </div>
       </div>
       ```
     - 欄位 placeholder 提供英中雙語參考句。
  3. **Q3: Which lyric line touched you the most? What did you learn?（歌詞打動處與核心啟發）**：
     - 欄位 ID：`id="student-quote"`。
     - **必備獨立雙語鷹架方塊 (Scaffolding Box)**：
       ```html
       <div class="bg-indigo-50/70 border border-indigo-200 rounded-xl p-3 mb-2 text-xs text-slate-600">
         <span class="font-bold text-indigo-800">💡 Sentence Starter (你可以這樣開頭)：</span>
         <div class="mt-1.5 space-y-1 font-mono text-[11px]">
           <p>• <strong>My favorite line is "..." because...</strong> (我最喜歡這句歌詞，因為...)</p>
           <p>• <strong>From this song, I learned that...</strong> (從這首歌中，我學到...)</p>
           <p class="text-slate-500 pt-0.5">📝 Example: <span class="text-slate-700 italic">"..."</span> (...)</p>
         </div>
       </div>
       ```
     - 欄位 placeholder 提供英中雙語參考句。
- **結算前漏填貼心提醒機制 (Pre-Submission Reflection Guard)**：
  - 結算函式 `grandSubmitChallenge()` 啟動時，若 `student-reason` 與 `student-quote` 皆為空，必須跳出友善 `confirm()` 提醒：
    ```javascript
    const sReason = document.getElementById('student-reason').value.trim();
    const sQuote = document.getElementById('student-quote').value.trim();
    if (!sReason && !sQuote) {
      const skipReflection = confirm("💡 貼心提醒：您尚未填寫最後的「學習反思問答」！\n若未填寫，成果認證卡將會缺少學習歷程的反思文字。\n\n確定要直接結算領取小卡嗎？（按「取消」可回去填寫）");
      if (!skipReflection) {
        const refSec = document.getElementById('reflection-section');
        if (refSec) refSec.scrollIntoView({ behavior: 'smooth' });
        document.getElementById('student-reason').focus();
        return;
      }
    }
    ```

### 8. 單字庫朗讀發音按鈕 (Web Speech API TTS)
- 每個重點單字與常用搭配詞旁均內建 **「🔊 朗讀」** 按鈕，使用瀏覽器原生 Web Speech API (`en-US`) 免費即時發音，無須依賴外部付費音訊 API。

### 9. 遊戲化動態特效 (Gamified Visual Feedback)
- 引用 `canvas-confetti` 庫，根據結算成績觸發 4 級動態視覺特效：
  - **80 ~ 100 分**：魔杖星光 🧙‍♀️✨ + 雙側全彩 Confetti 彩帶噴發。
  - **60 ~ 79 分**：熱氣球升空飄浮動畫 🎈☁️。
  - **40 ~ 59 分**：畫面搖晃警告 (Screen Shake) 😬🧹。
  - **40 分以下**：全螢幕灰階降濾鏡 + 逼真雨滴落下動畫 🌧️。

### 10. 純淨化課堂成果認證卡規範 (Neutral & Grounded Student Certificate)
- **成果小卡純淨化與去身分化（關鍵原則！）**：
  - 成果小卡專屬學生個人，**絕不出現任何教師姓名、絕不出現 `hsinyuchi` 或任何導師個人標籤**。
  - **嚴禁使用官方誇大或沉重機構名義**（如 `Verified High School English Department`、`Digital Learning Evidence` 或「高中英文課堂自主學習成果」）。
  - 保持親切純樸、溫暖鼓勵的課堂小卡風格（頁尾僅保留：`English Song Listening Challenge` | `Keep Learning & Singing! 🎵`），將焦點完全回歸學生的聽力突破與反思心得。
  - 將回饋區塊標題純化為「🌟 挑戰回饋 (Challenge Feedback)」，免去指導老師簽名或主觀說教感。
- **收錄完整學生反思問答（絕不截斷！）**：完整呈現推薦星等、理由與歌詞心得，作為扎實的自主學習歷程紀錄。
- **智慧激勵短評適合 A1~A2 學生理解**：採親切基礎英文，並**一律附上繁體中文註解**（100 分、80~90 分、60~70 分、< 60 分）。
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
3. **聽懂這首歌：青年共鳴賞析與背景戰績 (Youth-Oriented Song Story)**：
   - 以「面向高中職生」的對話式熱血共鳴語調撰寫（嚴禁教案說教口吻）。
   - 整合【歌手檔案與超狂大獎戰績卡】（葛萊美、奧斯卡、告示牌紀錄）與【青春共感與背後寓意短文】。
4. **深度意境賞析與雙語歌詞 (Song Appreciation & Lyrics)**：文化情意導讀、全曲完整中英對照歌詞。
5. **學生自我反思問答 (Count on Me 規格)**：包含 1~5 星滑桿與動態短評、Q2 與 Q3 獨立雙語鷹架方塊（Sentence Starters ＋ 英中對照範例）。

---

### Step 3: 高質感 HTML5 互動網頁開發 (單檔純前端)
技術堆疊：`HTML5` + `Tailwind CSS (CDN)` + `Vanilla JavaScript` + `html2canvas (CDN)` + `canvas-confetti (CDN)`。

#### 網頁核心模組與「Count on Me 黃金母版規範」(Gold Master Standard)：
所有後續曲目開發，**架構、模組順序、DOM ID 與動態邏輯必須 100% 嚴格完全參照《Count on Me》旗艦母版**，僅可置換代表主題色系（如 Amber ➜ Purple ➜ Teal）與教材內容，確保品質一致且零回歸錯誤。

1. **Header 導覽與右上角鎖定計時器 (Timer Locked Top-Right)**：
   - 包含課堂延伸主題徽章、歌曲大標題與副標。
   - **計時器卡片鎖定右上角**：Header 內部採用 `flex items-center justify-between`，文字區設 `flex-1 min-w-0 pr-2`，計時器卡片設 `flex-shrink-0 min-w-[120px]`，確保在任何螢幕解析度或長標題下皆鎖定在右上角，絕不折行沉底！
2. **YouTube 播放視窗 (含防版權跳轉備援按鈕)**：右上角必備 `▶️ 若無法直接播放，點此開啟 YouTube 觀看`。
3. **聽力測驗區 (`#quiz-area`) 與黏性進度條 (Sticky Progress Bar)**：
   - 頂部懸浮吸頂進度條：含 `🎵 聽力三選一 (10 題，每題 10 分)`、即時進度文字 `#progress-text` (`0/10`)、雙色漸層進度條 `#progress-bar`。
   - 點擊空格彈出 3 個辨音選項，單手作答，套用防遮擋 CSS：`.lyric-line.active-line`（`z-index: 500`）與 `.cloze-blank.has-popover`（`z-index: 1000 !important`）。
   - 聽力區底部配置兩大快捷操作鈕：`✅ 即時對答案 (Check Answers)`（呼叫 `checkAnswersOnly()`）與 `⬇️ 繼續往下學習與填寫反思`（錨點平滑跳轉至 `#reflection-section`）。
4. **單字深究區 (Vocabulary Study)**：5 大重點單字片語，內建 🔊 Web Speech API 原生真人發音。
5. **高中核心句型解析 (Target Sentence Patterns)**：2 大高頻大考句型公式、歌詞示範與升學造句。
6. **聽懂這首歌：青年共鳴與背後寓意區塊**（歌手超狂戰績卡 + 對話式短文）。
7. **學生自我反思問答區 (`#reflection-section`)**：標準 Count on Me 雙語鷹架模組（1~5 星滑桿、雙語 Sentence Starters、雙語範例、`student-reason`、`student-quote`）。
8. **頁尾 Grand Submit 區塊**：大卡片包裝之結算按鈕，內建「漏填反思貼心防呆守門員 (Reflection Guard)」，觸發 Confetti / 氣球 / 震動 / 灰階下雨 4 級遊戲化反饋。
9. **學習歷程認證卡 Modal 與 PNG 匯出**：生成純淨化雙語認證卡（100% 屬於學生個人成就、無教師名與官方生硬機構標籤），支援 `html2canvas` 一鍵匯出 PNG。
10. **頁尾教育版權聲明**：載明非商業教學用途與版權歸屬。

---

### Step 4: 交付成果與部署指南

1. **單檔與離線包產出**：
   - 產出單一完整 HTML（如 `Taylor_Swift_Shake_It_Off_網頁學習單.html`）。
   - 自動打包對應之 `_site.zip` 離線與部署壓縮檔。
2. **總覽 Hub 入口升級與首字母排序 (Alphabetical Order A-Z)**：
   - **首字母排序規則 (A-Z)**：總覽 Hub 中所有歌曲卡片，一律依「歌曲英文名稱首字母」自然排列（例如 Attention ➜ Count on Me ➜ Perfect Strangers），便於直覺檢索與管理。
   - **版權專注與去贅詞**：總覽 Hub 頂部橫幅聚焦教育版權聲明與合理使用原則，嚴禁浮誇宣傳贅句。
   - **無編號原則 (No Index Numbers)**：卡片頂部標籤一律改用「精選推薦」或「CEFR 等級/主題」，**絕不使用 FLAGSHIP 01/02 或流水號編號**，標題與橫幅亦不限制歌曲數量。
   - **即時純前端搜尋列 (Search & Filter Bar)**：
     - 位於 Header 與卡片之間，提供輸入框即時搜尋曲名、歌手、主題關鍵字與 CEFR 等級（分詞搜尋）。
     - 具備清除按鈕、動態計數徽章（如「顯示 2 / 3 首歌曲」）、熱門分類標籤快速切換。
     - 當無匹配結果時，顯示優雅的「查無符合歌曲」提示方塊與重設按鈕。
   - **三合一行動按鈕**：每首卡片皆提供三大按鈕：
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
