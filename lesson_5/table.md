# 用表格來表達資料吧！

現在試著用之前學過的技巧，寫個程式將資料庫中的資料用 網頁表格(Table)給顯示出來吧！

```html
    <table>
        <thead>
            <tr>
                <td>id</td>
                <td>姓名</td>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>1</td>
                <td>Orange</td>
            </tr>
        </tbody>
    </table>
```

> ### 小提示
> * 為了將資料一筆一筆的加到 table 中，可能會需要用到 jQuery 的 [append](http://api.jquery.com/append/) 函式
> * 為了讓表格更好看，可以套用 Bootstrap 的 [Table](http://getbootstrap.com/css/#tables) 樣式
