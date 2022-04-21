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
* 小於 768px 時，變成是直排：都佔12欄
* 有用到的元件：Navbar、Card、Alerts

navbar：

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Dropdown
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>
```

Card：

```html
<div class="card">
  <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
```

Alert：

```html
<div class="alert alert-primary" role="alert">
  A simple primary alert—check it out!
</div>
```



如下示意：

{% embed url="https://youtu.be/bMuqlCOrIi0" %}

參考作法：

{% embed url="https://codepen.io/carlos411/pen/OJJMXbV" %}



