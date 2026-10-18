# 素材來源與選用方式

更新：2026-10-15

這些素材隨作品放在同來源 assets/，遊玩時不連生成服務或素材來源網站。八檔缺漏時，內建 Canvas / Web Audio 仍能完整通關。

## assets/curtain-room.webp

原創虛構窗簾暗房，使用內建 imagegen 工具於本次專案生成；沒有複製參考截圖、電影或其他作品。生成為 940×1672 PNG，保留原尺寸轉為 WebP（quality 62），約 63 KB。不是相機照片、真實靈異證據或公有領域圖片。依生成服務適用條款使用；CC0 標示僅適用下方敲門聲。

生成提示：

```
Use case: photorealistic-natural / historical-scene.
Asset type: original fictional horror game background, full-bleed portrait 9:16.
Primary request: an exceptionally believable handheld home-camcorder still of a deserted modest Japanese apartment at night in 1998. A dark tall wooden cabinet along the left quarter, faded aged plaster and narrow horizontal wall paneling, closed shabby floral curtains occupying the right half, worn brown wooden floor visible across the lower quarter. The curtain folds and faded repetitive floral print feel slightly uncanny, but no supernatural subject appears yet.
Style: natural photographic realism with actual cloth weave, dust and scratches, flat low-light home-video exposure; subtle green/cyan night-camcorder cast, warm brown wood. The room must still be legible in the midtones; do not crush everything to black. No cinema spotlight, no theatrical fog. Composition is a static first-person view from the doorway, with the cabinet and curtains large enough for small phone screens.
Constraints: completely empty room, no people, no faces, no eyes, no ghosts, no hands, no blood. No letters, numbers, timestamp, subtitles, borders, UI or watermark. This is a fictional scene, not a reproduction of any existing movie or photo. Leave the lower room floor as space for game overlays. Slight analog softness without baked horizontal scanlines; the game adds its own VHS effect.
```

## assets/door-knock.wav

