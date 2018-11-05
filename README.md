# Larvata Naming Convention

Larvata 的命名原則，範圍包括：專案、目錄、檔案、應用程式內部設定等。

## Project 專案

專案命名的應用範圍包括：Redmine、Bitbucekt、Github 等。

0. 絕對不以數字作為名稱開頭。
0. 名稱保持全小寫英文 (a-z)、連接線 (-)、數字 (0-9)。
0. 格式為：客戶名稱-年份 (YYYY)-程式名字。
0. __禁止使用空白字元。__

- 範例：larvata-2016-my-awesome-app

## Files 檔案與目錄

0. 盡量不以數字作為檔案名或目錄名開頭。
0. 名稱保持全小寫英文 (a-z)、底線 (_)、數字 (0-9)。
0. 英文單詞之間用底線 (_) 連接，英文與數字之間不強制是否有連接底線。
0. __禁止使用空白字元。__

- 範例：larvata_logo.png，backup2016/

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

## Axure

0. 關閉自動更新版本。
0. 禁止手動更新版本。

## PhotoShop

0. 檔案命名 ...?
0. 圖層命名 ...?

## Docker

0. Image 與 Container 命名使用全小寫英文 (a-z)、底線 (-)、數字 (0-9)
0. 英文單詞之間用底線 (_) 連接，英文與數字之間不強制是否有連接底線。
0. __禁止使用空白字元。__

- 範例：larvata\_mysql，larvata\_nginx

## MySQL

0. 資料庫、資料表、欄位名稱使用全小寫英文 (a-z)、底線 (_)、數字 (0-9)
0. 英文單詞之間用底線 (_) 連接。
0. 英文與數字之間直接連接。
0. __禁止使用空白字元。__

- 範例：larvata\_database，users，first\_name

## Git

0. 依照專案類型建立適當的 .gitignore。
0. Branch 名稱保持全小寫英文 (a-z)、減號 (-)、數字 (0-9)。
0. Branch 名稱的英文單詞使用減號 (-) 連接。
0. __嚴格遵守 git-flow 流程。__

* git-flow 分：git-flow, git-flow-avh 目前公司內部還沒有定論 ...

### Git 全域設定

0. git config --global core.autocrlf true
0. git config --global core.filemode true

### Branch 命名原則

#### 使用 scoped-branch-name 樣式

使用 scoped branch name 是理想且合理的命名方式，亦即在分支名中使用 `/`。

* 重構的 branch 一律以 refactor/ 為前綴開頭
* 程式整理的 branch 一律以 syntax_enhancement/ 為前綴開頭
* 套件升級及相關設定的 branch 一律以 upgrade/ 為前綴開頭

範例：
- `feature/my-awesome-feature`
- `fix/issue-666`
- `release/0.1.0`

**note:** git-flow 也採用此法來命名分支。

#### 分支 section 使用 url-friendly 字元

建議使用 `/[a-zA-Z0-9-]+/` 作為 `feature/{placeholder}` 分支使用之字元，並應具有合理語意、且**動詞**一律採用**現在簡單式**。

命名邏輯範例：

- **IF** 有相關 issue/pull-request/redmine-issue
  - **issue**
    後綴採用 `issue-%d` 格式；例如 `fix/issue-26`
  - **pull-request**
    後綴採用 `pr-%d` 格式；使用例為 patch some problems derivative from another pull-request
  - **redmine-issue**
    後綴採用 `redmine-%d` 格式；例如 `feature/redmine-20324`
- **ELSE**
  - 採用直接關係功能導向語意作為命名方向，範例：
    - `feature/update-footer-copyright`
    - `feature/drop-contact-page`
    - etc.

#### 確保主要分支前綴命名列舉

使用如：

- `master`
- `develop`
- `feature`
- `hotfix`
- `release`
- ...

等，建立一套分支前綴作為第一原則。

#### 其它

如團隊引用 github-flow，討論是否採用 username-scoped-branch-name 配合 pull-request 作為主要分支命名方式

### Commit 命名原則

- 方便往後了解演變，單一 commit 完成單一主旨
- 如果有相關的 issue 需以 refs #issue 編號為前綴開頭

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

## References

