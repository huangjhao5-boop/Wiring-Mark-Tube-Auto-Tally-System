# ハード図面配線 & マークチューブ自動集計系統
### Hard Wiring Diagram & Mark Tube Auto-Aggregation System

[![Author](https://img.shields.io/badge/Author-M.K(TW)-indigo.svg)](https://github.com/)
[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/)
[![License](https://img.shields.io/badge/license-MIT-emerald.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Web%20%7C%20iPad%20%7C%20PC%20%7C%20Mobile-teal.svg)]()
[![Privacy](https://img.shields.io/badge/data_privacy-100%25%20Client--Side-orange.svg)]()

> **專為電氣控制盤、分電盤、自動控制配線工程設計的圖面視覺化配線與線號標籤（マークチューブ）自動集計系統。**
> 
> 解決傳統人工計算線號管數量繁瑣、容易漏算及圖面核對費時的痛點。支援匯入多頁 PDF / 圖檔，於瀏覽器中直接進行智慧吸附配線，並一鍵匯出符合日本電氣工事規範的 Excel 明細表與多頁標註圖面。

---

## 🌟 核心特色 (Key Features)

### 1. ⚡ 智慧導線吸附與折線作圖 (Intelligent Circuit Snapping)
- **黑線智慧吸附**：點擊底圖時自動捕捉並吸附電氣迴路黑線，精準定位無偏折。
- **直角正交路線自動計算**：自動避開現有線路，智慧產生正交直角折點。
- **即時角度提示**：支援 $0^\circ, 15^\circ, 30^\circ, 45^\circ, 75^\circ, 90^\circ$ 角度自動對齊與視覺化提示。

### 2. 🏷️ 線號管與端子台即時集計 (Mark Tube & Terminal Block Auto-Summary)
- **標籤視覺化標記**：線條中央即時渲染印字標籤（如 `101`, `COM`），端子台連接線路以琥珀色外框突顯。
- **高頻印字智慧推薦**：依據使用次數由多到少動態排序前 6 大常用印字標籤，點擊秒速套用。
- **管徑尺寸自動對應 (日本規格)**：
  - `0.5 ~ 1.25 SQ` $\longrightarrow$ **3.2Φ**
  - `2.0 SQ` $\longrightarrow$ **3.6Φ**
  - `3.5 SQ` $\longrightarrow$ **4.2Φ**
  - （每條配線自動計為 **2 個線號管**，勾選端子台連接自動累計 **1 點端子**）

### 3. 📱 iPad / 觸控筆 (Apple Pencil) / 行動裝置深度最佳化
- **觸控筆長按（0.5秒）加/刪折點**：筆尖停留在黑線上即可隨心所欲插入折點，停在折點上自動刪除。
- **Procreate 類雙觸控修飾手勢**：單指按住螢幕任一處 ＋ 筆尖點擊 ＝ 即刻插入折點。
- **側邊欄彈性開閉**：頂部「設定」與「明細」面板可隨時收合，提供 100% 滿版大畫布視野。
- **零滾動確認彈窗**：彈窗高度智慧緊湊化，平板與手機上無須捲動即可一覽全部 SQ、顏色與確定按鈕。

### 4. 📊 完整多頁面匯出功能 (Universal Multi-Page Export)
- **Excel (`.xlsx`) & CSV 下載**：自動產生標題篩選下拉選單、尺寸分類統計、合計總數。
- **多頁 PDF 圖面匯出**：可選擇「當前頁」、「全頁面一併輸出」或「指定頁碼（如 1, 3, 5-7）」。
- **高解析 PNG (ZIP) 打包**：多頁圖面自動打包為單一 ZIP 壓縮檔快速下載。

---

## 🎮 跨平台操作指南 (Shortcut & Gesture Cheat Sheet)

本系統針對 **電腦鍵鼠** 與 **iPad / 觸控筆** 進行了深度雙模優化：

| 操作情境 | 🖥️ パソコン操作 (PC 電腦端) | 📱 iPad / 觸控筆 (Apple Pencil) |
| :--- | :--- | :--- |
| **A 點 / B 點 設置** | 滑鼠左鍵點擊導線 | 筆尖 / 單指輕點導線（零延遲） |
| **新增折點 (Waypoint)** | • 導線或黑線上**雙擊**<br>• 按住 `Shift` ＋ 點擊 | • **筆尖長按 0.5 秒**（最推薦）<br>• 快速雙擊黑線<br>• 單指按住螢幕 ＋ 筆尖點擊 |
| **刪除折點** | 雙擊折點圓圈節點 | 筆尖長按折點圓圈節點 |
| **取消 A 點** | 滑鼠右鍵 或 `ESC` 鍵 | 雙指輕點螢幕 或 頂部 `[✕ 取消]` |
| **畫面縮放 (Zoom)** | 滑鼠滾輪（細緻平滑縮放） | 雙指捏合縮放 (Pinch to Zoom) |
| **畫面平移 (Pan)** | 滑鼠中鍵 拖曳 或 `Space` ＋ 拖曳 | 雙指滑動 或 單指拖曳空白處 |
| **展開 / 收合側欄** | 點擊頂部 `[設定]` / `[明細]` | 點擊頂部 `[設定]` / `[明細]` |

---

## 📐 集計規格標準 (Mark Tube Calculation Rules)

| 電線尺寸 (SQ) | 線號管規格 (Tube Size) | 1條配線線號管數量 | 端子台連接點數 | 支援電線色 |
| :---: | :---: | :---: | :---: | :---: |
| **0.5 SQ** | **3.2Φ** | 2 個 | 1 點 (有勾選時) | 赤、青、黄、緑、黒、白、紫、橙 |
| **0.75 SQ** | **3.2Φ** | 2 個 | 1 點 (有勾選時) | 赤、青、黄、緑、黒、白、紫、橙 |
| **1.25 SQ** | **3.2Φ** | 2 個 | 1 點 (有勾選時) | 赤、青、黄、緑、黒、白、紫、橙 |
| **2.0 SQ** | **3.6Φ** | 2 個 | 1 點 (有勾選時) | 赤、青、黄、緑、黒、白、紫、橙 |
| **3.5 SQ** | **4.2Φ** | 2 個 | 1 點 (有勾選時) | 赤、青、黄、緑、黒、白、紫、橙 |
| **5.5 SQ** | 特殊規格 (不列入管徑集計) | 2 個 | 1 點 (有勾選時) | 赤、青、黄、緑、黒、白、紫、橙 |

---

## 🚀 快速啟動 (Quick Start)

本系統為 **純前端單一檔案架構 (Zero-Dependencies Single-File Web App)**，無須安裝複雜的後端環境，**資料 100% 在本地瀏覽器運行，圖面絕對保密不外流**。

### 方法 1：直接於瀏覽器開啟
直接雙擊開啟 `index.html` 即可使用。

### 方法 2：透過本地伺服器運行（推薦，PDF 載入效能最佳）
```bash
# 進入專案目錄
cd wiring-app

# 使用 Python 啟動本地 HTTP 伺服器
python -m http.server 8000

# 於瀏覽器開啟
http://localhost:8000
```

### 方法 3：iPad / 平板在區域網路連線
1. 確認電腦與 iPad 連接相同 Wi-Fi。
2. 查詢電腦本機 IP（Windows 可在 CMD 輸入 `ipconfig`，例如 `192.168.1.100`）。
3. 在 iPad Safari 輸入 `http://192.168.1.100:8000` 即可無線作圖！

---

## 🛠️ 技術棧 (Tech Stack)

- **UI 框架**：[Tailwind CSS](https://tailwindcss.com/) (響應式深色工業風格設計)
- **圖示庫**：[Font Awesome 6](https://fontawesome.com/)
- **繪圖核心**：HTML5 Canvas 2D API (支援高解析度圖層與吸附演算法)
- **PDF 解析**：[PDF.js](https://mozilla.github.io/pdf.js/) (Mozilla 出品)
- **PDF 生成**：[jsPDF](https://github.com/parallax/jsPDF)
- **壓縮打包**：[JSZip](https://stuk.github.io/jszip/)
- **報表匯出**：[SheetJS (xlsx)](https://sheetjs.com/)

---

## 👨‍💻 作者資訊 (Author)

- **作者 (Author)**: **M.K(TW)**
- **專案名稱**: ハード図面配線 & マークチューブ自動集計系統 (Hard Wiring Diagram & Mark Tube Auto-Aggregation System)

---

## ⚠️ 免責聲明 (Disclaimer / 免責事項)

1. **輔助工具性質**：本系統為電氣工程配線與線號管數量統計之**輔助計算工具**。使用者在進行實際配盤、剪線、印字、端子壓接及送電前，仍應依據原廠電氣圖面與現場工安規範進行最終人工核對。
2. **免責約定**：作者不對因使用本系統計算誤差、圖面解析偏差或第三方瀏覽器相容性所可能導致之工程延誤、材料損耗或衍生性直接/間接損害承擔法律責任。
3. **資料安全**：本軟體為 100% 離線本機運算架構，使用者所載入之工程圖面及專案資料不會上傳至任何外部雲端伺服器。

---

## 📄 授權條款 (License)

本專案採用 **MIT License** 授權，歡迎自由修改、擴充與應用。
