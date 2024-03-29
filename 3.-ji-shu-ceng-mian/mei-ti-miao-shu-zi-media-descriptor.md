# 3.2 媒體描述 Media Features

## 範例 1：min-width

當螢幕寬度大於等於 768px 時，連結`<a>` 的文字顏色會變成紅色。

沒有寫 `Media Type` 的話，預設都是 `all`：

```css
@media (min-width: 768px){
  a{
    color: red;
  }
}
```

以上的原始碼，如果加上 Media Type 的會，等同於以下：

```css
@media all and (min-width: 768px){
  a{
    color: red;
  }
}
```

例：

{% embed url="https://codepen.io/carlos411/pen/yLBdEVG" %}



## 範例 2：max-width

當螢幕寬度小於等於 767.98px 時，連結`<a>` 的文字顏色會變成綠色。

```css
@media (max-width: 767.98px){
  a{
    color: green;
  }
}
```

例：

{% embed url="https://codepen.io/carlos411/pen/MWgMXJL" %}



## 範例 3：結合 min-width 與 max-width

當螢幕寬度大於等於 768px 且小於等於 991.98px 時，連結`<a>` 的文字顏色會變成橘色。

```css
@media (min-width: 768px) and (max-width: 991.98px){
  a{
    color: orange;
  }
}
```

例：

{% embed url="https://codepen.io/carlos411/pen/JjPQZJY" %}



## 範例 4：結合 Media Type

當是螢幕時，螢幕寬度大於等於 768px 且小於等於 991.98px 時，連結`<a>` 的文字顏色會變成紅色。

```css
@media screen and (min-width: 768px) and (max-width: 991.98px){
  a{
    color: red;
  }
}
```

例：

{% embed url="https://codepen.io/carlos411/pen/GRKbGMM" %}



## 範例 5：Media Query 的「或」

以半型逗號做分隔。

```css
@media screen and (min-width: 1200px), screen and (max-width: 767.98px){
  p{
    color: blue;
  }
}
```

{% embed url="https://codepen.io/carlos411/pen/XWbdaNz" %}



## 範例 6：orientation

orientation 可以設定當手持裝置是橫向或縱向時，需要套用的 CSS，可以設定的值有：

* **portrait** (縱向)
* **landscape** (橫向)

註：即使是桌面裝置，若高度 > 寬度時，會視為直向；寬度 > 高度時，視為橫向。

當是螢幕時，且設備為橫向(**landscape**)擺放時，連結 `<a>` 的文字顏色會是紅色；反之，若設備為直向(**portrait**)擺放時，會是藍色。

```css
@media screen and (orientation: landscape) {
  a{
    color: red;
  }
}

@media screen and (orientation: portrait) {
  a{
    color: blue;
  }
}
```

{% embed url="https://codepen.io/carlos411/pen/RXbWQd" %}
示範 Media Query 的 orientation
{% endembed %}