- 作者：Joseph SARDIN / BigSoundBank。
- 原素材：[Door Knock #95](https://bigsoundbank.com/door-knock-s0095.html)。
- 原檔：https://bigsoundbank.com/UPLOAD/mp3/0095.mp3
- 授權：來源頁明示 **CC0 1.0 / public domain**；允許修改及再散布。[授權說明](https://bigsoundbank.com/licenses.html)、[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/)。授權於 2026-10-13 查核。
- 修改：以瀏覽器原生解碼成 32000 Hz，裁出 0.13109375–0.68109375 秒，加入約 9 ms 淡入、18 ms 淡出，16-bit 單聲道 PCM WAV，0.55 秒、35244 bytes。遊戲另接低通與左右聲道，不含來源站影片或旁白。
- 鳴謝：Additional sounds: Joseph SARDIN – BigSoundBank.com。

## assets/window-ghost.webp

2026-10-13 使用內建 imagegen 工具原創生成。三張使用者提供的圖片僅作氛圍與解剖細節參考，產生不同的臉、姿態及構圖；不使用參考圖本身作遊戲資產。原 PNG 1122×1402 RGBA，保留原尺寸及透明 alpha，轉成 WebP（quality 58），251250 bytes。依生成服務適用條款使用，這張圖片沒有 CC0 標示。

用途：第一次驚嚇前才載入，頁內假視窗縮圖與貼近鬼臉共用；失敗用既有 Canvas 替代。原生成 PNG 保存於 work/，不含於公開包。

完整生成提示：

```
Use case: stylized-concept.
Asset type: original photorealistic horror apparition cutout for a portrait mobile browser game, with a genuinely transparent background.
Input images: all three supplied images are mood and anatomical-detail references only, not edit targets. Invent a visibly different fictional adult face and pose; do not reproduce, retouch, or strip the overprints from a reference.
Primary request: a singular unnerving adult apparition seen frontally at very close range. Its face is elongated and asymmetrical, the mottled pale gray skin has extremely fine realistic pores, dry creases and soot-like weathering. Deep black eye sockets surround small off-center milky pupils; one lid hangs lower. The expression is a frozen, strained smile opening into a long unnaturally dark mouth, with thin irregular crowded teeth individually visible, no blood. Dark sparse wet hair blends into the silhouette. Include narrow bare shoulders and two long bony hands reaching toward the viewer from the lower corners, slightly out of the plane of the face, with realistic distinct knuckles, tendons and fingernails, five anatomically legible fingers on each hand. Face dominant in the middle upper half, hands framing rather than covering the eyes.
Style: realistic makeup and practical-creature photography, not illustration, rendered with low-key analog home-video softness; textured monochrome with a very subtle cold cyan cast, readable pale highlights and deep shadow. It should feel like an impossible person found in a paused late-1990s home recording.
Composition: portrait 4:5 cutout, entire face, fingers and shoulders remain inside the frame, a little transparent padding at every edge. No other characters, no room, no UI, no letters, logos, borders or watermark. No gore, mutilation or wounds. Create an original image; do not imitate a particular stock photograph. Preserve actual transparent alpha around the subject.

```

## assets/tv-static.webp

使用者於2026-10-14提供的電視雪花PNG（1917×887，2216604 bytes）。本次僅等比例縮為960×444 WebP（quality55、method6），30922 bytes，保留完整構圖及右下標記。原檔保存於本機備份，不隨公開包提供。原始作者與授權尚未由附件提供，**不標示為CC0、公有領域或原創生成**；此來源狀態與敲門聲的CC0授權不同。

SHA256：`eba282b22a89529700d901287249b5850e93bccd7e34301ea5365bdf4ffc11b4`。

用途：進入底片／文件及文件歸零短暫過場，首次過場才請求。雜訊聲是Web Audio合成，沒有新增音訊資產；缺圖回退內建grain。首頁不顯示或預載，真正控制列不覆蓋。

## 上傳

把 index.html、README.md、手機測試.md、.nojekyll、ASSETS.md 及 assets/ 下八個素材一起上傳。共十三個檔案；不需要 work/、qa/、API 金鑰或 node_modules。只上傳 HTML 仍可玩，使用內建場景和合成敲聲。


## 底片支線（沒有新增資產）

機械眼壁、三至十眼、瞳孔與四位月日均由內聯 Canvas 程序原創繪製，不使用網路圖片、玩家鏡頭畫面或素材佔位圖。眼壁本身沒有額外資產；進入支線的短暫雪花過場會按需載入上述tv-static.webp，公開共八素材、十三檔。

## 原創鬼群（2026-10-14）

內建 imagegen 分別生成。使用者的三張附圖只作為長髮、回頭及暗眼的氛圍參考；公開包沒有附圖原檔、商標或水印。沒有使用 Gemini / Grok / 其他外部服務生成這批素材。所有原始PNG與精確提示詞保存在本機work/，公開只放WebP。

- assets/ghost-listener.webp：46922 bytes，512×768 RGBA，SHA256 9170845d86ba4d7db6e9174dfdb7bb71f2d8e11b7aa810f12ab9e0cb3c4de51b。提示詞：work/ghost-listener-prompt.txt；原圖：work/ghost-listener-original.png。
- assets/ghost-returner.webp：35692 bytes，512×768 RGBA，SHA256 f8d41b22526334557671ef5ce2b7cfb3eb908a4cbff031b5637ed2e7f56460ac。提示詞：work/ghost-returner-prompt.txt；原圖：work/ghost-returner-original.png。
- assets/ghost-mask.webp：45338 bytes，512×768 RGBA，SHA256 eba6a8fa0e2791bbae21a90d1b056a121e3d05a74a4fa28717397527d7d647b5。提示詞：work/ghost-mask-prompt.txt；原圖：work/ghost-mask-original.png。

僅執行等比例縮小與WebP格式轉換，保留真實alpha；沒有由程式去背或創作重畫。角色各自按關卡載入，失敗使用一次快取的程序輪廓。提示詞可供後續替換同身份。

## assets/scan-foley.wav（2026-10-15）

- 作者：小森平 / Taira Komori。
- 原素材頁：[人聲／腳步](https://taira-komori.net/human01tw.html)，使用walking_in_a_house1（木地板赤腳）；[開關聲](https://taira-komori.net/openclose01tw.html)，使用iron_door1_O（慢開鐵門）。
- 條款：[小森平免費音效使用說明](https://taira-komori.net/freesoundtw.html)，2026-10-15查核。允許作品中的遊戲使用及加工；不以獨立音效素材集再配布或販售，不熱連來源音檔，不標示為CC0或自己錄製。此檔僅作為本遊戲場景中的音效；要抽出再配布，須重新依作者條款確認。
- 修改：原生AudioContext解碼、OfflineAudioContext重採樣為16000Hz單聲道。腳步取原檔0.094875起0.35秒，慢開門取0.1361875起1.05秒；兩段間留0.06秒。各段峰值正規化0.65、12ms淡入／24ms淡出，合併PCM16 WAV。總1.46秒、46764 bytes。
- SHA256：7aacc18226ababf04764412d7bc3216e62f49d43a3abcc4160cf10a3481923f0。
- 用途：第二關已選音效並進入探索後才下載。腳步／門軸另外加低通／帶通及左右定位；缺漏用合成替代。心跳與鬼影出現的故障聲皆為程式合成，沒有外部聲檔。
- 鳴謝：Sound effects by Taira Komori / 小森平。原始下載與加工記錄保存在本機work/scan-audio-originals及work/scan-foley-manifest.json，公開包不提供原MP3，也不連來源站播放。

本輪只採小森平兩個切片；Pixabay、Mixkit、Zapsplat及Fesliyan僅作參考，沒有使用其素材或聲稱其全部素材為CC0。

第二關的60秒鬼影在Canvas暫存原創鬼像並九次偏移平均產生柔焦，沒有覆寫原WebP。快取只含原創鬼像，不存相機像素，沒有新增公開素材。
