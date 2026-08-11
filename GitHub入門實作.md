# GitHub 入門實作

目標：用最短路徑學會 GitHub 的基本工作流，最後做出一個可以上傳到 GitHub 的練習作品集資料夾。

## 你需要先懂的三個概念

| 名詞 | 白話解釋 |
| --- | --- |
| Git | 幫你記錄檔案修改歷史的工具 |
| GitHub | 放 Git 專案的雲端平台，也可以分享作品 |
| Repository | 一個專案資料夾，簡稱 repo |

簡單比喻：

- Git 像是「版本記錄器」
- GitHub 像是「雲端作品櫃」
- Repository 像是「一個作品資料夾」

## 第 1 步：建立你的第一個練習作品

這個資料夾目前就是你的練習區。

你可以先放這些檔案：

- `README.md`：介紹這個專案
- `Codex_AI工具實踐指南.md`：你的 AI 學習指南
- `GitHub入門實作.md`：這份 GitHub 練習筆記

## 第 2 步：初始化 Git

在終端機輸入：

```powershell
git init
```

這會讓目前資料夾開始被 Git 管理。

## 第 3 步：查看目前狀態

```powershell
git status
```

你會看到哪些檔案還沒被 Git 追蹤。

## 第 4 步：加入檔案

```powershell
git add .
```

意思是：把目前資料夾中的變更加入準備提交區。

## 第 5 步：建立第一個版本

如果 Git 第一次要求你設定使用者名稱與 Email，可以先在這個專案中設定：

```powershell
git config user.name "Your Name"
git config user.email "your-github-email@example.com"
```

這兩個資訊會出現在 commit 紀錄中，用來表示這次版本是誰建立的。

```powershell
git commit -m "Add AI learning and GitHub practice notes"
```

這會建立第一個版本紀錄。

## 第 6 步：到 GitHub 建立新 Repository

到 GitHub 網站建立一個新的 repository。

建議名稱：

```text
ai-learning-notes
```

建議設定：

- Public：如果你想展示作品
- Private：如果只是自己練習
- 不要勾選自動建立 README，因為我們本機已經有 README

## 第 7 步：連接 GitHub 遠端倉庫

GitHub 建好 repo 後，會給你類似這樣的網址：

```text
https://github.com/你的帳號/ai-learning-notes.git
```

回到終端機輸入：

```powershell
git remote add origin https://github.com/你的帳號/ai-learning-notes.git
git branch -M main
git push -u origin main
```

完成後，你的檔案就會出現在 GitHub 上。

## 第 8 步：以後的日常流程

每次改完檔案後，照這三步：

```powershell
git status
git add .
git commit -m "Describe what changed"
git push
```

中文理解：

1. 看看改了什麼
2. 把變更放進準備區
3. 建立版本紀錄
4. 上傳到 GitHub

## 建議你練習的三個小任務

### 任務 A：更新 README

請 Codex 幫你把 `README.md` 改得更像作品集首頁。

可用提示詞：

```text
請幫我更新 README.md，讓它像一個 AI 學習作品集首頁。
內容包含：我是誰、這個資料夾的用途、目前學到什麼、下一步計畫。
```

### 任務 B：建立學習日誌

請 Codex 建立：

```text
AI學習日誌.md
```

內容包含：

- 日期
- 今天學了什麼
- 我問 AI 什麼問題
- 我實際完成什麼
- 下次要練什麼

### 任務 C：練習版本更新

修改一個檔案後，練習：

```powershell
git status
git add .
git commit -m "Update learning notes"
git push
```

## 問 Codex 的好用句型

```text
請幫我檢查目前資料夾是否適合上傳到 GitHub，並告訴我還缺什麼。
```

```text
請幫我寫一份適合 GitHub 的 README.md。
```

```text
請幫我解釋 git status 的結果，我是初學者，請用白話說明。
```

```text
請幫我看這次 git diff，告訴我改了哪些內容，是否適合 commit。
```
