# 6 大量練習

以下若有用到 jQuery，可直接載入下面這行 jQuery：(放在 body 結束標籤之前)

```markup
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
```

## 練習

### 1 介面 hamburger icon

用 button 標籤做一個 hamburger icon。

提供 html：

```html
<button type="button" class="hamburger_icon">
  <span class="-hr -top"></span>
  <span class="-hr -middle"></span>
  <span class="-hr -bottom"></span>
</button>
```



切換 class (使用 jQuery)：

```javascript
// 按鈕狀態的切換
$("button.hamburger_icon").on("click", function(){
  $(this).toggleClass("-on");
});
```

切換 class (使用 JavaScript)：

```javascript
// 按鈕狀態的切換
var hamburger_icon = document.getElementsByClassName("hamburger_icon")[0];
hamburger_icon.addEventListener("click", function(){
  hamburger_icon.classList.toggle("-on");
});
```

結果示意：

{% embed url="https://youtu.be/6rJP4TZF4SU" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/rNBErJy" %}





### 2 套用 hamburger icon 的外掛

[套件官網](https://jonsuh.com/hamburgers/)。

[官方所提供的 css 在這](https://raw.githubusercontent.com/jonsuh/hamburgers/master/dist/hamburgers.css)。

自行挑選一個效果，學會套用。只需要看官網裡的 Usage 1 \~ 4 點即可。



切換 class (以下有 jQuery 及 JS 版本)：

```javascript
/*
// jQuery 版本
$("button.hamburger").on("click", function(){
  $(this).toggleClass("is-active");
});
*/

// JavaScript 版本
var btn_hamburger = document.getElementsByClassName("hamburger")[0];
btn_hamburger.addEventListener("click", function(){
  this.classList.toggle("is-active");
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



## 4 導覽列開啟，不推開底下內容

直接使用這個 CodePen，也可建立新的網頁檔來寫：

{% embed url="https://codepen.io/carlos411/pen/gOoVjJa?editors=1010" %}

撰寫 CSS，完成以下參考作法的結果。





參考作法：

{% embed url="https://codepen.io/carlos411/pen/NWXQBeb" %}



### 5 使用 Flexbox 做版位佈局

提供 HTML 如下：

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

請直接參考下方 CodePen 的畫面結果，實作看看。



參考作法：

{% embed url="https://codepen.io/carlos411/pen/MWWJQvQ" %}



### 6 內容圖片佔滿版

提供 HTML 如下：

```markup
<div class="img_block">
  <img src="https://picsum.photos/id/867/2000/300">
</div>
```

* 當螢幕寬度小於等於 `767.98px` 以下時，`圖片`要在 `div.img_block` 區塊水平方向、垂直方向皆置中；且 `div.img_block` 需佔滿螢幕，且寬高比需是 `2:1`。
* 請參考下方 CodePen 的畫面結果，實作看看。





參考作法：

{% embed url="https://codepen.io/carlos411/pen/JjjELmR" %}





### 7 有 10 個項目的排版

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

請直接參考下方 CodePen 的畫面結果，實作看看。



參考作法：

{% embed url="https://codepen.io/carlos411/pen/QWWdrbX" %}





### 8 圓角與內距，相對於文字大小

提供 html：

```markup
<button type="button" class="btn">加入會員</button>
```

提供部份 CSS：

```css
* {
  box-sizing: border-box;
}
html{
  font-size: 62.5%;
}

button.btn{
  cursor: pointer;
  font-size: 1.6rem;
  background-image: linear-gradient(#ddd, #bbb);
  text-aling: center;
  border: 1px solid hsla(0, 0%, 0%, .2);
  text-shadow: 0 1px 1px white;
  box-shadow: 0 1px 0 white inset;
  transition: font-size 1s;
  
  
  padding: 4px 8px;
  border-radius: 8px;
}
```

執行以下兩點：

1、按鈕點擊然後尚未放開的狀態，套用以下 CSS：

```css
border: 1px solid hsla(0, 0%, 0%, .3);
box-shadow: 1px 2px 3px rgba(0,0,0, .6) inset;
text-shadow: 0 1px 0px #ccc;
```

2、當螢幕寬度小於等於 767.98px 時，將按鈕的文字大小變成原來(1.6rem)的兩倍大(使用 rem 單位)，然後按鈕的 `padding` 及 `border-radius` 也要**自動**變兩倍大。



參考作法：

{% embed url="https://codepen.io/carlos411/pen/GRpLpLB" %}



### 9 左側區塊的縮合

提供 html：

```markup
<button type="button" class="btn_toggle">縮合</button>

<div class="parent_flex">
  
  <div class="left_block">
    
    內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容內容
    
  </div>
  
  <div class="right_block -on">
    <div class="inner_content">
      <p>這是段落這是段落這是段落這是段落這是段落</p>
      <img src="https://via.placeholder.com/300x150">
    </div>
  </div>
  
</div>
```

提供 JS：

```javascript
// JavaScript 版本
var btn_toggle = document.getElementsByClassName("btn_toggle")[0];
btn_toggle.addEventListener("click", function(){
  let right_block = document.getElementsByClassName("right_block")[0];
  right_block.classList.toggle("-on");
});


// jQuery 版本
/*
$("button.btn_toggle").on("click", function(){
  $("div.left_block").toggleClass("-on");
});
*/
```





參考作法：

{% embed url="https://codepen.io/carlos411/pen/qBOGPwz" %}





### 10 Youtube iframe 影片 RWD

提供以下 iframe 影片，它的寬高比為 `560:315`，也就是 `16:9`。

```markup
<iframe height="315" width="560" class="test" src="https://www.youtube.com/embed/-RAdHJ-aquE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

執行完的結果示意：

{% embed url="https://youtu.be/uEzbFE37CI8" %}



參考作法：

{% embed url="https://codepen.io/carlos411/pen/PoGdRmB" %}



### 11 聊天對話框的展開縮合

提供 html：

```html
<div style="height: 1000px; border: 1px solid purple;"></div>

<article class="chat_block">
  
  <header class="header">
    <button type="button" class="btn_toggle">
      <span class="on">開啟</span>
      <span class="off">關閉</span>
    </button>
  </header>
  
  <section>
    其它區域
  </section>
  
</article>
```

提供 JS：

```javascript
var btn_toggle = document.getElementsByClassName("btn_toggle")[0];
btn_toggle.addEventListener("click", function(){
  this.closest("article.chat_block").classList.toggle("-on");
});
```

參考以下的結果示意，實作看看。且在螢幕寬度小於等於 575.98px 時，就讓對話框直接消失。



參考作法：

{% embed url="https://codepen.io/carlos411/pen/OJzKoLX" %}





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

[https://alldata.sgp1.digitaloceanspaces.com/sample/youtube\_layout\_practice.zip](https://alldata.sgp1.digitaloceanspaces.com/sample/youtube\_layout\_practice.zip)



