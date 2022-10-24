## 분류 : #Selenium 

---
## 관련문서
- [[Selenium]]

----
### 요약(사용설명)

---
### 내용
getAttribute 는 html코드를 string으로 가져오기 위해 있다.

쓰는방법
```HTML
<input id="search_form_input_homepage" class="js-search-input search__input--adv" type="text" autocomplete="off" name="q" tabindex="1" value="" autocapitalize="off" autocorrect="off">
```
```Java

WebElement searchTextBox= driver.findElement(By.id("search_form_input_homepage"));

String typeValue=searchTextBox.getAttribute("type");

String autocompleteValue=searchTextBox.getAttribute("autocomplete");


String nonExistingAttributeValue=searchTextBox.getAttribute("nonExistingAttribute");

```

그외에 getAttribute("innerHTML")
을 하면 태그 내부의 

----
### 외부문서
-[설명 문서](https://www.browserstack.com/guide/getattribute-method-in-selenium)

----
### 업데이트
-  2022/10/24 (월요일) - 18:50 : 첫 작성
