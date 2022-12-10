## 분류 : #Selenium 

---
## 관련문서
- [[Jsoup]]
----
### 요약(사용설명)

이거 하기전에 selenium 을 maven 파일에 적용해야한다
[selenium 다운로드](https://mvnrepository.com/artifact/org.seleniumhq.selenium/selenium-java)
그후 자기자신의 chrome버전의 chromedriver를 다운로드 를 해야한다
만약 다른 브라우저 를 사용할거면 다른 브라우저의 드라이버가 필요하다


---
### 내용
webdriver API를 통해 브라우저를 제어한다.
다양한 언어를 사용할수 있다.

자바스크립에 의해 동적으로 생성되는 사이트의 데이터를 크롤링할때 사용한다

## select
```Java
WebDriver driver = new ChromeDriver();

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

+추가
By.cssSelector는 위부터 하나하나 다 써줘야 하는 반면에
다른 것은 중간을 뛰어서 할수있다. 예)
```HTML
<HTML>
	<body>
		<div id="1">
			<div id="1-1">
			</div>
		</div>
	</body>
</HTML>
```
```Java

driver.findElement (by.cssSelector("body > #1-1"));       불가능
driver.findElement (by.cssSelector("body > #1 > #1-1"));    가능
처음 부모"body" 를 설정할때는 원하느 부분 부터 시작할수있지만
그이후로 자식은 모두 표기해줘야한다.

WebElement m = driver.findElement(By.cssSelector("body"));
m = m.findElement(By.id("1-1"));                         가능
이방식은 find element를 계속 해서 사용하기때문에 부모를 다시설정 할수있다.

```

!주의
findElement는 가장 표면에 있는것 부터 가장 깊은 곳에 있는것 까지 조건만 맞다면 다 같은 급으로 대리고 온다
원하는 태그 안에 같은 태그가 존제 해서 태그가 2개씩 찍히지 않는지 찾아보자



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
click은 모드 webElement에서 작동한다.


----
### 외부문서

- [예제1](https://beomi.github.io/2017/02/27/HowToMakeWebCrawler-With-Selenium/)
- [예제2](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=hancury&logNo=220355263166)
- 
----
### 업데이트
-  2022/10/23 (일요일) - 21:04 : 첫 작성
-  2022/10/24 (월요일) - 19:46 : +추가
