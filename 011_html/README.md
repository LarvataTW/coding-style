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

