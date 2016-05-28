# CRUD 資料庫的基本操作

***CRUD*** 是設計資料系統時很重要的基本技巧，也有人叫他「增刪改查」，分表代表了：

* 新增 (Create)
* 查詢 (Read)
* 修改 (Update)
* 刪除 (Delete)

這四個操作非常基本也非常重要，讓我們從 ***C (Create)*** 開始吧！

<br>

## 插入資料 (Create)

打開你的瀏覽器的主控臺，輸入以下程式碼：

```javascript
studentCollection.insert({
    name: "Koding",
    age: 18
});
```
請注意，insert 函式接受的是一個 ***物件*** 哦！(還記得物件長什麼樣子嗎？)
所以上面的程式碼相當於是這樣：

```javascript
var newStudent = {
    name: "Koding",
    age: 18
};
studentCollection.insert(newStudent);
```

<br>

## 讀取資料 (Read)
新增了一筆資料，我們要如何知道是否成功寫入了呢？
Collection 的 `find` 函式可以從 studentCollection 中讀取所有的資料：
```javascript
studentCollection.find();
```

> ###想想看：
我們要如何「看到」讀取出來的資料呢？


### 動動手
現在試著多新增幾筆資料試試看吧！(10 mins)

<br>

## 儲存 & 讀取
問題來了，當我們刷新頁面時，資料統統不見了！這樣的資料庫一點意義也沒有嘛...

還好，Forerunner 支援 ***持久儲存(persistence)*** 的功能，我們可以用 `save` 函式來將 collection 中的資料儲存在瀏覽器中：

```javascript
studentCollection.save();
```

現在，加上幾筆資料，並且儲存他們後，刷新頁面看看吧！

###結果還是沒資料？
原來 Forerunner 設計的機制是：如果要使用之前儲存的資料，必須執行另一個函式 `load`:

```javascript
studentCollection.load();
```
執行一次上面這行程式碼，用 `find` 指令看看資料有沒有跑出來吧！

> ###注意！
> load 的執行是需要時間的，而 load 後面的程式碼並不會等 load 執行完才跟著執行，而是會先被執行。
>
> 這種情況在 javascript 中很常見，叫做 ***非同步(Asyncronise)***。
