# 汐衡能源｜能源分析儀表板

`React 19` · `TypeScript` · `Recharts` · `Base UI` · `Vite`

[**開啟 Demo**](https://cutecat8110.github.io/tideline-energy-demo/)

同圖比較四個港區的能源趨勢，透過左右刻度看清大小用量，再將查詢結果整理成報表。

![能源總覽](images/overview.png)

| 體驗順序 | 代表操作 |
| --- | --- |
| [能源總覽](https://cutecat8110.github.io/tideline-energy-demo/#/overview) | 三種能源摘要、四港比較線圖、左右刻度 |
| [港區趨勢](https://cutecat8110.github.io/tideline-energy-demo/#/ports/port-2?period=month&date=2026-09-18) | 日／月／年、前期虛線、時段定位與數據明細 |
| [分析報表](https://cutecat8110.github.io/tideline-energy-demo/#/reports) | 多條件查詢、分軸／同軸、三種圖表與匯出 |
| 查詢保存 | 保存五組條件、重新命名、移除與跨分頁更新 |

![港區趨勢](images/port.png)
![分析報表](images/reports.png)

點帳號欄右側的鑰匙帶入帳密，再按「登入」使用全部功能。支援亮暗主題、鍵盤操作，以及手機、桌面與 4K 版面。

<details>
<summary>實作重點</summary>

- 各港色彩固定；實線／虛線比較期間，分軸呈現不同量級，同軸比較實際大小。
- 點選曲線或用鍵盤定位日期與時段；缺值不補零，前期資料仍可比較。
- 資料狀態、單位與更新時間一起呈現；4K 版面放大字級，並排曲線與數值。
- 日期、合計、圖表與匯出共用資料函式。
- 查詢草稿與已套用條件分離，網址保留查詢、排序及頁碼。
- IndexedDB 交易及版本檢查，處理重複提交、儲存失敗與跨分頁衝突。
- 圖表／報表按頁載入，字型自本站提供，列印明細按需產生。

</details>

<details>
<summary>展示範圍</summary>

品牌、港區、設備及全部量測數據均為合成，期間為 2024/01/01–2026/09/30，更新時間固定為 2026/10/01。登入為展示入口，沒有正式身分驗證、即時量測或外部服務。已存條件與外觀保存在目前瀏覽器；重設會清除並登出，不影響其他作品。匯出為 CSV，列印使用瀏覽器功能。4K 為瀏覽器尺寸驗證，尚未實機測試電視牆。

</details>
