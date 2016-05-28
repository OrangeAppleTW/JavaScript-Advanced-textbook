<script   src="https://code.jquery.com/jquery-2.2.4.min.js"   integrity="sha256-BbhdlvQf/xTY9gja0Dq3HiwQF8LaCRTXxZKRutelT44="   crossorigin="anonymous"></script>

# 勾選方塊 (Checkbox)

有時候我們會在網頁中看到能夠「打勾」的方塊，他其實也是 input 的一種，現在想想看勾選方塊都用在什麼地方呢？

請在 JSBin 的中輸入以下 HTML 程式碼，看看發生了什麼事：

```html
<input type="checkbox" /> 我是勾選方塊
```

## Checkbox 的特性
checkbox 比較特別，每個 checkbox 其實都代表了一個值，
舉例來說：***如果文字輸入欄位是填充題，那勾選方塊就是複選題***。

而複選題是有 ***值*** 的，我們只看代表這個值的選項有沒有被勾選。但是我們要如何知道這個值是否被勾選呢？

## 使用 jQuery 來查看 checkbox 是否被勾選

要知道 checkbox 是否被點選，我們一樣可以使用 jQuery 很方便的知道，請看以下範例：

<input id="one-checkbox" type="checkbox" value="好學生"/> 我是好學生
<button id="button">點下了嗎？</button>

<script>
    $("body").on("click","#button", function(){
        if( $("#one-checkbox").prop("checked") ){ // 回傳布林值
            alert( "你是"+$("#one-checkbox").val() );
        } else {
            alert( "你不是"+$("#one-checkbox").val() );
        }
    });
</script>

```html
<input id="one-checkbox" type="checkbox" value="好學生"/> 我是好學生
<button id="button">點下了嗎？</button>

<script>
    $("body").on("click","#button", function(){
        if( $("#one-checkbox").prop("checked") ){ // 回傳布林值
            alert( "你是"+$("#one-checkbox").val() );
        } else {
            alert( "你不是"+$("#one-checkbox").val() );
        }
    });
</script>
```

##實作時間
在剛剛創造的網頁中加入「喜歡的水果」欄位，用 checkbox 加入4個選項：橘子、蘋果、香蕉、芭樂。


名字：<input type="text" /><br>
年齡：<input type="text" /><br>

<input class="fruitOption" type="checkbox" value="橘子"> 橘子
<input class="fruitOption" type="checkbox" value="蘋果"> 蘋果
<input class="fruitOption" type="checkbox" value="香蕉"> 香蕉
<input class="fruitOption" type="checkbox" value="芭樂"> 芭樂
<br>

<button>Hello</button>

--

當按下按鈕時會說出：
```
Hello, ____歲的_______。原來你喜歡吃 `水果1`, `水果2`....
```

<br>

> ###小提示：
請將所有要被檢查的勾選方塊都給定一個 id 或 class，並在點下按鈕後一一檢查是否被勾選。

### 挑戰題
當跳出訊息之後，除了原本在欄位中的內容要被清空之外，也要將勾選方塊回復為 “未勾選” 的狀態。
