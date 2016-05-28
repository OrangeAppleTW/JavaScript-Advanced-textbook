# 多個資料表的延伸應用

幾乎在所有使用資料庫的情形下，我們都不只使用一個資料表，而是會使用多個資料表儲存不同性質的資料，舉例來說，我們會把「學生」、「家長」、「老師」的資料分開儲存在不同的資料表中。
現在，我們就要來創建「家長(Parents)」、「導師 (Teachers)」兩個資料表 (collection)！

1. 初始化「teachers」、「parents」資料表
2. 在 console 手動產生幾筆資料(姓名、電話)，記得 save 喔！

> ### 小提醒
> 一般的資料庫中，資料表叫做 Table。但是在 ForerunnerDB 中，資料表叫做 Collection。


<br>

## 下拉式選單

當我們想為學生指定特定的家長時，我們總不希望慢慢地輸入家長的 ID 吧？
這時我們就可以使用預先產生的下拉式選單來讓使用者做更好的輸入，例如：

<select id="parent-id">
  <option value="">請選擇家長</option>
  <option value="1beda312sd">Orange</option>
  <option value="5b23fs45hj">Apple</option>
</select>

這個下拉式選單的 HTML 原始碼如下：

```html
<select id="parent-id">
  <option value="">請選擇家長</option>
  <option value="1beda312sd">Orange</option>
  <option value="5b23fs45hj">Apple</option>
</select>
```

<br>

### 欸？那如果我用 jQuery 對這個 select 標籤拿資料(`$.val()`)，會拿到什麼呢？
我們馬上來試試看！

<br>

### 如果我們想要預先選好某個選項，該怎麼做呢？
只要在 option 中加入 `selected` 就好囉！
```html
  <option value="5b23fs45hj" selected>Apple</option>
```
更簡單的方式是：直接使用 jQuery 設定這個 select 標籤的值，例如：
```javascript
$("#parent-id").val("5b23fs45hj");
```

<br>

## 實作時間
* 在修改學生資料的表單中加入選擇家長、導師的欄位，將家長、導師的 id 存入學生資料的 `parentId` 及 `teacherId` 中。
* 編輯學生時，家長及導師欄位會自動選好這個學生的家長及導師選項。

### 挑戰題
* 請加入新增家長及導師的功能，讓使用者可以用介面自行加入資料！

