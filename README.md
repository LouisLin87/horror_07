# 勿入 · DO NOT ENTER · 立入禁止

原創手機恐怖解謎，參考 Lomando 的探索與突發反差。繁體中文、英文、日文；三個場景、可選陷阱、隱藏印記及兩種結局。畫面、程式與預設聲音全部在 `index.html`，不需要安裝框架、API 金鑰或下載影片。

## 視覺方向

第一次進入是暖白、鼠尾草綠的「小小探險室」，用較溫和的文字邀請玩家依自己的步調開始。入口完全遮住走廊與 VHS，仍清楚標示恐怖內容及可選效果。按開始後轉為下面的恐怖畫面；被詛咒的重返入口維持暗紅。

1990 年代低解析類比恐怖：空曠走廊重複同一房號，深處只有紅色門縫；鬼臉以原創黑白交叉排線、左右不對稱的眼神與過寬笑容營造不自然感。牆面、衣物、長髮與骨節手指均由 Canvas 繪製並快取，不使用外站圖片。

畫布有 VHS 掃描線、雜訊與局部水平錯位，介面文字及按鈕保持穩定。局部錯位使用遊戲時間，暫停會凍結；系統「減少動態效果」停用撕裂、抖動與縮放，只保留靜態墨線及掃描線。全畫面紅色脈衝仍需玩家選擇閃光。HTML 維持低於 100 KB，沒有新增必要資產。

## 開始

先閱讀警告、填寫四位生日月日代碼（例如 `0618`）、確認已滿 18 歲，再按「準備好了，開始」。可填虛構日期；月日不包含年份，**不能驗證真實年齡**，成年資格由玩家自行確認。有效日期立即寫入本機 `player_birthday`，不傳送到伺服器；空白、未填滿或無效日期無法開始。

