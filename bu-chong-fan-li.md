# 6. 大量練習

以下有些會用到一點點 jQuery，直接提供 jQuery 載入的 CDN：(請放在 body 結束標籤之前)

```markup
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
```

## 練習

### 1 介面 hamburger icon

指定檔名：`hamburger_icon.html`

用 button 標籤做一個 hamburger icon：

切換 class (使用 jQuery)：

```javascript
// jQuery 版本：DOM 載入完成之後執行
$(function(){

  // 按鈕狀態的切換
  $("button.hamburger_icon").on("click", function(){
    $(this).toggleClass("-on");
  });
  
});
```

切換 class (使用 JavaScript)：

```javascript
// JavaScript 版本：DOM 載入完成之後執行
document.addEventListener('DOMContentLoaded', function(){
  
  // 按鈕狀態的切換
  var hamburger_icon = document.getElementsByClassName("hamburger_icon")[0];
  hamburger_icon.addEventListener("click", function(){
    hamburger_icon.classList.toggle("-on");
  });
  
});
```

結果示意：

{% embed url="https://youtu.be/6rJP4TZF4SU" %}



提供 html：

```markup
<button type="button" class="hamburger_icon">
  <span class="-hr -top"></span>
  <span class="-hr -middle"></span>
  <span class="-hr -bottom"></span>
</button>
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/rNBErJy" %}





### 2 套用 hamburger icon 的外掛

指定檔名：`hamburger_icon_with_plugin.html`

[官網](https://jonsuh.com/hamburgers/)

[官方所提供的 css 在這](https://raw.githubusercontent.com/jonsuh/hamburgers/master/dist/hamburgers.css)。

自行挑選一個效果，學會套用。只需要看 Usage 的 1 \~ 4 點即可。



切換 class (以下有 jQuery 及 JS 版本)：

```javascript
/*
// jQuery 版本
$(function(){
  
  $("button.hamburger").on("click", function(){
    $(this).toggleClass("is-active");
  });

});
*/

// JavaScript 版本
document.addEventListener("DOMContentLoaded", function(){
  
  var btn_hamburger = document.getElementsByClassName("hamburger")[0];
  btn_hamburger.addEventListener("click", function(){
    this.classList.toggle("is-active");
  });
  
});
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/xvVLyR" %}





### 3 導覽列縮合

指定檔名：`nav_switch.html`

提供 html：

```markup
<button type="button" class="btn_switch">導覽列縮合按鈕</button>

<nav class="main_nav">
  <ul class="nav_list">
    <li><a href="#">首頁</a></li>
    <li><a href="#">關於我們</a></li>
    <li><a href="#">分類頁</a></li>
  </ul>
</nav>
```

提供 jQuery 的展開縮合的做法(較簡單)：

```javascript
// 點擊按鈕，選單縮放
$("button.btn_switch").on("click", function(){
  $("nav.main_nav").slideToggle();
});
```



結果示意：

{% embed url="https://youtu.be/8Q7obn9a9hU" %}



參考作法(使用 jQuery 做展開縮合)：

{% embed url="https://codepen.io/carlos411/pen/XvGKQz" %}

以下提供 JavaScript 的展開縮合做法：

{% embed url="https://codepen.io/carlos411/pen/VwrMMjO" %}



### 4 三欄式 RWD - 使用 Flexbox

指定檔名：`rwd_with_flexbox.html`

說明：

* 768px 以上為桌機版；767px 以下為行動版。
* 左欄及右欄寬度各 200px，剩餘空間寬度都給中間欄。
* 限定使用 Flexbox 來製作三欄式 RWD 排版。

結果示意：

{% embed url="https://youtu.be/ABX7rKgLeXo" %}

提供 HTML 結果如下：

```markup
<div class="all_container">
  <div>
    左側<br>
    另一行
  </div>
  <div>
    中間
  </div>
  <div>
    右側
  </div>
</div>
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/MWWJQvQ" %}



### 5 內容圖片佔滿版

指定檔案：`full_width_image.html`

區塊滿版，高度250px，裡面一張圖片，如下結構：

```markup
<div class="img_block">
  <img src="https://picsum.photos/id/866/800/400">
</div>
```

並設定在 575px 以下行動版時，佔滿的區域比例為寬高1:1(即正方形)。

結果示意：

{% embed url="https://youtu.be/jQq3ocGodaw" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/JjjELmR" %}



### 6 區塊場景的滿版

指定檔名：`full_scene.html`

製作三個區塊，寬高都佔滿版，留意高度。分別任意指定不同的背景色以便觀察。

給定 html 如下：

```markup
<section class="scene scene_1">
  scene1
</section>

<section class="scene scene_2">
  scene2
</section>

<section class="scene scene_3">
  scene3
</section>
```

結果示意：

{% embed url="https://youtu.be/Fwd58Kpvrdc" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/XWWLXWL" %}





### 7 有 10 個項目的水平方向排版

指定檔名：`ten_items_scroll.html`

提供 html 如下：

```markup
<div class="list_container">
  <ul class="ul_list">
    <li class="item">
      <div class="item_block">
        <h1>標題1</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題2</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題3</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題4</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題5</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題6</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題7</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題8</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題9</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
    <li class="item">
      <div class="item_block">
        <h1>標題10</h1>
        <img src="https://picsum.photos/id/500/200/100">
      </div>
    </li>
  </ul>
