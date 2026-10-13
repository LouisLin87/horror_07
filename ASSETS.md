# 素材來源與選用方式

更新：2026-10-13

這些素材隨作品放在同來源 assets/，遊玩時不連生成服務或素材來源網站。三檔缺漏時，內建 Canvas / Web Audio 仍能完整通關。

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

## 上傳

把 index.html、README.md、手機測試.md、.nojekyll、ASSETS.md 及 assets/ 下三個素材一起上傳。共八個檔案；不需要 work/、qa/、API 金鑰或 node_modules。只上傳 HTML 仍可玩，使用內建場景和合成敲聲。
