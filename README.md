# 勿入 · DO NOT ENTER · 立入禁止

原創手機恐怖解謎，參考 Lomando 的探索與突發反差。繁體中文、英文、日文；五個關卡、可選陷阱、隱藏印記及兩種結局。程式、介面與替代視聽效果在 `index.html`，選用暗房、鬼臉圖片及實錄敲門聲放在 `assets/`。不需要框架、API 金鑰或影片。素材缺漏時仍能用內建版本通關。

英文與日文採自然口語：英文多用短句與縮寫，日文提示用日常說法；成年確認、相機及權限資訊仍明確。繁體中文保持原文。

## 視覺方向

第一次進入是暖白、鼠尾草綠的「小小探險室」，用較溫和的文字邀請玩家依自己的步調開始。入口完全遮住走廊與 VHS，仍清楚標示恐怖內容及可選效果。按開始後轉為下面的恐怖畫面；被詛咒的重返入口維持暗紅。

1990 年代低解析類比恐怖：空曠走廊重複同一房號，深處只有紅色門縫；鬼臉可選用原創寫實 WebP 素材，深陷眼窩、異常齒列與骨節手指營造不自然感；缺檔時使用黑白交叉排線的 Canvas 替代。牆面、衣物、長髮與骨節手指均由 Canvas 繪製並快取，不熱連外站圖片；第二關可使用隨作品附帶的原創 WebP 暗房。

畫布有 VHS 掃描線、雜訊與局部水平錯位，介面文字及按鈕保持穩定。局部錯位使用遊戲時間，暫停會凍結；系統「減少動態效果」停用撕裂、抖動與縮放，只保留靜態墨線及掃描線。全畫面紅色脈衝仍需玩家選擇閃光。HTML 維持低於 140 KB，三項選用素材，首次入口不載入它們。

## 假分頁增生

走廊眼睛陷阱及最後開門會觸發約五秒的演出：復古假視窗逐張堆疊，求救文字重複；短干擾聲之後約一秒完全安靜，再讓原創鬼臉貼近並尖叫。視窗裝飾全部畫在頁內 Canvas，最多八張；網址不改，不開新分頁、不下載程式。真正的暫停、靜音、退出、繼續按鈕一直可用。

切換背景會暫停；返回後要自行繼續。減少動態時呈現固定拼貼，不增生、縮放或撕裂；閃光及震動仍按玩家選擇。鬼臉在第一次驚嚇前才載入，404、離線或毀損可用原程序鬼臉完成事件。每事件只累加一次詛咒，通關仍清空儲存。

## 選用素材

第二關的虛構暗房使用本次 imagegen 原創生成的窗簾與舊櫃照片風背景（WebP 約 63 KB）；第一頁完全不請求圖片，到取景關才載入並快取。真正開相機時仍使用即時 video，圖片不取代鏡頭。

新增 `assets/window-ghost.webp` 原創透明鬼臉，1122×1402、約 251 KB；生成提示與來源記錄見 ASSETS.md。首次驚嚇前才載入，不延後入口顯示。

