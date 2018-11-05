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