</div>
```



參考作法：

{% embed url="https://codepen.io/carlos411/pen/QWWdrbX" %}





### 8 內容固定在螢幕上，但在其它內容的後方

指定檔名：`content_fixed.html`

觀察廣告區塊的介面效果：[https://youtu.be/abtFFCpcw5U](https://youtu.be/abtFFCpcw5U)

{% embed url="https://youtu.be/abtFFCpcw5U" %}

請做出如上廣告區塊的排版效果。

結果示意：

{% embed url="https://youtu.be/jNe2XwPi3uo" %}



註：此種效果建議用在行動版上，且內容不要太多。以免超出整個 100vh 的螢幕高度，以致於看不到內容。可從以下這個 codepen 開始實作：

{% embed url="https://codepen.io/carlos411/pen/gOaPWgZ" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/ZEGdXdW" %}





### 9 圓角與內距，相對於文字大小

指定檔名：`em_unit.html`

提供 html：

```markup
<div class="block">這是 div 文字<div>
```

提供 CSS：

```css
* {
  box-sizing: border-box;
}
div.block{
  border: 1px solid black;
  display: inline-block;

  font-size: 1rem;

  border-radius: 8px;
  padding: 2px 4px;
}

@media screen and (max-width: 767px){
  div.block{
    font-size: 2rem;
  }
}
```

上述的介面，div.block 裡的文字大小在螢幕寬度 767px 以下時，從 1rem 變成 2rem，也就是變成了 2 倍。但「圓角」及「內距 padding」部份，並沒有變成兩倍。

請調整成「圓角」及「內距 padding」，也要跟著文字大小改變。(提示：使用 em 單位。)

* 文字大小變兩倍： 圓角 8px → 16px。
* 文字大小變兩倍：內距 2px 4px → 4px 8px。



結果示意：

{% embed url="https://youtu.be/te0rNqgUyO8" %}





參考作法：

{% embed url="https://codepen.io/carlos411/pen/GRpLpLB" %}



### 10 左側區塊的縮合

指定檔名：`aside_toggle.html`



提供 html：

```markup
<button type="button" class="btn_toggle">縮合</button>

<div class="parent_flex">
  
  <div class="left_block -on">
    <div class="inner_content">
      <p>這是段落這是段落這是段落這是段落這是段落</p>
      <img src="https://via.placeholder.com/100x150">
    </div>
  </div>
  
  <div class="right_block">右側
  </div>
</div>
```

提供 JS：

```markup
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script>
  $(function(){
    
    $("button.btn_toggle").on("click", function(){
      $("div.left_block").toggleClass("-on");
    });
    
  });
</script>
```

方向(練習寫 Flexbox 模式，先將框線結構寫出來)：

* `div.left_block.-on` 會設定到 `flex-basis: 200px;`。
* `div.right_block` 會設定到 `flex-grow: 1;`。



參考作法：

{% embed url="https://codepen.io/carlos411/pen/qBOGPwz" %}





### 11 一列四個變成一列兩個

背景圖，一列四個變成一列兩個。

參考作法：

{% embed url="https://codepen.io/carlos411/pen/OKVQrm" %}





### 12 Youtube iframe 影片 RWD

提供以下：`560: 315 = 16:9`

```markup
<iframe height="315" width="560" class="test" src="https://www.youtube.com/embed/-RAdHJ-aquE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

結果示意：

{% embed url="https://youtu.be/uEzbFE37CI8" %}





參考作法：

{% embed url="https://codepen.io/carlos411/pen/PoGdRmB" %}



## 實作類似 Youtube 版型

建立 **`youtube_layout.html`** 來撰寫以下各步驟：

第一步：[https://youtu.be/\_WbrNB61JZ0](https://youtu.be/\_WbrNB61JZ0)

header 區域的高：60px。

側邊欄區域的寬：240px。

{% embed url="https://youtu.be/_WbrNB61JZ0" %}



第二步：[https://youtu.be/oRDd\_HPAGNk](https://youtu.be/oRDd\_HPAGNk)

{% embed url="https://youtu.be/oRDd_HPAGNk" %}



第三步：[https://youtu.be/MloMoEBTjKc](https://youtu.be/MloMoEBTjKc)

{% embed url="https://youtu.be/MloMoEBTjKc" %}



第四步：[https://youtu.be/EsNq1FjpD1s](https://youtu.be/EsNq1FjpD1s)

* 寬度小於等於 767px 時，介面調整。
* 模擬漢堡按鈕，點擊後出現導覽列。

{% embed url="https://youtu.be/EsNq1FjpD1s" %}



參考作法：



## 參考

### 1 套用 Font Awesome

[官網](https://fontawesome.com)

[下載範例](http://notes.carlos-studio.com/download/fontawesome\_sample.zip)

