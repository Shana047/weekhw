# README

### Looker Studio 報告
本資料已視覺化於 Looker Studio，請點擊下方連結查看：

🔗 [Looker Studio 報告](https://lookerstudio.google.com/reporting/6f43bdd9-018b-4c33-aa80-c3dcf25607ef)



## 重大職災統計資料

本資料集包含歷年重大職災的統計資訊，包含事故類型、發生地點、產業類別以及傷亡人數等。

### 資料概述
- **檔案名稱**: `歷年重大職災統計.csv`
- **欄位說明**:
  - `no`: 事故編號（數值）
  - `date`: 發生日期（日期型，部分缺失）
  - `type`: 職災類型（類別變數，例如墜落、跌倒、爆炸等）
  - `location`: 發生地點（類別變數，例如板橋區、汐止區等）
  - `category`: 產業類別（類別變數，例如製造業、營造業、運輸業等）
  - `deaths`: 死亡人數（整數型變數）
  - `injuries`: 受傷人數（整數型變數）

### 資料清理與處理建議
- 使用 `tidyverse` 進行資料處理，如 `mutate()` 轉換變數類型、`summarise()` 計算統計資訊。
- 若需解析 `date` 變數，可使用 `lubridate::ymd()` 轉換。
- `type`、`location` 和 `category` 為分類變數，建議使用 `forcats::as_factor()` 轉換。
- 使用 `dplyr::summarise()` 計算傷亡統計。


此報告包含事故類型分布、各產業災害統計及其他視覺化分析。
