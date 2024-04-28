###### 04/25

# 使用 CSS - Flex 網頁排版技巧

1. 軸線的觀念
2. 相關屬性
3. 對齊方式

## Flex 外層屬性(container)

使用 Flex 排版必須在最外層加上的必要屬性

```
display: flex;
```

1. 假設今天我們需要將 div 並排的話, 需要在 div 父層的 container 下 display:flex;的語法.
2. item 會依照父元素的關係依照比例做調整
3. item 會預設每一個 item 的高為等高, 會找到最高的 item

## 軸線

設定主軸 (一樣需要撰寫在最外層的父層 container)

```
flex-direction: row;(default)  左--->右
flex-direction: row-reverse;   左<---左
flex-direction: column;        由上至下
flex-direction: colum-reverse; 由下至上
```

主軸對齊方式 (會依照我們如何設定主軸的起點、終點而改變)

```
justify-content: flex-start;    針對主軸的起點來對齊
justify-content: flex-end;      針對主軸的終點來對齊
justify-content: center;        置中對齊,左右邊留白
justify-content: space-around;  固定左右邊的留白(中間的留白相同, 左右是中間的一半)
justify-content: space-evenly;  固定左右邊的留白(都是相同的)
justify-content: space-between; 左右邊貼齊
```

## 決定換行屬性

當我們的容器(container)滿了, 就不會依照比例去計算寬度. 而是會自動換行

```
flex-wrap: nowrap; (default)
flex-wrap: wrap;
```

## 交錯軸

永遠會跟主軸垂直, 一樣也會有起點、終點

交錯軸對齊方式

```
align-items: flex-start;    針對交錯軸的起點來對齊
align-items: flex-end;      針對交錯軸的終點來對齊
align-items: center;        置中對齊,左右邊留白
align-items: stretch;       交錯軸的起點至終點, 滿版呈現
align-items: baseline;
```

## Flex 小節作業
