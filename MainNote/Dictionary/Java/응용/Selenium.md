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
- driver.get('http://url.com')

- WebElement attr = dirver.findElement(By.id("email"));
- WebElement attr = dirver.findElement(By.className("email"));
- WebElement attr = dirver.findElement(By.linkText("email"));
```

----
### 외부문서

- [예제1](https://beomi.github.io/2017/02/27/HowToMakeWebCrawler-With-Selenium/)
----
### 업데이트
-  2022/10/23 (일요일) - 21:04 : 첫 작성
