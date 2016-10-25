# Larvata Coding Style

## PHP

## Ruby

## Python

## JavaScript

## CSS / SCSS / Compass

### class,id nameing

純上色用途命名使用底線串接:
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

## Rails

## Yii 2

## CodeIgniter

---

# Naming Convention

## Project

## Files

## PhotoShop Layer

---
# application structure guide

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

## html(view)

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

## css


## javascript

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
* http://editorconfig.org/