正常與詛咒入口都有「未滿 18 歲」按鈕（英文 Under 18／日文 18 歳未満）。點擊後在同一分頁前往[指定的 YouTube 影片](https://www.youtube.com/watch?v=hkQcoXDpJbA&list=RDhkQcoXDpJbA&start_radio=1)，不必填生日或同意遊戲效果。

可選音效、動作感應、震動及短暫閃光。動作感應預設不勾選；拒絕或無法使用時，滑動光圈仍可完成所有關卡。音效勾選時，開始按鈕立即解鎖音訊。

1. 滑動或傾斜手機照亮走廊，輕點地上的小骷髏。某些東西不應該碰；角落還藏著另一個線索。
2. 來回擦拭血紅的牆，停住手指不算。約三秒有效擦拭後出現驚嚇，仍能繼續擦，記住數字。
3. 擦拭達到足夠範圍後走向門鎖，用 3×4 虛擬鍵盤輸入四位生日代碼。答錯等待 30 秒；答對鍵盤碎裂、終極驚嚇，再顯示「遊戲破關」。攜帶不同線索會走向不同結局。

一般關卡可暫停、靜音或退出；驚嚇畫面也有退出與靜音。切換分頁自動暫停，回來需自行繼續。30 秒懲罰按真實經過時間計算，不受遊戲暫停影響。退出不解除尚未到期的鎖定；通關後清除紀錄，重玩回正常入口，不保存權限選擇。

## 手機生日密碼鎖

第三關包含 0–9、清除、確認共十二個 HTML 按鈕，三欄四列、每鍵至少 48 CSS px。密碼顯示使用 `output`，不是 `input`，所以門鎖點擊不會叫出手機原生鍵盤。只有入口的生日欄位會使用數字鍵盤提示；按 Enter／完成可收起欄位焦點。[MDN inputmode](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes/inputmode)。

四位字串保留前導零，與 `player_birthday` 比對；`0618` 永遠可作備用碼。不足四位只提示，不開始懲罰。錯誤的完整密碼觸發一次陷阱並累加詛咒；同意聲音時短暫尖叫，同意閃光且沒有減少動態時給一次紅色閃動。

鎖定遮罩阻擋遊戲及鍵盤輸入，保留靜音、退出及關閉分頁的能力。文字「怨靈鎖定你的手機」是劇情，**僅遊戲畫面受限制，不會鎖住手機系統或瀏覽器**。

| key | 用途 |
| --- | --- |
| `player_birthday` | 玩家主動輸入的四位月日，可填虛構日期 |
| `horror_lock_until` | 固定到期時間：答錯當下 `Date.now() + 30000` |
| `horror_lock_remaining` | 每當秒數變化寫入剩餘秒數 |
| `horror_lock_context` | 恢復第三關所需的隱藏印記布林值，沒有身份或權限 |

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

本上傳包僅四個檔案：`index.html`、`README.md`、`手機測試.md`、`.nojekyll`。

1. 解壓 ZIP，把這四個檔案放在 GitHub repository 最上層。
2. Settings → Pages → Deploy from a branch → `main` → `/(root)` → Save。
3. 部署成功後，用 GitHub 提供的 **HTTPS** 網址遊玩。

不必上傳製作資料夾 `work/`、`qa/`、`.scratch/` 或整個工作區。上傳資料夾已另外整理，不需挑選數十個工作檔。

入口語言可用 `?lang=zh`、`?lang=en`、`?lang=ja`。切換語言及分享會保留網址其他參數和 hash；新玩家的分享入口先顯示警告；同瀏覽器尚未結束的鎖定優先恢復。

## 手機限制與資產

動作感應需要支援的瀏覽器與安全環境。iOS 的系統授權請求與音訊解鎖在同一個開始手勢發出；拒絕、無 API 或約 4.5 秒無有效數據時自動使用觸控。普通 `http://192.168…` 區網網址主要測觸控，請用 GitHub Pages HTTPS 測感應器。[MDN 動作感應說明](https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/requestPermission_static)。

只有玩家選擇震動才呼叫 `[500, 200, 500]`；不支援時保留畫面與聲音。震動 API 在部分瀏覽器不可用，系統靜音與勿擾模式亦會影響效果，不能承諾每台手機振動。[MDN 震動說明](https://developer.mozilla.org/en-US/docs/Web/API/Navigator/vibrate)。

尖叫音效使用 1.0 網頁音量；網頁不能修改裝置的實體音量。預設不閃光；「減少動態效果」會關閉閃光及畫面抖動。Canvas、CSS 手勢與 viewport 依手機滿版遊戲需求限制頁面捲動及縮放，系統或瀏覽器的輔助縮放仍由使用者控制。

HTML 內的 `ASSETS` 預留 `scream.mp3` 與 `ghost.gif`。目前 `enabled: false`，由內建 Web Audio／HTMLAudio 備用尖叫及程序鬼臉提供效果，因此四檔案包可獨立遊玩。只有自行提供外部素材並設成 `true` 時，才需要一併上傳這兩檔。

## 隱私與驗證

不存取相機、麥克風或定位；感應器值不離開本頁。localStorage 保存玩家主動填寫的四位月日代碼、詛咒狀態、死亡事件次數、首次時間、鎖定截止時間及恢復關卡的印記，不保存姓名、生日年份、感應器數值或權限偏好，也不傳送紀錄。所有故事、角色和情節均為虛構，沒有真實追蹤或入侵。

瀏覽器檢查與實體手機分開記錄；檢查範圍和操作步驟見 [手機測試](手機測試.md)。手機感應、實際震動、耳機音量及 Threads 內建瀏覽器仍需實機操作。

## English

Read the warning and choose optional sound, motion, vibration and flash before starting. Drag the light if you decline motion access. Find the skull, wipe the wall, remember its numbers and open the door. A hidden seal changes the ending. Pause, mute and exit remain available; the page does not access your camera, microphone or location.

Enter a valid four-digit MMDD birthday code (fictional is OK) and confirm you are 18+. MMDD cannot verify your age. The final door uses twelve HTML buttons, with no native keyboard. A wrong code locks game input for 30 real seconds; a stored deadline survives reload and reopening. Your birthday code or 0618 opens the door, fractures the keypad and triggers a final scare. Victory clears **all origin storage**, including other apps' records. It cannot lock the phone OS or prevent manual storage/clock edits.

Upload the four files to the repository root and enable GitHub Pages on `main` / root. Use HTTPS for motion access. The single HTML includes its default artwork and synthesized sound. `?lang=en` opens the English entrance. Physical device behavior must be tested separately.

Displayed scares persist a curse and incident count in localStorage. Returning shows a red entrance, but sound and sensors still require your choice. From four incidents, the next run has half the beam radius and a 3-second scare timer instead of 10. Purify with seven rapid taps on blank entrance space or hold the red message for five seconds. Purification calls `localStorage.clear()`, deleting **all keys for this origin**, including other apps' records. Blocked storage falls back to the open page only.

## 日本語

警告を読み、音・センサー・振動・点滅を選んで開始してください。センサーを拒否しても、光を指で動かして遊べます。床の頭蓋骨を探し、壁を拭いて數字を覚え、扉を開けてください。隠された印で結末が変わります。一時停止・消音・終了が使えます。カメラ・マイク・位置情報は使いません。

四桁の誕生日の月日（架空でも可）を入力し、18 歳以上と確認してください。月日だけでは実際の年齢を確認できません。最後の扉は 12 個の HTML ボタンで、端末のキーボードを出しません。間違うとゲーム内入力が 30 秒停止し、再読み込みしても期限が続きます。誕生日コードか 0618 で開き、ボタンが崩れ、最後の恐怖画面とクリア画面が現れます。クリアは**同じオリジンの全記録**を削除します。端末の OS はロックできず、手動のデータ削除や時計変更も防げません。

四つのファイルをリポジトリ直下に置き、GitHub Pages の `main` / root を指定します。センサーは HTTPS で試してください。標準の画像と音は HTML 内蔵です。`?lang=ja` で日本語の入口を開けます。実機の動作は別途確認してください。

恐怖画面の表示回数と呪いを localStorage に保存します。再訪時は赤い入口になり、音とセンサーは再び選択が必要です。4 回以上で次の周回の光が半分、恐怖までの時間が 10 秒から 3 秒になります。入口の空白を素早く 7 回タップ、または赤い文章を 5 秒長押しすると浄化します。`localStorage.clear()` は**同じオリジンの全記録**を削除し、他のアプリにも影響します。保存が拒否された場合は現在のページ内だけで記憶します。
