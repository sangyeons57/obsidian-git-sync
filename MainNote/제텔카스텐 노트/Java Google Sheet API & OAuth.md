#Java#GoogleShhet #OAuth

[Java Quick Start 공식 구글시트 퀵스타트 가이드](https://developers.google.com/sheets/api/quickstart/java)

[Google Cloud](https://console.cloud.google.com/) 에서 프로젝트를 생성 해야한다.
API & Services 에서 Credentials부분에 들어가서
CREATE CREDENTIALS -> OAuth 부분을 선택한다
적합한 플렛폼을 선택해서 Json 파일을 다운 받는다

/resources부분에 해당파일을 넣은다

(!주위) 자바에서는 Gradle방식을 사용해야한다
->Maven 방식도 존제하기는 한는것 같다.

gradle.build파일 설정은 이렇게
[Github](https://github.com/googleworkspace/java-samples/blob/main/drive/quickstart/build.gradle)
```gradle
apply plugin: 'java'  
apply plugin: 'application'

mainClassName = 'DriveQuickstart'
sourceCompatibility = 11
targetCompatibility = 11
version = '1.0'

repositories {
	mavenCentral()  
}

dependencies {
	implementation 'com.google.api-client:google-api-client:2.0.0'
	implementation 'com.google.oauth-client:google-oauth-client-jetty:1.34.1' 
	implementation 'com.google.apis:google-api-services-drive:v3-rev20220815-2.0.0'  
}
```

jdk버전이랑 안 맞는 경우가있다 그때는 자바버전을 해당 버전에 맞게 해줘야한다