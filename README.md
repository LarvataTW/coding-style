# Larvata Naming Convention

Larvata 的命名原則，範圍包括：專案、目錄、檔案、應用程式內部設定等。

## Project 專案

專案命名的應用範圍包括：Redmine、Bitbucekt、Github 等。

1. 絕對不能以數字作為名稱開頭。
2. 名稱保持全小寫英文 (a-z)、連接線 (-)、數字 (0-9)
3. 格式為：客戶名稱-年份 (YYYY)-程式名字

- 範例：larvata-2016-my-awesome-app

## Files 檔案與目錄

1. 盡量不以數字作為檔案名或目錄名開頭。
2. 名稱保持全小寫英文 (a-z)、底線 (_)、數字 (0-9)
3. 格式為：xxx\_0123456789

- 範例：avatar_20161120.png，avatars\_2016/

## Axure 頁面

## PhotoShop 圖層

---

# Larvata Coding Style

Larvata 程式碼風格規範，Larvata 內部對各種程式語言的編寫規範。   
其應用原則有以下幾條，原則的權重以排序越後越重。

1. 遵循該程式語言的社群標準。
2. 若使用的 Framework 另有其規範，則以該規範為準。
3. 自行訂立的風格規範。

所有人員都應該安裝 [EditorConfig](http://editorconfig.org/) 作為編輯器風格控制器： 
[EditorConfig 外掛下載](http://editorconfig.org/#download)  
並使用 Larvata 的 [EditorConfig 設定檔](http://#)。

## PHP

1. __所有 *.php 檔案以 4 個空白為縮排。__
2. 

## Ruby

1. __所有 *.rb 檔案以 2 個空白為縮排。__
2. 

## Python

1. __所有 *.py 檔案以 2 個空白為縮排。__
2. 

## JavaScript

1. __所有 *.js 檔案以 4 個空白為縮排。__
2. 

## CSS / SCSS / Compass

1. __所有 \*.css，\*.scss 檔案以 4 個空白為縮排。__
2. 

### Class 與 ID 命名原則

純上色用途命名使用底線串接：
> index_page

js用途使用中線加上prefix:
> js-good-btn

id使用中線:
> main-menu

預設組件使用中線:
> w-100, t-center

預設組件 hack 使用中線放置於組件後，rwd hack前
> btn-blue-news-xs

rwd hack 使用中線放置於最後:
> index_page-xs

## HTML

1. __所有 *.html 檔案以 4 個空白為縮排。__
2. 

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

- rails: application
- yii2: main.php

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

* Issue #201
* http://mmdays.com/2007/04/24/coding-style/
* http://sideeffect.kr/popularconvention/