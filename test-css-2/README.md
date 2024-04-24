###### 04/23

# 使用 CSS 變更標籤特性

## 了解容器的概念

DIV, 用來排版用的 HTML 標籤
網頁排版都是有關容器的設定

## CSS reset 清除樣式

可以使用 CSS 覆蓋瀏覽器內建的樣式
[css reset](https://meyerweb.com/eric/tools/css/reset/);

## HTML 標籤 區塊元素

h1,
預設樣式為 display: block;

1. 盡可能佔滿整個版面
2. 區塊元素就算改變寬度也會另起一行來進行呈現

## HTML 標籤 行內元素

a,
span 本身不代表任何意思,屬於排版用的行內標籤
樣式為 display: inline;

1. 較常使用在段落裡面
2. 沒辦法直接設定寬高

## HTML 標籤 行內與區塊

1. 行內包含在區塊元素中 如 a 連結在 p 段落裡.
2. 行內可以設定為區塊. 如 a 連結改成區塊元素就可以設定寬高

## HTML div 標籤

沒有語意，單純拿來排版的標籤
使用後代選擇器
修改在 div 的範圍內標籤樣式
意思是在這個類別選擇器.style 底下所有的 a 標籤都會套用這個樣式

```
//html
<div class="style1">
  <a>我是a標籤</a>
</div>

//css
.style1 a {
  color: red;
}
```

在需要客製化樣式時, 就可以藉由 div 這個容器來製作個別樣式

## CSS 樣式 - margin 外邊界

每個區塊元素的特性是,當在裡面放多少東西時都會自動適應高度。
所以不建議把高度寫死，因為有可能會超出顯示的範圍。

```
margin: 30px; 上右下左 向外推
margin-top:
margin-right:
margin-bottom:
margin-left:
```

## CSS 樣式 - padding 留白距離

將區塊元素內的標籤內容向內推擠，與 margin 不同的是，margin 是向外推。

```
padding-left: 30px:
```

## Box Model(盒模型)

各個 HTML 標籤，會影響到寬高的只有 padding、border 會影響到實際的寬高，margin 雖然沒有影響實際寬高但在網頁上還是會佔用空間。

```
.box {
  width: 50px;
  height: 50px;
  padding: 50px;
  border: 10px solid red;
  /* 實際寬高為 170px x 170px */
  /*
  margin不影響實際寬高, 在網頁上還是會影響佔用空間,
  佔用空間為 270px x 270px
  */
  margin: 50px;
}
```

## margin 區塊水平置中的應用

這個區塊依照父元素的寬度來自動適應寬度

```
//左右邊平均分配空間形成置中
margin-left: auto;
margin-right: auto;
```

## text-align 文字水平置中

會依照這個區塊元素內的標籤來設定要怎麼對齊

```
text-align: center;
```

## CSS3 box-sizing

可以設定為將 padding, margin, border 的寬高設定, 讓寬高在計算後等於你實際設定的 width, height。

```
*, *:before, *:after{
  box-sizing: border-box;
}
```