回聲房加入 Joseph SARDIN / BigSoundBank 的 [Door Knock #95](https://bigsoundbank.com/door-knock-s0095.html) 實錄聲音，來源明示 CC0；裁成 0.55 秒、約 35 KB 的 WAV，加入淡入淡出，遊戲再以低通及左右聲道處理。只有玩家同意音效、按開始且可用 Web Audio 時才下載；不延後音訊解鎖。靜音、暫停、退出與驚嚇前靜默仍有效。[授權與處理記錄](ASSETS.md)。

素材放作品自己的 `assets/`，遊玩時不連來源站。下載慢、404、解碼失敗或離線都使用原來的 Canvas 房間／合成敲門聲，所有關卡有效。全部公開檔案未壓縮低於 700 KB；HTML 仍低於 140 KB。

## 開始

先閱讀警告、填寫四位生日月日代碼（例如 `0101`）、確認已滿 18 歲，再按「準備好了，開始」。可填虛構日期；月日不包含年份，**不能驗證真實年齡**，成年資格由玩家自行確認。有效日期立即寫入本機 `player_birthday`，不傳送到伺服器；空白、未填滿或無效日期無法開始。

正常與詛咒入口都有「未滿 18 歲」按鈕（英文 Under 18／日文 18 歳未満）。點擊後在同一分頁前往[指定的 YouTube 影片](https://www.youtube.com/watch?v=hkQcoXDpJbA&list=RDhkQcoXDpJbA&start_radio=1)，不必填生日或同意遊戲效果。

可選音效、動作感應、震動及短暫閃光。動作感應預設不勾選；拒絕或無法使用時，滑動光圈仍可完成所有關卡。音效勾選時，開始按鈕立即解鎖音訊。

1. **沒有人的走廊**：滑動或傾斜光圈、找小骷髏；可選印記改變結局。
2. **窗簾後的取景器**：選擇後鏡頭或虛構暗房。滑動光圈／傾斜對準左上、右上、中下的三個虛構異狀，再按「捕捉異狀」。捕捉只是遊戲收集，不拍照、不保存影像。
3. **牆後的名字**：來回擦血牆，約三秒有效移動後出現驚嚇；繼續擦出進門時的月日。
4. **不要回第四聲**：三扇門依序敲響，以同一順序點門牌。靜音時看亮起的門牌及字幕，同樣可解。可重播、可提示；第一次答錯出現驚嚇。
5. **最後一扇門**：3×4 虛擬鍵盤輸入月日。答錯等 30 秒；答對碎裂與終極驚嚇後破關，依印記走兩種結局。


一般關卡可暫停、靜音或退出；驚嚇畫面也有暫停、退出與靜音。切換分頁自動暫停，回來需自行繼續。30 秒懲罰按真實經過時間計算，不受遊戲暫停影響。退出不解除尚未到期的鎖定；通關後清除紀錄，重玩回正常入口，不保存權限選擇。

## 相機探索與隱私

相機通知在第二關單獨出現，首頁不會要求相機。按「開啟後鏡頭」才呼叫 `getUserMedia`：`audio:false`、後鏡頭優先、640×480 理想尺寸與 24 fps 理想影格率。`video` 使用 `muted`、`playsinline`；沒有 MediaRecorder、截圖儲存、辨識房間或影像上傳。畫面裡的手、臉和符號全是 Canvas **虛構疊圖**，不是偵測到實物。[MDN getUserMedia](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia)。

手機請使用 GitHub Pages **HTTPS**。像 `http://192.168.1.108:4194` 的區網網址通常不能開相機，仍可玩虛構暗房。拒絕權限、無鏡頭、相機被其他 App 佔用、播放失敗或仍在等待授權，皆可按「使用虛構暗房」完整通關。觸控永遠可用，感應器另依玩家已有選擇。

鏡頭開啟時顯示「無錄影」與「關閉鏡頭」；暫停、切背景、離開取景器、退出或 pagehide 會呼叫所有 track 的 `stop()` 並清空 `srcObject`。回前景不自動恢復：按繼續後用虛構場景，再由玩家主動重開。權限晚到也會以 token 檢查是否仍在同一關，已退出則立即停止新串流。[MDN stop](https://developer.mozilla.org/en-US/docs/Web/API/MediaStreamTrack/stop)。

## 手機生日密碼鎖

第五關包含 0–9、清除、確認共十二個 HTML 按鈕，三欄四列、每鍵至少 48 CSS px。密碼顯示使用 `output`，不是 `input`，所以門鎖點擊不會叫出手機原生鍵盤。只有入口的生日欄位會使用數字鍵盤提示；按 Enter／完成可收起欄位焦點。[MDN inputmode](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes/inputmode)。

四位字串保留前導零，與 `player_birthday` 比對；`0101` 永遠可作備用碼。不足四位只提示，不開始懲罰。錯誤的完整密碼觸發一次陷阱並累加詛咒；同意聲音時短暫尖叫，同意閃光且沒有減少動態時給一次紅色閃動。

鎖定遮罩阻擋遊戲及鍵盤輸入，保留靜音、退出及關閉分頁的能力。文字「怨靈鎖定你的手機」是劇情，**僅遊戲畫面受限制，不會鎖住手機系統或瀏覽器**。

| key | 用途 |
| --- | --- |
| `player_birthday` | 玩家主動輸入的四位月日，可填虛構日期 |
| `horror_lock_until` | 固定到期時間：答錯當下 `Date.now() + 30000` |
| `horror_lock_remaining` | 每當秒數變化寫入剩餘秒數 |
| `horror_lock_context` | 恢復第五關所需的隱藏印記布林值，沒有身份或權限 |

每次以 `ceil((until - Date.now()) / 1000)` 計算剩餘時間，重新整理或關頁重開沿用同一個截止時間；不以「每秒減一」推算，避免背景計時器節流造成延長。到期移除鎖定紀錄並恢復門鎖。重開時不自動啟動音訊或要求感應器；若想聽聲音，需按「開啟聲音」。[MDN Date.now](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/now)、[背景計時器限制](https://developer.mozilla.org/en-US/docs/Web/API/Window/setTimeout#reasons_for_delays_longer_than_specified)。

這是前端遊戲機制，無法防止玩家自己刪除 localStorage、編輯資料或修改本機時間。儲存被封鎖時只在目前頁面保留倒數，畫面會提示，不能承諾重開後仍在。

答對先顯示碎裂效果，接著終極驚嚇；驚嚇顯示的同時 `localStorage.clear()` 清掉所有同來源紀錄（包含生日、詛咒、鎖定及其他作品資料）。結局不再寫回結局編號，直到重玩／重新載入才建立新的正常狀態。減少動態時碎裂改為靜態淡化。

## 被記住的詛咒

首次載入初始化 `horror_player_status = normal`、`death_count = 0`，並用 `horror_first_visit` 保存首次進入的 ISO 日期時間。一般驚嚇**實際顯示**或輸錯完整密碼觸發陷阱時，立即寫入 `cursed` 並將死亡次數加一；不在每格動畫或每次刷新累加。終極通關驚嚇清除狀態，不再累加。網頁無法判斷人是否真的感到害怕，這裡的「死亡」是遊戲事件。

重整或重新開啟相同來源的網址，鎖定中的玩家優先恢復倒數。沒有鎖定時，若被詛咒則顯示暗紅入口與累計次數，跳過原本歡迎詞及「開始遊戲」。在新入口確認並按「面對它留下的記憶」才進入關卡；音訊和感應器依然需要使用者操作，不因詛咒而自動播放或要求權限。

- 詛咒重返的背景音採 `playbackRate = 0.5`；HTMLAudio 備用音效也使用半速並關閉保留音高。[HTMLMediaElement](https://developer.mozilla.org/en-US/docs/Web/API/HTMLMediaElement/playbackRate)、[Web Audio](https://developer.mozilla.org/en-US/docs/Web/API/AudioBufferSourceNode/playbackRate)。
- 一般走廊停留滿 10 秒觸發一次驚嚇，包含最後約 0.85 秒靜音。死亡 **4 次以上**的下一輪光圈半徑縮為一半，驚嚇提前至第 3 秒。暫停、背景和入口等待都不增加遊戲時間。
- 淨化彩蛋：在詛咒入口的空白處連續快速點 7 次（每次間隔不超過 450 ms，整段在 2.5 秒內），或按住紅色詛咒文字 5 秒。移動超過 12 px、多指、取消觸控、離開入口或切背景會取消長按。鍵盤可聚焦文字後按住空白鍵或 Enter 5 秒。
- 淨化顯示短暫白色覆層、清除紀錄並恢復首次入口；未選閃光或使用「減少動態」時改為低亮度白色覆層。正常退出、重玩及刷新不會解除詛咒。

**清除範圍：**淨化與通關依本版需求使用 `localStorage.clear()`，會清掉同一來源下**所有** localStorage key，包含其他遊戲的紀錄。例如 `帳號.github.io/遊戲A/` 和 `/遊戲B/` 通常共用來源；需要隔離時部署到不同來源。淨化立即重新建立正常狀態；通關結局保持清空，待下一次進入才初始化。[MDN clear()](https://developer.mozilla.org/en-US/docs/Web/API/Storage/clear)。

紀錄僅對同一瀏覽器與來源有效；HTTPS、HTTP、不同主機或連接埠不共用。無痕關閉、清除網站資料或瀏覽器封鎖儲存可能讓紀錄消失；儲存被拒絕時會顯示提示，退回目前頁面的記憶體狀態。請以 HTTP/HTTPS 測持久化，`file://` 的儲存行為不保證一致。[MDN localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage)。

## GitHub Pages

本上傳包僅八個檔案：`index.html`、`README.md`、`手機測試.md`、`.nojekyll`、`ASSETS.md` 及 `assets/` 下的三檔。

1. 解壓 ZIP，把五個根目錄檔案與完整 assets/ 資料夾放到 GitHub repository 最上層，保留資料夾結構。
2. Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save。
3. 部署成功後，用 GitHub 提供的 **HTTPS** 網址遊玩。

若網頁上傳出現無法處理檔案：重新整理上傳頁，先用 Choose your files 選 index.html，确认它出現在待提交清單，再加入其他根目錄檔案及整個 assets/ 資料夾。上傳包的 .nojekyll 現含一行註解，避免零位元組檔案的相容性疑點；這不是 GitHub 儲存服務錯誤的已確認原因。若連單獨 index.html 也失敗，改用另一個瀏覽器或網路後重試。ZIP 要先解壓，保留 assets/ 結構。

不必上傳製作資料夾 `work/`、`qa/`、`.scratch/` 或整個工作區。上傳資料夾已另外整理，不需挑選數十個工作檔。

入口語言可用 `?lang=zh`、`?lang=en`、`?lang=ja`。切換語言及分享會保留網址其他參數和 hash；新玩家的分享入口先顯示警告；同瀏覽器尚未結束的鎖定優先恢復。

## 手機限制與資產

動作感應需要支援的瀏覽器與安全環境。iOS 的系統授權請求與音訊解鎖在同一個開始手勢發出；拒絕、無 API 或約 4.5 秒無有效數據時自動使用觸控。普通 `http://192.168…` 區網網址主要測觸控，請用 GitHub Pages HTTPS 測感應器。[MDN 動作感應說明](https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/requestPermission_static)。

只有玩家選擇震動才呼叫 `[500, 200, 500]`；不支援時保留畫面與聲音。震動 API 在部分瀏覽器不可用，系統靜音與勿擾模式亦會影響效果，不能承諾每台手機振動。[MDN 震動說明](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/vibrate)。

尖叫音效使用 1.0 網頁音量；網頁不能修改裝置的實體音量。預設不閃光；「減少動態效果」會關閉閃光及畫面抖動。Canvas、CSS 手勢與 viewport 依手機滿版遊戲需求限制頁面捲動及縮放，系統或瀏覽器的輔助縮放仍由使用者控制。

HTML 內的 `ASSETS` 預留 `scream.mp3` 與 `ghost.gif`。目前 `enabled: false`，由內建 Web Audio／HTMLAudio 備用尖叫及程序鬼臉提供效果，因此八檔案包可獨立遊玩。只有自行提供外部素材並設成 `true` 時，才需要一併上傳這兩檔。

## 隱私與驗證

第二關的相機由玩家主動選擇，只使用 video，不請求麥克風或定位；相機和感應器資料不離開本頁。localStorage 保存玩家主動填寫的四位月日代碼、詛咒狀態、死亡事件次數、首次時間、鎖定截止時間及恢復關卡的印記，不保存姓名、生日年份、感應器數值或權限偏好，也不傳送紀錄。所有故事、角色和情節均為虛構，沒有真實追蹤或入侵。

瀏覽器檢查與實體手機分開記錄；檢查範圍和操作步驟見 [手機測試](手機測試.md)。手機感應、實際震動、耳機音量及 Threads 內建瀏覽器仍需實機操作。

## English

Read the warning and choose optional sound, motion, vibration and flash before starting. Drag the light if you decline motion access. Find the skull, collect three fictional camera overlays, wipe the wall, repeat a knocking sequence and unlock the final door. A hidden seal changes the ending. Pause, mute and exit remain available; the camera is optional in level 2, with a fictional-room alternative. No microphone, location, recording or upload.

Enter a valid four-digit MMDD birthday code (fictional is OK) and confirm you are 18+. MMDD cannot verify your age. The final door uses twelve HTML buttons, with no native keyboard. A wrong code locks game input for 30 real seconds; a stored deadline survives reload and reopening. Your birthday code or 0101 opens the door, fractures the keypad and triggers a final scare. Victory clears **all origin storage**, including other apps' records. It cannot lock the phone OS or prevent manual storage/clock edits.

Upload the five top-level files and the intact assets/ folder to the repository root and enable GitHub Pages on `main` / root. Use HTTPS for camera and motion access. The eye trap and final door include a five-second simulated browser-window cascade; no real windows open, and pause, mute and exit remain available. Reduced motion uses a still collage. The HTML includes fallback artwork and synthesized sound; upload the three assets and ASSETS.md for the photo room and recorded knock. `?lang=en` opens the English entrance. Physical device behavior must be tested separately.

Displayed scares persist a curse and incident count in localStorage. Returning shows a red entrance, but sound and sensors still require your choice. From four incidents, the next run has half the beam radius and a 3-second scare timer instead of 10. Purify with seven rapid taps on blank entrance space or hold the red message for five seconds. Purification calls `localStorage.clear()`, deleting **all keys for this origin**, including other apps' records. Blocked storage falls back to the open page only.

## 日本語

警告を読み、音・センサー・振動・点滅を選んで開始してください。センサーを拒否しても、光を指で動かして遊べます。頭蓋骨を探し、取景器の架空の異変を三つ集め、壁を拭き、ノックの順番を再現して最後の扉を開けます。隠された印で結末が変わります。一時停止・消音・終了が使えます。第2章のカメラは任意で、架空の部屋でもクリアできます。マイク・位置情報・録画・送信は使いません。

四桁の誕生日の月日（架空でも可）を入力し、18 歳以上と確認してください。月日だけでは実際の年齢を確認できません。最後の扉は 12 個の HTML ボタンで、端末のキーボードを出しません。間違うとゲーム内入力が 30 秒停止し、再読み込みしても期限が続きます。誕生日コードか 0101 で開き、ボタンが崩れ、最後の恐怖画面とクリア画面が現れます。クリアは**同じオリジンの全記録**を削除します。端末の OS はロックできず、手動のデータ削除や時計変更も防げません。

ルートの五つのファイルと assets/ フォルダーをそのままリポジトリ直下に置き、GitHub Pages の `main` / root を指定します。カメラとセンサーは HTTPS で試してください。代替の画像と音は HTML 内蔵です。目の罠と最後の扉は、ページ内の偽ウィンドウが増える五秒の演出です。実際のタブは開かず、停止・消音・終了できます。写真の部屋、恐怖の顔と実録ノックには assets/ と ASSETS.md もアップロードしてください。`?lang=ja` で日本語の入口を開けます。実機の動作は別途確認してください。

恐怖画面の表示回数と呪いを localStorage に保存します。再訪時は赤い入口になり、音とセンサーは再び選択が必要です。4 回以上で次の周回の光が半分、恐怖までの時間が 10 秒から 3 秒になります。入口の空白を素早く 7 回タップ、または赤い文章を 5 秒長押しすると浄化します。`localStorage.clear()` は**同じオリジンの全記録**を削除し、他のアプリにも影響します。保存が拒否された場合は現在のページ内だけで記憶します。
