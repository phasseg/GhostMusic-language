# GhostMusic 翻譯貢獻指南

這份 README 只用來說明如何貢獻翻譯檔案。若你要提交其他程式碼變更，請參考 `CONTRIBUTING.md`。

## 你可以貢獻什麼

- 新增新的語言檔
- 補齊既有語言檔缺少的字串
- 修正翻譯內容、標點、格式

所有翻譯檔都放在 `locales/` 目錄下。

## 語言檔格式

每個語言檔都是一個 JSON 檔，例如：

- `locales/en.json`
- `locales/zh_TW.json`

建議遵守以下規則：

- 檔名使用語言代碼，例如 `ja.json`、`ko.json`、`zh_TW.json`
- 所有檔案使用 UTF-8 編碼
- JSON 格式必須正確，不能有多餘逗號或重複 key
- 鍵名結構要和 `en.json` 盡量一致
- 保留佔位符，例如 `{name}`、`{count}`、`{title}`

## 新增或修改翻譯的步驟

1. Fork 這個專案
2. 在 `locales/` 新增或編輯你的語言檔
3. 確認 JSON 可以正常解析
4. 提交變更到你的分支
5. 開 Pull Request 到主專案

## 建議的檢查方式

在送出前，請先確認以下事項：

- 檔案只修改 `locales/` 底下的內容
- 沒有遺漏必要翻譯鍵
- 沒有把 Discord token 或其他敏感資料提交進去
- 佔位符格式沒有被改壞

如果你有啟用本專案提供的 git hook，push 時會自動阻擋非 `locales/` 的變更。

## 貢獻範例

如果你想新增日文翻譯，可以建立：

```text
locales/ja.json
```

然後以 `en.json` 為基礎，逐步翻成日文，保留原本的 key 結構。

## Pull Request 建議寫法

PR 標題建議簡單明確，例如：

- Add Japanese translations
- Improve Traditional Chinese translations
- Fix missing keys in English locale

PR 內容可以寫：

- 新增/更新了哪些語言
- 是否補齊了缺少的鍵
- 有沒有調整任何顯示文字

## 注意事項

- 不要修改和翻譯無關的檔案
- 不要提交含有 token、密碼或 API key 的設定檔
- 如果你需要新增欄位或調整翻譯結構，請先開 issue 討論

## 與專案內規則配合

本專案另外提供：

- `CONTRIBUTING.md`：較完整的翻譯貢獻規範
- `.github/workflows/validate-locales.yml`：Pull Request 檢查
- `.githooks/pre-push`：本機 push 限制範例

如果你只是想幫忙翻譯，直接編輯 `locales/` 就可以。
