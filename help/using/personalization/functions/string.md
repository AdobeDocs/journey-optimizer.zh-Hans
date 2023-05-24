---
title: 字串函式庫
description: 字串函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 9301d02be37c6aabad9c10a4cc43c20d3e3ee23e
workflow-type: tm+mt
source-wordcount: '1857'
ht-degree: 6%

---

# 字串函式 {#string}

瞭解如何在運算式編輯器中使用字串函式。

## 駝峰式大小寫 {#camelCase}

此 `camelCase` 函式會將字串中每個字詞的第一個字母變成大寫。

**语法**

```sql
{%= camelCase(string)%}
```

**示例**

以下函式會將設定檔街道地址中的第一個字詞變成大寫。

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## 字元代碼位於 {#char-code-at}

此 `charCodeAt` 函式會傳回字元的ASCII值，類似JavaScript中的charCodeAt函式。 它以字串和整數（定義字元的位置）作為輸入引數，並傳回其對應的ASCII值。

**语法**

```sql
{%= charCodeAt(string,int) %}: int
```

**示例**

以下函式傳回o的ASCII值，即111。

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

此 `concat` 函式將兩個字串合併為一個。

**语法**

```sql
{%= concat(string,string) %}
```

**示例**

以下函式會將個人資料城市和國家/地區結合在單一字串中。

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

此 `contains` 函式來決定字串是否包含指定的子字串。

**语法**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 執行檢查的字串。 |
| `STRING_2` | 要在第一個字串中搜尋的字串。 |
| `CASE_SENSITIVE` | 選擇性引數，用來判斷檢查是否區分大小寫。 可能的值： true （預設） / false。 |

**示例**

* 以下函式將檢查設定檔名字是否包含字母A （大寫或小寫）。 如果是這種情況，則會傳回「true」，否則會傳回「false」。

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* 下列查詢會區分大小寫，判斷個人的電子郵件地址是否包含「2010@gm」字串。

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## 不包含{#doesNotContain}

此 `doesNotContain` 函式來決定字串是否不包含指定的子字串。

**语法**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `STRING_1` | 執行檢查的字串。 |
| `STRING_2` | 要在第一個字串中搜尋的字串。 |
| `CASE_SENSITIVE` | 選擇性引數，用來判斷檢查是否區分大小寫。 可能的值： true （預設） / false。 |

**示例**

下列查詢會區分大小寫，判斷個人的電子郵件地址是否不包含字串「2010@gm」。

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## 結尾不是{#doesNotEndWith}

此 `doesNotEndWith` 函式來決定字串的結尾是否不是指定的子字串。

**语法**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串中搜尋的字串。 |
| `{CASE_SENSITIVE}` | 選擇性引數，用來判斷檢查是否區分大小寫。 可能的值： true （預設） / false。 |

**示例**

下列查詢會區分大小寫，判斷個人的電子郵件地址是否不以「.com」結尾。

```sql
doesNotEndWith(person.emailAddress,".com")
```

## 開頭不是{#doesNotStartWith}

此 `doesNotStartWith` 函式來決定字串的開頭是否不是指定的子字串。

**语法**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串中搜尋的字串。 |
| `{CASE_SENSITIVE}` | 選擇性引數，用來判斷檢查是否區分大小寫。 可能的值： true （預設） / false。 |

**示例**

下列查詢會區分大小寫，判斷個人的名稱是否不是以「Joe」開頭。

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## 編碼64{#encode64}

此 `encode64` 函式可用來編碼字串，以保留個人資訊(PI)，例如包含在URL中時。

**语法**

```sql
{%= encode64(string) %}
```

## 结束于{#endsWith}

此 `endsWith` 函式用來決定字串的結尾是否為指定的子字串。

**语法**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串中搜尋的字串。 |
| `{CASE_SENSITIVE}` | 選擇性引數，用來判斷檢查是否區分大小寫。 可能的值： true （預設） / false。 |

**示例**

下列查詢會區分大小寫，判斷個人的電子郵件地址是否以「.com」結尾。

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## 等于{#equals}

此 `equals` 函式用來決定字串是否等於指定的字串，須區分大小寫。

**语法**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**示例**

下列查詢會區分大小寫，判斷人員是否為「John」。

```sql
{%=equals(profile.person.name,"John") %}
```

## 等於忽略大小寫{#equalsIgnoreCase}

此 `equalsIgnoreCase` 函式來判斷字串是否等於指定的字串，不區分大小寫。

**语法**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**示例**

下列查詢會在不區分大小寫的情況下，判斷個人的姓名是否為「John」。

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## 擷取電子郵件網域 {#extractEmailDomain}

此 `extractEmailDomain` 函式用於擷取電子郵件地址的網域。

**语法**

```sql
{%= extractEmailDomain(string) %}
```

**示例**

以下查詢會擷取個人電子郵件地址的電子郵件網域。

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## 格式化貨幣 {#format-currency}

