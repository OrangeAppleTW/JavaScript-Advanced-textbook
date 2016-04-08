# 認識 ForerunnerDB
ForerunnerDB 是一個 JavaScript 寫成的資料庫。  並支援持久儲存功能，以及基本的搜尋功能。

> 官方網站：http://forerunnerdb.com/

<br>

## 開始吧
1. 創造一個新頁面 (隨便叫什麼名字，但必須是 `.html` 結尾)
2. 上傳 ForerunnerDB ([下載位置](js/fdb-all.min.js))
3. 在頁面中載入 ForerunnerDB 函式庫

> ### 找找看
> 這個新網頁的網址在哪呢？

<br>

## 創造資料庫

在 HTML 中，其實可以直接寫 JavaScript (但是在程式碼很多的時候，這不是一個好選擇)。


在`<body>`的尾巴(載入函式庫以後)，創造一個 `<script>` 區塊：
```html
<script>
    // ...程式寫在這裡
</script>
```

###創造第一個資料庫 (Database):
```javascript
var fdb = new ForerunnerDB();
var db = fdb.db("你的資料庫名稱");
```

這時，db變數中就裝有一個小小的資料庫啦！

<br>

## 創造 collection (Table)

在 Forerunner 中，一群相同類型的資料被放在 ***collection(集合)*** 中，其實就相當於 ***資料表(Table)*** 的概念啦。現在，讓我們創建第一個 Collection 吧！

```javascript
studentCollection = db.collection('students');
```

這時候，studentCollection 就代表了 db 這個資料庫中的一個資料表啦，顧名思義，裡面裝的當然就是學生資料囉！

<br>

> ### 小提醒
雖然 Forerunner 具有資料庫的一些基礎功能，
但他嚴格講起來不是一個正規的資料庫，
這邊是為了讓學生能用較輕量、簡單的方式學習資料庫的觀念，
因而選用 Forerunner
