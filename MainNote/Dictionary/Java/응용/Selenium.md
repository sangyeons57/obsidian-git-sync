## 분류 : 

---
## 관련문서
- [[Jsoup]]
----
### 요약(사용설명)

---
### 내용
webdriver API를 통해 브라우저를 제어한다.
다양한 언어를 사용할수 있다.

자바스크립에 의해 동적으로 생성되는 사이트의 데이터를 크롤링할때 사용한다

```Java
WebDriver driver = new ChromeDriver(); m 

url 접근
- get('http://url.com')

페이지에 element에 접근하는 메소드
-find_element_by_name('HTML_name')
-find_element_by_id('HTML_id')
-find_element_by_xpath('/html/body/some/xpath')
-find_element_by_css_selector('#css > div.selector')
-find_element_by_class_name('some_class_name')
-find_element_by_tag_name('h1')
```

----
### 외부문서

- [예제1](https://beomi.github.io/2017/02/27/HowToMakeWebCrawler-With-Selenium/)
----
### 업데이트
-  2022/10/23 (일요일) - 21:04 : 첫 작성
