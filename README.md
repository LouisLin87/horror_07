# 勿入 · DO NOT ENTER · 立入禁止

原創手機恐怖解謎，參考 Lomando 的探索與突發反差。繁體中文、英文、日文；五個主關卡、底片與 A_01_E 文件支線、Cozy Corner 庇護監控、可選陷阱、隱藏印記及兩種結局。程式、介面與替代視聽效果在 `index.html`，選用暗房、鬼臉、電視雪花圖片及實錄敲門、腳步與推門聲放在 `assets/`。不需要框架、API 金鑰或影片。素材缺漏時仍能用內建版本通關。

英文與日文採自然口語：英文多用短句與縮寫，日文提示用日常說法；成年確認、相機及權限資訊仍明確。繁體中文保持原文。

## 視覺方向

第一次進入是暖白、鼠尾草綠的「小小探險室」，用較溫和的文字邀請玩家依自己的步調開始。入口完全遮住走廊與 VHS，仍清楚標示恐怖內容及可選效果。按開始後轉為下面的恐怖畫面；被詛咒的重返入口維持暗紅。

1990 年代低解析類比恐怖：空曠走廊重複同一房號，深處只有紅色門縫；鬼臉可選用原創寫實 WebP 素材，深陷眼窩、異常齒列與骨節手指營造不自然感；缺檔時使用黑白交叉排線的 Canvas 替代。牆面、衣物、長髮與骨節手指均由 Canvas 繪製並快取，不熱連外站圖片；第二關可使用隨作品附帶的原創 WebP 暗房。

畫布有 VHS 掃描線、雜訊與局部水平錯位，操作文字及按鈕保持穩定；底片的敘事註記可短暫污染。局部錯位使用遊戲時間，暫停會凍結；系統「減少動態效果」停用撕裂、抖動與縮放，保留靜態畫面及解謎資訊。全畫面紅色脈衝仍需玩家選擇閃光。整合版 HTML 上限為 246000 bytes，公開包維持低於900000 bytes、十三檔及八項選用素材，首次入口不載入它們。

## 同頁庇護監控與文件支線

首頁依「小小探險室」參考恢復 COZY CORNER / TAKE A BREATH 品牌文字，保留暖白、鼠尾草綠、主標題、三語、警告、權限與0101月日確認的資訊順序。監控在開始遊戲後出現在右上角，用99.8%小按鈕保留畫面空間；展開可讀狀態、1,428±小幅波動的觀測員及舒適度，明確標示遊戲內模擬資料。看見第四眼或文件揭露後轉紅、舒適度0.4%，展開顯示「IT IS A CAGE. YOU CANNOT LEAVE.」。這是劇情文字，真正退出一直可用。點擊／聚焦其他操作自動收合；淨化／新輪會重設監控。

取景器找到三個異狀後，除了底片，也可按「閱讀系統文件」。A_01_E 的白色技術文件、三語、程式碼、融化邊緣與符文眼壁都內嵌在同一 HTML。它不是外站或 Microsoft 官方頁面；只在進入支線時建立文件畫面。文件可以單指捲動，遊戲外層仍滿版；目錄錨點只在文件內跳轉。

文件入口會再次說明本關效果與30秒同步倒數。故事剪貼簿同意預設關閉：未同意時複製原碼；同意後按「複製程式碼」才寫指定的純文字求救信，可另按「複製原始碼」。沒有自動複製、截取Ctrl+C、讀剪貼簿或執行內容。權限／API不可用時顯示手動選取文字。返回或退出會銷毀文件，晚到的操作／訊息不能重開支線。

向下閱讀到文件破裂，會在底層看見本輪月日 `SUBJECT_KEY`，接到最後密碼鎖。進入文件後有30**遊戲秒**同步倒數，最後一秒靜默；歸零觸發三秒深淵過場、55Hz心跳、低量電子聲與錯誤文字，然後回原取景器／底片。未選音效便無聲；反相需另選閃光，減少動態時無位移／反相。文件倒數及門後重演都使用遊戲時間，暫停／切背景凍結。

文件底部有返回、暫停、靜音、退出；內部語言選擇會同步主遊戲並保留網址其他參數及hash。返回不重開相機；找到的線索與原關進度保留，不需讀文件也可完成五關。文件重置只重置本文件與同步倒數，不自動改剪貼簿／清除詛咒。

