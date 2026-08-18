# VELA-8 · Monophonic Analogue Synthesizer

一台**虛構**手工類比合成器的互動產品頁。面板上的旋鈕可拖曳、八步定序器可點亮、示波器即時繪製波形，按下 **PLAY** 會透過 Web Audio API 真的發出聲音。

純靜態單檔（`index.html`），無建置流程、無相依套件。

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
