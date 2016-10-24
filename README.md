# Larvata Coding Style

## PHP

## Ruby

## Python

## JavaScript

## CSS / SCSS / Compass

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
