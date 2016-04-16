# 更新學生學生資料

來認識一下 Forerunner 的更新資料函式：
當我們要更新某筆資料，只要使用 `updateById` 函式，將資料的 `id` 以及 `內容` 傳入函式，即可更新資料。

```javascript
// 新的資料
var newData = {
    name: "Apple",
    grade: 6
}

// 對 id 為 1 的學生進行資料修改
DB.collection("students").updateById("1",newData);
```

廢話不多說，讓我們來實作資料更新的功能吧！

### 功能敘述：
* 當點下其中一名學生的編輯按鈕時，跳出修改學生 Modal
* Modal中有一個表格，填有該名學生的資料
* 使用者在修改資料以後，點選「送出」按鈕，便會照剛剛的資料進行修改
