多媒體程式設計期中專案 - 我個人履歷有使用的技巧說明

### 1. 頂部懸浮導覽列與平滑滾動 (CSS)
* **毛玻璃特效**：使用 CSS 的 `position: fixed` 搭配 `backdrop-filter: blur(5px)`，製作出具備半透明毛玻璃質感的頂部導覽列。
* **平滑滾動**：在 html 標籤加入 `scroll-behavior: smooth`，點擊導覽列連結時會平滑滑動至對應的錨點區域。

### 2. 個人標語光澤跑馬燈動畫 (CSS)
* **文字遮罩與漸層**：利用 CSS 的 `linear-gradient` 搭配 `-webkit-background-clip: text` 將背景漸層套用至文字本身。
* **Keyframes 動畫**：使用 `@keyframes` 改變 background-position，創造出光線由左至右平滑掃過文字表面的金屬光澤動態效果。

### 3. 技能總覽 - 3D翻轉與動態圓形進度條 (CSS + JS)
* **3D 翻轉卡片**：運用 CSS 的 `perspective` 賦予景深，搭配 `transform: rotateY(180deg)` 與 `transform-style: preserve-3d`，達成卡片正反面平滑的 3D 翻轉效果。
* **JS 圓形讀條演算法**：背面進度條捨棄傳統長條圖，改用 CSS `conic-gradient` 繪製圓餅圖。並透過 JavaScript 的 `requestAnimationFrame` 寫入非線性緩動函數 (Easing function)，確保使用者每次翻開卡片或鼠標滑過時，進度條都會從 0% 流暢且平滑地長至對應的熟練度。

### 4. 個人經歷 - 幻燈片預覽與影片自動播放 (JS)
* **Hover 幻燈片輪播**：使用 JavaScript 監聽 `mouseenter` 與 `mouseleave` 事件。當鼠標懸停於專案圖片時，透過 `setInterval` 定時器動態替換 `<img>` 的 src 路徑，實現專案截圖的自動幻燈片播放；移開時則自動還原並清除定時器。
* **影片狀態連動**：在翻轉卡片的點擊事件中加入邏輯判斷。當卡片翻至背面時，JS 會自動選取背面的 `<video>` 標籤並觸發 `.play()`；若翻回正面則觸發 `.pause()`，達成極佳的互動多媒體體驗。

### 5. 聯絡資訊 - 互動式圖文小卡 (CSS)
* 延續 3D 翻轉技術，將原本平面的聯絡資訊製作成雙面卡片。正面展示直觀的 Icon 圖片，點擊翻轉後呈現詳細文字資訊與外部連結，增加版面趣味性並節省空間。