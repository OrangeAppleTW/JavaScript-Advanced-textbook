# 操作多筆資料 (包含)

我們已經學到了不少搜尋的方式，現在來考慮這種情況：
> 當我們要搜尋的資料可能有許多筆，但是又無法用數字來比較時，例如想找出屬於『甲班』以及『乙班』的學生時，我們該如何做呢？

<br>

## 包含條件 `$in`
```javascript
result = collection.find({
    name: {
        $in: ["Orange", "Apple"]
    }
});
```

<br>

##挑戰時間
在網頁上增加幾個     `checkbox`，當點下「搜尋」按鈕時會只顯示班級符合勾選選項的學生。

> ### 小提示
> * checkbox 的 HTML 語法：`<input type="checkbox" />`
> * 取得勾選狀態：`$( elem ).prop( "checked" )`