Android Chrome 與 iOS Safari 的基礎遊玩都以觸控為主。相機與動作感應需 HTTPS 及玩家手勢授權，拒絕仍可用虛構場景；剪貼簿有手動回退，震動依瀏覽器／裝置支援。[相機安全環境](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia)、[感應器手勢](https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/requestPermission_static)。實機待測見手機測試.md；Windows WebKit 引擎不等於iPhone，也沒有Web Audio API，不能據此宣稱Safari音效已驗證。

## 假分頁增生

走廊眼睛陷阱及最後開門會觸發約五秒的演出：復古假視窗逐張堆疊，求救文字重複；短干擾聲之後約一秒完全安靜，再讓原創鬼臉貼近並尖叫。視窗裝飾全部畫在頁內 Canvas，最多八張；網址不改，不開新分頁、不下載程式。真正的暫停、靜音、退出、繼續按鈕一直可用。

切換背景會暫停；返回後要自行繼續。減少動態時呈現固定拼貼，不增生、縮放或撕裂；閃光及震動仍按玩家選擇。鬼臉在第一次驚嚇前才載入，404、離線或毀損可用原程序鬼臉完成事件。每事件只累加一次詛咒，通關仍清空儲存。

## 取景器底片支線

第二關收集三個異狀後，可選「檢查底片」，也可直接進下一關。支線是原創 Canvas 眼壁與機械管線，不需下載新圖片。進底片會關閉相機；返回時保留收集進度，用虛構暗房繼續，不自動重新開鏡頭。

光圈半徑為 80 CSS px；手機單指拖曳、桌面滑鼠移動、方向鍵或已同意的感應器都能控制。先照準左側眼睛，第一次只有三隻。把光圈移遠，再照回來，會多出第四隻；其中一隻瞳孔慢慢看向光。眼數變化有短暫停留門檻，手抖不會立刻改變，且不會自動增加詛咒或尖叫。

密碼在另一處的右下小面板。第四眼出現後，照準文字並按「記下線索」，會記下入口填的四位月日。回到原路，最後門鎖會顯示記錄；答錯再重整，門後重演進度與已找到的線索也會恢復。沒有看支線仍可依血牆的月日通關。

暫停／切到背景會凍結光圈、眼神及眼數的停留計時。系統減少動態時瞳孔固定，三眼／四眼解謎仍保留；可隨時回取景器、提示、靜音及退出。每格重鋪黑幕，移過的地方會重新變暗，不會永久擦開底圖。眼壁與文字都是虛構場景，不偵測玩家房間。

## 底片的文字異常

第四眼出現後，旁邊的紀錄仍寫「觀察結果：三隻眼睛」。首次記下密碼時，會短暫變成「觀察結果：你也被看見了」，接著出現符號亂碼與局部 1px 抖動；約 3.6 個遊戲秒後還原紀錄，留下「它正在讀你」。重複保存不重播；回取景器或退出立即還原，重新遊玩才重置。

這是敘事效果，與正常 zh / en / ja 翻譯分開。按鈕、權限警告、密碼數字、線索提示及倒數保持可讀，切換語言後按目前語言還原。CthulhuLocalizer 使用 TreeWalker 與 Map，只改標記敘事 span，沒有全頁亂碼、外站或新儲存紀錄。暫停／背景凍結事件與 CSS 動畫；減少動態顯示靜態符號。最後密碼鎖及原五關玩法照常有效。

## 電視雪花與雜訊過場

使用玩家提供的雪花圖，完整構圖等比例縮成960×444、約31KB WebP。進入底片或A_01_E文件支線時出現約0.65秒訊號中斷；文件倒數30秒歸零時再出現0.7秒雪花，接入原本三秒異變。過場只蓋場景，暫停、返回、靜音、退出保留。

雜訊使用同一Web Audio context合成：帶通白噪音、短促淡入淡出與斷續包絡。只有已同意音效、未靜音且正在遊玩才播放；暫停與切背景凍結，退出停止。沒有音效同意時只有畫面。系統減少動態使用固定雪花／雜訊快照，不增加全畫面亮暗閃爍。首頁不預載此圖；失敗仍用內建grain，載入不阻塞遊玩。桌面音訊波形已驗證，實機耳機聽感另測。

## 選用素材

