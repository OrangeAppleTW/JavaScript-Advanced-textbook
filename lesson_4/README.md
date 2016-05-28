# 表單介面及資料的讀取

## 如何建立表單？

我們常在網頁中看見輸入的欄位，也是一種 HTML 標籤喔，他叫做 `<input />`
而我們在使用這個標籤時，有兩個很重要的特徵(attributes)需要搞懂。

### type
input 標籤有非常多不同的類型(type)，常見的有 `text`(文字欄位)、`checkbox`(勾選方塊)。

例如：

我是文字輸入欄位：<input type="text" />
<input type="checkbox" /> 我是勾選方塊


以下是 HTML:

```html
我是文字輸入欄位：<input type="text" />
<input type="checkbox" /> 我是勾選方塊
```

--

有興趣的同學可以在這個網頁看到不同的 type： http://www.w3schools.com/html/html_form_input_types.asp


### value

可以說是 input 標籤最重要的一個特徵，顧名思義，就是「值」的意思。
我們會在接下來的範例中展示他的用法給大家看。



##文字輸入欄位
請在 JSBin 的中輸入以下 HTML 程式碼，看看發生了什麼事：

```html
Name: <input type=”text” value=”Orange” />
```









