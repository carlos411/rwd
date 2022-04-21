# 4.5 元件 Components

## 改寫元件基本樣式的規則

改寫樣式的基本原則：不要去改變原來 bootstrap 的原始碼，而是透過覆寫的方式，也就是加上自己的樣式(class)，以麵包屑介面為例，以下的 `class="my_breadcrumb"` 是自己加上的：

```markup
<nav aria-label="breadcrumb" class="my_breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item"><a href="#">Library</a></li>
    <li class="breadcrumb-item active" aria-current="page">Data</li>
  </ol>
</nav>
```

css：

```css
nav.my_breadcrumb ol.breadcrumb{
  background-color: black;
}
nav.my_breadcrumb ol.breadcrumb .breadcrumb-item > a{
  color: red;
}
nav.my_breadcrumb ol.breadcrumb .breadcrumb-item.active{
  color: white;
}
nav.my_breadcrumb ol.breadcrumb .breadcrumb-item+.breadcrumb-item::before{
  color: green;
}
```

例：

{% embed url="https://codepen.io/carlos411/pen/zYGvowv" %}



## 練習 1：建立一個頁面

建立檔名：`bootstrap_grid_and_components.html`

* 中間區域是一個 container。
* 最上方導覽列佔滿版。
* md 範圍以上(768px 以上)：左邊佔9欄，右邊佔3欄
* sm 範圍以下(767px以下)變成是直排：都佔12欄
* 有用到的元件：Navbar、Card、Alerts

如下示意：

{% embed url="https://youtu.be/bMuqlCOrIi0" %}

參考作法：

{% embed url="https://codepen.io/carlos411/pen/OJJMXbV" %}