* [http://mmdays.com/2007/04/24/coding-style/](http://mmdays.com/2007/04/24/coding-style/)
* [http://sideeffect.kr/popularconvention/](http://sideeffect.kr/popularconvention/)
* [https://github.com/showcases/clean-code-linters](https://github.com/showcases/clean-code-linters)


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

main frame file:

- rails: /app/views/latouts/application.html.erb
- yii2: /views/layouts/main.php

page file:
> follow controller name and action name(use yii2 as sample)
> controller/action

- controller/newsController/indexAction -> view/news/index.php
- controller/newsController/createAction -> view/news/create.php

partial page file
> controller/_action_part

- controller/newsController/indexAction -> view/news/index.php
- controller/newsController/indexAction?tab=all -> view/news/_index_all.php
- controller/newsController/indexAction?tab=past -> view/news/_index_past.php

## CSS / SCSS

1. 以 [Airbnb CSS](https://github.com/airbnb/css) 規範為基礎。
2. __所有 \*.css，\*.scss 檔案以 2 個空白為縮排。__ 

## JavaScript

1. <del>以 [Airbnb JavaScript](https://github.com/airbnb/javascript) 規範為基礎。</del>
2. 以 [StandardJS](http://standardjs.com/) 規範為基礎。
3. __所有 *.js 檔案以 4 個空白為縮排。__
4. 寫於view內的js應該都置於page的最外層，include檔案內勿撰寫獨立inline js, 共用partial view檔的js應獨立拆出成為共用檔案

### 按鈕行為

當按鈕被使用者click時，需要依照觸發後的行為做相對應的處置

### 送出資料

此時需注意按鈕在當次操作行為完成前不能被重複click，故必須處置的pattern可以是：   
> click按鈕時使用.js-lock class有無判斷來鎖定後續的行為是否可以在事件完成前被重複觸發

```
$(btn).click(function(){   
  if($(btn).hasClass('js-lock')){   
    return false;//如果有lock class就不能再繼續行為
  }else{
    $(btn).addClass('js-lock')//開始鎖定按鈕
    //繼續發送的ajax行為直到行為結束
    $(btn).removeClass('js-lock')//解除鎖定按鈕
});
```

### modal觸發

實務上modal觸發常常需要抓取資料填入modal內，故需要在click按鈕觸發modal同時執行其他獲取資料行為
> click btn, 綁定一個事件獲取相關資訊後回填至modal結構內，modal內容部分由半透明變回正常不透明

```
$(btn).click(function(){
  $(modal-body).css(opacity:0.3);//modal內容的部分刷淡讓使用者知道內容尚未ready
  $(modal-body).addClass('js-lock')//也可以把整個body跟送出按鈕等等加上lock
  //獲取資料ajax或是由頁面內（通常是列表）data-xxx來獲取資訊
  //將資料填回modal-body內的部分（通常使用id來綁定欄位）
  $(modal-body).css(opacity:1);//資料備齊了，可以把資訊變回正常顏色
  $(modal-body).removeClass('js-lock')//最後解除所有可以按的畫面與按鈕的lock,使用者可正常操作modal內容
});
```

site scope js file:
> put in one or two general js file

- application.js
- common.js
- init.js

page scope js file:
> follow controller/action_part role

- controller/newsController/indexAction -> js/news/index.js
- controller/newsController/indexAction?tab=all -> js/news/index_all.js
## PHP

1. 以 [PSR-2](http://www.php-fig.org/psr/psr-2/) 規範為基礎。
1. __所有 *.php 檔案以 2 個空白為縮排。__

## Python

1. 以 [PEP-0008](https://www.python.org/dev/peps/pep-0008/) 規範為基礎。
2. __所有 *.py 檔案以 4 個空白為縮排。__ 

## Ruby

1. 以 [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide) 規範為基礎。
2. 以 [RuboCop](https://github.com/bbatsov/rubocop) 作為語法檢查工具。
3. __所有 *.rb 檔案以 2 個空白為縮排。__

## Rails

1. Rails 以 [Rails Style Guide](https://github.com/bbatsov/rails-style-guide) 規範為基礎。
2. 禁止使用 SQLite 作為開發環境、生產環境的資料庫。

## Swift

1. 以 [raywenderlich.com](https://github.com/raywenderlich/swift-style-guide) 規範為基礎。
2. __所有 *.swift 檔案以 2 個空白為縮排。__

