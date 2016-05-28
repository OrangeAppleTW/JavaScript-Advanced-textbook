#文字輸入欄位
請在 JSBin 的中輸入以下 HTML 程式碼，看看發生了什麼事：

```html
Name: <input type=”text” value=”Orange” />
```

## 取得欄位中的文字
但是我們要怎麼用 JavaScript 取得欄位中的文字呢？
我們可以使用 jQuery 這麼做：

```javascript
$(selector).val();
```

當然也能設定欄位中的值啦：

```javascript
$(selector).val("OrangeApple");
```

<br>

## 實作時間
在你的網頁中加入兩個欄位「名字」及「年齡」，以及一個按鈕：

名字：<input type="text" /><br>
年齡：<input type="text" />
<button>Hello</button>

--

當按下按鈕時，網頁會跳出以下訊息：
```
Hello, _____ 歲的 _______ 你好 ~
```

### 挑戰題
當跳出訊息之後，原本在欄位中的內容會被清空。



