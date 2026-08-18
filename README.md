# 前端 UI 展示

兩個純靜態、無建置流程的互動頁面，用來展示不像 AI 生成的前端設計。

| 路徑 | 頁面 |
|---|---|
| `/` | **VELA-8** — 虛構手工類比合成器的互動產品頁 |
| `/white-knight` | **白騎士症候群** — 可互動的心理側寫 |

## VELA-8 · Monophonic Analogue Synthesizer

面板上的旋鈕可拖曳、八步定序器可點亮並自選音高、示波器即時繪製波形，按下 **PLAY** 會透過 Web Audio API 真的發出聲音。純靜態單檔（`index.html`）。

## 白騎士症候群 · Interactive Essay

暖黑手抄本風格的心理側寫（`white-knight/index.html`）。包含一段四幕分支故事測驗（選擇後揭露真相）、可互動的「拯救的循環」軌道（走一圈累加關係次數），以及照顧 vs 拯救的對照互動。

## 本機預覽

直接用瀏覽器打開 `index.html` 即可，或起一個簡單的靜態伺服器：

```bash
npx serve .
```

## 部署

靜態網站，Vercel 會自動把 `index.html` 服務在根路徑，無需額外設定。

## 技術

- 手刻 CSS/SVG 擬物 UI：旋鈕、推桿、LED、螺絲、木側頰、絲印標籤
- Web Audio API：振盪器 → 24dB 低通濾波器 → 包絡 → 主音量，含前瞻式排程器
- Canvas 即時示波器
- 響應式、支援鍵盤操作與 `prefers-reduced-motion`

> 註：HALCYON INSTRUMENTS 與 VELA-8 皆為虛構品牌與商品，本頁僅為前端 UI／Web Audio 工藝展示。