第二關的虛構暗房使用本次 imagegen 原創生成的窗簾與舊櫃照片風背景（WebP 約 63 KB）；第一頁完全不請求圖片，到取景關才載入並快取。真正開相機時仍使用即時 video，圖片不取代鏡頭。

`assets/window-ghost.webp` 為原始透明窗鬼，1122×1402、約 251 KB；生成提示與來源記錄見 ASSETS.md。首次眼睛陷阱／最終驚嚇前才載入，不延後入口顯示。

回聲房加入 Joseph SARDIN / BigSoundBank 的 [Door Knock #95](https://bigsoundbank.com/door-knock-s0095.html) 實錄聲音，來源明示 CC0；裁成 0.55 秒、約 35 KB 的 WAV，加入淡入淡出，遊戲再以低通及左右聲道處理。只有玩家同意音效、按開始且可用 Web Audio 時才下載；不延後音訊解鎖。靜音、暫停、退出與驚嚇前靜默仍有效。[授權與處理記錄](ASSETS.md)。

素材放作品自己的 `assets/`，遊玩時不連來源站。下載慢、404、解碼失敗或離線都使用原來的 Canvas 房間／合成敲門聲，所有關卡有效。全部公開檔案未壓縮低於 900000 bytes；HTML 低於 246000 bytes，文件支線沒有額外下載資產。

## 開始

先閱讀警告、填寫四位生日月日代碼（例如 `0101`）、確認已滿 18 歲，再按「準備好了，開始」。可填虛構日期；月日不包含年份，**不能驗證真實年齡**，成年資格由玩家自行確認。有效日期立即寫入本機 `player_birthday`，不傳送到伺服器；空白、未填滿或無效日期無法開始。

正常與詛咒入口都有「未滿 18 歲」按鈕（英文 Under 18／日文 18 歳未満）。點擊後在同一分頁前往[指定的 YouTube 影片](https://www.youtube.com/watch?v=hkQcoXDpJbA&list=RDhkQcoXDpJbA&start_radio=1)，不必填生日或同意遊戲效果。

可選音效、動作感應、震動及短暫閃光。動作感應預設不勾選；拒絕或無法使用時，滑動光圈仍可完成所有關卡。音效勾選時，開始按鈕立即解鎖音訊。

1. **沒有人的走廊**：滑動或傾斜光圈、找小骷髏；可選印記改變結局。
2. **窗簾後的取景器**：選擇後鏡頭或虛構暗房。滑動光圈／傾斜對準左上、右上、中下的三個虛構異狀，再按「捕捉異狀」。捕捉只是遊戲收集，不拍照、不保存影像。
3. **牆後的名字**：來回擦血牆，約三秒有效移動後出現驚嚇；繼續擦出進門時的月日。
4. **不要回第四聲**：三扇門依序敲響，以同一順序點門牌。靜音時看亮起的門牌及字幕，同樣可解。可重播、可提示；第一次答錯出現驚嚇。
5. **最後一扇門**：3×4 虛擬鍵盤輸入月日。答錯進入「門後的你」，長按清除三秒可重試；答對碎裂與終極驚嚇後破關，依印記走兩種結局。


一般關卡可暫停、靜音或退出；驚嚇畫面也有暫停、退出與靜音。切換分頁自動暫停，回來需自行繼續。門後重演隨暫停凍結，退出保留這段記憶；通關後清除紀錄，重玩回正常入口，不保存權限選擇。

## 相機探索與隱私

相機通知在第二關單獨出現，首頁不會要求相機。按「開啟後鏡頭」才呼叫 `getUserMedia`：`audio:false`、後鏡頭優先、640×480 理想尺寸與 24 fps 理想影格率。`video` 使用 `muted`、`playsinline`；沒有 MediaRecorder、截圖儲存、辨識房間或影像上傳。畫面裡的手、臉和符號全是 Canvas **虛構疊圖**，不是偵測到實物。[MDN getUserMedia](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia)。

手機請使用 GitHub Pages **HTTPS**。像 `http://192.168.1.108:4194` 的區網網址通常不能開相機，仍可玩虛構暗房。拒絕權限、無鏡頭、相機被其他 App 佔用、播放失敗或仍在等待授權，皆可按「使用虛構暗房」完整通關。觸控永遠可用，感應器另依玩家已有選擇。

鏡頭開啟時顯示「無錄影」與「關閉鏡頭」；暫停、切背景、離開取景器、退出或 pagehide 會呼叫所有 track 的 `stop()` 並清空 `srcObject`。回前景不自動恢復：按繼續後用虛構場景，再由玩家主動重開。權限晚到也會以 token 檢查是否仍在同一關，已退出則立即停止新串流。[MDN stop](https://developer.mozilla.org/en-US/docs/Web/API/MediaStreamTrack/stop)。

## 手機生日密碼鎖

第五關包含 0–9、清除、確認共十二個 HTML 按鈕，三欄四列、每鍵至少 48 CSS px。密碼顯示使用 `output`，不是 `input`，所以門鎖點擊不會叫出手機原生鍵盤。只有入口的生日欄位會使用數字鍵盤提示；按 Enter／完成可收起欄位焦點。[MDN inputmode](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes/inputmode)。

四位字串保留前導零，與 `player_birthday` 比對；`0101` 永遠可作備用碼。不足四位只提示，不開始懲罰。錯誤的完整密碼觸發一次陷阱並累加詛咒；門後會重演按鍵；需明確允許進入才出現短驚嚇。

完整錯碼進入門後重演：保留本輪可見鍵與相對按鍵節奏，另一側再輸入已填月日，約10.8遊戲秒後邀請。可隨時長按清除三秒打斷，直接重試；「允許進入」需玩家明確按下才觸發短驚嚇，繼續後返回門鎖。數字、清除、確認與退出都由頁內按鈕完成，不鎖手機系統。

| Key | 用途 |
| --- | --- |
| `horror_door_echo` | v1遭遇、四次鍵與時間／排列、重演進度、月日快照、印記及線索 |

每秒與階段邊界保存，重整／新分頁先靜音暫停，按繼續才推進；再開不會重複累加同一次錯碼。退出保留，解除／淨化／通關清除。拒絕localStorage僅本頁記憶。舊horror_lock_*期限轉回暫停的正常鍵盤，不等30秒、不捏造按鍵。

## 被記住的詛咒

首次載入初始化 `horror_player_status = normal`、`death_count = 0`，並用 `horror_first_visit` 保存首次進入的 ISO 日期時間。一般驚嚇**實際顯示**或輸錯完整密碼觸發陷阱時，立即寫入 `cursed` 並將死亡次數加一；不在每格動畫或每次刷新累加。終極通關驚嚇清除狀態，不再累加。網頁無法判斷人是否真的感到害怕，這裡的「死亡」是遊戲事件。

重整或重新開啟相同來源的網址，門後遭遇中的玩家優先恢復靜音暫停畫面。沒有遭遇時，若被詛咒則顯示暗紅入口與累計次數，跳過原本歡迎詞及「開始遊戲」。在新入口確認並按「面對它留下的記憶」才進入關卡；音訊和感應器依然需要使用者操作，不因詛咒而自動播放或要求權限。

- 詛咒重返的背景音採 `playbackRate = 0.5`；HTMLAudio 備用音效也使用半速並關閉保留音高。[HTMLMediaElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/playbackRate)、[Web Audio](https://developer.mozilla.org/en-US/docs/Web/API/AudioBufferSourceNode/playbackRate)。
- 一般走廊停留滿 10 秒觸發一次驚嚇，包含最後約 0.85 秒靜音。死亡 **4 次以上**的下一輪光圈半徑縮為一半，驚嚇提前至第 3 秒。暫停、背景和入口等待都不增加遊戲時間。
- 淨化彩蛋：在詛咒入口的空白處連續快速點 7 次（每次間隔不超過 450 ms，整段在 2.5 秒內），或按住紅色詛咒文字 5 秒。移動超過 12 px、多指、取消觸控、離開入口或切背景會取消長按。鍵盤可聚焦文字後按住空白鍵或 Enter 5 秒。
- 淨化顯示短暫白色覆層、清除紀錄並恢復首次入口；未選閃光或使用「減少動態」時改為低亮度白色覆層。正常退出、重玩及刷新不會解除詛咒。

**清除範圍：**淨化與通關依本版需求使用 `localStorage.clear()`，會清掉同一來源下**所有** localStorage key，包含其他遊戲的紀錄。例如 `帳號.github.io/遊戲A/` 和 `/遊戲B/` 通常共用來源；需要隔離時部署到不同來源。淨化立即重新建立正常狀態；通關結局保持清空，待下一次進入才初始化。[MDN clear()](https://developer.mozilla.org/en-US/docs/Web/API/Storage/clear)。

紀錄僅對同一瀏覽器與來源有效；HTTPS、HTTP、不同主機或連接埠不共用。無痕關閉、清除網站資料或瀏覽器封鎖儲存可能讓紀錄消失；儲存被拒絕時會顯示提示，退回目前頁面的記憶體狀態。請以 HTTP/HTTPS 測持久化，`file://` 的儲存行為不保證一致。[MDN localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)。

## GitHub Pages

本上傳包僅十三個檔案：`index.html`、`README.md`、`手機測試.md`、`.nojekyll`、`ASSETS.md` 及 `assets/` 下的八檔。

1. 解壓 ZIP，把五個根目錄檔案與完整 assets/ 資料夾放到 GitHub repository 最上層，保留資料夾結構。
2. Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save。
3. 部署成功後，用 GitHub 提供的 **HTTPS** 網址遊玩。

若網頁上傳出現無法處理檔案：重新整理上傳頁，先用 Choose your files 選 index.html，确认它出現在待提交清單，再加入其他根目錄檔案及整個 assets/ 資料夾。上傳包的 .nojekyll 現含一行註解，避免零位元組檔案的相容性疑點；這不是 GitHub 儲存服務錯誤的已確認原因。若連單獨 index.html 也失敗，改用另一個瀏覽器或網路後重試。ZIP 要先解壓，保留 assets/ 結構。

不必上傳製作資料夾 `work/`、`qa/`、`.scratch/` 或整個工作區。上傳資料夾已另外整理，不需挑選數十個工作檔。

入口語言可用 `?lang=zh`、`?lang=en`、`?lang=ja`。切換語言及分享會保留網址其他參數和 hash；新玩家的分享入口先顯示警告；同瀏覽器尚未解除的門後遭遇優先恢復。

## 手機限制與資產

動作感應需要支援的瀏覽器與安全環境。iOS 的系統授權請求與音訊解鎖在同一個開始手勢發出；拒絕、無 API 或約 4.5 秒無有效數據時自動使用觸控。普通 `http://192.168…` 區網網址主要測觸控，請用 GitHub Pages HTTPS 測感應器。[MDN 動作感應說明](https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/requestPermission_static)。

只有玩家選擇震動才呼叫 `[500, 200, 500]`；不支援時保留畫面與聲音。震動 API 在部分瀏覽器不可用，系統靜音與勿擾模式亦會影響效果，不能承諾每台手機振動。[MDN 震動說明](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/vibrate)。

尖叫音效使用 1.0 網頁音量；網頁不能修改裝置的實體音量。預設不閃光；「減少動態效果」會關閉閃光及畫面抖動。Canvas、CSS 手勢與 viewport 依手機滿版遊戲需求限制頁面捲動及縮放，系統或瀏覽器的輔助縮放仍由使用者控制。

HTML 內的 `ASSETS` 預留 `scream.mp3` 與 `ghost.gif`。目前 `enabled: false`，由內建 Web Audio／HTMLAudio 備用尖叫及程序鬼臉提供效果，因此十三檔案包可獨立遊玩。只有自行提供外部素材並設成 `true` 時，才需要一併上傳這兩檔。

## 隱私與驗證

第二關的相機由玩家主動選擇，只使用 video，不請求麥克風或定位；相機和感應器資料不離開本頁。localStorage 保存玩家主動填寫的四位月日代碼、詛咒狀態、死亡事件次數、首次時間、四次遊戲按鍵與間隔、門後進度及恢復關卡的印記，不保存姓名、生日年份、感應器數值或權限偏好，也不傳送紀錄。所有故事、角色和情節均為虛構，沒有真實追蹤或入侵。

瀏覽器檢查與實體手機分開記錄；檢查範圍和操作步驟見 [手機測試](手機測試.md)。手機感應、實際震動、耳機音量及 Threads 內建瀏覽器仍需實機操作。

## English

Read the warning and choose optional sound, motion, vibration and flash before starting. Drag the light if you decline motion access. Find the skull, collect three fictional camera overlays, wipe the wall, repeat a knocking sequence and unlock the final door. A hidden seal changes the ending. Pause, mute and exit remain available; the camera is optional in level 2, with a fictional-room alternative. No microphone, location, recording or upload.

Enter a valid four-digit MMDD birthday code (fictional is OK) and confirm you are 18+. MMDD cannot verify your age. The final door uses twelve HTML buttons, with no native keyboard. A wrong code starts a replay of your own key presses behind the door. Hold Clear for 3 seconds to stop it, or wait for the invitation and choose to let them in. Reload restores the scene paused and muted. Your birthday code or 0101 opens the door, fractures the keypad and triggers a final scare. Victory clears **all origin storage**, including other apps' records. It cannot lock the phone OS or prevent manual storage/clock edits.

Upload the five top-level files and the intact assets/ folder to the repository root and enable GitHub Pages on `main` / root. Use HTTPS for camera and motion access. The eye trap and final door include a five-second simulated browser-window cascade; no real windows open, and pause, mute and exit remain available. Reduced motion uses a still collage. The HTML includes fallback artwork and synthesized sound; upload the four assets and ASSETS.md for the photo room, recorded knock, ghost and short TV-static transitions. `?lang=en` opens the English entrance. Physical device behavior must be tested separately.

Displayed scares persist a curse and incident count in localStorage. Returning shows a red entrance, but sound and sensors still require your choice. From four incidents, the next run has half the beam radius and a 3-second scare timer instead of 10. Purify with seven rapid taps on blank entrance space or hold the red message for five seconds. Purification calls `localStorage.clear()`, deleting **all keys for this origin**, including other apps' records. Blocked storage falls back to the open page only.

## 日本語

警告を読み、音・センサー・振動・点滅を選んで開始してください。センサーを拒否しても、光を指で動かして遊べます。頭蓋骨を探し、取景器の架空の異変を三つ集め、壁を拭き、ノックの順番を再現して最後の扉を開けます。隠された印で結末が変わります。一時停止・消音・終了が使えます。第2章のカメラは任意で、架空の部屋でもクリアできます。マイク・位置情報・録画・送信は使いません。

四桁の誕生日の月日（架空でも可）を入力し、18 歳以上と確認してください。月日だけでは実際の年齢を確認できません。最後の扉は 12 個の HTML ボタンで、端末のキーボードを出しません。間違うと扉の向こうでさっきの操作が再生されます。消去を3秒長押しで止めるか、招待を待って中に入れるか選べます。再読み込み後は一時停止・消音で再開します。誕生日コードか 0101 で開き、ボタンが崩れ、最後の恐怖画面とクリア画面が現れます。クリアは**同じオリジンの全記録**を削除します。端末の OS はロックできず、手動のデータ削除や時計変更も防げません。

ルートの五つのファイルと assets/ フォルダーをそのままリポジトリ直下に置き、GitHub Pages の `main` / root を指定します。カメラとセンサーは HTTPS で試してください。代替の画像と音は HTML 内蔵です。目の罠と最後の扉は、ページ内の偽ウィンドウが増える五秒の演出です。実際のタブは開かず、停止・消音・終了できます。写真の部屋、恐怖の顔と実録ノックには assets/ と ASSETS.md もアップロードしてください。`?lang=ja` で日本語の入口を開けます。実機の動作は別途確認してください。

恐怖画面の表示回数と呪いを localStorage に保存します。再訪時は赤い入口になり、音とセンサーは再び選択が必要です。4 回以上で次の周回の光が半分、恐怖までの時間が 10 秒から 3 秒になります。入口の空白を素早く 7 回タップ、または赤い文章を 5 秒長押しすると浄化します。`localStorage.clear()` は**同じオリジンの全記録**を削除し、他のアプリにも影響します。保存が拒否された場合は現在のページ内だけで記憶します。


## 每三秒換位的密碼鍵盤

最後的月日密碼鎖會每三個遊戲秒重排0–9。十個數字始終各一個，可見數字就是會輸入的數字；已輸入的月日、原密碼與0101備用碼不變。清除／確認及退出等控制保持位置，數字按鈕也保留原尺寸。

手指或滑鼠按住時暫緩，放開至少0.25秒再換；多指全部放開或取消才恢復。暫停、切背景、驚嚇與門後重演期間不換，恢復不補跑多次。Tab／Enter鍵盤操作聚焦數字時保護焦點；系統減少動態保持固定排列。進門鎖、重試、退出與重玩重新計時。沒有新的權限、素材、外部套件或interval。

English: The digits shuffle every 3 seconds. Watch the labels; your entered code stays put. Clear and confirm stay in place. Holding a key, pausing, keyboard focus, and reduced motion stop the shuffle.

日本語：3秒ごとに数字が入れ替わるよ。押す前によく見てね。入力済みの数字は変わらない。消去と確認は同じ場所。長押し・一時停止・キーボード操作・動きを減らす設定では入れ替わらない。

## 門後的你

門後的虛構盥洗室由Canvas快取繪製，採用參考中的破瓷磚、裸露管線及黑窗構圖。鏡像鍵盤重演本輪四次可見按鍵，保留相對節奏（過長停頓壓縮到四秒區段），接著自行輸入月日。沒有預測下一次操作，也不使用鏡頭或麥克風。

重演及三秒清除都受遊戲時鐘控制；指頭移開／第二指／取消／失焦／暫停會取消未完成清除。鍵盤Space／Enter可長按。音效、靜音、退出與減少動態沿用設定。約10.8秒出現邀請，可繼續清除或明確允許進入；後者接短驚嚇後仍可重試。

通關的終極驚嚇顯示時會清空整個同來源localStorage，包含其他作品的紀錄；結局不再寫回詛咒。淨化亦依既有規則清空同來源，普通退出與刷新不清除。

## 新增的三隻原創鬼

傾聽者在走廊的故障後移近；短髮回頭客藏在取景器、敲門答錯時側轉入鏡；微笑面具藏在可擦開的血牆與門後黑窗。原始窗鬼保留在眼睛陷阱和最後假視窗，共四種身份。三種新驚嚇有不同取景、姿態、合成音高及左右聲道；未選音效不發聲，HTMLAudio備用為通用尖叫。不是額外三個關卡，而是讓原關卡各有不同的鬼。

首頁不下載它們；進入走廊兩遊戲秒／取景器／血牆或門後才載入。三張新增圖共約125KiB，任一缺圖仍可玩，退出不會被晚到圖片重啟。全部故事與角色為虛構。素材見ASSETS.md，實機項目見手機測試.md。

## 第二關：隨機鬼影與移動探索

後鏡頭可在不同空間持續探索，收集進度保留；鬼影是畫面疊圖，並非真實空間的AR定位。相機模式保留中央視野、降低周邊暗角，三隻原創鬼隨機從兩側短暫現身。虛構暗房也有同樣機制。

選好鏡頭或暗房後，首輪等4.5–7.5遊戲秒；每次消失後再等6–10遊戲秒。角色洗牌不連續重複，出現1.1–1.9秒，有淡入淡出／微小偏頭；減少動態為2.4秒固定姿態。它們不是收集目標、不增加死亡；提示已包含中文、口語英文及日文。

選音效後搭配短促低聲道合成氣音；暫停凍結畫面與時鐘，切到背景會關閉鏡頭，回來需要手動繼續並重新開後鏡頭。重新開鏡頭、進入底片／文件或離關，清除本輪鬼影與聲音，不在背景累積遭遇。首頁沒有新增下載，素材共八項、公開十三檔，預算維持246000／900000 bytes。

## 第二關：靠近的聲音（2026-10-15）

選音效並選好暗房／鏡頭後，隨機鬼影等待期間加入兩次左右腳步、慢推門聲與雙拍低頻心跳。越接近現身，心跳越快；最後0.85遊戲秒完全安靜，現身才接短故障雜訊與既有氣音。這些聲音是劇情音效，與實際房間中的人或物沒有辨識關係。

腳步及推門採小森平的實錄短切片，加工成單一1.46秒、46764-byte WAV；只有已選音效、開始操作第二關且Web Audio正在運行才按需下載。作者／原素材頁／自訂免費使用條款及加工記錄見ASSETS.md，並非CC0。缺檔、毀損或離線自動使用合成聲；晚到只快取，不突然補播。

心跳及故障聲由原生Web Audio合成，不需要Gemini、外部套件或金鑰。暫停凍結音訊與遊戲秒數；靜音立即停止這輪音源、不補播錯過的腳步，退出中止載入，離關及進底片／文件清理聲音。背景恢復仍需手動繼續。桌面原生音訊、靜默區段與波形已檢查；iPhone17／Sony1IV耳機音色、左右定位及背景行為依手機測試.md實測。
