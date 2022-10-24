## 분류 : #Selenium 

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

## select
```Java
WebDriver driver = new ChromeDriver(); m 

url 접근
- driver.get('http://url.com')

- WebElement attr = dirver.findElement(By.id("id"));
- WebElement attr = dirver.findElement(By.className("class"));
- WebElement attr = dirver.findElement(By.linkText("link"));

- WebElement attr = dirver.findElement(By.xpath("/html/body/div"));
- WebElement attr = dirver.findElement(By.xpath(".//span[@class='fbw']/p"));

- WebElement firstName = driver.findElement(By.cssSelector("tag#id.class"));
- WebElement firstName = driver.findElement(By.cssSelector("tag[name='n']"));

```

## send
```Java
driver.findElement(By.name("search_query")).sendKeys("검색어");
해당 element 아마도 검색창 에 입력할수있다.

```

## click
```Java
driver.findElement(By.linkText("검색어")).click();
driver.findElement(By.partialLinkText("검색어")).click();
```



----
### 외부문서

- [예제1](https://beomi.github.io/2017/02/27/HowToMakeWebCrawler-With-Selenium/)
- [예제2](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=hancury&logNo=220355263166)
- 
----
### 업데이트
-  2022/10/23 (일요일) - 21:04 : 첫 작성