此 `formatCurrency` 函式可用來根據第二個引數中作為字串傳遞的區域設定，將任何數字轉換為對應的語言敏感型貨幣表示法。

**语法**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**示例**

此查詢傳回56.00英鎊

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## 取得url主機 {#get-url-host}

此 `getUrlHost` 函式來擷取URL的主機名稱。

**语法**

```sql
{%= getUrlHost(string) %}: string
```

**示例**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

傳回「www.myurl.com」

## 取得url路徑 {#get-url-path}

此 `getUrlPath` 函式來擷取URL網域名稱之後的路徑。

**语法**

```sql
{%= getUrlPath(string) %}: string
```

**示例**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

傳回「/contact.html」

## 取得url通訊協定 {#get-url-protocol}

此 `getUrlProtocol` 函式來擷取URL的通訊協定。

**语法**

```sql
{%= getUrlProtocol(string) %}: string
```

**示例**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

傳回「http」

## 索引： {#index-of}

此 `indexOf` 函式可用來傳回第二個引數第一次出現的位置（在第一個引數中）。 如果沒有相符專案，則傳回–1。

**语法**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要在第一個引數中搜尋的字串 |

**示例**

```sql
{%= indexOf("hello world","world" ) %}
```

傳回6。

## 为空 {#isEmpty}

此 `isEmpty` 函式來判斷字串是否為空白。

**语法**

```sql
{%= isEmpty(string) %}
```

**示例**

如果設定檔的行動電話號碼為空，則以下函式會傳回「true」。 否則，會傳回「false」。

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## 不是空的 {#is-not-empty}

此 `isNotEmpty` 函式來判斷字串是否不是空的。

**语法**

```sql
{= isNotEmpty(string) %}: boolean
```

**示例**

如果設定檔的行動電話號碼非空白，則以下函式會傳回「true」。 否則，會傳回「false」。

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## 最後一個索引： {#last-index-of}

此 `lastIndexOf` 函式可用來傳回第二個引數最後一次出現的位置（在第一個引數中）。 如果沒有相符專案，則傳回–1。

**语法**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要在第一個引數中搜尋的字串 |

**示例**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

傳回7。

## 左側修剪 {#leftTrim}

此 `leftTrim` 函式可用來移除字串開頭的空格。

**语法**

```sql
{%= leftTrim(string) %}
```

## 长度 {#length}

此 `length` 函式來取得字串或運算式中的字元數。

**语法**

```sql
{%= length(string) %}
```

**示例**

以下函式傳回設定檔城市名稱的長度。

```sql
{%= length(profile.homeAddress.city) %}
```

## 按讚{#like}

此 `like` 函式來判斷字串是否符合指定的模式。

**语法**

```sql
{%= like(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 比對第一個字串的運算式。 建立運算式有兩個支援的特殊字元： `%` 和 `_`. <ul><li>`%` 用於表示零個或多個字元。</li><li>`_` 用於表示正好一個字元。</li></ul> |

**示例**

下列查詢會擷取設定檔所在的所有城市，且其中包含「es」模式。

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## 小寫{#lower}

此 `lowerCase` 函式會將字串轉換為小寫字母。

**语法**

```sql
{%= lowerCase(string) %}
```

**示例**

此函式將設定檔名字轉換為小寫字母。

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## 匹配{#matches}

此 `matches` 函式來判斷字串是否符合特定的規則運算式。 請參閱 [本檔案](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) 以取得規則運算式中比對模式的詳細資訊。

**语法**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**示例**

下列查詢會在不區分大小寫的情況下，判斷個人的名稱是否以「John」開頭。

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## 遮色片 {#mask}

此 `Mask` 函式可用來以「X」字元取代字串的一部分。

**语法**

```sql
{%= mask(string,integer,integer) %}
```

**示例**

下列查詢會將「123456789」字串取代為「X」字元，前兩個字元和最後兩個字元除外。

```sql
{%= mask("123456789",1,2) %}
```

查詢傳回 `1XXXXXX89`.

## MD5 {#md5}

此 `md5` 函式用於計算及傳回字串的md5雜湊。

**语法**

```sql
{%= md5(string) %}: string
```

**示例**

```sql
{%= md5("hello world") %}
```

傳回「5eb63bbe01eeed093cb22bb8f5acdc3」

## 不等於{#notEqualTo}

此 `notEqualTo` 函式來判斷字串是否不等於指定的字串。

**语法**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**示例**

下列查詢會區分大小寫判斷個人的姓名是否為「John」。

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## 不等於忽略大小寫 {#not-equal-with-ignore-case}

此 `notEqualWithIgnoreCase` 函式是用來比較兩個字串，忽略大小寫。

**语法**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要與第一個字串進行比較的字串。 |

**示例**

下列查詢會判斷人員姓名是否為「john」，不區分大小寫。

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## 規則運算式群組{#regexGroup}

此 `Group` 函式是根據提供的規則運算式來擷取特定資訊。

**语法**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING}` | 執行檢查的字串。 |
| `{EXPRESSION}` | 比對第一個字串的規則運算式。 |
| `{GROUP}` | 要比對的運算式群組。 |

