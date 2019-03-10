# Larvata Naming Convention

Larvata 的命名原則，範圍包括：專案、目錄、檔案、應用程式內部設定等。

## Project 專案

專案命名的應用範圍包括：Redmine、Bitbucket、Gitlab、Github 等。

1. 絕對不以數字作為名稱開頭。
2. 名稱保持全小寫英文 (a-z)、連接線 (-)、數字 (0-9)。
3. 格式為：客戶-年份-代碼，其中年份可省略。
4. __禁止使用空白字元。__

- 範例：larvata-awesome-app、client-2018-good-project

## Files 檔案與目錄

1. 盡量不以數字作為檔案名或目錄名開頭。
2. 名稱保持中文、英文、底線 (_)、數字 (0-9)。
3. 英文單詞之間用底線 (_) 連接，英文與數字之間不強制是否有連接底線。
4. __禁止使用空白字元。__

- 範例：larvata_logo.png、backup2016/、客戶_合約書.doc、客戶_報價單.doc

## 專案目錄結構與檔案放置原則

1. follow function list name, translate all to english first
2. decide and name all controller
3. fill in all actions in controller
4. check ajax call actions
5. generate blank all related view files
6. check partial view needs, generate more partial for action pages
7. decide page class name
8. decide big or reuseable component class name
9. make css file and partial files
10. generate page related js files

