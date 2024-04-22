###### 04/22

# CSS 基礎教學

HTML 結構, CSS 樣式

## 插入 CSS 檔案

在 html 中插入 CSS 檔案
較常出現錯誤, 載入位置錯誤, 單字拼錯.

```
<link rel=""stylesheet href="style.css">

//在style.css中的格式
/*
選擇器 {
  屬性: 設定值;
  屬性: 設定值;
}
*/

h1 {
  color: red;
  font-size: 16px;
}
```

## CSS 選擇器

1. 標籤選擇器 HTML 標籤, 所有相同標籤都會吃到 CSS 設定.
2. 擬態選擇器 HTML 標籤:hover, :active, 使用者體驗優化. 當滑鼠移動至標籤上時改變樣式
3. 類別選擇器 希望不同標籤可以有不同樣式(客製化樣式), 使用 class, React 是 className.

## CSS 優化文字排版

```
字形:font-family
字形大小:font-size
行距:line-height
靠左靠右置中:text-align
首行縮排:text-indent
下引線、刪除線:text-decoration
字元間距:letter-spacing
```

## HTML 標籤加上線條的 CSS 樣式

```
//CSS樣式
//border: 線條大小 線條樣式 顏色;
// 線條樣式: 實心solid, 點點dotted, 長條dashed
h1 {
  border: 1px solid blue;
}

//上下左右 border-left, border-right, border-top, border-bottom
```

## CSS 權重

權重相同時候設定的樣式會蓋掉前設定樣式

```
//HTML標籤: 1分
<div class="header">
  <p>123</p>
</div>

//class: 10分
.header {
  //CSS樣式
}

//使用id設定樣式的方法
//id: 100分
<h1 id="header"></h1>

#header {
  color: red;
}

//CSS也可以直接寫在標籤內
//權重: 1000分
<h1 style="color:red;"></h1>

//important 權重最高
<p style="color:red !important;">important</p>
```