**示例**

下列查詢用於從電子郵件地址中擷取網域名稱。

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## 替换 {#replace}

此 `replace` 函式可用來將字串中的指定子字串取代為另一個子字串。

**语法**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 必須取代子字串的字串。 |
| `{STRING_2}` | 要取代的子字串。 |
| `{STRING_3}` | 取代子字串。 |

**示例**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

傳回「Hello Mark，這是您的每月電子報！」

## 全部取代{#replaceAll}

此 `replaceAll` function可用來將符合「regex」運算式的文字的所有子字串取代為指定的常值「replacement」字串。 Regex有特殊處理「\」和「+」，所有regex運算式都遵循PQL逸出策略。 取代會從字串的開頭到結尾進行，例如，將字串「aaa」中的「aa」取代為「b」將會產生「ba」而不是「ab」。

**语法**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> 當當作第二個引數的運算式是特殊規則運算式字元時，請使用雙反斜線(`//`)。  特殊規則運算式字元包括：[.， +， *， ？， ^， $， (， )， [， ]，{， }， |， \.]
> 
> 進一步瞭解 [oracle檔案](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}。

## 右側修剪 {#rightTrim}

此 `rightTrim` 函式移除字串結尾的空格。

**语法**

```sql
{%= rightTrim(string) %}
```

## 拆分 {#split}

此 `split` 函式可用來依指定字元分割字串。

**语法**

```sql
{%= split(string,string) %}
```

## 开始于{#startsWith}

此 `startsWith` 函式來決定字串的開頭是否為指定的子字串。

**语法**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| 参数 | 描述 |
| --------- | ----------- |
| `{STRING_1}` | 執行檢查的字串。 |
| `{STRING_2}` | 要在第一個字串中搜尋的字串。 |
| `{CASE_SENSITIVE}` | 選擇性引數，用來判斷檢查是否區分大小寫。 預設情況下，此項設為true。 |

**示例**

下列查詢會區分大小寫，判斷個人的名稱是否以「Joe」開頭。

```sql
{%= startsWith(person.name,"Joe") %}
```

## 字串至日期 {#string-to-date}

此 `stringToDate` 函式會將字串值轉換為日期時間值。 它需要兩個引數：日期時間的字串表示和格式器的字串表示。

**语法**

```sql
{= stringToDate("date-time value","formatter" %}
```

**示例**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## 字串至整數 {#string-to-integer}

此 `string_to_integer` 函式用於將字串值轉換為整數值。

**语法**

```sql
{= string_to_integer(string) %}: int
```

## 字串至數字 {#string-to-number}

此 `stringToNumber` 函式用於將字串轉換為數字。 對於無效的輸入，它會傳回相同的字串作為輸出。

**语法**

```sql
{%= stringToNumber(string) %}: double
```

## 子字串 {#sub-string}

此 `Count string` 函式用來傳回開始索引和結束索引之間字串運算式的子字串。
**语法**

```sql
{= substr(string, integer, integer) %}: string
```

## 字首大寫{#titleCase}

此 **titleCase** 函式可用來將字串中每個字詞的首字母變成大寫。

**语法**

```sql
{%= titleCase(string) %}
```

**示例**

如果這個人住在華盛頓高街，這個函式會傳回華盛頓高街。

```sql
{%= titleCase(profile.person.location.Street) %}
```

## 至Bool {#to-bool}

此 `toBool` 函式可用來將引數值轉換為布林值（視其型別而定）。

**语法**

```sql
{= toBool(string) %}: boolean
```

## 結束日期時間 {#to-date-time}

此 `toDateTime` 函式用於將字串轉換為日期。 針對無效輸入，它會傳回epoch日期作為輸出。

**语法**

```sql
{%= toDateTime(string, string) %}: date-time
```

## 僅至日期時間 {#to-date-time-only}

此 `toDateTimeOnly` 函式用於將引數值轉換為僅日期時間值。 針對無效輸入，它會傳回epoch日期作為輸出。 此函式接受字串、日期、長欄位和整數欄位型別。

**语法**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## 修剪 {#trim}

此 **trim** 函式會移除字串開頭和結尾的所有空格。

**语法**

```sql
{%= trim(string) %}
```

## 大寫{#upper}

此 **大寫** 函式會將字串轉換為大寫字母。

**语法**

```sql
{%= upperCase(string) %}
```

**示例**

此函式將設定檔姓氏轉換為大寫字母。

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## Url解碼 {#url-decode}

此 `urlDecode` 函式用於解碼url編碼的字串。

**语法**

```sql
{%= urlDecode(string) %}: string
```

## Url編碼 {#url-encode}

此 `Count only null` 函式用於對字串進行url編碼。

**语法**

```sql
{%= urlEncode(string) %}: string
```
