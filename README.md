# Larvata Naming Convention

Larvata 的命名原則，範圍包括：專案、目錄、檔案、應用程式內部設定等。

## Project 專案

專案命名的應用範圍包括：Redmine、Bitbucekt、Github 等。

1. 絕對不能以數字作為名稱開頭。
2. 名稱保持全小寫英文 (a-z)、連接線 (-)、數字 (0-9)
3. 格式為：客戶名稱-年份 (YYYY)-程式名字
4. __禁止使用空白字元。__

- 範例：larvata-2016-my-awesome-app

## Files 檔案與目錄

1. 盡量不以數字作為檔案名或目錄名開頭。
2. 名稱保持全小寫英文 (a-z)、底線 (_)、數字 (0-9)
3. 英文單詞之間用底線 (_) 連接，英文與數字之間不強制是否有連接底線。
4. __禁止使用空白字元。__

- 範例：larvata_logo.png，backup2016/

## Git

1. 依照專案類型建立適當的 .gitignore 
2. branch 名稱保持全小寫英文 (a-z)、底線 (_)、數字 (0-9)
3. 重構的 branch 一律以 `refactor_` 為前綴開頭
4. __嚴格遵守 git-flow 流程__

* git-flow 分：git-flow, git-flow-avh 目前公司內部還沒有定論 ...

### Git 全域設定

1. git config --global core.autocrlf true
2. git config --global core.filemode true

## MySQL

1. 資料庫、資料表、欄位名稱使用全小寫英文 (a-z)、底線 (_)、數字 (0-9)
2. 英文單詞之間用底線 (_) 連接，英文與數字之間不強制是否有連接底線。
3. __禁止使用空白字元。__

- 範例：larvata\_database，users，first\_name

## Docker

1. Image 與 Container 命名使用全小寫英文 (a-z)、底線 (_)、數字 (0-9)
2. 英文單詞之間用底線 (_) 連接，英文與數字之間不強制是否有連接底線。
3. __禁止使用空白字元。__

- 範例：larvata\_mysql，larvata\_nginx

## Axure

1. 關閉自動更新版本。
2. 禁止手動更新版本。

## PhotoShop

1. 檔案命名 ...?
2. 圖層命名 ...?

---

# Larvata Coding Style

Larvata 程式碼風格規範，Larvata 內部對各種程式語言的編寫規範。   
其應用原則有以下幾條：

1. 遵循該程式語言的社群標準。
2. 若使用的 Framework 另有其規範，則以該規範為準。
3. 自行訂立的風格規範。
4. __原則的權重以排序越後的越重 (後者覆蓋前者)__。

所有人員都應該安裝 [EditorConfig](http://editorconfig.org/) 作為編輯器風格控制器： 
[EditorConfig 外掛下載](http://editorconfig.org/#download)  
並使用 Larvata 的 [EditorConfig 設定檔](https://raw.githubusercontent.com/LarvataTW/coding-style/master/editorconfig)，下載另存到：`~/.editorconfig`。

## PHP

1. 以 [PSR-2](http://www.php-fig.org/psr/psr-2/) 規範為基礎。
1. __所有 *.php 檔案以 4 個空白為縮排。__

## Python

1. 以 [PEP-0008](https://www.python.org/dev/peps/pep-0008/) 規範為基礎。
2. __所有 *.py 檔案以 2 個空白為縮排。__ 

## Ruby

1. 以 [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide) 規範為基礎。
2. 以 [RuboCop](https://github.com/bbatsov/rubocop) 作為語法檢查工具。
3. __所有 *.rb 檔案以 2 個空白為縮排。__

## Rails

1. Rails 以 [Rails Style Guide](https://github.com/bbatsov/rails-style-guide) 規範為基礎。
2. 禁止使用 SQLite 作為開發環境、生產環境的資料庫。

## HTML

1. 以 [http://codeguide.co](http://codeguide.bootcss.com/) 規範為基礎。
2. __所有 *.html 檔案以 4 個空白為縮排。__

### Class 命名原則

CSS 樣式用途，使用全小寫英文與底線連接，例如：   
> `red_text`

Hack 調整用途，使用全小寫英文與底線連接，並加上說明描述與後綴：`-hack`，例如：
> `red_text_xs-hack`

JS 用途，使用全小寫英文與中線連接，並加上前綴 `js-`，例如：   
> `js-change-color`

### ID 命名原則

使用全小寫英文與中線連接，例如:
> `my-only-one-div`

## JavaScript

1. <del>以 [Airbnb JavaScript](https://github.com/airbnb/javascript) 規範為基礎。</del>
2. 以 [StandardJS](http://standardjs.com/) 規範為基礎。
3. __所有 *.js 檔案以 4 個空白為縮排。__
4. 寫於view內的js應該都置於page的最外層，include檔案內勿撰寫獨立inline js, 共用partial view檔的js應獨立拆出成為共用檔案

## CSS / SCSS

1. 以 [Airbnb CSS](https://github.com/airbnb/css) 規範為基礎。
2. __所有 \*.css，\*.scss 檔案以 4 個空白為縮排。__ 

## Swift

1. 以 [raywenderlich.com](https://github.com/raywenderlich/swift-style-guide) 規範為基礎。
2. __所有 *.swift 檔案以 2 個空白為縮排。__

---

# 專案目錄結構與檔案放置原則

## project file generate sequence

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

## HTML

main frame file:

- rails: /app/views/latouts/application.html.erb
- yii2: /views/layouts/main.php

page file:
> follow controller name and action name(use yii2 as sample)
> controller/action

- controller/newsController/indexAction -> view/news/index.php
- controller/newsController/createAction -> view/news/create.php

partial page file
> follow parent view file name with underscore and selft name
> controller/_action_part

- controller/newsController/indexAction -> view/news/index.php
- controller/newsController/indexAction?tab=all -> view/news/_index_all.php
- controller/newsController/indexAction?tab=past -> view/news/_index_past.php

## CSS


## JavaScript

site scope js file:
> put in one or two general js file

- application.js
- common.js
- init.js

page scope js file:
> follow controller/action_part role

- controller/newsController/indexAction -> js/news/index.js
- controller/newsController/indexAction?tab=all -> js/news/index_all.js

---

# References

* [http://mmdays.com/2007/04/24/coding-style/](http://mmdays.com/2007/04/24/coding-style/)
* [http://sideeffect.kr/popularconvention/](http://sideeffect.kr/popularconvention/)
* [https://github.com/showcases/clean-code-linters](https://github.com/showcases/clean-code-linters)

## Git

### Branch 命名原則

- 嚴格遵守 git-flow 流程
- branch 名稱保持全小寫英文 (a-z)、底線 (_)、數字 (0-9)
- 重構的 branch 一律以 refactor_ 為前綴開頭
- 程式整理的 branch 一律以 syntax_enhancement_ 為前綴開頭
- 套件升級及相關設定的 branch 一律以 upgrade_ 為前綴開頭

### Commit 命名原則

- 方便往後了解演變，單一 commit 完成單一主旨
- 如果有相關的 issue 需以 refs #issue編號 為前綴開頭
